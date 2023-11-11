## Introduction
**Abstraction** - System hides certain details which makes the user interaction super easy.
eg - Car Driving, 
Tally software (this is a Business Software for commerce applications).

DBMS shows the user an "Abstract VIEW" of the data.

**Main Objective:**
This gives multiple users their own personalized view of the data according to their needs.


## Three Schema Architecture of a Database (3 Abstract Levels of a DB) :

**Schema** => Design

**1. Physical / Internal Level** :
• Lowest Level of Abstraction
• Low Level Data Structures Used
• It has **Physical Schema** which shows Physical Structure of a DB (like a blueprint).
• Shows how data is stored in a disk.
• Talks about: Storage Allocation, Data Compression, Encryption etc.
Goal: Make algorithms which allows us fast access to data.

**2. Logical / Conceptual Level**:
• Tells us how data looks logically, i.e. what data is stored in a DB and what relationships exist among those data.
• User at logical level does not need to know about the physical-level structures.
• Goal: Easy to use.
• Advantage - Physical Data Independance

**3. View Level / External Level**:
• Highest Level of Abstraction
• End users sit at the View Level
• We have a View Schema (sub schema) here, which shows different data and schemas (sub-schemas) to different end users, according to their needs.
• They provide *security restrictions* to avoid accessing and viewing unauthorized data. 

## Instance of a DataBase
At a particular point of time, what all information is stored in a DB and where is it stored in a Database is called an instance of a DataBase.
Data may change here over time.

Schema however does not change that frequently.

**DB Schema = Logical Schema (generally)**

Things that are stored inside a Logical (DB) Schema:
1. attributes of table
2. consistency constraints (eg. name should not be null). One should always have a primary key in a DB which uniquely identifies the data and **primary key should not be null, always.**
3. Relationships

We make apps and websites by referring to the logical schema.

## Data Models
It Provides a way to describe the design of a DB at logical level.

eg. ER Model, Relational Model, OO Model, Object Relational Data Model (OO Model + Relational Model) etc.

**Data Semantics - What is the meaning of the data**

## DataBase Languages
1. DDL (Data Definition Language) - Helps in defining the schema

2. DML (Data Manipulation Language) - It does, Retrieval, Insertion, Updation, and Deletion of information in a DB.

SQL has both DDL and DML features included inside it.

Query Language - A part of DML which has statements which requests the retrieval of information.

## Interface

If we have a database that understands SQL and our main code understands host languages like C, Cpp, Java, JS, Python etc. then we need an API (Application Programming **Interface**) to communicate between the two entities. 

Say java has an API called, JDBC (Java DataBase Connectivity) and Cpp has ODBC.
These 2 communicate with the DataBase.

## DBA (DataBase Administrator) 
A person who has access to both 
• the data and 
• the programs that access the data


#### IMP
DBA Functions:
• Schema Definition
• Storage Structure and Access Methods
• Schema and Physical Organisation Modifications
• Authorization Control (Kisko kya dikhana hai)
• Routine Maintainence - 
    • Periodic Backups
    • Security Patches (avoid getting hacked)
    • Any Upgrades

*DBA* works mostly in **Logical Level** and somewhat in *Physical level*.
*End user* works in *View Level*

## DBMS Application Architecture

1. Tier 1 Architecture - All client, Server and DB are in 1 machine.
eg. Localhost

2. Tier 2 Architecture - Has 2 parts, Client and Server
eg - Used in LAN based apps (used in home in a few devices only)
Client sends SQL query statements to the server via the network and API. Inside the server side, there is a DB which responds to that client's request. 

3. Tier 3 Architecture - Has 3 Parts, Client, App Server, and DB
eg - Used in www applications in the modern era all around the world.

Client Server here contacts with the App server while sending querries, which then contacts to the DB. The DB then responds back to App Server and the App server responds back to the Client Side.

Advantages - 
• Scalability increases due to diatributed application servers i.e. we can have many client and server side machines.
• Data corruption reduces due to inclusion of App Server layer in the middle.
• Client cannot access DB directly, hence it is more secure now.

