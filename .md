## SQL Server Cheat Sheet

<details>
<summary> 1. Data Definition Language (DDL)</summary>
Used for defining and modifying database schemas.

- **CREATE**
  - **Syntax**: `CREATE TABLE table_name (column_name data_type, ...);`
  - **Example**: 
    ```sql
    CREATE TABLE Employees (
        EmployeeID int,
        FirstName varchar(255),
        LastName varchar(255),
        BirthDate datetime
    );
    ```
  - **Use**: Creates a new table called `Employees`.

- **ALTER**
  - **Syntax**: `ALTER TABLE table_name ADD|MODIFY column_name data_type;`
  - **Example**: 
    ```sql
    ALTER TABLE Employees ADD Email varchar(255);
    ```
  - **Use**: Adds a new column `Email` to the `Employees` table.

- **DROP**
  - **Syntax**: `DROP TABLE table_name;`
  - **Example**: 
    ```sql
    DROP TABLE Employees;
    ```
  - **Use**: Deletes the `Employees` table.
</details>

<details>
<summary> 2. Data Manipulation Language (DML)</summary>
Used for inserting, updating, deleting, and managing data within tables.

- **INSERT**
  - **Syntax**: `INSERT INTO table_name (column1, column2, ...) VALUES (value1, value2, ...);`
  - **Example**: 
    ```sql
    INSERT INTO Employees (EmployeeID, FirstName, LastName, BirthDate) VALUES (1, 'Jane', 'Doe', '1980-01-15');
    ```
  - **Use**: Inserts a new record into `Employees`.

- **UPDATE**
  - **Syntax**: `UPDATE table_name SET column1 = value1 WHERE condition;`
  - **Example**: 
    ```sql
    UPDATE Employees SET Email = 'jane.doe@example.com' WHERE EmployeeID = 1;
    ```
  - **Use**: Updates the `Email` of an employee.

- **DELETE**
  - **Syntax**: `DELETE FROM table_name WHERE condition;`
  - **Example**: 
    ```sql
    DELETE FROM Employees WHERE EmployeeID = 1;
    ```
  - **Use**: Deletes a record from `Employees`.
</details>

<details>
<summary> 3. Data Query Language (DQL)</summary>
Used for querying data.

- **SELECT**
  - **Syntax**: `SELECT column1, column2 FROM table_name WHERE condition;`
  - **Example**: 
    ```sql
    SELECT FirstName, LastName FROM Employees WHERE BirthDate < '1990-01-01';
    ```
  - **Use**: Retrieves specific employee records.
</details>

<details>
<summary> 4. Data Control Language (DCL)</summary>
Used for defining access permissions.

- **GRANT**
  - **Syntax**: `GRANT permission_type ON database_name.table_name TO 'username';`
  - **Example**: 
    ```sql
    GRANT SELECT, UPDATE ON Employees TO User123;
    ```
  - **Use**: Grants select and update permissions on `Employees` to `User123`.

- **REVOKE**
  - **Syntax**: `REVOKE permission_type ON database_name.table_name FROM 'username';`
  - **Example**: 
    ```sql
    REVOKE UPDATE ON Employees FROM User123;
    ```
  - **Use**: Revokes update permissions from `User123`.
</details>

<details>
 <summary>5. Transaction Control Language (TCL) </summary>
Used for managing transactions.

- **BEGIN TRANSACTION**
  - **Syntax**: `BEGIN TRANSACTION;`
  - **Example**: 
    ```sql
    BEGIN TRANSACTION;
    ```
  - **Use**: Starts a new transaction.

- **COMMIT**
  - **Syntax**: `COMMIT;`
  - **Example**: 
    ```sql
    COMMIT;
    ```
  - **Use**: Commits the current transaction.

- **ROLLBACK**
  - **Syntax**: `ROLLBACK;`
  - **Example**: 
    ```sql
    ROLLBACK;
    ```
  - **Use**: Reverts changes made during the current transaction.
 
</details>
