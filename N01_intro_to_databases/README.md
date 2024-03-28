# Intro to Databases

# What is Database?

- A database is a system to store and manage data in a structured and very efficient way.
- In your code you already have variables, dictionaries, lists, etc. They all store data in some way already. <b>Why would you need to have a separate database?</b>
  - Here your code is <b> static </b>, it doesn't really change over time once you run it
  - Modifications to the code occur only during development stages.
  - Once the Python program starts running, it maintains its state until terminated.
  - Changes in the code take effect only after re-running the program.

## Operations to do with data?

In many cases, you need your program to be able to <b>create</b> and store data, <b>read</b> it, <b>update</b> it, <b>delete</b> it, etc.

## Problems to handle data in your code:

- Scalability Issue: Hard to handle large amounts of data efficiently

* <b>Data Integrity:</b> Difficult to keep data accurate and consistent.
* <b>Concurrency Problems:</b> Managing simultaneous data access and changes is challenging.
* <b>Security Risks:</b> Protecting data from unauthorized access becomes complex.
* <b>Backup and Recovery:</b> Creating reliable data backup and restore processes is tough.
* <b>Maintenance Difficulty:</b> Updating and fixing data-related code gets harder over time.
* <b>Performance Limitations:</b> Data access and processing may be slow.
* <b>Analysis Challenges:</b> Conducting complex data analysis is unmanageable.

## Solution of above problems:

<b>Databases</b> are designed to solve these problems, making the process of handling data much more efficient, and independent of your code.

## How to interact with Database?

- Single file database: Manage data efficiently in a compact, easy-to-access file, streamlining data storage, retrieval, and maintenance in a simplified database format. E.g SQLite
- Server Database: Deploy a database as an application on a server, where it operates on multiple files in optimized formats, similar to a web server but with specialized communication protocols for efficiency. This setup allows your code to interact with the database server, potentially located on a different machine, rather than directly handling files. Our code will interact with database application and that database application will read and modifies its data files because it is more efficient then our code. E.g PostgreSQL, MySQL, or MongoDB.
* Distributed servers: Implement a group of server applications across multiple machines to enhance efficiency and data handling capacity, allowing your code to interact with one or multiple servers, while being aware of the complexities introduced by distributed systems

# Database Categories:

- <b>SQL Databases</b> and <b>NoSQL Databases</b>

## SQL Database:

- In SQL database we store the data in form of table.
- Table is just data in a grid, with different columns and rows, pretty much like a single spreadsheet.
  - Row represent a specific item or record
  * Column represent a specific attribute or field of that record.
