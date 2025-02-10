# Home Sales Analysis using PySpark  

## Overview  
This project utilizes **PySpark SQL** to analyze home sales data, answering key questions regarding home prices based on various attributes such as the number of bedrooms, bathrooms, floors, square footage, and view ratings. The project also explores performance improvements using caching and partitioning.  

## Technologies Used  
- **Apache Spark** (PySpark)  
- **AWS S3** (for reading data)  
- **Parquet format** (for optimized storage)  
- **GitHub** (for version control)  

## Dataset  
The dataset used for this analysis is **home_sales_revised.csv**, which is stored in an AWS S3 bucket.  

## Tasks Completed  
✔ **Load Data**: Read the dataset into a PySpark DataFrame from AWS S3.  
✔ **Create Temporary Table**: Register the DataFrame as a temporary SQL table named `home_sales`.  
✔ **Data Analysis Using SparkSQL**:  
   - Calculate the **average price** for four-bedroom homes sold per year.  
   - Determine the **average price** of homes with three bedrooms and three bathrooms for each year they were built.  
   - Find the **average price** of homes with three bedrooms, three bathrooms, two floors, and a minimum of 2,000 square feet, per year built.  
   - Compute the **average home price per "view" rating** for homes with an average price of at least $350,000 and measure query runtime.  
✔ **Optimize Performance**:  
   - Cache the `home_sales` table and re-run queries to compare performance.  
   - Partition data by `date_built` in Parquet format and evaluate query performance improvements.  
✔ **Cleanup**:  
   - Uncache the `home_sales` table and verify its removal from cache.  

## Installation & Setup  
To run this project, you need:  
- Apache Spark & PySpark installed  
- Jupyter Notebook or a compatible environment  
- AWS credentials (if accessing the dataset from S3)  

### Running the Notebook  
1. Clone this repository:  
   ```bash
   git clone https://github.com/yourusername/Home_Sales.git
   cd Home_Sales
   ```
2. Open `Home_Sales.ipynb` in Jupyter Notebook.  
3. Execute each cell to process and analyze the data.  

## Results  
- The use of **caching** and **partitioning** significantly improved query performance.  
- Partitioning by `date_built` in **Parquet format** resulted in faster query execution compared to the raw CSV file.  
- Insights on home sales trends were obtained efficiently using **SparkSQL**.  
