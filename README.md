A. Business Report Summary
The DVD rental store wants to identify which film categories generate the highest revenue to optimize pricing strategies, inventory management, and promotional efforts. By analyzing rental transactions and revenue across different film categories, the store can prioritize stocking high-performing categories and adjust marketing efforts accordingly.
 
A1. Identify the Specific Fields for Detailed and Summary Tables
Detailed Table: category_revenue_details
Column	Data Type	Description
rental_id*	INTEGER	Unique identifier for each rental transaction
film_id	INTEGER	ID of the rented film
film_title	VARCHAR(255)	Title of the rented film
category_name	VARCHAR(100)	Genre/category of the film
rental_rate	NUMERIC(5,2)	Rental price per transaction
rental_date	TIMESTAMP	Date and time of the rental transaction
return_date	TIMESTAMP	Date and time when the rental was returned
Summary Table: category_revenue_summary
Column	Data Type	Description
category_name*	VARCHAR(100)	Film category/genre
total_rentals	INTEGER	Total number of rentals per category
total_revenue	NUMERIC(10,2)	Total revenue generated per category
avg_rental_price	NUMERIC(5,2)	Average rental price per transaction in the category
 
A2. Describe the Types of Data Fields
•	INTEGER: rental_id, film_id, total_rentals
•	TIMESTAMP: rental_date, return_date
•	VARCHAR: film_title, category_name
•	NUMERIC: rental_rate, total_revenue, avg_rental_price
 
A3. Identify Two Tables from the Dataset
1.	rental – Contains details of each rental transaction, including rental date and return date.
2.	film_category – Links films to their respective categories.
3.	payment – Contains the revenue data from each rental transaction.
 
A4. Identify a Field That Requires Custom Transformation
•	Field: rental_rate (or total_revenue)
•	Transformation: A user-defined function (UDF) will be created to format revenue for better readability, converting numeric values into a formatted currency format ($XX.XX).
•	Example User-Defined Function (UDF):
Why? This ensures that reports display monetary values in an easy-to-read format.

A5. Explain the Business Uses of the Tables
•	Detailed Table (category_revenue_details)
o	Allows deep analysis of rental trends at the category level.
o	Helps understand customer preferences across different film genres.
o	Identifies underperforming categories that may need better promotions.
•	Summary Table (category_revenue_summary)
o	Provides a high-level view of revenue trends by category.
o	Helps managers decide which film categories to stock more or less.
o	Guides promotional efforts by identifying top-performing genres.
 
A6. Explain the Frequency of Report Refresh
•	Recommended Refresh Rate: Monthly
o	Since revenue trends are influenced by seasonal demand (e.g., holidays, summer break), a monthly refresh provides stable insights.
o	It allows the business to adjust inventory and marketing strategies accordingly.
o	A quarterly analysis could be used for long-term planning.

