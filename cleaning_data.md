What issues will you address by cleaning the data?
The sales_report table was dropped as its records were found in both the product and the sales_by_sku tables.
It was verified that all entries in the product table are unique.
The products table (SKU; PK), sales_records (productSKU; FK), sales_by_sku (productSKU; FK), and all_sessions (productSKU; FK) tables were linked.
Rows in the all_sessions table missing country and city were deleted.
A new column called newrevenue was created on the analytics table, and it was populated with the product of unit_price and units_sold.
A new column was inserted into the all_sessions table to split the product category.




Queries:
Below, provide the SQL queries you used to clean your data.
Dropped the sales_report tables as the records found there exists in both the product and the sales_by_colums: DROP TABLE sales_report

Verified that all entries in the product table is unique: Count of all records in the products table - 1092. select count(*) from products

    Count of distincts records in the SKU column of the products table: 1092
    select distinct count(sku)
    from products
   
    Deleted rows in the all_sessions table missing country and city: Count of all records in the all_sessions table - 15134. select count(*) from all_sessions
        Count of records missing either country or city value - 8656.
    select count(*)
    from all_sessions
    where country LIKE '%not%' or city LIKE '%not%'

    Deleting records missing either country or city value - 
    delete from all_sessions
    where country LIKE '%not%' or city LIKE '%not%'

    Verification: number of records in table - 6478
    select count(*)
    from all_sessions
    Inserted the product of unit_price and units_sold into the new column creared called newrevenue on the analytics table. Creating new column newrevevnue. alter table analytics add newrevenue big int;

    Updating newrevenue column
    update analytics
    SET newrevenue = 
    (case 
   		when revenue is not null then cast(revenue as bigint)
   		ELSE (unit_price * units_sold)
    end)
Inserted a new column in all_sessions table with a split of the product category Creating new column productcategory. alter table all_sessions add productcategory text;

Updating productcategory column
	update all_sessions
SET productcategory = split_part(v2productcategory,'/', 2);



    Verification: number of records in table - 6478
    select count(*)
    from all_sessions
