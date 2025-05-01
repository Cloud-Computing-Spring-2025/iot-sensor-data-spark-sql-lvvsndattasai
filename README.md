This project demonstrates how PySpark and Spark SQL can be used to analyze IoT sensor data effectively. The pipeline involves data loading, cleaning, aggregation, time-based pattern discovery, sensor ranking, and pivot-based analysis.

---

## Project Overview

- **Dataset**: `sensor_data.csv`
- **Tools Used**: Apache Spark (PySpark), Spark SQL, Python 3.11, macOS (Anaconda environment)
- **Goal**: Gain actionable insights from IoT sensor readings, focusing on temperature and humidity trends.

---

## Tasks Breakdown

### Task 1: Load Data & Explore

- Loaded `sensor_data.csv` into Spark DataFrame
- Previewed 5 sample rows
- Counted total entries: **10**
- Identified unique locations

**Output**: `task1_output.csv`

---

### Task 2: Filter & Aggregate

- Filtered temperatures between **18°C and 30°C**
  - Valid Records: **7**
  - Outliers: **3**
- Calculated average temperature and humidity per location

**Output**: `task2_output.csv`

---

### Task 3: Time-Based Trends

- Converted timestamps to proper `timestamp` type
- Extracted `hour_of_day` from each entry
- Computed average temperature for each hour

**Output**: `task3_output.csv`

---

### Task 4: Sensor Ranking

- Calculated average temperature per `sensor_id`
- Applied `dense_rank()` for descending temperature order

**Output**: `task4_output.csv`

---

### Task 5: Pivot Table Analysis

- Created pivot: `location` vs `hour_of_day`
- Highlight: **BuildingA_Floor1 at 8 AM** recorded highest temperature of **34.5°C**

**Output**: `task5_output.csv`

---

## Summary

By leveraging Spark SQL, we uncovered:
- Temperature patterns by hour
- High-performing and underperforming sensors
- Location-based climate trends

---
