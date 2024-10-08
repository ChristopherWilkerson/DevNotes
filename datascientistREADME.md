



## Sept 7th, 2024 ##

Manipulation
Statements
4 mins 

The code below is a SQL statement. A statement is text that the database recognizes as a valid command. Statements always end in a semicolon ;.

CREATE TABLE table_name (
   column_1 data_type, 
   column_2 data_type, 
   column_3 data_type
);

Let’s break down the components of a statement:

    CREATE TABLE is a clause. Clauses perform specific tasks in SQL. By convention, clauses are written in capital letters. Clauses can also be referred to as commands.
    table_name refers to the name of the table that the command is applied to.
    (column_1 data_type, column_2 data_type, column_3 data_type) is a parameter. A parameter is a list of columns, data types, or values that are passed to a clause as an argument. Here, the parameter is a list of column names and the associated data type.

The structure of SQL statements vary. The number of lines used does not matter. A statement can be written all on one line, or split up across multiple lines if it makes it easier to read. In this course, you will become familiar with the structure of common statements.
Manipulation
Create
4 min

CREATE statements allow us to create a new table in the database. You can use the CREATE statement anytime you want to create a new table from scratch. The statement below creates a new table named celebs.

CREATE TABLE celebs (
   id INTEGER, 
   name TEXT, 
   age INTEGER
);

1. CREATE TABLE is a clause that tells SQL you want to create a new table.
2. celebs is the name of the table.
3. (id INTEGER, name TEXT, age INTEGER) is a list of parameters defining each column, or attribute in the table and its data type:

    id is the first column in the table. It stores values of data type INTEGER
    name is the second column in the table. It stores values of data type TEXT
    age is the third column in the table. It stores values of data type INTEGER

Instructions

    Checkpoint 1 Passed

    1.

    Now that you have a good understanding of SQL syntax, we can create a new table. We’ve cleared the database from the previous exercises. Confirm no celebs table exists by entering the following in the code editor:

    SELECT * FROM celebs;

    Look at the results. The database should be empty!

Checkpoint 2 Passed

2.

Now that we know the database is empty, let’s create a new celebs table.

In the code editor, type:

CREATE TABLE celebs (
   id INTEGER, 
   name TEXT, 
   age INTEGER
); 

We will learn how to view this table in a later exercise after we have added some data to it.
Manipulation
Insert
7 min

The INSERT statement inserts a new row into a table.

We can use the INSERT statement when you want to add new records. The statement below enters a record for Justin Bieber into the celebs table.

INSERT INTO celebs (id, name, age) 
VALUES (1, 'Justin Bieber', 29);

    INSERT INTO is a clause that adds the specified row or rows.
    celebs is the table the row is added to.
    (id, name, age) is a parameter identifying the columns that data will be inserted into.
    VALUES is a clause that indicates the data being inserted.
    (1, 'Justin Bieber', 29) is a parameter identifying the values being inserted.
        1: an integer that will be added to id column
        'Justin Bieber': text that will be added to name column
        29: an integer that will be added to age column

SELECT * FROM celebs


Manipulation
Alter
3 min

The ALTER TABLE statement adds a new column to a table. You can use this command when you want to add columns to a table. The statement below adds a new column twitter_handle to the celebs table.

ALTER TABLE celebs 
ADD COLUMN twitter_handle TEXT;

1. ALTER TABLE is a clause that lets you make the specified changes.
2. celebs is the name of the table that is being changed.
3. ADD COLUMN is a clause that lets you add a new column to a table:

    twitter_handle is the name of the new column being added
    TEXT is the data type for the new column

4. NULL is a special value in SQL that represents missing or unknown data. Here, the rows that existed before the column was added have NULL (∅) values for twitter_handle.

Manipulation
Update
4 min

The UPDATE statement edits a row in a table. You can use the UPDATE statement when you want to change existing records. The statement below updates the record with an id value of 4 to have the twitter_handle @taylorswift13.

UPDATE celebs 
SET twitter_handle = '@taylorswift13' 
WHERE id = 4; 

1. UPDATE is a clause that edits a row in the table.
2. celebs is the name of the table.
3. SET is a clause that indicates the column to edit.

    twitter_handle is the name of the column that is going to be updated
    @taylorswift13 is the new value that is going to be inserted into the twitter_handle column.

4. WHERE is a clause that indicates which row(s) to update with the new column value. Here the row with a 4 in the id column is the row that will have the twitter_handle updated to @taylorswift13.

Manipulation
Delete
2 min

The DELETE FROM statement deletes one or more rows from a table. You can use the statement when you want to delete existing records. The statement below deletes all records in the celebs table with no twitter_handle:

DELETE FROM celebs 
WHERE twitter_handle IS NULL;

    DELETE FROM is a clause that lets you delete rows from a table.
    celebs is the name of the table we want to delete rows from.
    WHERE is a clause that lets you select which rows you want to delete. Here we want to delete all of the rows where the twitter_handle column IS NULL.
    IS NULL is a condition in SQL that returns true when the value is NULL and false otherwise.

Manipulation
Constraints
6 min

Constraints that add information about how a column can be used are invoked after specifying the data type for a column. They can be used to tell the database to reject inserted data that does not adhere to a certain restriction. The statement below sets constraints on the celebs table.

CREATE TABLE celebs (
   id INTEGER PRIMARY KEY, 
   name TEXT UNIQUE,
   date_of_birth TEXT NOT NULL,
   date_of_death TEXT DEFAULT 'Not Applicable'
);

1. PRIMARY KEY columns can be used to uniquely identify the row. Attempts to insert a row with an identical value to a row already in the table will result in a constraint violation which will not allow you to insert the new row.

2. UNIQUE columns have a different value for every row. This is similar to PRIMARY KEY except a table can have many different UNIQUE columns.

3. NOT NULL columns must have a value. Attempts to insert a row without a value for a NOT NULL column will result in a constraint violation and the new row will not be inserted.

4. DEFAULT columns take an additional argument that will be the assumed value for an inserted row if the new row does not specify a value for that column.



SQL is a programming language designed to manipulate and manage data stored in relational databases.

    A relational database is a database that organizes information into one or more tables.
    A table is a collection of data organized into rows and columns.

A statement is a string of characters that the database recognizes as a valid command.

    CREATE TABLE creates a new table.
    INSERT INTO adds a new row to a table.
    SELECT queries data from a table.
    ALTER TABLE changes an existing table.
    UPDATE edits a row in a table.
    DELETE FROM deletes rows from a table.


Queries
As
4 min

Knowing how SELECT works, suppose we have the code below:

SELECT name AS 'Titles'
FROM movies;

Can you guess what AS does?

AS is a keyword in SQL that allows you to rename a column or table using an alias. The new name can be anything you want as long as you put it inside of single quotes. Here we renamed the name column as Titles.

Some important things to note:

    Although it’s not always necessary, it is considered best practice to surround your aliases with single quotes.
        Note that this practice is specific to SQLite, the RDBMS used in this exercise. When you work with other RDBMSs, notably PostgreSQL, no quotes or double quotes may be required in place of single quotes.
    When using AS, the columns are not being renamed in the table. The aliases only appear in the result.

Queries
Distinct
3 min

When we are examining data in a table, it can be helpful to know what distinct values exist in a particular column.

DISTINCT is used to return unique values in the output. It filters out all duplicate values in the specified column(s).

For instance,

SELECT tools 
FROM inventory;

might produce:
tools
Hammer
Nails
Nails
Nails

By adding DISTINCT before the column name,

SELECT DISTINCT tools 
FROM inventory;

the result would now be:
tools
Hammer
Nails

Filtering the results of a query is an important skill in SQL. It is easier to see the different possible genres in the movie table after the data has been filtered than to scan every row in the table.

Queries
Where
4 min

We can restrict our query results using the WHERE clause in order to obtain only the information we want.

Following this format, the statement below filters the result set to only include top rated movies (IMDb ratings greater than 8):

SELECT *
FROM movies
WHERE imdb_rating > 8;

How does it work?

    The WHERE clause filters the result set to only include rows where the following condition is true.

    imdb_rating > 8 is the condition. Here, only rows with a value greater than 8 in the imdb_rating column will be returned.

The > is an operator. Operators create a condition that can be evaluated as either true or false.

Comparison operators used with the WHERE clause are:

    = equal to
    != not equal to
    > greater than
    < less than
    >= greater than or equal to
    <= less than or equal to

There are also some special operators that we will learn more about in the upcoming exercises.

Queries
Like I
2 min

LIKE can be a useful operator when you want to compare similar values.

The movies table contains two films with similar titles, ‘Se7en’ and ‘Seven’.

How could we select all movies that start with ‘Se’ and end with ‘en’ and have exactly one character in the middle?

SELECT * 
FROM movies
WHERE name LIKE 'Se_en';

    LIKE is a special operator used with the WHERE clause to search for a specific pattern in a column.

    name LIKE 'Se_en' is a condition evaluating the name column for a specific pattern.

    Se_en represents a pattern with a wildcard character.

The _ means you can substitute any individual character here without breaking the pattern. The names Seven and Se7en both match this pattern.

Like II
4 min

The percentage sign % is another wildcard character that can be used with LIKE.

This statement below filters the result set to only include movies with names that begin with the letter ‘A’:

SELECT * 
FROM movies
WHERE name LIKE 'A%';

% is a wildcard character that matches zero or more missing characters in the pattern. For example:

    A% matches all movies with names that begin with letter ‘A’
    %a matches all movies that end with ‘a’

We can also use % both before and after a pattern:

SELECT * 
FROM movies 
WHERE name LIKE '%man%';

Here, any movie that contains the word ‘man’ in its name will be returned in the result.

LIKE is not case sensitive. ‘Batman’ and ‘Man of Steel’ will both appear in the result of the query above.

Queries
Is Null
2 min

By this point of the lesson, you might have noticed that there are a few missing values in the movies table. More often than not, the data you encounter will have missing values.

Unknown values are indicated by NULL.

It is not possible to test for NULL values with comparison operators, such as = and !=.

Instead, we will have to use these operators:

    IS NULL
    IS NOT NULL

To filter for all movies with an IMDb rating:

SELECT name
FROM movies 
WHERE imdb_rating IS NOT NULL;
Between
7 min

The BETWEEN operator is used in a WHERE clause to filter the result set within a certain range. It accepts two values that are either numbers, text or dates.

For example, this statement filters the result set to only include movies with years from 1990 up to, and including 1999.

SELECT *
FROM movies
WHERE year BETWEEN 1990 AND 1999;

When the values are text, BETWEEN filters the result set for within the alphabetical range.

In this statement, BETWEEN filters the result set to only include movies with names that begin with the letter ‘A’ up to, but not including ones that begin with ‘J’.

SELECT *
FROM movies
WHERE name BETWEEN 'A' AND 'J';

However, if a movie has a name of simply ‘J’, it would actually match. This is because BETWEEN goes up to the second value — up to ‘J’. So the movie named ‘J’ would be included in the result set but not ‘Jaws’.

Between
7 min

The BETWEEN operator is used in a WHERE clause to filter the result set within a certain range. It accepts two values that are either numbers, text or dates.

For example, this statement filters the result set to only include movies with years from 1990 up to, and including 1999.

SELECT *
FROM movies
WHERE year BETWEEN 1990 AND 1999;

When the values are text, BETWEEN filters the result set for within the alphabetical range.

In this statement, BETWEEN filters the result set to only include movies with names that begin with the letter ‘A’ up to, but not including ones that begin with ‘J’.

SELECT *
FROM movies
WHERE name BETWEEN 'A' AND 'J';

However, if a movie has a name of simply ‘J’, it would actually match. This is because BETWEEN goes up to the second value — up to ‘J’. So the movie named ‘J’ would be included in the result set but not ‘Jaws’.
Queries
And
5 min

Sometimes we want to combine multiple conditions in a WHERE clause to make the result set more specific and useful.

One way of doing this is to use the AND operator. Here, we use the AND operator to only return 90’s romance movies.

SELECT * 
FROM movies
WHERE year BETWEEN 1990 AND 1999
   AND genre = 'romance';

    year BETWEEN 1990 AND 1999 is the 1st condition.

    genre = 'romance' is the 2nd condition.

    AND combines the two conditions.

AND Venn Diagram

With AND, both conditions must be true for the row to be included in the result.



Queries
Or
3 min

Similar to AND, the OR operator can also be used to combine multiple conditions in WHERE, but there is a fundamental difference:

    AND operator displays a row if all the conditions are true.
    OR operator displays a row if any condition is true.

Suppose we want to check out a new movie or something action-packed:

SELECT *
FROM movies
WHERE year > 2014
   OR genre = 'action';

    year > 2014 is the 1st condition.

    genre = 'action' is the 2nd condition.

    OR combines the two conditions.

OR Venn Diagram

With OR, if any of the conditions are true, then the row is added to the result.

Queries
Or
3 min

Similar to AND, the OR operator can also be used to combine multiple conditions in WHERE, but there is a fundamental difference:

    AND operator displays a row if all the conditions are true.
    OR operator displays a row if any condition is true.

Suppose we want to check out a new movie or something action-packed:

SELECT *
FROM movies
WHERE year > 2014
   OR genre = 'action';

    year > 2014 is the 1st condition.

    genre = 'action' is the 2nd condition.

    OR combines the two conditions.

OR Venn Diagram

With OR, if any of the conditions are true, then the row is added to the result.


Queries
Limit
3 min

We’ve been working with a fairly small table (fewer than 250 rows), but most SQL tables contain hundreds of thousands of records. In those situations, it becomes important to cap the number of rows in the result.

For instance, imagine that we just want to see a few examples of records.

SELECT *
FROM movies
LIMIT 10;

LIMIT is a clause that lets you specify the maximum number of rows the result set will have. This saves space on our screen and makes our queries run faster.

Here, we specify that the result set can’t have more than 10 rows.

LIMIT always goes at the very end of the query. Also, it is not supported in all SQL databases.

Queries
Case
8 min

A CASE statement allows us to create different outputs (usually in the SELECT statement). It is SQL’s way of handling if-then logic.

Suppose we want to condense the ratings in movies to three levels:

    If the rating is above 8, then it is Fantastic.
    If the rating is above 6, then it is Poorly Received.
    Else, Avoid at All Costs.

SELECT name,
 CASE
  WHEN imdb_rating > 8 THEN 'Fantastic'
  WHEN imdb_rating > 6 THEN 'Poorly Received'
  ELSE 'Avoid at All Costs'
 END
FROM movies;

    Each WHEN tests a condition and the following THEN gives us the string if the condition is true.
    The ELSE gives us the string if all the above conditions are false.
    The CASE statement must end with END.

In the result, you have to scroll right because the column name is very long. To shorten it, we can rename the column to ‘Review’ using AS:

SELECT name,
 CASE
  WHEN imdb_rating > 8 THEN 'Fantastic'
  WHEN imdb_rating > 6 THEN 'Poorly Received'
  ELSE 'Avoid at All Costs'
 END AS 'Review'
FROM movies;


Queries
Review
<1 min

Congratulations!

We just learned how to query data from a database using SQL. We also learned how to filter queries to make the information more specific and useful.

Let’s summarize:

    SELECT is the clause we use every time we want to query information from a database.
    AS renames a column or table.
    DISTINCT return unique values.
    WHERE is a popular command that lets you filter the results of the query based on conditions that you specify.
    LIKE and BETWEEN are special operators.
    AND and OR combines multiple conditions.
    ORDER BY sorts the result.
    LIMIT specifies the maximum number of rows that the query will return.
    CASE creates different outputs.


Aggregate Functions
Introduction
3 min

SQL Queries don’t just access raw data, they can also perform calculations on the raw data to answer specific data questions.

Calculations performed on multiple rows of a table are called aggregates.

In this lesson, we have given you a table named fake_apps which is made up of fake mobile applications data.

Here is a quick preview of some important aggregates that we will cover in the next five exercises:

    COUNT(): count the number of rows
    SUM(): the sum of the values in a column
    MAX()/MIN(): the largest/smallest value
    AVG(): the average of the values in a column
    ROUND(): round the values in the column

Let’s get started!


Count
3 min

The fastest way to calculate how many rows are in a table is to use the COUNT() function.

COUNT() is a function that takes the name of a column as an argument and counts the number of non-empty values in that column.

SELECT COUNT(*)
FROM table_name;

Here, we want to count every row, so we pass * as an argument inside the parenthesis.


SQL makes it easy to add all values in a particular column using SUM().

SUM() is a function that takes the name of a column as an argument and returns the sum of all the values in that column.

What is the total number of downloads for all of the apps combined?

SELECT SUM(downloads)
FROM fake_apps;

This adds all values in the downloads column.

Aggregate Functions
Max / Min
2 min

The MAX() and MIN() functions return the highest and lowest values in a column, respectively.

How many downloads does the most popular app have?

SELECT MAX(downloads)
FROM fake_apps;

The most popular app has 31,090 downloads!

MAX() takes the name of a column as an argument and returns the largest value in that column. Here, we returned the largest value in the downloads column.

MIN() works the same way but it does the exact opposite; it returns the smallest value.


SQL uses the AVG() function to quickly calculate the average value of a particular column.

The statement below returns the average number of downloads for an app in our database:

SELECT AVG(downloads)
FROM fake_apps;

The AVG() function works by taking a column name as an argument and returns the average value for that column.

Round
5 min

By default, SQL tries to be as precise as possible without rounding. We can make the result table easier to read using the ROUND() function.

ROUND() function takes two arguments inside the parenthesis:

    a column name
    an integer

It rounds the values in the column to the number of decimal places specified by the integer.

SELECT ROUND(price, 0)
FROM fake_apps;

Here, we pass the column price and integer 0 as arguments. SQL rounds the values in the column to 0 decimal places in the output.

Aggregate Functions
Group By I
11 min

Oftentimes, we will want to calculate an aggregate for data with certain characteristics.

For instance, we might want to know the mean IMDb ratings for all movies each year. We could calculate each number by a series of queries with different WHERE statements, like so:

SELECT AVG(imdb_rating)
FROM movies
WHERE year = 1999;

SELECT AVG(imdb_rating)
FROM movies
WHERE year = 2000;

SELECT AVG(imdb_rating)
FROM movies
WHERE year = 2001;

and so on.

Luckily, there’s a better way!

We can use GROUP BY to do this in a single step:

SELECT year,
   AVG(imdb_rating)
FROM movies
GROUP BY year
ORDER BY year;

GROUP BY is a clause in SQL that is used with aggregate functions. It is used in collaboration with the SELECT statement to arrange identical data into groups.

The GROUP BY statement comes after any WHERE statements, but before ORDER BY or LIMIT.


## Sep 13th ##

Multiple Tables
Primary Key vs Foreign Key
8 min

Let’s return to our example of the magazine subscriptions. Recall that we had three tables: orders, subscriptions, and customers.

Each of these tables has a column that uniquely identifies each row of that table:

    order_id for orders
    subscription_id for subscriptions
    customer_id for customers

These special columns are called primary keys.

Primary keys have a few requirements:

    None of the values can be NULL.
    Each value must be unique (i.e., you can’t have two customers with the same customer_id in the customers table).
    A table can not have more than one primary key column.

Let’s reexamine the orders table:
order_id 	customer_id 	subscription_id 	purchase_date
1 	2 	3 	2017-01-01
2 	2 	2 	2017-01-01
3 	3 	1 	2017-01-01

Note that customer_id (the primary key for customers) and subscription_id (the primary key for subscriptions) both appear in this.

When the primary key for one table appears in a different table, it is called a foreign key.

So customer_id is a primary key when it appears in customers, but a foreign key when it appears in orders.

In this example, our primary keys all had somewhat descriptive names. Generally, the primary key will just be called id. Foreign keys will have more descriptive names.

Why is this important? The most common types of joins will be joining a foreign key from one table with the primary key from another table. For instance, when we join orders and customers, we join on customer_id, which is a foreign key in orders and the primary key in customers.


Multiple Tables
Cross Join
17 min

So far, we’ve focused on matching rows that have some information in common.

Sometimes, we just want to combine all rows of one table with all rows of another table.

For instance, if we had a table of shirts and a table of pants, we might want to know all the possible combinations to create different outfits.

Our code might look like this:

SELECT shirts.shirt_color,
   pants.pants_color
FROM shirts
CROSS JOIN pants;

    The first two lines select the columns shirt_color and pants_color.
    The third line pulls data from the table shirts.
    The fourth line performs a CROSS JOIN with pants.

Notice that cross joins don’t require an ON statement. You’re not really joining on any columns!

If we have 3 different shirts (white, grey, and olive) and 2 different pants (light denim and black), the results might look like this:
shirt_color 	pants_color
white 	light denim
white 	black
grey 	light denim
grey 	black
olive 	light denim
olive 	black

3 shirts × 2 pants = 6 combinations!

This clothing example is fun, but it’s not very practically useful.

A more common usage of CROSS JOIN is when we need to compare each row of a table to a list of values.

Let’s return to our newspaper subscriptions. This table contains two columns that we haven’t discussed yet:

    start_month: the first month where the customer subscribed to the print newspaper (e.g., 2 for February)
    end_month: the final month where the customer subscribed to the print newspaper

Suppose we wanted to know how many users were subscribed during each month of the year. For each month (1, 2, 3) we would need to know if a user was subscribed. Follow the steps below to see how we can use a CROSS JOIN to solve this problem.


Multiple Tables
Union
3 min

Sometimes we just want to stack one dataset on top of the other. Well, the UNION operator allows us to do that.

Suppose we have two tables and they have the same columns.

table1:
pokemon 	type
Bulbasaur 	Grass
Charmander 	Fire
Squirtle 	Water

table2:
pokemon 	type
Snorlax 	Normal

If we combine these two with UNION:

SELECT *
FROM table1
UNION
SELECT *
FROM table2;

The result would be:
pokemon 	type
Bulbasaur 	Grass
Charmander 	Fire
Squirtle 	Water
Snorlax 	Normal

SQL has strict rules for appending data:

    Tables must have the same number of columns.
    The columns must have the same data types in the same order as the first table.

With
12 min

Often times, we want to combine two tables, but one of the tables is the result of another calculation.

Let’s return to our magazine order example. Our marketing department might want to know a bit more about our customers. For instance, they might want to know how many magazines each customer subscribes to. We can easily calculate this using our orders table:

SELECT customer_id,
   COUNT(subscription_id) AS 'subscriptions'
FROM orders
GROUP BY customer_id;

This query is good, but a customer_id isn’t terribly useful for our marketing department, they probably want to know the customer’s name.

We want to be able to join the results of this query with our customers table, which will tell us the name of each customer. We can do this by using a WITH clause.

WITH previous_results AS (
   SELECT ...
   ...
   ...
   ...
)
SELECT *
FROM previous_results
JOIN customers
  ON _____ = _____;

    The WITH statement allows us to perform a separate query (such as aggregating customer’s subscriptions)
    previous_results is the alias that we will use to reference any columns from the query inside of the WITH clause
    We can then go on to do whatever we want with this temporary table (such as join the temporary table with another table)

Essentially, we are putting a whole first query inside the parentheses () and giving it a name. After that, we can use this name as if it’s a table and write a new query using the first query.


Review
<1 min

In this lesson, we learned about relationships between tables in relational databases and how to query information from multiple tables using SQL.

Let’s summarize what we’ve learned so far:

    JOIN will combine rows from different tables if the join condition is true.

    LEFT JOIN will return every row in the left table, and if the join condition is not met, NULL values are used to fill in the columns from the right table.

    Primary key is a column that serves a unique identifier for the rows in the table.

    Foreign key is a column that contains the primary key to another table.

    CROSS JOIN lets us combine all rows of one table with all rows of another table.

    UNION stacks one dataset on top of another.

    WITH allows us to define one or more temporary tables that can be used in the final query.


Data Setup
Dimensions and Measures, Discrete and Continuous
9 min

Okay, there’s a lot to take in here, but this exercise is one of the most integral to understanding Tableau’s data language. Take your time and refer back to the chart on the right as needed.

During the Loading Data lesson, we saw how Tableau assigns different field types to data (numeric, string, geographic, etc.). Tableau also categorizes each of these fields by their role in our visuals. Tableau calls the two roles dimensions and measures.

Dimension icons are blue and represent discrete fields: categories and descriptive variables.

Measure icons are green and represent continuous fields: numbers that we can perform calculations on.

Tableau is usually pretty accurate in assigning dimensions or measures to a data type, but it’s always good to double-check. Remember when we changed the Tree ID field from a number to a string? Tableau had assigned this field as a measure because it contained numbers. But we knew that the numbers actually represented unique IDs, and we changed the data type to a string so that Tableau will treat this variable as a dimension.

Why does this matter? Let’s check out Borocode – a field with numbers 1-5 to represent the boroughs of New York City: Manhattan, the Bronx, Queens, Brooklyn, and Staten Island – and see what happens if we let Tableau treat Borocode as a measure instead of a dimension.

When Borocode is read as a Number and Measure, Tableau aggregates the Borocode field in the SUM() formula. (Notice that the Borocode Pill is green and has been wrapped in the SUM() formula.)

This is a snip from a Tableau worksheet. The columns shelf has "SUM(Borocode)" and is encircled in a green pill. The rows shelf has "Boroname" and it has a blue pill around it. The chart is a bar graph with "Boroname" on the y-axis and "Sum of Borocode" on the x-axis. There are five horizontal bars that have labels to the left of each one. They read from top to bottom, "Bronx", "Brooklyn", "Manhattan", "Queens", and "Staten Island". The values to the right of each bar are labeled from top to bottom as, "170,406", "531,879", "65,423", "1,002,204", and "526,590"

Since the field was “numerical” and set as a measure, Tableau summed the values in that field and created a bar graph to represent the totals. This doesn’t tell us anything meaningful because the numbers represent categories! Manhattan has just a small bar in the graph because its Borocode is 1 rather than 4 or 5.

When we change the data type so that Tableau reads Borocode as a String and Dimension, however, Borocode now functions as an ID or label for each borough. Tableau will no longer attempt to do any calculations on this field, and we can see here how it corresponds with the variable Boroname.

This is a Tableau workbook. In the rows shelf, there is "Boroname" and "Borocode" and they are each encircled in a blue pill. There is a chart below with five rows and three columns of data. The first column name is "Boroname" and the data in this column from top to bottom reads, "Bronx", "Brooklyn", "Manhattan", "Queens", and "Staten Island". The second column name is "Borocode" and the data in this column reads from top to bottom, "2", "3", "1", "4", and "5". The third column has no name and the entire data says "Abc" in each row.

With that sorted out, we can use the field to make a map that uses the Borocode variable to apply color to each borough, for example.

This is a Tableau worksheet. In the columns shelf is "Longitude(generated)" and the rows shelf has "Latitude(generated). The "Borocode" column is on the color shelf and the "Zipcode" column is on the detail shelf. There is a map with all the different regions and each section of "Borocode" is a different color. The top left region has blue dots, meaning they have a Borocode of 1. The top right region has orange dots, meaning they have a Borocode of 2. The middle region has red dots, meaning they have a Borocode of 3. The middle right region has blueish-green dots, meaning they have a Borocode of 4. The bottom left region has green dots, meaning they have a Borocode of 5.

Let’s open our workbook with the Tree Census Data so we can explore another example together.


Part I: Designing a Story

Many successful data visualizations and dashboards start by working on paper first. This is where the storytelling process begins.

Think about the following, and write or sketch out what comes to mind:

    What is the objective, or core question(s), of the viz? In other words, What question do you want to answer?
    Who is the intended audience?
    What data will be used and what insights can be drawn from it?

With these questions in mind, we can begin to carve out the viewer’s journey. If we’re making an argument, we may want to identify supporting data and think about the best sequence to present it in. For a narrative, we may want to give viewers the option to explore the data to come up with their own conclusion, or we might choose to lead the viewer to a specific conclusion.

Generally, the best way to present a story in Tableau is using a dashboard, which is a combination of several visualizations that can be arranged in a single presentation, like an interactive poster. We may also opt to use a Tableau story, which is a series of visualizations or dashboards. Stories allow us to use buttons to navigate through the views, like turning pages of a book.

Tableau offers some commonly used approaches to storytelling with data that can help us find focus in a visualization or dashboard.

    Change Over Time: Uses temporal data to illustrate trends or shifts
    Drill Down: Starts with the bigger picture, then gets into finer details
    Zoom Out: Starts with a smaller detail then gets into broad and high-level picture
    Contrast: Depicts differences between 2+ subjects
    Intersections: Explores how 2 initially separate dimensions may converge
    Factors: Takes a broader subject and divides it into factors (types/categories)
    Outliers: Highlights and profiles outlier in the data


list1 = [1,2,3,4]

To convert this to a one-dimensional ndarray with one row and four columns, we can use the np.array() function:

array1 = np.array(list1)
print(array1)

Output:

[1 2 3 4]

To get a two-dimensional ndarray from a list, we must start with a Python list of lists:

list2 = [[1,2,3],[4,5,6]]
array2 = np.array(list2)
print(array2)

Output:

[[1 2 3]
 [4 5 6]]

In the above output, you may notice that the NumPy array print-out is displayed in a way that clearly demonstrates its multi-dimensional structure: two rows and three columns.

Many operations can be performed on NumPy arrays which makes them very helpful for manipulating data:

    Selecting array elements

    Slicing arrays

    Reshaping arrays

    Splitting arrays

    Combining arrays

    Numerical operations (min, max, mean, etc)

Mathematical operations can be performed on all values in a ndarray at one time rather than having to loop through values, as is necessary with a Python list. This is very helpful in many scenarios. Say you own a toy store and decide to decrease the price of all toys by €2 for a weekend sale. With the toy prices stored in an ndarray, you can easily facilitate this operation.

toyPrices = np.array([5,8,3,6])
print(toyPrices - 2)

Output:

[3 6 1 4]

If, however, you had stored your toy prices in a Python list, you would have to manually loop through the entire list to decrease each toy price.

toyPrices = [5,8,3,6]
# print(toyPrices - 2) -- Not possible. Causes an error
for i in range(len(toyPrices)):
    toyPrices[i] -= 2
print(toyPrices)

Output:

[3,6,1,4]

Pandas Series and Dataframes

Just as the ndarray is the foundation of the NumPy library, the Series is the core object of the pandas library. A pandas Series is very similar to a one-dimensional NumPy array, but it has additional functionality that allows values in the Series to be indexed using labels. A NumPy array does not have the flexibility to do this. This labeling is useful when you are storing pieces of data that have other data associated with them. Say you want to store the ages of students in an online course to eventually figure out the average student age. If stored in a NumPy array, you could only access these ages with the internal ndarray indices 0,1,2.... With a Series object, the indices of values are set to 0,1,2... by default, but you can customize the indices to be other values such as student names so an age can be accessed using a name. Customized indices of a Series are established by sending values into the Series constructor, as you will see below.

A Series holds items of any one data type and can be created by sending in a scalar value, Python list, dictionary, or ndarray as a parameter to the pandas Series constructor. If a dictionary is sent in, the keys may be used as the indices.

# Create a Series using a NumPy array of ages with the default numerical indices
ages = np.array([13,25,19])
series1 = pd.Series(ages)
print(series1)

Output:

0  |  13
1  |  25
2  |  19
dtype: int64

When printing a Series, the data type of its elements is also printed. To customize the indices of a Series object, use the index argument of the Series constructor.

# Create a Series using a NumPy array of ages but customize the indices to be the names that correspond to each age
ages = np.array([13,25,19])
series1 = pd.Series(ages,index=['Emma', 'Swetha', 'Serajh'])
print(series1)

Output:

Emma    |  13
Swetha  |  25
Serajh  |  19
dtype: int64

Series objects provide more information than NumPy arrays do. Printing a NumPy array of ages does not print the indices or allow us to customize them.

ages = np.array([13,25,19])
print(ages)

Output:

[13 25 19]

Another important type of object in the pandas library is the DataFrame. This object is similar in form to a matrix as it consists of rows and columns. Both rows and columns can be indexed with integers or String names. One DataFrame can contain many different types of data types, but within a column, everything has to be the same data type. A column of a DataFrame is essentially a Series. All columns must have the same number of elements (rows).

There are different ways to fill a DataFrame such as with a CSV file, a SQL query, a Python list, or a dictionary. Here we have created a DataFrame using a Python list of lists. Each nested list represents the data in one row of the DataFrame. We use the keyword columns to pass in the list of our custom column names.

dataf = pd.DataFrame([
    ['John Smith','123 Main St',34],
    ['Jane Doe', '456 Maple Ave',28],
    ['Joe Schmo', '789 Broadway',51]
    ],
    columns=['name','address','age'])

This is how the DataFrame is displayed:

          name      |   address     |   age
0    | John Smith   | 123 Main St   |   34
1    | Jane Doe     | 456 Maple Ave |   28
2    | Joe Schmo    | 789 Broadway  |   51

The default row indices are 0,1,2..., but these can be changed. For example, they can be set to be the elements in one of the columns of the DataFrame. To use the names column as indices instead of the default numerical values, we can run the following command on our DataFrame:

dataf.set_index('name')

Output:

   name      |   address     |  age
John Smith   | 123 Main St   |   34
Jane Doe     | 456 Maple Ave |   28
Joe Schmo    | 789 Broadway  |   51

DataFrames are useful because they make it much easier to select, manipulate, and summarize data. Their tabular format (a table with rows and columns) also makes it easier to label, simpler to read, and easier to export data to and from a spreadsheet. Understanding the power of these new data structures is the key to unlocking many new avenues for data manipulation, exploration, and analysis!


Loading and Saving CSVs
4 min

When you have data in a CSV, you can load it into a DataFrame in Pandas using .read_csv():

pd.read_csv('my-csv-file.csv')

In the example above, the .read_csv() method is called. The CSV file called my-csv-file is passed in as an argument.

We can also save data to a CSV, using .to_csv().

df.to_csv('new-csv-file.csv')

In the example above, the .to_csv() method is called on df (which represents a DataFrame object). The name of the CSV file is passed in as an argument (new-csv-file.csv). By default, this method will save the CSV file in your current directory.


Setting indices
7 min

When we select a subset of a DataFrame using logic, we end up with non-consecutive indices. This is inelegant and makes it hard to use .iloc().

We can fix this using the method .reset_index(). For example, here is a DataFrame called df with non-consecutive indices:
	First Name 	Last Name
0 	John 	Smith
4 	Jane 	Doe
7 	Joe 	Schmo

If we use the command df.reset_index(), we get a new DataFrame with a new set of indices:
	index 	First Name 	Last Name
0 	0 	John 	Smith
1 	4 	Jane 	Doe
2 	7 	Joe 	Schmo

Note that the old indices have been moved into a new column called 'index'. Unless you need those values for something special, it’s probably better to use the keyword drop=True so that you don’t end up with that extra column. If we run the command df.reset_index(drop=True), we get a new DataFrame that looks like this:
	First Name 	Last Name
0 	John 	Smith
1 	Jane 	Doe
2 	Joe 	Schmo

Using .reset_index() will return a new DataFrame, but we usually just want to modify our existing DataFrame. If we use the keyword inplace=True we can just modify our existing DataFrame.

Calculating Column Statistics
9 min

Aggregate functions summarize many data points (i.e., a column of a dataframe) into a smaller set of values.

Some examples of this type of calculation include:

    The DataFrame customers contains the names and ages of all of your customers. You want to find the median age:

print(customers.age)
>> [23, 25, 31, 35, 35, 46, 62]
print(customers.age.median())
>> 35

    The DataFrame shipments contains address information for all shipments that you’ve sent out in the past year. You want to know how many different states you have shipped to (and how many shipments went to the same state).

print(shipments.state)
>> ['CA', 'CA', 'CA', 'CA', 'NY', 'NY', 'NJ', 'NJ', 'NJ', 'NJ', 'NJ', 'NJ', 'NJ']
print(shipments.state.nunique())
>> 3

    The DataFrame inventory contains a list of types of t-shirts that your company makes. You want a list of the colors that your shirts come in.

print(inventory.color)
>> ['blue', 'blue', 'blue', 'blue', 'blue', 'green', 'green', 'orange', 'orange', 'orange']
print(inventory.color.unique())
>> ['blue', 'green', 'orange']

The general syntax for these calculations is:

df.column_name.command()

The following table summarizes some common commands:
Command 	Description
mean 	Average of all values in column
std 	Standard deviation
median 	Median
max 	Maximum value in column
min 	Minimum value in column
count 	Number of values in column
nunique 	Number of unique values in column
unique 	List of unique values in column

Aggregates in Pandas
Calculating Aggregate Functions I
8 min

When we have a bunch of data, we often want to calculate aggregate statistics (mean, standard deviation, median, percentiles, etc.) over certain subsets of the data.

Suppose we have a grade book with columns student, assignment_name, and grade. The first few lines look like this:
student 	assignment_name 	grade
Amy 	Assignment 1 	75
Amy 	Assignment 2 	35
Bob 	Assignment 1 	99
Bob 	Assignment 2 	35
… 		

We want to get an average grade for each student across all assignments. We could do some sort of loop, but Pandas gives us a much easier option: the method .groupby.

For this example, we’d use the following command:

grades = df.groupby('student').grade.mean()

The output might look something like this:
student 	grade
Amy 	80
Bob 	90
Chris 	75
… 	

In general, we use the following syntax to calculate aggregates:

df.groupby('column1').column2.measurement()

where:

    column1 is the column that we want to group by ('student' in our example)
    column2 is the column that we want to perform a measurement on (grade in our example)
    measurement is the measurement function we want to apply (mean in our example)


Aggregates in Pandas
Calculating Aggregate Functions IV
8 min

Sometimes, we want to group by more than one column. We can easily do this by passing a list of column names into the groupby method.

Imagine that we run a chain of stores and have data about the number of sales at different locations on different days:
Location 	Date 	Day of Week 	Total Sales
West Village 	February 1 	W 	400
West Village 	February 2 	Th 	450
Chelsea 	February 1 	W 	375
Chelsea 	February 2 	Th 	390

We suspect that sales are different at different locations on different days of the week. In order to test this hypothesis, we could calculate the average sales for each store on each day of the week across multiple months. The code would look like this:

df.groupby(['Location', 'Day of Week'])['Total Sales'].mean().reset_index()

The results might look something like this:
Location 	Day of Week 	Total Sales
Chelsea 	M 	402.50
Chelsea 	Tu 	422.75
Chelsea 	W 	452.00
… 		
West Village 	M 	390
West Village 	Tu 	400
… 		

Aggregates in Pandas
Pivot Tables
10 min

When we perform a groupby across multiple columns, we often want to change how our data is stored. For instance, recall the example where we are running a chain of stores and have data about the number of sales at different locations on different days:
Location 	Date 	Day of Week 	Total Sales
West Village 	February 1 	W 	400
West Village 	February 2 	Th 	450
Chelsea 	February 1 	W 	375
Chelsea 	February 2 	Th 	390
We suspected that there might be different sales on different days of the week at different stores, so we performed a `groupby` across two different columns (`Location` and `Day of Week`). This gave us results that looked like this:
Location 	Day of Week 	Total Sales
Chelsea 	M 	300
Chelsea 	Tu 	310
Chelsea 	W 	375
Chelsea 	Th 	390
… 		
West Village 	Th 	450
West Village 	F 	390
West Village 	Sa 	250
… 		
In order to test our hypothesis, it would be more useful if the table was formatted like this:
Location 	M 	Tu 	W 	Th 	F 	Sa 	Su
Chelsea 	300 	310 	375 	390 	300 	150 	175
West Village 	300 	310 	400 	450 	390 	250 	200
… 							

Reorganizing a table in this way is called pivoting. The new table is called a pivot table.

In Pandas, the command for pivot is:

df.pivot(columns='ColumnToPivot',
         index='ColumnToBeRows',
         values='ColumnToBeValues')

For our specific example, we would write the command like this:

# First use the groupby statement:
unpivoted = df.groupby(['Location', 'Day of Week'])['Total Sales'].mean().reset_index()
# Now pivot the table
pivoted = unpivoted.pivot(
    columns='Day of Week',
    index='Location',
    values='Total Sales')

Just like with groupby, the output of a pivot command is a new DataFrame, but the indexing tends to be “weird”, so we usually follow up with .reset_index().

Working with Multiple DataFrames
Inner Merge II
8 min

It is easy to do this kind of matching for one row, but hard to do it for multiple rows.

Luckily, Pandas can efficiently do this for the entire table. We use the .merge() method.

The .merge() method looks for columns that are common between two DataFrames and then looks for rows where those column’s values are the same. It then combines the matching rows into a single row in a new table.

We can call the pd.merge() method with two tables like this:

new_df = pd.merge(orders, customers)

This will match up all of the customer information to the orders that each customer made.



Inner Merge III
10 min

In addition to using pd.merge(), each DataFrame has its own .merge() method. For instance, if you wanted to merge orders with customers, you could use:

new_df = orders.merge(customers)

This produces the same DataFrame as if we had called pd.merge(orders, customers).

We generally use this when we are joining more than two DataFrames together because we can “chain” the commands. The following command would merge orders to customers, and then the resulting DataFrame to products:

big_df = orders.merge(customers)\
    .merge(products)


Merge on Specific Columns
8 min

In the previous example, the .merge() function “knew” how to combine tables based on the columns that were the same between two tables. For instance, products and orders both had a column called product_id. This won’t always be true when we want to perform a merge.

Generally, the products and customers DataFrames would not have the columns product_id or customer_id. Instead, they would both be called id and it would be implied that the id was the product_id for the products table and customer_id for the customers table. They would look like this:
Customers
id	customer_name	address	phone_number
1	John Smith	123 Main St.	212-123-4567
2	Jane Doe	456 Park Ave.	949-867-5309
3	Joe Schmo	798 Broadway	112-358-1321
Products
id	description	price
1	thing-a-ma-jig	5
2	whatcha-ma-call-it	10
3	doo-hickey	7
4	gizmo	3

**How would this affect our merges?**

Because the id columns would mean something different in each table, our default merges would be wrong.

One way that we could address this problem is to use .rename() to rename the columns for our merges. In the example below, we will rename the column id to customer_id, so that orders and customers have a common column for the merge.

pd.merge(
    orders,
    customers.rename(columns={'id': 'customer_id'}))

