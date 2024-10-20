# IPL Data Analysis using Apache Spark, Amazon S3, and Matplotlib

This project demonstrates how to list, ingest, cleanse, transform, and analyze IPL cricket match data using Apache Spark on Databricks, with data stored in Amazon S3. The project showcases performance optimization techniques like caching and broadcast joins, and it visualizes the results using Matplotlib.

## Project Overview

### Dataset
The IPL dataset consists of two main parts for each match:
- **Ball-by-ball data**: Detailed events for each ball bowled during the match.
- **Match-related information**: General match details such as teams, venue, and outcomes.

### Tools and Technologies
- **Apache Spark** (via Databricks)
- **Amazon S3** for data storage
- **Boto3** to interact with S3
- **Python** for data processing and visualization
- **Matplotlib** for charting

## Key Features

1. **Data Ingestion**
   - Used Boto3 to list and retrieve IPL match data stored in Amazon S3.
   - Data split into two distinct DataFrames for ball-by-ball details and match information.

2. **Data Cleansing & Transformation**
   - Cleansed both ball-by-ball and match data, handling missing values and standardizing formats.
   - Transformed the datasets to suit analysis needs using Spark DataFrame transformations.

3. **Performance Optimization**
   - Utilized caching to store intermediate results in memory, reducing recomputation.
   - Applied broadcast joins to optimize large dataset joins.

4. **Data Storage**
   - Stored the final, partitioned DataFrames back into Amazon S3 for efficient retrieval.

5. **Data Analysis**
   - Performed grouping and aggregation to analyze key IPL statistics such as player performance, team trends, and match outcomes.

6. **Visualization**
   - Visualized key insights using **Matplotlib**, including:
     - Player performance trends.
     - Run distributions.
     - Team win-loss ratios.
