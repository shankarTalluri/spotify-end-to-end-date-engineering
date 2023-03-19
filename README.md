# Spotify-End-to-End-Data-Engineering

## Intorduction 
### This include extracting data from spotify API , validate and tranform data from spotify web
### This pipeline extarct the data from Spotify API, extract required fields into dataframe and save it as JSON files on S3.
### Later this json files on S3 are used to read the JSON files and prepare the required files like album, songs, atrist and save them as CSV files

## Architecture
![Architecture Daigram](https://github.com/shankarTalluri/spotify-end-to-end-date-engineering/blob/main/Spotify_ETL_Project_Architecture.JPG)

### About Dataset /API
This API contains information about music Albums, Artists & Songs [API link](https://developer.spotify.com/documentation/)

### Services used
1. **S3 (Simple Storage service)** Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. You can use Amazon S3 to store and retrieve any amount of data at any time, from anywhere. 

2. **AWS LAMDA** AWS Lambda is a serverless compute service that runs your code in response to events and automatically manages the underlying compute resources for you.

3. **AWS Cloud Watch** it's monitoring serive for AWS resources and applications you run on them. We can use this to trigger the Lamda function based on file changes on S3.

4. **AWS Glue Crawler** it's fully managed service service that automatically crawls (reads) your data sources, identifies data formats and infers the schemas to create an AWS Glue Data Catalog

5. **AWS Data Catalog** it's fully managed metadata respository that makes it easy to discover and manage data on AWS. You can use Data catalog with other AWS services subch as **Athena**.
 
6. **AES Athena** it's interactive query service that makes it easy to analyse data in S3 using standard SQL. You can use Athena to analyse data in your Glue catalog oe S3 buckets

### install packages
```
pip install pandas
pip install spotify

```

### Project execution flow
Extract data from API --> trigger (Every one hours) --> Run Lamda function extract Code --> Store raw data in S3 as JSON files --> trigger (when ever file arrived into landing) --> Run tranform function --> Query data using Athena
