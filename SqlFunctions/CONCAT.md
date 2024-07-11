Function in SQL

# CONCAT

Concat functions allows you to concatenate two or more strings.

{
    CONCAT(string1, string2, ..., string_n)
}

Concat function also allows to concatenate two or more columns within a table

{
    SELECT CONCAT(column1, ' ', column2) AS alias FROM table_name ;
}

*** However , CONCAT will *return NULL* if any of the input strings is NULL .

# CONCAT_WS

*avoid this, you can use the CONCAT_WS function which accepts a separator as the first argument and then a list of strings to concatenate .*

{
    SELECT CONCAT_WS(' ',Column1,Column2) as Alias from table_name ;
}

