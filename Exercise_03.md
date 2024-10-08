## Question 1
### Write a query that lists the names of all countries and airports. Select Iceland as the country and assign the following aliases:
### name column of the country table:  alias "country name"
### name column of the airport table: alias "airport name"
SELECT country.name as "country name", airport.name as "airport name"
FROM country, airport
WHERE country.iso_country = airport.iso_country and country.name = "Iceland";

![Q1](https://github.com/user-attachments/assets/cc784c20-fe88-43bc-8af8-89306bc0e446)

## Question 2
### Write a query  to list the names of all large airports in France. Assign the name column the alias "airport name".
SELECT airport.name as "airport name"
FROM airport, country
where airport.iso_country=country.iso_country and country.name = "France" AND airport.type = "large_airport";

![Q2](https://github.com/user-attachments/assets/5bbf5148-c7d2-4964-a1a3-d682150ba6db)

## Question 3
### Write a query that lists the names and country names of all airports on Antartica.
select country.name as "country_name", airport.name as "airport_name"
from airport, country
where airport.iso_country = country.iso_country and country.continent = "AN";

![Q3](https://github.com/user-attachments/assets/55c458b9-7ba0-4ba7-b98a-ba74b177c1ac)

## Question 4
### What is the height of Heini's current location measured from the sea level?
SELECT elevation_ft
from airport, game
where location = ident and screen_name="Heini";

![Q4](https://github.com/user-attachments/assets/8e33238e-6351-4738-bf94-2127c83900ec)

## Question 5
### What is the height of Heini's current location measured from the sea level? Print out the result in meters and assign the result the alias elevation_m. One feet corresponds to 0.3048 meters.
select elevation_ft * 0.3048 as "elevation_m"
from airport, game
where location = ident and screen_name="Heini";

![Q5](https://github.com/user-attachments/assets/9e87d52f-fa68-4ee9-a142-091f1cd870e3)

## Question 6
### What is the name of the airport Ilkka is currently at?!
select airport.name as "name"
from airport, game
where location = ident and screen_name = "Ilkka";

![Q6](https://github.com/user-attachments/assets/5cda5dc3-7ddc-4088-a7e5-2203323716f0)

## Question 7
### What is the name of the country Ilkka is currently at?
select country.name as "name"
from country, airport, game
where location = ident and airport.iso_country = country.iso_country and screen_name = "Ilkka";

![Q7](https://github.com/user-attachments/assets/57fa6278-a807-4aec-8161-9a07d18d3274)

## Question 8
### List the weather condition goals Heini as achieved so far.
select name from goal, game, goal_reached where game.id=game_id and goal.id=goal_id and screen_name="Heini";

![Q9](https://github.com/user-attachments/assets/2e688883-30f4-4fc9-bb9f-ebd282ccd84d)

## Question 9
### Print out the name of the airport where Ilkka achieved the clouds weather goal. 
select airport.name from airport, goal_reached, goal, game
where ident = location and goal.id = goal_reached.goal_id and game.id = goal_reached.game_id and screen_name = "Ilkka"

![Q 9](https://github.com/user-attachments/assets/0304f29b-59e9-4928-b7f8-887825af6314)

## Question 10
### Print out the name of the country where Ilkka achieved the clouds goal.
select country.name
from country, game, goal, goal_reached, airport
where airport.iso_country = country.iso_country and ident=location AND
game_id=game.id AND goal_id=goal.id and screen_name = "Ilkka" and goal.name = "CLOUDS";

![Q 10](https://github.com/user-attachments/assets/87c8b6e5-1126-463a-8e08-e03a83449800)
