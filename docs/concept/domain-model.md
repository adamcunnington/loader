# DOMAIN MODEL

## Introduction
The flow of data through the pipeline will be as follows:

Data Source -> Data Lake (Raw) -> Data Lake (Processed) -> Data Warehouse (Staging)

Let's explore each stage in detail:
- Data Source: A data source must be a storage technology that data can be extracted from with minimal business rules. More sources will be supported over time but APIs will remain out of scope; an upstream process must deal with extraction from the true source into a supported data source.
    - Data Set: We refer to a single extract of structured/semi-structured data from a data source as a data set.
    - Data Feed: Whilst a single extract of data is a data set, a data set is said to be part of a data feed. A data feed has a schema (can evolve so long as it is backwards compatible) and a configuration which describes rules that govern behaviour for processing a new data set and loading it into the data warehouse.
- Data Lake (Raw): The immutable storage location for totally untransformed data. Depending on the method used to extract data from the data source, we may know absolutely nothing about the data at this stage except for the number of files
- Data Lake (Processed): The immutable? storage location for data that has been ....