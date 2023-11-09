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




