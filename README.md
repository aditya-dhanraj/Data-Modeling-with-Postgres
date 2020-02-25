# Sparkify Postgres ETL

This project extract, transform and loads 5 main informations from the Sparkify app (an app to listen to your favorite musics) logs:

- songplays
- users
- songs
- artists
- time - (timestamps breakdown into comprehensible columns)

With this structured database we can extract several insightful informations and can find several hidden patterns in listeners data.

## Objective 
You will learn three most useful concepts from this project

* Data modeling with Postgres
* Database star schema creation
* Building ETL PipeLine using python

# Running the ETL
First you must create the PostgreSQL database structure, by doing:

    python create_tables.py
    
After Creation parse the logs files:

    python etl.py

# Database Schema

The schema used for this exercise is the Star Schema: " One Fact Table surround by 4 Dimension Table "

[Database Schema!](img/StarSchema.PNG "Star Schema")

## The project file structure

We have a small list of files, easy to maintain and understand the Concept:

**sql_queries.py**   -  Contains all your sql queries to use throughout the ETL process 
**create_tables.py** -  File reponsible to create the schema structure into the PostgreSQL database
**etl.py**           -  Reads and processes files from song_data and log_data and load them into the tables.
**etl.ipynb**        -  The python notebook that was written to develop the logic behind the etl.py process.
**test.ipynb**       -  Displays the first few rows of each table, to certify if our ETL process was being successful (or not).

## Author
**Aditya Dhanraj** - [Linkedin Profile](https://www.linkedin.com/in/aditya-dhanraj).
