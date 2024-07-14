# COALESCE

COALESCE function is used to replace possible NULL   value with desired value while retreiving/querrying   the data.

```
    Syntax:-
    COALESCE( column , replacement_value );
    SELECT ename,COALSCE(salary,0) as Salary from employee ;
    returns 0 in place of possible NULL in salary column
```