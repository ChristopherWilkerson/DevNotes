
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
