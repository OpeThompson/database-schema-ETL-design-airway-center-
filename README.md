# database-schema-ETL-design-airway-center-
This project showcases a database solution for the Airways Disease Research Center. It features an ETL pipeline for loading clinical data into PostgreSQL, MongoDB for unstructured data, and a CI/CD pipeline for automated deployment using Jenkins.
# Airways Disease Research Center Database

This repository contains the code and resources for setting up a relational and NoSQL database for the Airways Disease Research Center at the Pulmonology Department, Wake Forest University School of Medicine.

## Features:
- PostgreSQL and MongoDB integration.
- ETL pipeline for loading clinical data into PostgreSQL.
- NoSQL solution using MongoDB to store unstructured research data.
- Automated CI/CD pipeline for database deployment.

## Directory Structure:
- `/data/` - Contains the sample CSV files with mock patient and clinical trial data.
- `/scripts/` - Includes the ETL pipeline code, database schema creation scripts, and MongoDB integration code.
- `/ci-cd/` - CI/CD pipeline setup using Jenkins for automating database deployments.
- `requirements.txt` - List of required Python libraries.

## Getting Started

### Prerequisites:
- PostgreSQL installed locally or in the cloud (e.g., AWS RDS).
- MongoDB (local or Atlas cloud version).
- Python 3.x with `pandas`, `sqlalchemy`, `psycopg2`, and `pymongo` installed.

### Setting Up PostgreSQL

1. Clone this repository:
    ```bash
    git clone https://github.com/your-username/airways-disease-research-center.git
    cd airways-disease-research-center
    ```

2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Run the database schema script:
    ```bash
    psql -h localhost -U postgres -d airways_research_center -f scripts/create_tables.sql
    ```

4. Run the ETL pipeline to load sample data:
    ```bash
    python scripts/etl_pipeline.py
    ```

### MongoDB Setup

1. Ensure MongoDB is running locally or on Atlas cloud.
2. Run the MongoDB loading script:
    ```bash
    python scripts/mongo_load.py
    ```

### CI/CD Pipeline

The repository includes a Jenkinsfile for setting up automated deployments using Jenkins. The CI/CD pipeline will:
- Test the ETL process.
- Deploy schema changes and load data.

