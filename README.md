# 🎧 Spotify API End-to-End Data Engineering Project Using AWS and Python

## 📌 Introduction
This project demonstrates a fully automated **ETL (Extract, Transform, Load)** pipeline using the **Spotify API** on **AWS Cloud**. The pipeline is designed to retrieve data about songs, albums, and artists from the Spotify API, process and clean the data using Python, and load it into an AWS data store for querying and analytics.

## 🧩 Architecture
![Spotify_ETL_Architecture](https://github.com/gurramcharan/spotify-api-End-to-End-ETL-using-AWS-Python/blob/main/spotify_api_etl_architecture.jpg)

## 🔁 Project Execution Flow
**Extract data from Spotify API → Trigger Lambda function (every 1 hour) → Store raw data in S3 → Trigger transform Lambda → Clean and format data → Load transformed data into S3 → Run AWS Glue Crawler → Update AWS Glue Data Catalog → Query using Amazon Athena**

## 📂 Dataset / API Details
We use the [Spotify Web API](https://developer.spotify.com/documentation/web-api), which provides structured metadata about:
- 🎤 Music Artists  
- 💽 Albums  
- 🎵 Songs  

## 🚀 AWS Services Used
- **Amazon S3**: Used as the main data lake to store raw and transformed JSON/CSV files.
- **AWS Lambda**: Serverless compute that handles scheduled data extraction and transformation logic.
- **Amazon CloudWatch**: Monitors the Lambda executions and logs performance, errors, and invocations.
- **AWS Glue Crawler**: Automatically scans the S3 bucket and updates the schema for downstream analytics.
- **AWS Glue Data Catalog**: Acts as a metadata repository that helps Athena understand the structure of the data.
- **Amazon Athena**: Serverless query service used to run SQL queries directly on the data stored in S3.

## 🛠️ Packages Used
```bash
pip install pandas
pip install numpy
pip install spotipy
```
