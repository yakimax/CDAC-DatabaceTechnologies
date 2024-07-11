# LENGTH

LENGTH function is used to find out the length of a string
also it is used for finding length of all rows of a column.

{
    LENGTH('string') ;

    OR

    SELECT Column1 , LENGTH(Column1) AS Length_column1 from table_name ;
}

# Usage with DISTINCT

distinct lengths of specified fields.

{
    Select DISTINCT LENGTH(Column1) AS Colukmn1_Lengths from table_name ;
}

# Usage with WHERE Clause

{
    Select * from table_name where LENGTH(column1) < x ;
}