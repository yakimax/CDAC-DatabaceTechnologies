# VIEWS

Views are virtual table that does not store data directly .
They are essentially a saved sql querry .
 

# CREATE VIEW

{
    CREATE VIEW view_name AS
    SELECT * from table_name ;
}

# MODIFY VIEW

{
    CREATE OR REPLACE VIEW view_name 
    SELECT column1,column2 from table_name ;
}

# DROP VIEW

{
    DROP VIEW view_name ;
}

NOTE : *we cannot use order by clause in Views*