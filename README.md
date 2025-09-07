
---

# Spotify Dataset Analysis using SQL

## 🎵 Project Overview

This project provides a comprehensive analysis of a Spotify dataset using SQL. It explores various aspects of music tracks, artists, and albums to uncover insights through a series of queries. The script is structured to demonstrate a progression of SQL skills, with queries organized into **Easy**, **Medium**, and **Advanced** levels of complexity.

The analysis answers key business questions such as identifying top-performing tracks, understanding audio feature distributions, and comparing platform performance.

---

## 📊 Dataset

The analysis is performed on a single table named `spotify`. This table contains detailed information about tracks, including:

* **Track Metadata**: `track`, `artist`, `album`, `album_type`, `duration_min`
* **Performance Metrics**: `views`, `likes`, `comments`, `stream`
* **Audio Features**: `danceability`, `energy`, `liveness`, `tempo`, `valence`
* **Platform-Specific Data**: `channel`, `licensed`, `official_video`, `most_played_on`

The initial part of the script includes basic data exploration and a cleaning step to remove entries with a duration of zero.

---

## 🛠️ SQL Analysis & Queries

The SQL script is broken down into three main sections based on query complexity.

### Easy Level

This section covers fundamental SQL operations for basic data retrieval and aggregation.
* **Retrieve** tracks with over 1 billion streams.
* **List** all unique albums and their corresponding artists.
* **Calculate** the total number of comments for licensed tracks.
* **Count** the total number of songs released by each artist.

### Medium Level

This section introduces more complex calculations, groupings, and conditional logic.
* **Calculate** the average danceability score for tracks in each album.
* **Find** the top 5 tracks with the highest energy values.
* **Identify** tracks streamed more frequently on Spotify than on YouTube.
* **Aggregate** total views for all tracks associated with each album.

### Advanced Level

This section demonstrates the use of advanced SQL techniques like window functions, subqueries, and Common Table Expressions (CTEs).
1.  **Top 3 Tracks per Artist**: Uses the `DENSE_RANK()` window function to find the top 3 most-viewed tracks for every single artist.
2.  **Above-Average Liveness**: Employs a subquery to filter for tracks where the liveness score is higher than the overall average across all songs.
3.  **Album Energy Range**: Uses a `WITH` clause (CTE) to efficiently calculate the difference between the highest and lowest energy values for tracks within each album.

---

## 💡 Key SQL Concepts Demonstrated

This project showcases proficiency in a wide range of SQL concepts, including:

* **Data Definition Language (DDL)**: `CREATE TABLE`
* **Data Manipulation Language (DML)**: `DELETE`
* **Aggregate Functions**: `COUNT()`, `SUM()`, `AVG()`, `MAX()`, `MIN()`
* **Filtering and Sorting**: `WHERE`, `ORDER BY`, `LIMIT`
* **Grouping Data**: `GROUP BY`
* **Advanced Techniques**:
    * **Window Functions**: `DENSE_RANK() OVER (PARTITION BY ...)`
    * **Common Table Expressions (CTEs)**: `WITH` clause
    * **Subqueries**
    * **Conditional Logic**: `CASE` statements
    * **Handling Nulls**: `COALESCE`

---

## 

1.  **Schema Setup**: Use the `CREATE TABLE spotify (...)` statement from the `.sql` file to create the table structure in your SQL database (e.g., PostgreSQL, MySQL, SQL Server).
2.  **Data Ingestion**: Populate the newly created table with the Spotify dataset.
3.  **Execute Queries**: Run the queries from the file individually to explore the data and see the analysis in action.# Spotify-Advance-SQL-Project
