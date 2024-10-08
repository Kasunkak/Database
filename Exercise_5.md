## Question 1
### One country has an airport where the airport name begins with the word "Satsuma". Print out the name of the country.
select name from country where iso_country in(
select iso_country from airport where name like 'Satsuma%');

![Q1](https://github.com/user-attachments/assets/2998bcf4-007d-4be0-97e6-f1b866431100)

## Question 2
### List the names of all airports in Monaco.
select name from airport
where iso_country in(
select iso_country from country
where name = 'Monaco');

![Q2](https://github.com/user-attachments/assets/8d8c24af-fc5d-4f7e-a937-2ee3b41db22f)

## Question 3
### List the names of all players who have achieved the clouds goal.
select screen_name from game
where id in (
select game_id from goal_reached
where goal_id in (
select id from goal
where name = "CLOUDS"));

![Q3](https://github.com/user-attachments/assets/3e40018a-2e42-4fcd-becc-0a2f9164fce4)

## Question 4
### List all countries that have no airports.
select name from country
where iso_country not in(
select iso_country from airport);

![Q4](https://github.com/user-attachments/assets/a22da6bb-f39e-4fbf-ba67-6b757af87b6b)

## Question 5
### Which weather goals has Heini not achieved yet?
select name from goal
where id not in(
select goal_id from goal_reached
where game_id in (
select id from game
where screen_name = "Heini"));

![Q5](https://github.com/user-attachments/assets/9fb51b8b-3424-4efe-82bb-27fec911eec1)
