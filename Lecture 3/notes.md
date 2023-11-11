## Introduction
**ER Model - Entity Relationship Model** 
It is a type of data model (works at logical level). It represents real world with entities and relationships among those entities.

We need *attributes* to describe an entity.

**Attributes** define data (and Entity Set (see later)).

eg. Student => Entity
Attributes - Student ID, name, ph no., Address, Batch, course

Attributes are limited (to make the database neat and non bulky).

**Entity** - This is a *real world object* which is distinguishable from other objects.
eg Student, College etc

We can identify an entity uniquely.
Entity has a *Unique ID*.

Unique Attribute is also called **Primary Key**

## Entity Set
It is a set of entities of the same type that share the same properties or attributes.
eg Student, Customer of a bank

1 Student = Entity 
Many Students = Entity Set

In ER diagram, we use Entity and Entity Set Interchangebly.

## Relationships

They join 2 or more entities.

eg. Customer places Order

*Customer* and *Order* are Entities
*places* define the relationship between these 2 entities.

ER Diagram is like a blueprint of a DB.

Put consistency constraints in Attributes, such as:
- Domain
- Values
    - permitted values
    - non permitted values

These all make the DB consistent.

## Types of Attributes
 
