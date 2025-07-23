# 📊 MovieLens 100K Analysis with Apache Spark and Cassandra

## 📁 Course
**STQD6324 – Data Management**  
**Semester 2, 2024/2025**

## 📌 Objective
This project analyzes the [MovieLens 100K Dataset](https://grouplens.org/datasets/movielens/) using **PySpark (Spark 2)** and **Apache Cassandra** to execute a set of analytical queries through a reproducible data pipeline.

---

## 🚀 Technologies Used
- Python
- Apache Spark 2
- Apache Cassandra
- HDFS
- PySpark (RDDs and DataFrames)
- Zeppelin

---

## 📂 Dataset
Files used:
- `u.user`: User information
- `u.data`: Ratings (user ID, movie ID, rating)
- `u.item`: Movie metadata and genres

---

## 📈 Tasks Completed

1. **Load and Parse Data**
   - Parsed and uploaded `u.user`, `u.data`, and `u.item` into HDFS.
   - Converted raw files into RDDs and then into DataFrames.
   - Stored the data into Apache Cassandra keyspace `movielens`.

2. **Write and Read from Cassandra**
   - Written tables: `users`, `ratings`, and `titles`.
   - Verified by reading back into Spark.

3. **Queries Executed**
   - i. **Average rating for each movie**
   - ii. **Top 10 movies with the highest average rating**
   - iii. **Identify users (≥ 50 ratings) and their favourite movie genre**
   - iv. **List users younger than 20**
   - v. **List scientists aged 30–40**

---

## 🧪 Reproducibility
The script ensures reproducibility by:
- Cleaning the target directory before downloading new files.
- Parsing functions are modular and reusable.
- Outputs and queries are consistent for every execution.

---

## 🗃️ Keyspace & Table Structure (Cassandra)
- **Keyspace**: `movielens`
- **Tables**:
  - `users(user_id, age, gender, occupation, zip)`
  - `ratings(user_id, movie_id, rating)`
  - `titles(movie_id, title, genre_columns...)`

---

## 📊 Example Output
- Users under 20  
- Top genre per user with ≥ 50 ratings  
- Top 10 movies by average rating

---

## 📝 How to Run

1. Ensure **Spark 2** and **Cassandra** are running.
2. Upload the MovieLens files to `hdfs:///tmp/ml-100k/`.
3. Run the notebook or script step-by-step:
   - Parsing → DataFrames → Write to Cassandra → Read → Queries

---

## 🧾 License
This project is for educational purposes under the Data Science Master's program at UKM.

---

## 👨‍💻 Author
Hazim Fitri  
Master's in Data Science & Analytics  
