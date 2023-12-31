# ETL-Airflow-pipeline-S3_Snowflake_mail
Build and Automate loading data from S3 to Snowflake with email notification using airflow

![Screen Shot 2023-12-30 at 9 00 59 PM](https://github.com/devaa07/ETL-Airflow-pipeline-S3_Snowflake_mail/assets/126756574/968bfb67-454b-4117-a283-331fc67eb327)


# Step 1: Creating an EC2 instance and assign the key-value pair and security-group

# Step 2: Install the required dependencies on EC2 instance
        sudo apt update
        sudo apt install python3-pip
        sudo apt install python3.10-venv
        python3 -m venv airflow_snow_venv
        source airflow_snow_venv/bin/activate
        sudo pip install apache-airflow
        pip install apache-airflow-providers-snowflake
        pip install snowflake-connector-python
        pip install snowflake-sqlalchemy
        pip install apache-airflow-providers-amazon

# Step 3: create the S3 bucket and create a folder inside the bucket

# Step 4: create the dag folder inside airflow folder and create the DAG code
          airflow_snowflake_s3_email.py

# Step 5: Create the Snowflake Database, warehouse, schema, stage and file format inside the snowflake

![Screen Shot 2023-12-30 at 9 20 18 PM](https://github.com/devaa07/ETL-Airflow-pipeline-S3_Snowflake_mail/assets/126756574/5194b887-ab82-4803-97bf-4d466ccfa6f5)

# Step 6: Update the DAG code and create the snowflake connection id with airflow (conn_id_snowflake) and test the connection.

<img width="1423" alt="Screen Shot 2023-12-30 at 9 23 18 PM" src="https://github.com/devaa07/ETL-Airflow-pipeline-S3_Snowflake_mail/assets/126756574/65ab7c82-0b69-4ae0-ad1e-fb4e4abe8340">

# Step 7: Login into gmail and create the APP(Mail) and it generate the password. copy the password for future use.

![Screen Shot 2023-12-30 at 9 25 32 PM](https://github.com/devaa07/ETL-Airflow-pipeline-S3_Snowflake_mail/assets/126756574/28042033-9052-4796-80e7-0d1cef43f64a)

# Step 8: Go to airflow.config file and change the email settings. 

![Screen Shot 2023-12-30 at 9 26 33 PM](https://github.com/devaa07/ETL-Airflow-pipeline-S3_Snowflake_mail/assets/126756574/d6fa5004-ef17-49c1-a99f-0a0a15a1aec8)

# Step 9: Update the email related python code inside the DAG file and trigger the DAG. Verify the email and that's it !!

![Screen Shot 2023-12-30 at 9 27 53 PM](https://github.com/devaa07/ETL-Airflow-pipeline-S3_Snowflake_mail/assets/126756574/60f0dee9-c0d7-4700-8ef9-19e09523767f)





