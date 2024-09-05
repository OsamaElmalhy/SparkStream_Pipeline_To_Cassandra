# Spark Streaming from API with Airflow, Kafka, Cassandra, Control Centre, and Schema Registry

## Overview
This project demonstrates the process of setting up a data pipeline for streaming data from an API into Apache Spark using a variety of technologies. These include:

- Apache Airflow for orchestrating workflows
- Apache Kafka for messaging
- Apache Cassandra for data storage
- Confluent Control Centre for monitoring
- Schema Registry for managing schemas

The pipeline ensures real-time processing and storage of data, providing scalability and fault-tolerance.

## Steps to Setup and Run the Project

### Step 1: Environment Setup
- Use Docker to pull images for Apache Kafka, Apache Cassandra, Apache Airflow, Confluent Control Centre, and any necessary dependencies.
- Ensure proper configuration of Docker containers to facilitate communication between Kafka, Cassandra, and Airflow.

### Step 2: Start Kafka and Cassandra Clusters
- Launch the Docker containers for Apache Kafka and Apache Cassandra.
  - Kafka will handle messaging.
  - Cassandra will store the processed data.

### Step 3: Define Airflow DAGs
- Create Airflow DAGs to define the workflow for the pipeline:
  - Fetch data from the API.
  - Send the data to Kafka.
  - Process the data using Spark Streaming.
  - Store the processed data in Cassandra.

### Step 4: Configure Airflow
- Configure Airflow to manage task sequencing and dependencies.
- Set up scheduling in Airflow to trigger the pipeline execution according to the desired interval or condition.

### Step 5: Run the Pipeline
- Start the pipeline by initiating Airflow.
- Airflow will execute the tasks defined in the DAGs based on the configured schedule and task dependencies.

### Step 6: Monitor the Pipeline
- Use the Airflow UI to monitor the task execution and dependencies in real-time.
- Monitor Kafka clusters and topics with Confluent Control Centre to ensure proper data flow through the pipeline.

### Step 7: Access Processed Data
- The processed data can be accessed in the Cassandra database.
- Analyze the data or use it according to the project’s needs.

---

This setup ensures the integration of various components, enabling real-time data streaming, processing, and storage.
