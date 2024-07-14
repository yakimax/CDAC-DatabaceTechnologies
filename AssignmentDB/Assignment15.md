1) Assume there is a table called Multicust, with all of the same column definitions as Salespeople. Write a command that inserts all salespeople with more than one customer into this table.

```
insert into multicust select * from salespeople where snum = ANY (select snum,count(cnum)cust from customer group by snum having cust > 1)
```

2) Write a command that deletes all customers with no current orders.

```
delete from customers where cnum NOT IN ( select cnum from customer join orders on orders.cnum = customer.cnum );
```

3) Write a command that increases by twenty percent the commissions of all salespeople with total orders above Rs.3000.

```
update salespeople set comm = comm + .20 where snum = any  (select distinct salespeople.snum from salespeople join orders on salespeople.snum = orders.snum) ; 
```