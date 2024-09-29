# Exercise 2
## Question 1
### Write a query that prints out all the columns in the goal table.
select*from goal;

![Exercise 2 Q1](https://github.com/user-attachments/assets/bc1bdcd2-8e42-4273-9aa5-38e7b5787c17)

## Question 2
### Write a query that prints out the name and type of each airport in Finland. The country code for Finland is: FI.
SELECT name, type
FROM airports
WHERE country_code = 'FI';


