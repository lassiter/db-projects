- What data types do each of these values represent?

"A Clockwork Orange" would be a string.
42 would be an integer.
09/02/1945 would be a date formated as MM-DD-YYYY or DD-MM-YYYY.
98.7 would be a float.
$15.99 would be a money data type with a varchar for $.

- Explain in your own words when a database might be used. Explain when a text file might be used.
  You would use a database for when you're needing to store tables of data in a consistant format that is indexable and easily accessible via a query language like SQL.

  You would use a text file for when data doesn't need to be accessed via specific tables at a row/column range or intersection. You would use an a text file to write a novel while you might use a database to keep record of characters or scenes to relate them to eachother.

- Describe one difference between SQL and other programming languages.

SQL is data agnostic, meaning it isn't inherently tied to the variable names passed to it while every other language has data assigned to a variable name. SQL stands for Structured Query Language, meaning that it provides the "slots" for queries variables to be interpreted and retrieve data.

- In your own words, explain how the pieces of a database system fit together at a high level.

A database is a box with binders, being tables, each binder has pages of spreadsheets made up of columns and indexes. You can use a database to simply look at a certain row of a certain table or make it complex as you imagine by combining and inserting columns of data based on a point of data like an index.

You can then query a table or a joined table, to retrieve information as needed based on your query's parameters.

- Explain the meaning of table, row, column, and value.

A value is a piece of data inserted into a row at a column or passed in a query.

You can have many tables and join them together based on a value.

A column is a series of types of data on a table with names like "Zipcode" which would likely be an Integer.

A row is a group of values retained in a series of columns linked to a particular value like an Index.

So, if I had a customer table and was looking for 10001 as a zipcode; I would then select all the rows in the customer table that have 10001 in the column.

- List 3 data types that can be used in a table.
String, Integer, Float.

- Given this payments table, provide an English description of the following queries and include their results:
```sql
  SELECT date, amount
  FROM payments;

  SELECT amount
  FROM payments
  WHERE amount > 500;

  SELECT *
  FROM payments
  WHERE payee = 'Mega Foods';
```

  1. Show me only the `date` and `amount` of each row from the `payments` table.
  2. Show me only the `amount` of each row where `amount` is greater than 500 from the `payments` table.
  3. Show me all the records of each row where "Mega Foods" is the `payee` from the `payments` table..

- Given this users table, write SQL queries using the following criteria and include the output:

  - The email and sign-up date for the user named DeAndre Data.
  ```sql
    SELECT email, sign_up_date
    FROM user
    WHERE name = 'DeAndre Data';
  ```
  - The user ID for the user with email 'aleesia.algorithm@uw.edu'.
  ```sql
    SELECT user_id
    FROM user
    WHERE email = 'aleesia.algorithm@uw.edu';
  ```
  - All the columns for the user ID equal to 4.
  ```sql
    SELECT *
    FROM user
    WHERE id = 4;
  ```