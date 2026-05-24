E-Commerce Data Cleaning Pipeline

Objective: Build a robust Python ETL pipeline to transform a messy, 24-column e-commerce dataset into a clean, structured 6-column format for downstream BI analytics.

Tech Stack

Python | Pandas | Jupyter Notebook

Key Transformations

    Strategic Slicing: Isolated core analytical features (product_id, title, final_price, rating) before dropping nulls to achieve a 0% data loss rate.

    String Sanitization: Cleaned messy final_price strings by stripping currency symbols (₹), commas, and quotes, safely casting them to floats.

    Feature Engineering: Injected a baseline quantity vector and calculated total_amount = final_price * quantity.

    Deduplication: Executed an identity check, confirming 100% uniqueness across the final 1,000 product rows.

Project Deliverables

    Week1_Assignment.ipynb: The complete ETL codebase.

    cleaned_shopping_dataset.csv: The optimized, analysis-ready dataset.Commerce Data Exploration and Cleaning with Pandas
