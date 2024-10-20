![image](https://github.com/user-attachments/assets/c85c56ae-5b30-4502-84db-9c770153a81c)# Exercise 2
## Question 1
### Write a query that prints out all the columns in the goal table.
select*from goal;

![Ex 2 Question 1](https://github.com/user-attachments/assets/166d2344-f51f-414c-b535-a21de44bbb47)


## Question 2
### Write a query that prints out the name and type of each airport in Finland. The country code for Finland is: FI.
SELECT name, type
FROM airports
WHERE country_code = 'FI';

![Ex2 Question 2](https://github.com/user-attachments/assets/ccaea60a-0154-4c39-a9b5-f986967ea8e8)


## Question 3
### Write a query that prints out the names of all Finnish airports in alphabetical order. The country code for Finland is: FI.
SELECT name
FROM airports
WHERE country_code = 'FI'
ORDER BY name ASC;

![Ex2 Question 3](https://github.com/user-attachments/assets/2a2ca44d-5a0c-45ef-8fbe-945abe4f8bd8)


## Question 4
### Write a query that prints out the name and type of each Finnish airport. Order the result first by type and secondly by name.
SELECT name, type
FROM airports
WHERE country_code = 'FI'
ORDER BY type, name;

![Ex2 Question 4](https://github.com/user-attachments/assets/f781062b-6d55-4b68-bb24-198526413af4)


## Question 5
### Write a query that prints out the names of all countries that start with the letter F from the country table.
SELECT name
FROM country
WHERE name LIKE 'F%';

![Ex2 Question 5](https://github.com/user-attachments/assets/1f3d3ac6-a01d-45f9-892e-e557c0f32dd1)


## Question 6
### Write a query that prints out all country names in the country table that include the letter F.
SELECT name
FROM country
WHERE name LIKE '%F%';

![Ex2 Question 6](https://github.com/user-attachments/assets/2cab9d78-073c-4ea4-b127-759873546cf5)


## Question 7
### What is Vesa's current location? 
SELECT location 
FROM game 
WHERE screen_name = "Vesa";

![Ex2 Question 7](https://github.com/user-attachments/assets/266022e0-24ac-4050-b8b9-fd7f3f2a36eb)


## Question 8
### How much of his CO2 budget has Ilkka consumed? 
SELECT co2_consumed 
FROM game 
WHERE screen_name = "Ilkka";

![Ex2 Question 8](https://github.com/user-attachments/assets/7a6e43d0-fec5-43f8-8428-6f99d3cfd50b)


## Question 9
### What is the original CO2 budget? Print out the CO2 budget value only once.
SELECT co2_budget 
FROM game 
LIMIT 1;

![Ex2 Question 9](https://github.com/user-attachments/assets/a9b8f5f2-0cc5-4c1a-8f11-23e7e7a6044a)


## Question 10
### How much of his CO2 budget does Ilkka have left? Complete the query so that the result includes the following fields: screen_name, co2_budget, co2_consumed and co2_left.
select screen_name, co2_budget, co2_consumed, co2_budget - co2_consumed as co2_left from game;

![Ex2 Question 10](https://github.com/user-attachments/assets/040992d8-2ba0-4684-9e00-29088256339e)

