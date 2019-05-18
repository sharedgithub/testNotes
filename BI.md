---- Chapter 2 - Intro to Data and Data Science - The Different Data Science Fields ------


-------- Chapter 10 .Statistics - Descriptive Statistics -------------
1. Data is classified on the basis of Types and Measurement level

Types of Data ?
- Numeric - represents numbers
a. Continuos - infinite and impossible to count (decimal values)
example - weight can be in decimal, time can be in seconds like 12:02:000031, distance, height, 

b. Discrete - value will be integer always, we can imagine data in each set 
example - no of childers,  score in exam, grade of any collage, number of objects, physical money, area etc

- Categprical - descipbes category or groups
example - Ans like yes or no, car brand, city name, country name etc

Levels of Measurements ?
- Qualitative 

a. nominal - cannot be ordered
example - car brand, city name, country name etc

b.ordinal - can be ordered
example - rate your lunch (can be order negative to postive)

- Quantitative -
a. Intervals - dont have true zeros
example - temprature (Celsius or Fahrenheit)


b. Ratios -It has trues zeros
example - no of apple with me and you is 2times
temprature Kelvin is ratios has true zero

2. Visualizations of data ?
 a. Categorical data visualizations

	- Frequency distribution table - category v/s frequency (number of units sold)
	- Bar chart - cloumn chart
	- Pie chart - % of total each brand (relatative frequecy comparision)
	- Pareto diagram - Categories are shown in descending order of frequency (column chart with cummulative frequecny i.e. sum of relative frequencies (polygonal line) combine (pie chart and bar chart)) it is on name Ville Fred-o parenteau.

		80%-20% rule says 80% of effects comes from 20% of the causes if we resolve 20% then automatically 80% problems will be solved)
 b. Numerical data visualizations 
 
	- Frequency distribution table - arrange data set and find out frequency, group data into intervals, 
	how to choose theses intervals (5 to 20) = largest value - smallest number / no of desired intervals
	
	Histogram

 c. Relationship between two variables - Cross table and  Scatter plot
 
	- Cross table - contengency table - calc sum of each column and rows
side by side bar charts can be useful to understand inventor type and their invenstments

	- Scatter Plot - two numerical variable
	
3. What is mean median and mode ? - This is measure of central tendency
	- Mean - simple avg
	- Median - arrange data in ascending order and then find median by formula (n+1)/2 (n = no of data or positions)
	- Mode - max no of time some values appears that max value is mode, we can have 2 to 3 modes but not more than that
	
4. Whats is measure of assymetry ? 
	- Skewness - Skewness is asymmetry in a statistical distribution, in which the curve appears distorted or skewed either to the left or to the right. 
	
	- Left Skewness - mean < median, outliers on left i.e. negative skew 
	- Right Skewness - mean > median, outliers on right skew values is postive hence also called as postive skew
	- Zero Skewness - mean , median and mode is equal
	
	in excel skew is calculted by skew() formula.
	Skew is used to understand where the data is situated

5. Measures of variability ? - single varible
	- Variance - it measure dispersion of set of data points around their mean
	Populations variance - sigma sequare is sum of square of difference between population value & population mean divided by total number of observations 
	
	and sample variance - S sequare is sum of square of difference between sample value & sample mean divided by total number of sample observations 
	Population & Sample variance has different values, excel formula (VAR.P() & VAR.S())
	
	- Standard deviations - Variance is pretty large and hard to compare hence standar deviations are used which is square root of population variance or sample variance - excel formula STDEV.S
		
	- Coefficient of variation - is devision of standar deviation and its mean
	compare data set having same or different variability

6. Covarience ? - multiple variables
(x-mean x)* (y - mean y)/N
Covariance can be postive - moving in same directions or negative - moving in opposite directions or zero - moving independently

7. Correlation ? - It gives correlation between two variable and formula is covarianc/standard deviations

values will be between 1 to -1 = Postive correlations
zero = coeffe and house price
-1 = company making ice creame and company making umbrella




---------------Chapter 17. Part 3 Relational Database Theory & Introduction to SQL ------------------

1. SQL - Structured Query Language

2. Table is called as entity, rows are called as horizontal entity, columns are called as vertical entity and each recod is called as entity instanaces

3. Types of Databases ?
- Relational and non relational

4. Spread sheet and database
- Spread speed - formattibng, cell can contain functions or formula, relationships are not maitained, not consistence if we update one id related reocrds will not be updated automatically whereas in database it will be one separate table same can be updated easily, extensive analysis

database - extensive, easy to retrive data, faster, data intigrity and consistency

5. Database digrams are 
entity relationship diagram
relational scheme diagram

6. WHat is Primary key ?
Primary is key is unique value and does not have null value in it.
Primary key can be single column or combination of two to three columns but not more than that


Unique keys - can have null value, it cannot be primary key
table may have multiple unique keys

7. Relationship 

One to many
Many to Many
One to One

many is shown as >|
One is shown as ||
zero is shown as O
Zero or many as O>

----------- Chapter 18. SQL - Install and get to know MySQL------------------

1. SQL workbench and isntaller needs to be installed and also visual c++

2. If you get some error message like cannot connect then go to command prompt - write cd (mysql bin path)
write- mysql -u root -p
Enter password

CREATE USER ''@'localhost'
IDENTIFIED WITh mysql_native_password BY '';

GRANT ALL PRIVILeGES ON *.* TO 'nativeuser'@'localhost';

-----------------Chapter 21. SQL - Practical Application of the SQL SELECT Statement------------------
1. SELECT
2. Where
3. AND
4. OR
5. IN ('',''),;
6. NOt IN ('','');
7. like ('abc%');
like ('abc_); (_ is wildcard)
like (a_%_%);
like h[oa]t - finds hot,hat but not hit or het etc
h[^oa]t - ^ Represents any character not in the brackets
h[a-t]t  it  - Represents a range of characters
8. Not Like ('abc%');
9. Between - select * from table_name where column1 BETWEEN '' and '';
10. not between - select * from table_name where column1 NOT BETWEEN '' and '';
11. is null - SELECT * FROM table where column is null;
12. is not null - SELECT * FROM table where column is not null;
13. Comparison operators - =, > , <=, < , <> or !=
14. distinct - Select distinct columns from table_name;
15. Count(); - SELECT COUNT(column) FROM table_name;
SUM();MIN();MAX();AVG();
16. Order by  - Select * from table order by column1, column2 asc|desc; if not mentioned asc or desc than sql retrive data in ascending order
17. Group by - SELECT column_name(s) FROM table_name WHERE condition GROUP BY column_name(s)ORDER BY column_name(s);
18. Aliases - SELECT column_name AS alias_name FROM table_name;
19. Having - SELECT column_name(s) FROM table_name WHERE condition GROUP BY column_name(s) HAVING condition ORDER BY column_name(s); (having is used with aggrecate function instead of where after group by)
20. Limit - SELECT column_name(s) FROM table_name WHERE condition LIMIT number;


----- Chapter 22. SQL - Expanding on MySQL Aggregate Functions--------------
1. Count () - SELECT count (*) FROM Products; or select count (distinct column) from table;
2.Min (), Max (), AVG ()
3. ROUND(#,decimal value)

---------------Chapter 23. SQL - SQL JOINs ----------------------

1. Joins - intersection
2. Inner join  - Select table1/table2 columns from table1 inner join table2 on column1 = column2, (Inner join fetches data common to both table)
3. Right Join - retrive data common to both data and right table
4. Left join -  retrive data common to both data and left table
5. Union - 
The UNION operator is used to combine the result-set of two or more SELECT statement
Retrives distinct value 
SELECT column_name(s) FROM table1
UNION
SELECT column_name(s) FROM table2;
6. Union ALL - derive duplicate data
SELECT column_name(s) FROM table1
UNION ALL
SELECT column_name(s) FROM table2;


--------------Chapter 24. SQL - SQL Subqueries ---------------------------

1. Subqueries - nasted queries example - Select * from table1 where column1 in (Select column1 from table2 )
2. Exists - Select * from table1 where exists (Select column1 from table2 where table1.column1 = table2.column2 )

exists is faster in retriving large amount of data whereas IN is faster withn small amount of data

------------ Chapter 25. SQL - Stored Routines --------------------------



---------------- Chapter 26. Statement Cases ----------------------
1. Case  - can be used for multiple conditions

Select emp_no,first_name, last_name, 
case when gender = 'M' Then 'Male'  
     when geneder = 'F' Then 'Female' 
	else 'Unknown' END as geneder 
from Emplyees

2. If - is used for single conditon 

Select emp_no,first_name, last_name, 
if(gender = 'M' ,'Male', 'Female') as geneder 
from Emplyees
 
 
----------------Chapter 27. Part 4 Introduction to Tableau -----------------
1. Tableau is used for data visulaization and preparing dashboards like geographiical location visualization
2. Excel is data creation tool - used for multilayer calculations, Pre processing of data 
3. In tablo uploading data is easy and create dashboards
4. Tablo Join -
	Inner Join - Inner join is used for fetching matching data in two tables
	Left Join - Left table of key column matching data will be retrive from right table
	Right Join - Right table of key column matching data will be retrived from left table

