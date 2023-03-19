# Spotify-End-to-End-Data-Engineering

## Intorduction 
### This include extracting data from spotify API , validate and tranform data from spotify web
### This pipeline extarct the data from Spotify API, extract required fields into dataframe and save it as JSON files on S3.
### Later this json files on S3 are used to read the JSON files and prepare the required files like album, songs, atrist and save them as CSV files

## Architecture
![Architecture Daigram](https://github.com/shankarTalluri/spotify-end-to-end-date-engineering/blob/main/Spotify_ETL_Project_Architecture.JPG)

## Services used
1. **S3 (Simple Storage service)
2. **AWS LAMDA
3. **Cloud Watch for triggering
4. 
