# Spark Docker Setup and Execution

This project demonstrates how to set up Apache Spark on a Docker container and perform basic operations using Python and Spark's PySpark library. Follow the steps below to replicate the setup and execution.

---

## Prerequisites

First I Ensured the following are installed on my system:
   **Java**: OpenJDK 1.8 or above
   ```bash
   java -version
   ```
   Output:
   ![6D1669AC-128A-4984-84B5-CB950D7675F4_1_201_a](https://github.com/user-attachments/assets/d3dc1c72-edff-40ba-a987-9d004cacfe8a)


   **Python**: Python 3.9 or above
   ```bash
   python3 --version
   ```
   Output:
   ![6D1669AC-128A-4984-84B5-CB950D7675F4_4_5005_c](https://github.com/user-attachments/assets/f29f2c76-ddf6-4b2a-ae00-8d9a1b8f6bc9)


---

## Setting Up Apache Spark

   **Download and Extract Spark**:  
   Placed the extracted Spark folder on my Desktop.

   **Set the SPARK_HOME environment variable**:  
      ![6D1669AC-128A-4984-84B5-CB950D7675F4_1_201_a](https://github.com/user-attachments/assets/ae263964-2b99-4ec2-8c3a-362d98fbe3c6)

   **Verify Spark Installation**:  
   I Run the following command to check if Spark is correctly installed:
   - Spark Shell (Scala):
     ```bash
     spark-shell --version
     ```
     Output:
      ![6D1669AC-128A-4984-84B5-CB950D7675F4_1_201_a](https://github.com/user-attachments/assets/d88daf35-2165-45a4-8cdc-d7b47a675599)

     
   - PySpark:
     ```bash
     pyspark
     ```
     <img width="1599" alt="Screenshot 2024-12-13 at 8 12 02 PM" src="https://github.com/user-attachments/assets/272b9391-23a8-44d0-b9f7-5f3f4b0d4f4c" />

   Run a PySpark example:
   Placed the Python script (`EDA_netflix.py`) in the Spark folder and execute:
   ```bash
   python EDA_netflix.py
   ```
   Output : "Run python file to get output"


# Pulling Docker Image for Spark

   **Runing my Python script:**
   running command **"python EDA_netflix.py"**

   Output:

   <img width="1169" alt="Screenshot 2024-12-14 at 1 19 29 AM" src="https://github.com/user-attachments/assets/396664ab-b46c-4104-9217-3ea32e553b5d" />

## Setting Up Apache Spark Environment

### Verifying the Spark Docker Container

   **Run the Apache Spark Docker Container**
   ```bash
   docker run -it --rm apache/spark-py /bin/bash
   ```

   The output confirms the container is running:

   <img width="1169" alt="Screenshot 2024-12-14 at 1 19 48 AM" src="https://github.com/user-attachments/assets/3ed55765-40d4-4acb-9219-347fde0ebde8" />

   **Verify Spark Version**

   Re-run the version command: **spark-submit --version**

   <img width="702" alt="Screenshot 2024-12-14 at 1 20 04 AM" src="https://github.com/user-attachments/assets/b87ef70f-7502-476b-8dba-d33ae4ed16a3" />

## Copying Files to the Docker Container

To transfer necessary files (EDA_netflix.py and netflix_titles.csv) into the container:

<img width="1271" alt="Screenshot 2024-12-14 at 1 36 00 AM" src="https://github.com/user-attachments/assets/7fd00c37-271a-46df-b2b8-0c1c6320745f" />

### Docker image created visible on Docker UI

<img width="1680" alt="Screenshot 2024-12-14 at 1 36 06 AM" src="https://github.com/user-attachments/assets/5583ff36-6f1a-4136-9c74-20042bd55cf3" />

### Verified Files have been transfered to Container

<img width="564" alt="Screenshot 2024-12-14 at 1 37 34 AM" src="https://github.com/user-attachments/assets/1f044f18-f604-4fbb-a0b6-d3d69ac52a40" />


# Running the Script in Docker

To execute the EDA script, the following command was used by me:

Command:
**/opt/spark/bin/spark-submit --driver-memory 2G --executor-memory 2G /opt/spark/work-dir/EDA_netflix.py**

The output from the Spark job includes the following information:

1. Total records: The total number of rows in the dataset (8809 in this case).
2. A table showing the number of missing values in each column and the percentage of missing values relative to the total number of rows.
3. A table summarizing various statistics for each column, including:
count: The number of non-null values.
mean: The average value (applicable to numeric columns).
stddev: The standard deviation (applicable to numeric columns).
min: The minimum value.
max: The maximum value.
4. A list of all unique values found in the "type" column.
5. A table showing the number of entries for each unique value in the "type" column.
6. A table showing the top 10 countries with the most entries in the "country" column.
7. A table showing a sample of the "release_year" distribution (top 10 rows).
8. A sample of the data for US movies, showing the same columns as the original data sample.







