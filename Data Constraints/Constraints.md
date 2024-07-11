## Data Constraints

Data constraints in SQL are used to specify rules for the data in a table. Constraints are used to limit the type of data that can go into a table. This ensures the accuracy and reliability of the data in the table.

Types of SQL Data Constraints :-

# NOT NULL 
    - Ensures that a column cannot have a NULL 

```
CREATE TABLE Students (
    ID int NOT NULL,
    Name varchar(255) NOT NULL,
    Age int
);
```

```
    ALTER TABLE Employees
    MODIFY Address varchar(255) NOT NULL;
```

# UNIQUE 
    - Ensures that all values in a column are different
```
CREATE TABLE Students (
    ID int NOT NULL UNIQUE,
    Name varchar(255) NOT NULL,
    Age int
);
```

```
    ALTER TABLE table_name
    ADD UNIQUE (column1, column2, ...);
```

# PRIMARY KEY 
    - A combination of a NOT NULL and UNIQUE. Uniquely identifies each row in a table
```
CREATE TABLE Students (
    ID int NOT NULL,
    Name varchar(255) NOT NULL,
    Age int,
    PRIMARY KEY (ID)
);
```

```
    ALTER TABLE Employees
    ADD PRIMARY KEY (ID);
```

# FOREIGN KEY 
    - Prevents actions that would destroy links between tables
```
CREATE TABLE Orders (
    OrderID int NOT NULL,
    OrderNumber int NOT NULL,
    ID int,
    PRIMARY KEY (OrderID),
    FOREIGN KEY (ID) REFERENCES Students(ID)
);
```

```
    ALTER TABLE child_table
    ADD FOREIGN KEY (fk_column)
    REFERENCES parent_table (parent_key_column)
```

# CHECK 
    - Ensures that the values in a column satisfies a specific condition

```
CREATE TABLE Students (
    ID int NOT NULL,
    Name varchar(255) NOT NULL,
    Age int,
    CHECK (Age>=18)
);
```

```
    ALTER TABLE Employees
    ADD CONSTRAINT CHK_EmployeeAge CHECK (Age >= 21 AND Age <= 60);
```

# DEFAULT 
    - Sets a default value for a column if no value is specified
```
CREATE TABLE Students (
    ID int NOT NULL,
    Name varchar(255) NOT NULL,
    Age int,
    City varchar(255) DEFAULT 'Unknown'
);
```


# CREATE INDEX 
    - Used to create and retrieve data from the database very quickly
