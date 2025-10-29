# Netflix-Data-Set
## Project Overview

This project focuses on performing data analysis and insight extraction from a Netflix dataset using Apache Hive.
The primary goal is to utilize Hive’s SQL-like querying capabilities to analyze key trends in Netflix content, such as genre popularity, release year trends, content type distribution, country-based insights, and director/actor contributions.
The project demonstrates how to manage structured entertainment data on a Big Data platform (Cloudera/Hadoop) and use HiveQL for large-scale analytical querying and decision-making.

## Dataset Description

# The dataset, netflix_cleaned.csv, contains detailed information about various movies and TV shows available on Netflix, including:

# Show ID

# Title

# Director

# Cast

# Country

# Date Added

# Release Year

# Rating

# Duration (Minutes/Seasons)

# Listed In (Genre)

# Description

# Type (Movie/TV Show)

##Objectives

# The key objectives of this project are:

# To import and store Netflix content data into Hive tables efficiently.

# To perform analytical queries on content trends and patterns.

# To extract meaningful business and content insights such as:

# Most common genres on Netflix.

# Top countries producing the most content.

# Trend of movie releases over the years.

# Average duration of movies.

# Most frequent directors or cast members.

# Distribution of Movies vs. TV Shows.

# Technologies Used

# Apache Hive

# Hadoop (Cloudera Environment)

# HiveQL (SQL-like Queries)

# CSV File Data Ingestion

# HDFS Storage

# Steps Performed

# Database and Table Creation

# Created a new Hive database named netflix_db.

# Designed a table schema to match the structure of netflix_cleaned.csv.

## Data Loading

Uploaded the CSV file to HDFS.

Loaded the data into the Hive table using the LOAD DATA INPATH command.

Data Exploration and Querying
Executed various HiveQL queries for analytical purposes:

SELECT COUNT(*) FROM netflix; → Total number of titles available on Netflix.

SELECT type, COUNT(*) FROM netflix GROUP BY type; → Distribution of Movies vs. TV Shows.

SELECT country, COUNT(*) FROM netflix GROUP BY country ORDER BY COUNT(*) DESC LIMIT 10; → Top 10 countries producing content.

SELECT listed_in, COUNT(*) FROM netflix GROUP BY listed_in ORDER BY COUNT(*) DESC LIMIT 10; → Most popular genres.

SELECT release_year, COUNT(*) FROM netflix GROUP BY release_year ORDER BY release_year; → Trends in content production over years.

SELECT director, COUNT(*) FROM netflix GROUP BY director ORDER BY COUNT(*) DESC LIMIT 5; → Most active directors.

SELECT AVG(duration) FROM netflix WHERE type='Movie'; → Average movie duration.

## Insight Visualization

#Used Hive outputs to create summary tables and charts for better interpretation of content trends.

## Key Insights

The majority of content on Netflix consists of Movies, with a smaller proportion of TV Shows.

The United States, India, and the United Kingdom are among the top contributors of Netflix content.

Dramas, Comedies, and Documentaries dominate the genre distribution.

Average movie duration is approximately 100 minutes, while TV shows mostly have 1–2 seasons.

The number of releases increased significantly after 2015, indicating growth in Netflix’s content library.

Certain directors and actors appear frequently, showing Netflix’s partnerships and recurring collaborations.

## Conclusion

This project demonstrates how Apache Hive can be leveraged for large-scale data analysis of entertainment datasets such as Netflix.
By integrating HiveQL queries with Big Data tools, analysts can uncover content trends, audience preferences, and production patterns that support strategic decisions in the entertainment industry.
The use of Hive on Cloudera/Hadoop showcases the scalability and efficiency of big data platforms in handling large datasets for analytical reporting.
