-- Project: Coffee Sales Analysis ETL Script
-- Description: Clean, standardize, and prepare coffee sales transaction data
-- Author: [Your Name]

-- STEP 1: REMOVE DUPLICATE TRANSACTIONS
DELETE FROM coffee_sales_raw
WHERE transaction_id IN (
    SELECT transaction_id FROM (
        SELECT transaction_id,
               ROW_NUMBER() OVER (
                   PARTITION BY transaction_date, transaction_time, product_id, store_id
                   ORDER BY transaction_id
               ) AS rn
        FROM coffee_sales_raw
    ) AS duplicates
    WHERE rn > 1
);

-- STEP 2: CONVERT DATE AND TIME TO STANDARD FORMATS
ALTER TABLE coffee_sales_raw
ALTER COLUMN transaction_date DATE;

ALTER TABLE coffee_sales_raw
ALTER COLUMN transaction_time TIME;

-- STEP 3: CLEAN QUANTITY AND UNIT PRICE DATA
-- Remove or fix negative and null quantities or prices
UPDATE coffee_sales_raw
SET transaction_qty = NULL
WHERE transaction_qty <= 0;

UPDATE coffee_sales_raw
SET unit_price = NULL
WHERE unit_price <= 0;

-- Fill null quantities or prices with median or fallback values if business rules allow
-- Example using a placeholder fallback of 1
UPDATE coffee_sales_raw
SET transaction_qty = 1
WHERE transaction_qty IS NULL;

UPDATE coffee_sales_raw
SET unit_price = 3.50
WHERE unit_price IS NULL;

-- STEP 4: CREATE A CLEANED TABLE
CREATE TABLE coffee_sales_cleaned AS
SELECT
    transaction_id,
    transaction_date,
    transaction_time,
    transaction_qty,
    store_id,
    store_location,
    product_id,
    unit_price,
    product_category,
    product_type,
    product_detail,
    -- Calculate total sale amount
    transaction_qty * unit_price AS total_sale
FROM coffee_sales_raw;

-- STEP 5: ENRICH WITH TIME INTELLIGENCE
ALTER TABLE coffee_sales_cleaned
ADD COLUMN transaction_month VARCHAR(15),
ADD COLUMN transaction_weekday VARCHAR(10),
ADD COLUMN transaction_hour INT;

UPDATE coffee_sales_cleaned
SET transaction_month = DATENAME(month, transaction_date),
    transaction_weekday = DATENAME(weekday, transaction_date),
    transaction_hour = DATEPART(HOUR, transaction_time);

-- STEP 6: STANDARDIZE TEXT FIELDS
-- Uniform casing and removing leading/trailing spaces
UPDATE coffee_sales_cleaned
SET store_location = UPPER(LTRIM(RTRIM(store_location))),
    product_category = INITCAP(LTRIM(RTRIM(product_category))),
    product_type = INITCAP(LTRIM(RTRIM(product_type))),
    product_detail = INITCAP(LTRIM(RTRIM(product_detail)));

-- STEP 7: VALIDATION QUERIES (OPTIONAL)
-- View top-selling products
SELECT TOP 5
    product_type,
    SUM(transaction_qty) AS total_quantity_sold,
    SUM(total_sale) AS total_revenue
FROM coffee_sales_cleaned
GROUP BY product_type
ORDER BY total_revenue DESC;

-- View store performance
SELECT
    store_location,
    COUNT(transaction_id) AS total_transactions,
    SUM(total_sale) AS total_sales
FROM coffee_sales_cleaned
GROUP BY store_location
ORDER BY total_sales DESC;

-- View sales by day of week
SELECT
    transaction_weekday,
    SUM(total_sale) AS total_revenue
FROM coffee_sales_cleaned
GROUP BY transaction_weekday
ORDER BY total_revenue DESC;
