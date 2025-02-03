Business Report Summary

The DVD rental store aims to identify which film categories generate the highest revenue. By analyzing rental transactions and revenue across various film categories, the store can:

    Optimize Pricing Strategies: Adjust rental rates based on the revenue performance of each film category.
    Improve Inventory Management: Stock more films in high-performing categories and review the mix of underperforming ones.
    Enhance Promotional Efforts: Focus marketing initiatives on film categories that generate higher revenue, thereby attracting more customers.

A1. Specific Fields for Detailed and Summary Tables

Detailed Table: category_revenue_details
Column	Data Type	Description
rental_id*	INTEGER	Unique identifier for each rental transaction
film_id	INTEGER	Identifier for the rented film
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
avg_rental_price	NUMERIC(5,2)	Average rental price per transaction within the category

A2. Types of Data Fields

    INTEGER: rental_id, film_id, total_rentals
    TIMESTAMP: rental_date, return_date
    VARCHAR: film_title, category_name
    NUMERIC: rental_rate, total_revenue, avg_rental_price

A3. Identified Tables from the Dataset

    rental – Contains details for each rental transaction (including dates).
    film_category – Links films to their respective categories (genres).
    payment – Holds the revenue data associated with each rental transaction.

A4. Field Requiring Custom Transformation

    Field: rental_rate (alternatively, total_revenue)

    Transformation:
    Create a User-Defined Function (UDF) to convert numeric revenue values into a formatted currency string (e.g., $XX.XX).

    Why:
    This transformation ensures that monetary values are displayed in a consistent, easy-to-read format, enhancing readability and aiding decision-makers.

A5. Business Uses of the Tables

Detailed Table (category_revenue_details):

    Granular Analysis: Provides in-depth insights into individual rental transactions by film category.
    Customer Preferences: Helps analyze trends and preferences across different film genres.
    Performance Monitoring: Identifies underperforming categories that might require additional promotions or adjustments.

Summary Table (category_revenue_summary):

    High-Level Overview: Offers a concise snapshot of overall revenue trends by film category.
    Inventory Decision Support: Assists managers in making informed decisions on which categories to prioritize for stocking.
    Marketing Strategy: Guides promotional efforts by highlighting the top-performing genres, enabling targeted marketing initiatives.

A6. Frequency of Report Refresh

    Recommended Refresh Rate: Monthly
        Seasonal Considerations: Monthly updates capture seasonal variations (e.g., holiday spikes, summer trends) that affect rental behavior.
        Timely Strategy Adjustments: Frequent refreshes allow the business to promptly adjust inventory levels and marketing strategies based on the latest data.
        Long-Term Analysis: While monthly reporting offers actionable insights for operational decisions, quarterly reviews can complement this data for long-term strategic planning.
