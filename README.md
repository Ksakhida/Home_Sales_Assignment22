# Home_Sales_Assignment22

## Overview
This project analyzes home sales data using SparkSQL, conducted on Google Colab. The goal was to calculate various metrics related to home sales and optimize query performance using caching and partitioning techniques.

## Folder Structure
- **Home_Sales_Assignment22/**  
  ├── **Home_Sales/**  
  │   ├── Home_Sales.ipynb *(Not used)*  
  │   ├── Home_Sales_colab.ipynb *(Used for all analysis)*  
  │   ├── Analysis_Report.docx *(Contains detailed report)*  
  ├── **README.md** *(This file)*  

## Analysis Summary
### Data and Queries
- **Dataset**: `home_sales_revised.csv`
- The data was analyzed to compute the following metrics:
  1. Average price of four-bedroom homes by year.
  2. Average price of homes with 3 bedrooms and 3 bathrooms, categorized by year built.
  3. Average price of homes with 3 bedrooms, 3 bathrooms, 2 floors, and ≥ 2,000 sqft, categorized by year built.
  4. Average price per view rating for homes with prices ≥ $350,000.

### Performance Optimization
- **Caching**: Used to improve query performance, reducing runtime significantly.
- **Partitioning**: The data was partitioned by `date_built`, and parquet format was used to further optimize query speed.
  
### Key Results
1. **Average Price of Four-Bedroom Houses** (2019-2022):  
   Minor fluctuations, with the highest price in 2021.
2. **Average Price for 3-Bedroom, 3-Bathroom Homes**:  
   Stable pricing, with slight increases over the years.
3. **Average Price for Homes with Specific Conditions**:  
   Prices peaked in 2012 and 2013, showing market variability.
4. **View Rating and Prices**:  
   Strong correlation between higher view ratings and higher home prices.
5. **Performance Comparison**:  
   - **Cached**: 0.568s  
   - **Uncached**: 1.828s  
   - **Parquet**: 0.725s  

## Notes
- The project was executed using the `Home_Sales_colab.ipynb` file due to installation challenges with the regular Jupyter Notebook.
- All analysis and query execution were done in **Google Colab** to overcome local issues.
  
## Conclusion
This analysis successfully met the project requirements, including data processing, query execution, and performance optimizations, with the use of Google Colab enabling efficient completion of the tasks.
