# question 1
select elevation_ft as "max(elevation_ft)"
from airport
where elevation_ft in (select max(elevation_ft) from airport);
![screenshot](screenshots/AggregateQueries_Q1.png)

# question 2 
select country.continent, count(*)
from country 
group by country.continent;
![screenshot](screenshots/AggregateQueries_Q2.png)

# question 3 
select screen_name, count(*)
from game, goal_reached
where game.id = goal_reached.game_id
group by screen_name;
![screenshot](screenshots/AggregateQueries_Q3.png)

# question 4 
select screen_name 
from game 
where game.co2_consumed in (select min(co2_consumed) from game
where game.location in (select ident from airport));
![screenshot](screenshots/AggregateQueries_Q4.png)

# question 5 
select country.name, count(*)
from country, airport
where country.iso_country = airport.iso_country
group by country.name 
order by count(*) desc;
![screenshot](screenshots/AggregateQueries_Q5.png)

# question 6 
select country.name
from country, airport
where country.iso_country = airport.iso_country
group by country.name
having count(*)>1000;
limit 50;
![screenshot](screenshots/AggregateQueries_Q6.png)

# question 7 
select name
from airport 
where elevation_ft in (select max(elevation_ft) from airport);
![screenshot](screenshots/AggregateQueries_Q7.png)

# question 8 
select name 
from country 
where country.iso_country in (select iso_country from airport
where airport.elevation_ft in (select max(elevation_ft) from airport));
![screenshot](screenshots/AggregateQueries_Q8.png)

# question 9 
select count(*)
from goal
where goal.id in (select goal_id from goal_reached
where game_id in (select game.id from game
where game.screen_name = "Vesa"));
![screenshot](screenshots/AggregateQueries_Q9.png)

# question 10
select name 
from airport 
where airport.latitude_deg in (select min(latitude_deg) from airport);
![screenshot](screenshots/AggregateQueries_Q10.png)