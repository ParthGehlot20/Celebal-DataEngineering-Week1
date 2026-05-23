E-Commerce Data Exploration and Cleaning with Pandas

📋 Project Objective

The goal of this project is to build a robust ETL (Extract, Transform, Load) pipeline using Python and the Pandas library. This pipeline processes a raw, unorganized e-commerce dataset, handles messy text formatting, and outputs a highly optimized, structured analytical format ready for downstream business intelligence tasks.

🗂️ Dataset Overview

    Source: Kaggle Shopping Dataset (by Anvit Kumar)

    Raw Data Dimensions: 1,000 product rows × 24 columns

    Final Cleaned Dimensions: 1,000 product rows × 6 columns

    Primary Attributes Retained: product_id, title, final_price, rating, quantity, total_amount

🛠️ Data Cleaning & Processing Workflow

The data processing pipeline implemented within the Jupyter Notebook follows these critical milestones:

    Data Ingestion: Loaded the raw Combined_dataset.csv into a Pandas DataFrame using pd.read_csv().

    Strategic Column Isolation: To avoid unnecessary data loss from heavily unpopulated text columns (like videos and what_customers_said), the dataset was immediately sliced to isolate the core analytical features (product_id, title, final_price, rating).

    Missing Value Resolution: Applied a strict .dropna() protocol to the isolated subset, ensuring robust data integrity without sacrificing valid rows.

    Deduplication Sweep: Executed an identity check to remove duplicate records, confirming 100% data uniqueness across the 1,000 retained rows.

    String Sanitization & Type Conversion: - Addressed messy string artifacts in the final_price column.

        Systematically stripped currency symbols (₹), commas (,), and quotes (") using string replacement functions.

        Safely cast the sanitized text into a standardized float decimal data type (pd.to_numeric).

    Feature Engineering (Derived Columns):

        Injected a static baseline quantity vector (2 units per transaction) to facilitate revenue modeling.

        Engineered a new vector column named total_amount using the mathematical broadcasting operation: total_amount = final_price * quantity

    Data Persistence: Saved the final, optimized 6-column table structure locally as cleaned_shopping_dataset.csv, omitting row indices to maintain structural cleanliness.

📊 Technical Highlights & Transformations

Unlike basic data imputation, this pipeline prioritized Data Quality over Quantity. By surgically selecting target columns before dropping nulls, the pipeline achieved a 0% data loss rate on the core product metrics. Furthermore, the conversion of complex currency strings into usable float integers demonstrates an ability to handle real-world, dirty data environments.

📦 Project Deliverables & Folder Structure

📁 Celebal-DataEngineering-Week1/
│
├── 📄 README.md

├── 📓 Week1_Assignment.ipynb

└── 📊 cleaned_shopping_dataset.csv