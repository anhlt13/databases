# question 1 
update game
set game.location = (select ident from airport
where airport.name = "Nottingham Airport");
update game
set co2_consumed = (co2_consumed +500)
where game.screen_name = "Vesa";
![screenshot](screenshots/UpdateQueries_Q1.png)

# question 2 
b. goal_reached

# question 3 
delete from goal_reached;
![Screenshot](screenshots/UpdateQueries_Q3.png)

# question 4 
delete from game;
![Screenshot](screenshots/UpdateQueries_Q4.png)