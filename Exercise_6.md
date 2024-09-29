## Question1
### What is the elevation of the highest airport location?
select max(elevation_ft)
from airport;

![Q1](https://github.com/user-attachments/assets/1569277c-f673-4fc3-b0c5-5ee746e4f5e6)

## Question 2
### Write a query that lists all continents and the number of countries on them.
select continent, count(*)
from country
group by continent;

![Q2](https://github.com/user-attachments/assets/f7b3e513-6769-45a4-a827-c3f725a08879)

## Question 3
### List the names of all players and the number of weather goals they have achieved.
select screen_name, count(*)
from game, goal_reached
where id = game_id
group by screen_name;

![Q3](https://github.com/user-attachments/assets/422da628-d45b-41af-a019-a4aed60d30b4)

## Question 4
### Which player has the smallest carbon foot print?
select screen_name
from game
where co2_consumed in(
select min(co2_consumed)
from game
);

![Q4](https://github.com/user-attachments/assets/2d7fe60f-63bc-4116-a03b-d595a52bc3e0)

## Question 5
### Print out the names of all countries and the number of airports in each country. Order the results by the airport count in descending order. Only include the top 50 countries with the largest number of airports.
select country.name, count(*)
from airport, country
where airport.iso_country = country.iso_country
group by country.iso_country
order by count(*) desc
limit 50;

![Q5](https://github.com/user-attachments/assets/cc276088-3632-4b46-86a2-2e99743abf16)

## Question 6
### List the countries with more than 1000 airports. Use the iso_country field in the query.
select country.name
from airport, country
where airport.iso_country = country.iso_country
group by country.iso_country
having count(*) > 1000;

![Q6](https://github.com/user-attachments/assets/006660cb-b7e6-4334-910b-ec1261a8b8c7)

## Question 7
### Print out the name of the highest airport in the world.
select name
from airport
where elevation_ft in (
select max(elevation_ft)
from airport
);

![Q7](https://github.com/user-attachments/assets/2322dad4-c374-462e-aa0c-4c7fb01c3211)

## Question 8
### In which country does the highest airport reside in?
select name
from country
where iso_country in (
select iso_country
from airport
where elevation_ft in(
select max(elevation_ft)
from airport
)
);

![Q8](https://github.com/user-attachments/assets/77c7985a-de85-477f-b436-cf9fabe1fd04)

## Question 9
### How many weather goals has Vesa achieved so far?
select count(*)
from game, goal_reached
where id = game_id and screen_name = "Vesa"
group by screen_name;

![Q9](https://github.com/user-attachments/assets/0a204e05-5e72-4ddb-93d1-1d1f486aea02)

## Question 10
### What is the name of the airport that resides closest to the polar regions?
select name
from airport
where latitude_deg in(
select min(latitude_deg)
from airport
);

![Q10](https://github.com/user-attachments/assets/4aa03bf5-ac07-4bfe-ae36-ea08aeaf5a0e)
