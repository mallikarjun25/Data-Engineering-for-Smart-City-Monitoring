# Smart City Monitoring System

## Overview
This repository contains the codebase for a Smart City Monitoring System, which aims to process and analyze real-time data streams from various sources within smart cities. The system utilizes Apache Spark Structured Streaming for data processing, Apache Kafka for data streaming, and Amazon S3 for data storage. The project includes Python scripts for data generation, Spark scripts for data processing, and Docker configurations for deployment.

## Contents
- `main.py`: Python script for generating simulated vehicle movement data and producing it to Kafka topics.
- `spark-city.py`: Spark script for processing streaming data from Kafka topics and writing it to Amazon S3.
- `docker-compose.yml`: Docker configuration file for deploying Kafka, Spark, and other services.
- `Smart city analysis report.pbix`: Power BI dashboard report
- `requirements.txt`: Python dependencies required for running the project.
- `README.md`: Instructions and overview of the project.

## Project Architecture
The Smart City Monitoring System efficiently processes real-time data streams using Apache Kafka and Spark. Data is ingested from various sources, including vehicle sensors, GPS devices, traffic cameras, weather stations, and emergency systems. The processed data is stored in Amazon S3, where it can be analyzed and visualized using tools like PowerBI.

## Getting Started
1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/smart-city-monitoring.git
    ```

2. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. Set up Docker environment:

    ```bash
    docker-compose up -d
    ```

4. Run the data generation script:

    ```bash
    python main.py
    ```

5. Run the Spark streaming script:

    ```bash
    spark-submit --packages org.apache.spark:spark-sql-kafka-0-10_2.13:3.5.0,org.apache.hadoop:hadoop-aws:3.3.1,com.amazonaws:aws-java-sdk:1.11.469 spark-city.py
    ```

6. Monitor the data processing and analysis in the PowerBI dashboard.


## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
