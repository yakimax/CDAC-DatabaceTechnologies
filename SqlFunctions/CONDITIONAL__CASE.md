# CASE

CASE statement in sql is used to perform WHEN-THEN-ELSE Logic within sql queries .

```
CASE
    WHEN condition1 THEN 'result1' ;
    WHEN condition2 THEN 'result2' ;
    WHEN condition3 THEN 'result3' ;
    -
    -
    -
    ELSE default_result ;
END
```

EX:-
    SELECT product_name,price
    (CASE
        WHEN price > 30,000 THEN '30% discount'
        WHEN price > 20,000 THEN '20% discount'
        WHEN price > 10,000 THEN '10% discount'
        ELSE 'not on sale'
    END)
    from products ;

