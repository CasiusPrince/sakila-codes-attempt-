# sakila-codes-attempt-

show databases;
use sakila;
show tables;
select * from actor;
select * from actor where first_name = 'john';
select * from actor where last_name like 'neeson';
select * from actor where actor_id%10 = 0;
select * from film;
select * from film where film_id = 100;
select * from film where rating = 'r';
select * from film where rating != 'r';
select * from film order by length desc limit 10;
select film_id, length from film order by length desc;
show tables;
select title from film where special_features = 'deleted scenes';
select last_name from actor group by last_name having count(last_name) =1 order by last_name desc;
select last_name from actor group by last_name having count(last_name) >1 order by count(last_name) desc;
show tables;
select f.actor_id, a.first_name, a.last_name, COUNT(f.actor_id) FROM film_actor f JOIN actor a ON f.actor_id=a.actor_id GROUP BY f.actor_id ORDER BY COUNT(f.actor_id) DESC LIMIT 1;
SELECT AVG(length) FROM film; SELECT category, AVG(length) FROM film_list GROUP BY category;
SELECT film_id, title FROM film WHERE description LIKE '%robot%';
SELECT COUNT(release_year) FROM film WHERE release_year=2010;
SELECT title FROM film_list WHERE category='Horror';
