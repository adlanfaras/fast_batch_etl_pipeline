# Fast Batch ETL Pipeline

## Overview

This project is a fast and efficient batch ETL (Extract, Transform, Load) pipeline designed to handle large volumes of data with minimal latency. The pipeline is built to be scalable, reliable, and easy to configure for various data sources and destinations.

## Features

- **High Performance**: Optimized for fast data processing and minimal latency using Apache Spark.
- **Scalability**: Easily handles increasing volumes of data with distributed processing.
- **Modular Design**: Easy to extend and customize with a plug-and-play architecture.
- **Data Transformation**: Utilizes dbt (Data Build Tool) for transforming data.
- **Error Handling**: Robust mechanisms to handle and log errors.
- **Configurable**: Simple configuration for different data sources and targets using YAML.
- **Data Storage**: Supports multiple destinations including AWS S3, Google BigQuery, and relational databases.

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/fast-batch-etl-pipeline.git
    cd fast-batch-etl-pipeline
    ```

2. Install dependencies:
    ```sh
    pip install -r requirements.txt
    ```

## Usage

1. Configure your data sources and destinations in the `config.yaml` file.
2. Run the ETL pipeline:
    ```sh
    python main.py
    ```

## Configuration

Edit the `config.yaml` file to set up your data sources, transformations, and destinations. Example configuration:

```yaml
sources:
  - type: mysql
    host: your-database-host
    port: 3306
    database: your-database
    username: your-username
    password: your-password

transformations:
  - type: dbt
    project_dir: path/to/dbt/project
    profiles_dir: path/to/dbt/profiles

destinations:
  - type: s3
    bucket: your-s3-bucket
    path: /data/output/
