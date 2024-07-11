1) Write a query that counts all orders for October 3.

![Assignment7](image-19.png)

2) Write a query that counts the number of different non-NULL city values in the Customers table. 

![Assignment7](image-20.png)

3) Write a query that selects each customer’s smallest order.

![Assignment7](image-21.png)

4) Write a query that selects the first customer, in alphabetical order, whose name begins with G.

![Assignment7](image-22.png)

5) Write a query that selects the highest rating in each city. 

![Assignment7](image-23.png)

6) Write a query that counts the number of salespeople registering orders for each day. (If a salesperson has more than one order on a given day, he or she should be counted only once).

![Assignment7](image-24.png)

Partially solved
{
    select odate , count(odate) as Orders_Count from ( select sname,orders.odate from salespeople inner join orders on orders.snum = salespeople.snum ) as o group by odate ;
}

