# Homework 2

* Assigned: 10/4
* Due: 10/16 at 10:00AM via Gradescope
* worth 3.75% of your grade 

Highly recommend to draft your answers using this template ([pdf](hw2_template.pdf), [latex](hw2_template.tex)).

## Update logs
### 10.11.2018
#### Added
- 'You can answer relational algebra with sub steps.' is added to the description of **1. Relational Algebra**.

### 10.08.2018
#### Added
- 'Make sure your SQL can be executed.' is added to the description of **3. SQL**.

### 10.05.2018
#### Changed
- 2.5 T1 ⨝<sub>T1.A&lt;T2.B</sub> (σ<sub>B&lt;=2</sub>(T2))

#### Added
- 'Simply answer NULL if you believe the resulting table is empty or there are some errors with the expressions' is added to the description of **2. More Relational Algebra**.


## 1. Relational Algebra

**(2 points each, 4 points total)**

Consider the simplified schema below (primary keys are in **bold**):

* liquors(**lid**, name, price, manufacturer)
  
* sales(**month**, **seller**, **liquors**, county, quantity)

Note: sales(liquors) references liquors(lid), and month is a text field (e.g. January, February).

Construct relational algebra for the following queries, you can answer relational algebra with sub steps:

* **Q1**: Find the names of liquors that had at least one sale in "Clarke" or "Marshall" counties for the month of November.

* **Q2**: Find the names of manufacturers that sold at least three different liquors during the month of January in "Marshall" county.

**Note:** Please use only operators covered in class. For Q2, it might help to think about the "at least two" case and then expand it to "at least three".



## 2. More Relational Algebra

**(1 point each, 6 points total)**

Simply answer NULL if you believe the resulting table is empty or there are some errors with the expressions.

Given the following tables


T1

|A | B | C |  
|---|---|---|
|1 | x | a |
|2 | y | b |
|2 | z | c | 

T2

B | C | D
---|---|---
1 | x | c
2 | y | c
3 | x | a


Write the result table for the relational algebra expressions:


1. π<sub>A,B</sub>(T1)
2. T1 × π<sub>A</sub>(T1)
3. T1 ⨝<sub>T1.B=T2.C</sub> T2 
4. T1 − (T1 ∩ T2)
5. T1 ⨝<sub>T1.A&lt;T2.B</sub> (σ<sub>B&lt;=2</sub>(T2))
6. T1 ⨝ (σ<sub>B=c</sub>(T2))

## 3. SQL
Write the following relational algebra expressions in SQL. Make sure your SQL can be executed.

**Note:** You don't need to know the full schema to translate these statements.

1. π<sub>name,age</sub>(Student)
2. Student × π<sub>age</sub>(Student)
3. Student ⨝<sub>Student.name=Teacher.name</sub> Teacher 
4. Student − (Student ∩ Teacher)
5. (σ<sub>year=2018</sub>(Student) )⨝<sub>Student.age&lt;Teacher.age</sub> (σ<sub>name=engene</sub>(Teacher))
6. Student ⨝ (σ<sub>age&lt;=50</sub>(Teacher))


## Submission

Submit a PDF file containing your answers to Gradescope.

Consider using a text editor. Scanned documents are fine, but make sure your answers are readable.

