# SUBSTRING

SUBSTRING function is used to extract a part of the string 
mentioning the starting position and the length of extraction .

{
    SUBSTRING('string',start,length);
    EX:-
    SUBSTRING('Hello_World',1,5);
    result => 'Hello'
}

on table

{
    SELECT SUBSTRING(Column1,start,length) AS Extracted_String from table_name ;
}
