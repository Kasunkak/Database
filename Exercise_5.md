## Question 1
### One country has an airport where the airport name begins with the word "Satsuma". Print out the name of the country.
select name from country where iso_country in(
select iso_country from airport where name like 'Satsuma%');

![Q 1](https://github.com/user-attachments/assets/b888567f-7b2b-4a90-9d31-75580293e9f9)


## Question 2
### List the names of all airports in Monaco.
select name from airport
where iso_country in(
select iso_country from country
where name = 'Monaco');

![Q 2](https://github.com/user-attachments/assets/7c62059d-79f1-421d-9fd5-2effa25ac2a5)


## Question 3
### List the names of all players who have achieved the clouds goal.
select screen_name from game
where id in (
select game_id from goal_reached
where goal_id in (
select id from goal
where name = "CLOUDS"));

![Q 3](https://github.com/user-attachments/assets/5ba4be67-7b6d-4645-9e00-78ae675a079b)


## Question 4
### List all countries that have no airports.
select name from country
where iso_country not in(
select iso_country from airport);

![Q 4](https://github.com/user-attachments/assets/d3804b8f-4adf-43de-8225-04b5e337b179)


## Question 5
### Which weather goals has Heini not achieved yet?
select name from goal
where id not in(
select goal_id from goal_reached
where game_id in (
select id from game
where screen_name = "Heini"));

![Q 5](https://github.com/user-attachments/assets/ae5cbd23-7294-4272-bc10-613f499e2a73)

