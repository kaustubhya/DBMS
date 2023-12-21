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
1. Simple - It cannot be divided further.
eg. Customer Account number, Student Roll no.

2. Composite - Can be divided into sub-parts
eg. Name of a person (divide into first, middle and last names), **Address**
User can refer either the entire component or a part of it.
In ER Diagram this attribute has many other sub attributes.

3. Single Valued - Attribute having only one value.
eg. Student ID, Loan Number of a loan

4. Multi Valued - Attributes having more than one value.
eg, Phone Number, Nominee name on some insurance.
Limit constraints (upper or lower limits) may be applied.
In ER Diagram, this attribute is encircled 2 times.

5. Derived - Value of this type of attribute may be derived from the value of other related attributes.
eg. Age (can be derived from DOB), loan age, membership period, etc.

In ER diagram, this attribute is encircled by a dotted ellipse.

## Null Value
Value is not assigned to an attribute.

Reason:
- Attribute may be NA (Non Applicable)
- Attribute may be Unknown (missing)
- Attribute may be Not Unknown (Not Unknown YET)

## Entity Types

Let us see the entity types:
1. Strong Entity - It has an independent existence inside the DB.
eg. Student inside a University
It can be recognised by a Primary Key.
(say Student_Id)

2. Weak Entity - It is dependent on a Strong Entity.
It can not be recognised by a Primary Key.
If there is no strong entity, a weak entity can not exist here.
eg. Loan - Strong Entity
Payment - Weak Entity

Weak Relation - Concentric Diamonds ◈
Dotted Line - Weak Primary Key 
Weak Entity - Concentric Rectangles 
(see image)

Strong relation egs:
- Customer places order
- Professor teaches course

## Degree of Relation
How many entities participate in a particular relationship.

Types:
- Unary - Only 1 participant
eg. In an organisation, employee only manages employee

- Binary - 2 participants
eg. Customer places order (seen before)

- Ternary - 3 participants 
eg. Employee-Job-Branch (see image)

Ternary and Unary very rare. Binary very common.

## Relationship Constraints

1. Mapping Cardinality - Number of entities to which another entity can be associated via a relationship. 

    - One to One (1 : 1) - eg. Citizen has Adhaar Card (One Citizen has only 1 adhaar card and one aadhar card belongs to a unique citizen)
    This has a mapping cardinality of 1.

    A → B (only one relation) (see figure)

    - One to Many (1 : N) - eg. Citizen  has Vehicles (One Citizen can have many vehicles but multiple vehicles are registered under a single citizen)
    (see figure)

    - Many to One (N : 1) - eg. Courses taken by Professor (Many courses can be taught by a single professor and one professor handles or teaches many courses) 
    (see figure)

    - Many to Many (N : M) - eg. Customers buy Products (Many customers buy many products and many products are bought by many customers)
    (see figure)

    eg2 - Students attend Courses (same explaination)

2. Participation Constraints (aka *Minimum Cardinality Constraints*)
    Types:
    - Total Participation - All Entities are involved in atleast one relationship.
    eg. Customer (borrow) Loan
    Use a *Double Line* in relation. (see figure)

    -  Partial Participation - All Entities may not be involved in relationships.
    same eg. (see figure)
    Use a *Single Line* in relation.

    **Weak entity has total participation constraint but strong entity may not have total participation constraint**.
    (see imp image)

    (Also see the symbols of different types in the pdf). 
