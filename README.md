# Spark and PySpark

This guide documents the setup process for Apache Spark and PySpark on a macOS system, followed by a simple example.

---

## Prerequisites

First We Ensured the following are installed on my system:
1. **Java**: OpenJDK 1.8 or above
   ```bash
   java -version
   ```
   Output:
   ![6D1669AC-128A-4984-84B5-CB950D7675F4_1_201_a](https://github.com/user-attachments/assets/d3dc1c72-edff-40ba-a987-9d004cacfe8a)


2. **Python**: Python 3.9 or above
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
   Place the Python script (`EDA_netflix.py`) in the Spark folder and execute:
   ```bash
   python EDA_netflix.py
   ```
   Output : "Run python file to get output"


# Pulling Docker Image for Spark

   **Run your Python script:**
   running command **"python EDA_netflix.py"**

   Output:

   <img width="1169" alt="Screenshot 2024-12-14 at 1 19 29 AM" src="https://github.com/user-attachments/assets/396664ab-b46c-4104-9217-3ea32e553b5d" />




