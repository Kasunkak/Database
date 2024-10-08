## Question 1
### List all Finnish airports that provide scheduled services. The result must include both the name of the country as well as the name of the airport.
select country.name as "country name", airport.name as "airport name"
from country inner join airport on country.iso_country=airport.iso_country
where country.name="Finland"
and airport.scheduled_service="yes";

![Q 1](https://github.com/user-attachments/assets/6ebc26ee-58de-44c5-8ae4-85636675336c)

## Question 2
### List the names and current airports of all players.
select screen_name, airport.name
from game inner join airport on game.location = airport.ident;

![Q 2](https://github.com/user-attachments/assets/3b443940-325c-4e97-b228-7a497f8eb479)

## Question 3
### List the names and current countries of all players.
select screen_name, country.name
from game inner join airport on game.location = airport.ident
inner join country on country.iso_country=airport.iso_country;

![Q 3](https://github.com/user-attachments/assets/57a61eb8-1bcd-4862-861b-00c45ec5b4dd)

## Question 4
### List the names of all airports that include the string "Hels" and the names of any players that might currently be on any of the listed airports.
select airport.name, screen_name
from airport left join game on airport.ident = game.location
where airport.name like "%Hels%";

![Q 4](https://github.com/user-attachments/assets/7de46473-0a1c-4652-8567-f9ecee852f29)

## Question 5
### List the names of all weather goals and the names of any players that have so far achieved the listed goals.
select name, screen_name
from goal left join goal_reached on goal.id = goal_reached.goal_id
left join game on goal_reached.game_id = game.id;

![Q 5](https://github.com/user-attachments/assets/7831396f-edf3-4f44-83ee-db9953597484)
