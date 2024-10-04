# question 1 
select * from goal;
![screenshot](screenshots/SingleTableQueries_Q1.png)

# question 2
select name, type from airport where iso_country like "FI";
![screenshot](screenshots/SingleTableQueries_Q2.png)

# question 3
select name, iso_country from airport where iso_country ="FI" order by name desc;
![screenshot](screenshots/SingleTableQueries_Q3.png)

# question 4
select name, type from airport where iso_country like "FI" order by type asc, name asc;
![screenshot](screenshots/SingleTableQueries_Q4.png)

# question 5 
select name from country where name like "F%";
![screenshot](screenshots/SingleTableQueries_Q5.png)

# question 6
select name from country where name like "%F%";
![screenshot](screenshots/SingleTableQueries_Q6.png)

# question 7 
select location from game where screen_name = "Vesa";
![screenshot](screenshots/SingleTableQueries_Q7.png)

# question 8 
select co2_consumed from game where screen_name like "Ilkka";
![screenshot](screenshots/SingleTableQueries_Q8.png)

# question 9 
select co2_budget from game limit 1;
![screenshot](screenshots/SingleTableQueries_Q9.png)

# question 10
select  screen_name, co2_budget, co2_consumed,co2_budget-co2_consumed as co2_left  from game;
![screenshot](screenshots/SIngleTableQueries_Q10.png)
