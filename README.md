# SQL-PROJECT
This is my first project in SQL. I decided to familiarise myself with the syntax and writing queries in mysql.

## Analysis for Apple Iphone XR (64GB) Black

![SQL PORTFOLIO](https://github.com/OpeyemiJagunmolu/SQL-PROJECT/assets/122671659/99e9fee0-fc54-4a47-b97d-38f723c5d5fe)

## PROBLEM STATEMENT
Write queries to sort out various data from the dataset

#### Questions and Queries

CREATE DATABASE apple_iphone;

-- SELECT ALL DATA FROM TABLE

SELECT * FROM iphone_data;

-- SELECT THE FIRST 10 ROWS AND THE NEXT 10 ROWS FROM THE TABLE

SELECT * FROM iphone_data
LIMIT 10
OFFSET 10;

-- FROM THE TABLE SELECT THE COLUMN PRODUCT

SELECT product FROM iphone_data;

-- HOW MANY ROWS CONTAINS THE PRODUCT COLUMN?

SELECT COUNT(product) FROM iphone_data;

-- FROM THE TABLE SELECT TOTAL COMMENTS

SELECT total_comments FROM iphone_data;

-- CALCULATE THE SUM OF TOTAL COMMENTS

SELECT total_comments, SUM(total_comments) AS "tc" FROM iphone_data;

-- WHAT IS THE NUMBER OF ROWS FOR TOTAL COMMENTS?

SELECT COUNT(total_comments) FROM iphone_data;

-- SELECT THE ROWS FOR REVIEW COUNTRY

SELECT review_country FROM iphone_data;

-- WHICH COUNTRY WAS THE PRODUCT REVIEWED

SELECT DISTINCT review_country FROM iphone_data;

-- WHAT ARE THE REVIEW RATINGS FOR IPHONE XR (64GB) BLACK 

SELECT review_rating FROM iphone_data;

-- ORDER THE REVIEW RATINGS FROM THE HIGHEST TO THE LOWEST

SELECT review_rating FROM iphone_data
ORDER BY review_rating DESC;

-- SELECT THE VARIOUS RATINGS FOR THE PHONE

SELECT review_rating FROM iphone_data WHERE review_rating = '5.0 out of 5 stars';

SELECT review_rating FROM iphone_data countrow WHERE review_rating = '5.0 out of 5 stars';

SELECT review_rating FROM iphone_data WHERE review_rating = '5.0 out of 5 stars';

SELECT * FROM iphone_data WHERE review_rating LIKE '4.0 out of 5 stars';

SELECT * FROM iphone_data WHERE review_rating LIKE '3.0 out of 5 stars';

SELECT review_rating FROM iphone_data WHERE review_rating LIKE '2.0 out of 5 stars';

SELECT review_rating FROM iphone_data WHERE review_rating = '1.0 out of 5 stars';

-- WHAT ARE THE VARIOUS COUNTS FOR EACH RATINGS?
SELECT review_rating, COUNT(review_rating) AS "ratingscount" FROM iphone_data GROUP BY review_rating;  

-- WHAT IS THE AVERAGE REVIEW RATING?

SELECT review_rating, AVG(review_rating) AS avg_rating FROM iphone_data;

-- WHAT ARE THE VARIOUS REVIEW DATES?

SELECT reviewed_at FROM iphone_data;

-- WHAT IS THE TOTAL HELPFUL COUNT?

SELECT helpful_count, SUM(helpful_count) AS hc FROM iphone_data;


_Disclaimer: This dataset is a dummy supplied by Pomerol Partners._

[DataDNA Dataset Challenge - March 2023.csv](https://github.com/OpeyemiJagunmolu/SQL-PROJECT/files/11480917/DataDNA.Dataset.Challenge.-.March.2023.csv)

[SQL Project on Apple Iphone Review.pdf](https://github.com/OpeyemiJagunmolu/SQL-PROJECT/files/11480919/SQL.Project.on.Apple.Iphone.Review.pdf)


