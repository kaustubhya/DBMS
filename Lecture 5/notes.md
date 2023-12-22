Steps to make ER diagram:
1. Identify the entity sets.
2. Identify the attributes and their types
3. Identify the relations and their constraints

• Constraints:
- Mapping
- Participation

Eg. Banking System ER Model (see slides) 

Requirements:
- Banking System -> Branches (name of branch (primary key))
- Bank -> Customer
- Customers -> Accounts and take loan
- Customer associated with some banker
- Bank has employees
- Accounts:
    - savings
    - current
- Loan originated by the branch
Loan >= 1 customers (same loan issued to multiple customers)   
• payment schedules of loans  

Take some assumptions like these while drawing ER diagrams in interviews.

♦ Defining the entity sets:
1. Branch
2. Customers
3. Employee
4. Saving Account
5. Current Account
6. Loan
7. Payment (Loan Payment (Weak Entity))

Here we can either go 'top-down or bottom-up', we will go *bottom-up* here (between Savings Account and Current Account)

Generalize (bottom-up) them both to make an Account Entity.

♦ Defining Attributes:
1. Branch -> name (pri key), city, assets, liabilities
2. customer -> cust-id (pri key), name, address (composite attribute), contact no. (multivalued attribute), DOB, age (derived attribute)
3. Employee -> emp-id(pri key), name, contact no., dependent name(multivalued),
years of service(derived attribute), start date(single valued)
4. Saving Account -> interest rate, daily withdrawl limit.
5. Current Account -> per transaction changes, overdraft amount.
6. *'Generalised Entity (of 4 and 5)'* *"Account"* -> acc-number (pri-key), balance.
7. Loan -> loan_number (pri key), amount
8. Weak Entity Payment -> Payment Number, date, amount 

♦ Relationship and Constraints Define:
1. Customer borrow loan
M-:=N
2. Loan originated by bank
N=:-1
3. Loan-Loan-payment(weak relation)=Payment(Weak Entity)
1-:=N
4. Customer deposit Account
M:N
5. Customer banker Employee
N:1
6. Employee managed by Employee  (Many bank employees handled by 1 Bank Manager)
N:1
(Unary Relationship) 

(see ER diagram in slides)