# Home_Sales

In this challenge, we utilized SparkSQL to query a database containing home sales information and practiced using Big Data optimization tools such as partitioning and caching data.

## SparkSql

After reading in the .csv file to a DataFrame, we created a temporary view. Then we used SparkSQL to run several queries on the data such as:

    -Average price of a four-bedroom house sold per year
    -Average price of a 3 bedroom/3 bathroom house sold by year built
    -Average price of a 3 bedrom/3 bathroom house with two floors and greater than or equal to 2,000 sqft sold by year built
    -Average price of a home by "view" rating having an average price greater than or equal to $350,000

Runtimes were calculated for each of the above queries.

## Caching the Data

Next we cached the temporary table we created in the previous step, checked to see if the table was cached, and ran the last query again to compare the runtime. The original runtime was 1.41 seconds and the runtime with the cached data was improved to .91 seconds.

## Partitioning the Data

Lastly we partitioned the data by the "date_built" field, read the data into a DataFrame, created a temporary view for the partitioned data, and ran the last query again. The runtime for the partitioned data was .54 which is significantly better than the previous two runtimes.

## Uncaching the Data

At the end of the Session, we uncached the temporary table and checked to make sure the table was uncached.

