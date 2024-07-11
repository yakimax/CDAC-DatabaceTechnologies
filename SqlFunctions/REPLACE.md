# REPLACE

REPLACE function in used in sql to subsitute a part/whole of string occurence within a string.
Arguments : input_string,string_to_replace,replacement_string

{
    REPLACE(input_string,string_to_replace,replacement_string)
    EX:-
    SELECT name,REPLACE(column1,'some_string','replacement') as
    replaced_namesfrom table_name ;
}