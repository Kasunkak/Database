## Question 1
### List all Finnish airports that provide scheduled services. The result must include both the name of the country as well as the name of the airport.
select country.name as "country name", airport.name as "airport name"
from country inner join airport on country.iso_country=airport.iso_country
where country.name="Finland"
and airport.scheduled_service="yes";

![Question 1](https://github.com/user-attachments/assets/4fba05c9-1f38-4ab6-b94e-f46b3d2b347d)


## Question 2
### List the names and current airports of all players.
select screen_name, airport.name
from game inner join airport on game.location = airport.ident;

![Question 2](https://github.com/user-attachments/assets/9e7aef7a-e610-4d5b-83f2-b717ce893213)


## Question 3
### List the names and current countries of all players.
select screen_name, country.name
from game inner join airport on game.location = airport.ident
inner join country on country.iso_country=airport.iso_country;

![Question 3](https://github.com/user-attachments/assets/752aa97d-6ebc-4940-81d7-c377ea620efe)


## Question 4
### List the names of all airports that include the string "Hels" and the names of any players that might currently be on any of the listed airports.
select airport.name, screen_name
from airport left join game on airport.ident = game.location
where airport.name like "%Hels%";

![Question 4](https://github.com/user-attachments/assets/d338fcf9-39c8-4935-a7da-2b60628d6c94)


## Question 5
### List the names of all weather goals and the names of any players that have so far achieved the listed goals.
select name, screen_name
from goal left join goal_reached on goal.id = goal_reached.goal_id
left join game on goal_reached.game_id = game.id;

![Question 5](https://github.com/user-attachments/assets/ecd7e036-bb73-45db-9d1b-7761e586bd6e)

