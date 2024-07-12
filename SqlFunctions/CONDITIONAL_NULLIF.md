# NULLIF

NULLIF function is a comparison function ,it take two arguments.
it compares two expressions and return NULL if both are equal and first expression if not .

```
    NULLIF(expression1,expression2)
```

Applied as :

```
    SELECT NULLIF(expression1,expression2)  from table_name ;
```

EX:-
    select NULLIF(Email,'NA') from employee ;
    returns null if record in email field found 'NA'