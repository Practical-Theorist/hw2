# Homework 2

* Assigned: 10/4
* Due: 10/16 at 10:00AM via Gradescope
* worth 3.75% of your grade 



# 1. Relational Algebra

**(2 points each, 4 points total)**

Consider the simplified schema below (primary keys are in **bold**):

* liquors(**lid**, name, price, manufacturer)
  
* sales(**month**, **seller**, **liquors**, county, quantity)

Note: sales(liquors) references liquors(lid), and month is a text field (e.g. January, February).

Construct relational algebra for the following queries:

* **Q1**: Find the names of liquors that had at least one sale in "Clarke" or "Marshall" counties for the month of October.

* **Q2**: Find the names of manufacturers that sold at least two different liquors during the month of October in "Clarke" county.



# 2. More Relational Algebra

**(1 point each, 6 points total)**

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


Express the results for the relational algebra expressions:


1. π<sub>B,C</sub>(T2)
2. T1 × π<sub>A</sub>(T1)
3. T1 ⨝<sub>T1.C=T2.D</sub> T2 
4. T2 − (T1 ∩ T2)
5. T2 ⨝<sub>T1.A&lt;T2.B</sub> (σ<sub>B&lt;=2</sub>(T2))
6. T1 ⨝ (σ<sub>D=c</sub>(T2))



# Submission

Submit a PDF file containing your answers to Gradescope.

Consider using a text editor. Scanned documents are fine, but make sure your answers are readable.

