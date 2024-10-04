# question 1  
select country.name as "country name", airport.name as "airport name"
from airport
inner join country on country.iso_country = airport.iso_country
where country.name = "Finland";
![screenshot](screenshots/Join_Q1.png)

# question 2  
select game.screen_name, airport.name 
from game 
inner join airport on game.location = airport.ident;
![screenshot](screenshots/Join_Q2.png)

# question 3 
select game.screen_name, country.name 
from country
inner join airport on airport.iso_country = country.iso_country 
inner join game on airport.ident = game.location;
![screenshot](screenshots/Join_Q3.png)

# question 4 
select airport.name, game.screen_name 
from game 
right join airport on airport.ident = game.location
where airport.name like "%hels%";
![screenshot](screenshots/Join_Q4.png)

# question 5 
select goal.name, game.screen_name 
from game
right join goal_reached on goal_reached.game_id = game.id
right join goal on goal_reached.goal_id = goal.id;
![screenshot](screenshots/Join_Q5.png)