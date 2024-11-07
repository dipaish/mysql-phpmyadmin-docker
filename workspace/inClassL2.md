## In-Class Task 2: Working with Tables - Create Table

1. **Create a Database**: Write a SQL statement to create a new database named fnameClass2 (replace fname with your first name).
2. **Use the Database**: Use the newly created database fnameClass2 for the following tasks.
    1. Create a table named **author** with the following columns:
        - aut_id (integer)
        - aut_fname (varchar, 50 characters)
        - country (varchar, 50 characters)
        - home_city (varchar, 50 characters)
        - created_at (timestamp)

    2. Create a table named **student** with the following columns:
        - student_id (integer, primary key)
        - fname (varchar, 50 characters)
        - lname (varchar, 50 characters)
        - country (varchar, 50 characters)

    3. **Create a Duplicate Structure of a Table:** Create a table named **dup_student** with the same structure as the **student** table without copying the data. 

    4. **Copy Table with Data**: Create a new table **students_copy** that duplicates the structure and data of the **student** table.

    5. Create a table named **author1** with the same structure as author but ensure **aut_id** is a primary key. 

    6. **Add Primary Key Using ALTER TABLE**:
Add a primary key constraint to the **aut_id** column in the author table.

    7. **Remove Primary Key Constraint**:
Remove the primary key constraint from the **aut_id** column in the author1 table.

    8. **Create a Table with a Composite Key** : Create a table named **orders** with columns order_id, product_id, quantity, and set order_id and product_id as a composite primary key.

    10. **Create a Temporary Table**
Create a temporary table named temp_students with the same structure as the **student** table.

    11. **Create a Table with a NOT NULL Constraint**: Create a table named books with columns book_id, title, and author, and ensure that title cannot be null.


    12. **Create a Table with a CHECK Constraint**:  Create a table named employees with columns emp_id, emp_name, salary, and add a CHECK constraint to ensure salary is greater than zero.

    13. **Create a Table with a DEFAULT Constraint** : Create a table orders with a status column having a default value of ‘Pending’.


    14. **Create a Table with a UNIQUE Constraint** Create a table users with a user_id as primary key and an email column with a UNIQUE constraint.

    15. **Describe the Table**: Use the DESCRIBE statement to view the structure of the student table

    16. **Drop a Table**: Drop the students table from the database.
    
    17. **Truncate a Table** : Remove all rows from the dup_students table without deleting the table itself.



