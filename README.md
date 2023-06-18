# NOT FINAL README

# Building a SQL Database

## Table of Contents
- [Introduction](#introduction)
- [Scraping Information](#scraping-information)
- [Table Creation and Relationship Definition](#table-creation-and-relationship-definition)
- [Connecting SQL Database to Python](#connecting-sql-database-to-python)

## Introduction

In this project, my goal is to create a new SQL database using MySQL and Sequel Ace while delving into the fundamental concepts of primary keys, foreign keys, and best practices for Relational Database Management Systems (RDBMS). To make the learning experience more engaging and practical, I have chosen to create a database specifically for the Pokemon Trading Card Game. By using this popular game as an example, I aim to provide a concrete context for understanding and implementing these important database concepts.

Key objectives include;
1.) Scraping information from a specific website 
  * [Bulbapedia](https://bulbapedia.bulbagarden.net/wiki/Main_Page)
  *
2.) Define the tables and their relationship.
  * card_energy_types, cards, cardtype, energy_types, expansions, rarity, sets.

3.) Establish a connection between the SQL database and Python for data storage and querying.
  * import mysql.connector



## Scraping Information
The first step of this project involved scraping information from the website [Bulbapedia/wiki/expansions](https://bulbapedia.bulbagarden.net/wiki/List_of_Pokémon_Trading_Card_Game_expansions).
The target was to retrieve specific data that would be stored in the SQL database.

Key objectives include;
1.) Explore pages, find valuable data, determine expansion, and set names.

2.) Understand links, tables, and HTML structure.

3.) Use Selenium to gather pages, and use BS4 to create html soup. Begin to extract information and create meaningful data.

## Table Creation and Relationship Definition
Once the necessary data was scraped, the next step was to create tables in SQL. The SQL language was employed to design and define the tables required for storing the scraped information. Relationships between the tables were established to represent the connections and dependencies between different entities within the database. This step involved careful consideration of the data structure and design to ensure optimal organization and efficiency.

Key objectives include;
1.) Create a cards table to hold the main item
 * Primary Key ID (Auto-Increment), Serial Number, Card Name, Rarity, and Set.

2.) Expansion, Set, Rarity, Energy, tables
 * Primary Key, REF / FOREIGN KEY
  

## Connecting SQL Database to Python
To integrate the SQL database with Python, a connection needed to be established between the two. The Jupyter Notebook environment was utilized to facilitate this connection. Python scripts were written to connect to the SQL database and enable the transfer of data from the scraped information. Queries were executed within the notebook, allowing for seamless interaction with the SQL database and retrieval of desired information.

Key objectives include;
1.) Create a file to store credentials to a SQL server. (Username and Password) 
 * env.py

   
2.) Establish a connection from Python to MySQL.
   * '''
    connection = mysql.connector.connect(
    host='localhost',
    user= username,
    password=password,
    database='PokemonTCG'
    '''

3.) Create a Script to send all information from dataframe to tables.
 * Send Serial Number
 * Send Card Name
 * Send Rarity
 * Send Set


## Conclusion
This project aimed to document the learning process and creation of an SQL database. By scraping data from a specific website, defining table relationships, and connecting the SQL database to Python, a comprehensive understanding of the database creation process was achieved. This README provides an overview of the project's key points and serves as a guide for anyone interested in exploring the steps taken to learn and create an SQL database.
