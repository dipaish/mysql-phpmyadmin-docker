## In-Class Task 1: Getting Started with Database

1. Write a SQL statement to create a new database named fname_lname (replace fname and lname with your first and last name, respectively).

2. Use the SHOW DATABASES; command to verify that the database has been created.

3. Write a SQL statement to set the newly created database fname_lname as the current database.

4. Write a SQL statement to to create a new database named database24. 

5. Write a SQL statement to drop the fname_lname database.

6. Write a SQL statement to set the newly created database database24 as the current database.

6. Write a SQL statement to display the list of tables in the selected database. 

7. Run the following SQL statement to create a table in database24. 

```
CREATE TABLE students (
    id INT AUTO_INCREMENT PRIMARY KEY,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    email VARCHAR(100) UNIQUE
);
```
