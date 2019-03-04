1. Which are the different genres?

SELECT DISTINCT(Prime_genre)
FROM data
ORDER BY Prime_genre;



Book
Business
Catalogs
Education
Entertainment
Finance
Food & Drink
Games
Health & Fitness
Lifestyle
Medical
Music
Navigation
News
Photo & Video
Productivity
Reference
Shopping
Social Networking
Sports
Travel
Utilities
Weather

2. Which is the genre with more apps rated? Games

SELECT  prime_genre, sum(rating_count_tot) as total 
FROM data
GROUP BY prime_genre
ORDER BY total desc
LIMIT 1;

Games	52878491


3. Which is the genre with more apps? Games

SELECT prime_genre, COUNT(*) AS total
FROM data
GROUP BY prime_genre
ORDER BY total desc
LIMIT 1;

Games	3862



4. Which is the one with less? Catalogs

SELECT prime_genre, COUNT(*) AS total
FROM data
GROUP BY prime_genre
ORDER BY total
LIMIT 1;

Catalogs	10

5. Take the 10 apps most rated.

SELECT  track_name, rating_count_tot
FROM data
ORDER BY rating_count_tot desc
LIMIT 10;


Facebook	2974676
Instagram	2161558
Clash of Clans	2130805
Temple Run	1724546
Pandora - Music & Radio	1126879
Pinterest	1061624
Bible	985920
Candy Crush Saga	961794
Spotify Music	878563
Angry Birds	824451

6. Take the 10 apps best rated by users.

SELECT  track_name, user_rating, rating_count_tot
FROM data
ORDER BY user_rating DESC, rating_count_tot desc
LIMIT 10;


Head Soccer						5	481564
Plants vs. Zombies					5	426463
Sniper 3D Assassin: Shoot to Kill Gun Game		5	386521
Geometry Dash Lite					5	370370
Infinity Blade						5	326482
Geometry Dash						5	266440
Domino's Pizza USA					5	258624
CSR Racing 2						5	257100
Pictoword: Fun 2 Pics Guess What's the Word Trivia	5	186089
Plants vs. Zombies HD					5	163598

7. Take the rate of the 10 apps most rated. 4.35

Facebook		2974676	3.5
Instagram		2161558	4.5
Clash of Clans		2130805	4.5
Temple Run		1724546	4.5
Pandora - Music & Radio	1126879	4
Pinterest		1061624	4.5
Bible			985920	4.5
Candy Crush Saga	961794	4.5
Spotify Music		878563	4.5
Angry Birds		824451	4.5

8. Take the rate of the 10 apps best rated. average 5

Head Soccer						5	481564
Plants vs. Zombies					5	426463
Sniper 3D Assassin: Shoot to Kill Gun Game		5	386521
Geometry Dash Lite					5	370370
Infinity Blade						5	326482
Geometry Dash						5	266440
Domino's Pizza USA					5	258624
CSR Racing 2						5	257100
Pictoword: Fun 2 Pics Guess What's the Word Trivia	5	186089
Plants vs. Zombies HD					5	163598

9. What do you see here?
Most rated have lower average rating than 

10. How could you take the top 3 regarding the user ratings but also the number of votes?

SELECT  track_name, rating_count_tot, user_rating
FROM data
ORDER BY rating_count_tot desc
LIMIT 10;

11. Does people care about the price?