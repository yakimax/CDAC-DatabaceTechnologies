1) Write a query that selects all customers whose ratings are equal to or greater than ANY of Serres’.

```
select cname from customer where rating = ANY (select rating from customer join salespeople on customer.snum = salespeople.snum where salespeople.sname = 'serres')
```

![Assignment11](image-37.png)

2) Write a query using ANY or ALL that will find all salespeople who have no customers located in their city.

!missing case
![Assignment11](image-38.png)

3) Write a query that selects all orders for amounts greater than any for the customers in London.

```
select * from orders where amt > ANY (select amt from orders join customer on orders.cnum = customer.cnum where city = 'london') ;
```

![Assignment11](image-39.png)

4) Write the above query using MIN or MAX.

```
select * from orders where amt > (select max(amt) from orders join customer on customer.cnum = orders.cnum where customer.city = 'london') ;
```

![Assignment11](image-40.png)