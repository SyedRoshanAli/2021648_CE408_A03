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
   ```
   Python 3.9.7
   ```

---

## Setting Up Apache Spark

1. **Download and Extract Spark**:  
   Place the extracted Spark folder on your Desktop or preferred location.

2. **Set the SPARK_HOME environment variable**:  
   Open your terminal and edit the `~/.zshrc` file:
   ```bash
   nano ~/.zshrc
   ```
   Add the following line:
   ```bash
   export SPARK_HOME=/Users/username/Desktop/Spark/spark-3.5.3-bin-hadoop3-scala2.13
   export PATH=$SPARK_HOME/bin:$PATH
   ```
   Save and exit. Then, source the file to update the terminal environment:
   ```bash
   source ~/.zshrc
   ```
   Confirm the variable:
   ```bash
   echo $SPARK_HOME
   ```
   Expected Output:
   ```
   /Users/username/Desktop/Spark/spark-3.5.3-bin-hadoop3-scala2.13
   ```

3. **Verify Spark Installation**:  
   Run the following commands to check if Spark is correctly installed:
   - Spark Shell (Scala):
     ```bash
     spark-shell --version
     ```
     Output:
     ```
     Welcome to
          ____              __
         / __/__  ___ _____/ /__
        _\ \/ _ \/ _ `/ __/  '_/
       /__ / .__/\_,_/_/ /_/\_\   version 3.5.3
          /_/
     ```

   - PySpark:
     ```bash
     pyspark
     ```
     Expected Python REPL with Spark context.

---

## Installing PySpark

1. Install PySpark using pip:
   ```bash
   pip install pyspark
   ```
   Verify installation:
   ```bash
   python -c "import pyspark"
   ```
   If no errors are shown, PySpark is installed successfully.

2. Run a PySpark example:
   Place the Python script (`EDA_netflix.py`) in the Spark folder and execute:
   ```bash
   python EDA_netflix.py
   ```


