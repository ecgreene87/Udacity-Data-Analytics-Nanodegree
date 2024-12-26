# Purpose of database

The Sparkify database will serve as a centralized structured repository for song and user activity data that they have been collecting. By modeling this data in a relational database using PostgreSQL, the company can transition from a unstructured JSON files to a format that is optimized for analytical queries. </p>


# Analytical Goals

1. Understand what songs users are listening to
2. Run queries to analyze user activity


# How to run scripts

1. Run --create_tables.py-- to start the database
2. Run --test.ipynb-- to ensure all tables were created properly. Restart Kernel
3. Run --etl.pbynb--
4. Run --create_tables.py-- to restart the database
5. Run --etl.py-- to start the ETL pipeline



# File descriptions

--data-- folder that contains song and log data
--sql_queries.py-- repository of SQL queries used in other files
--create_tables.py-- drops and recreates database environment using queries from sql_queries.py 
-test.ipynb-- series of tests to verify proper creation of database tables
--etl.ipynb-- reads and processes files from song_data and log data and loads them into tables
--etl.py-- performs data extraction from song_data and log_data<


# Schema Design

The schema for Sparkify's database is the star schema. The schema consists of one fact table and several dimension tables. This type of schema simplifies queries and ensure normalization of the database.

# ETL Pipeline

Extract - Read JSON files(log_data, song_data)
Transform - Format data to match the schema
Load - Insert data into SQL tables and execute queries<
