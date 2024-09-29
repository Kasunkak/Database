![image](https://github.com/user-attachments/assets/c85c56ae-5b30-4502-84db-9c770153a81c)# Exercise 2
## Question 1
### Write a query that prints out all the columns in the goal table.
select*from goal;

![Exercise 2 Q1](https://github.com/user-attachments/assets/bc1bdcd2-8e42-4273-9aa5-38e7b5787c17)

## Question 2
### Write a query that prints out the name and type of each airport in Finland. The country code for Finland is: FI.
SELECT name, type
FROM airports
WHERE country_code = 'FI';

![Exercise 2 Q2](https://github.com/user-attachments/assets/6adfe165-a50e-416e-ac44-4bf086afd651)

## Question 3
### Write a query that prints out the names of all Finnish airports in alphabetical order. The country code for Finland is: FI.
SELECT name
FROM airports
WHERE country_code = 'FI'
ORDER BY name ASC;

![Exercise2 Q3](https://github.com/user-attachments/assets/f2920d1a-139a-442e-92f0-22cffa9143fa)

## Question 4
### Write a query that prints out the name and type of each Finnish airport. Order the result first by type and secondly by name.
SELECT name, type
FROM airports
WHERE country_code = 'FI'
ORDER BY type, name;

![Exercise 2 Q4](https://github.com/user-attachments/assets/0bd47a99-c37f-43e8-95c2-ecaef7bcfa29)

## Question 5
### Write a query that prints out the names of all countries that start with the letter F from the country table.
SELECT name
FROM country
WHERE name LIKE 'F%';

![Exercise 2 Q5](https://github.com/user-attachments/assets/7ccdded6-7331-4461-976f-38863976790b)

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
