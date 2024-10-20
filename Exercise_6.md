## Question1
### What is the elevation of the highest airport location?
select max(elevation_ft)
from airport;

![Q 1](https://github.com/user-attachments/assets/92f414a0-a0fe-491b-97ca-a3f276f86361)


## Question 2
### Write a query that lists all continents and the number of countries on them.
select continent, count(*)
from country
group by continent;

![Q 2](https://github.com/user-attachments/assets/fad2a972-70f1-4bef-b356-f99e7c2df33b)


## Question 3
### List the names of all players and the number of weather goals they have achieved.
select screen_name, count(*)
from game, goal_reached
where id = game_id
group by screen_name;

![Q 3](https://github.com/user-attachments/assets/32e1ed60-887d-437c-ad23-0945afd53b7c)


## Question 4
### Which player has the smallest carbon foot print?
select screen_name
from game
where co2_consumed in(
select min(co2_consumed)
from game
);

![Q 4](https://github.com/user-attachments/assets/75be9836-d9fc-4f72-be90-eb7a7af63654)


## Question 5
### Print out the names of all countries and the number of airports in each country. Order the results by the airport count in descending order. Only include the top 50 countries with the largest number of airports.
select country.name, count(*)
from airport, country
where airport.iso_country = country.iso_country
group by country.iso_country
order by count(*) desc
limit 50;

![Q 5](https://github.com/user-attachments/assets/8b059792-75d9-4fb7-a43e-1cb45d70abcc)


## Question 6
### List the countries with more than 1000 airports. Use the iso_country field in the query.
select country.name
from airport, country
where airport.iso_country = country.iso_country
group by country.iso_country
having count(*) > 1000;

![Q 6](https://github.com/user-attachments/assets/8020024b-4a7d-43e0-b522-a6a6467903eb)


## Question 7
### Print out the name of the highest airport in the world.
select name
from airport
where elevation_ft in (
select max(elevation_ft)
from airport
);

![Q 7](https://github.com/user-attachments/assets/4455fdbe-364f-4ea4-a199-599283b582aa)


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

![Q 8](https://github.com/user-attachments/assets/dc65984a-97df-454d-bd10-c35d9fcb2890)


## Question 9
### How many weather goals has Vesa achieved so far?
select count(*)
from game, goal_reached
where id = game_id and screen_name = "Vesa"
group by screen_name;

![Q 9](https://github.com/user-attachments/assets/b2608b63-b45f-4c4b-8712-b2b8aec6f6f2)


## Question 10
### What is the name of the airport that resides closest to the polar regions?
select name
from airport
where latitude_deg in(
select min(latitude_deg)
from airport
);

![Q 10](https://github.com/user-attachments/assets/4f4bf542-7b3a-46a4-b516-fb6d63338347)

