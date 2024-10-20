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

![Exercise 2 Q6](https://github.com/user-attachments/assets/eecfb75d-21e5-4c63-bb8c-ced68266fd2c)

## Question 7
### What is Vesa's current location? 
SELECT location 
FROM game 
WHERE screen_name = "Vesa";

![Exercise Q7](https://github.com/user-attachments/assets/7de5b4d8-a11c-4abd-8acc-6ba5dd10c107)

## Question 8
### How much of his CO2 budget has Ilkka consumed? 
SELECT co2_consumed 
FROM game 
WHERE screen_name = "Ilkka";

![Exercise 2 Q8](https://github.com/user-attachments/assets/a2e8e9d8-62fd-41d5-95d9-d061ea9521f5)

## Question 9
### What is the original CO2 budget? Print out the CO2 budget value only once.
SELECT co2_budget 
FROM game 
LIMIT 1;

![Exercise 2 Q9](https://github.com/user-attachments/assets/1e6c16ce-0acf-4bd1-9e60-e853888d7a76)

## Question 10
### How much of his CO2 budget does Ilkka have left? Complete the query so that the result includes the following fields: screen_name, co2_budget, co2_consumed and co2_left.
select screen_name, co2_budget, co2_consumed, co2_budget - co2_consumed as co2_left from game;

![Exercise 2 Q10](https://github.com/user-attachments/assets/97a240ad-0b95-4123-baed-65eba60f8f40)
