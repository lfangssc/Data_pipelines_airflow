# udacity_data_pipelines_airflow
## Project: Data Pipelines with Airflow
A music streaming company, Sparkify, has decided that it is time to introduce more automation and monitoring to their data warehouse ETL pipelines and 
come to the conclusion that the best tool to achieve this is Apache Airflow.

## Datasets
This project provides two datasets. Here are the s3 links for each:
- Log data: s3://udacity-dend/log_data
- Song data: s3://udacity-dend/song_data

## Project Template
The project template package contains three major components for the project:
- The dag template has all the imports and task templates in place, and the task dependencies. 
- The operators folder with operator templates
- A helper class for the SQL transformations

The tree structure of the files

    - dags: 
            - udacity_example_dag.py
    - plugins:
            - helper: sql_queries.py
    - operators:
             - data_quality.py
             - load_dimension.py
             - load_fact.py
             - stage_redshif.py
    - create_tables.sql
    
    
 ## Deployment
 1. setup redshift and get endpoint, db_name(in airflow named as Schema), login info.
 2. in ariflow UI connections, create conn_id=aws_credentials and conn_id=redshift
 3. start the DAG by switching the state on/off
