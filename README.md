E-Commerce Data Clean Up Process

Goal: Build an Extraction, Transformation, Load (ETL) pipeline in Python that will take an unstructured data set of 24 columns from an E-Commerce website and turn it into a cleanly structured, analytic-ready data set of 6 columns.

Technologies Used

Python | Pandas Library | Jupyter Notebook

Major Transformations

        1.Strategic Slicing: Isolated the most substantive data points for analysis (product_id, title, final_price and rating) prior to removing null values to ensure a 0% loss of data.

        2.String Sanitization: Removed multiple characters (₹, commas, and '' quotes) from the final_price column to prepare the data for use as numerical values, then converted to float data type.

        3.Feature Engineering: Added a baseline quantity column and calculated total_value = final_price * quantity.

        4.Deduplication: Performed an identity check to confirm uniqueness of the final 1,000 product rows - that there are no duplicates.

Project Outputs

        Week1_Assignment.ipynb: The complete ETL pipeline codebase. 

        cleaned_shopping_dataset.csv: The final data set that is ready for analysis.
