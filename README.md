<h1>Analyzing Netflix Movies</h1>

 ### [Medium Article Demonstration](https://medium.com/@sebastienwebdev/analyzing-netflix-movies-insights-from-imdb-ratings-647140c8f6ca)

<h2>Description</h2>
This project explores Netflix's movie offerings using a SQL-based analysis of IMDb data. The dataset includes details like movie titles, casts, descriptions, durations, IMDb ratings, votes, release years, genres, and certificates, offering insights into trends and viewer preferences.
<br />

<h2>Environments & Utilies Used </h2>

- <b>macOS</b> 
- <b>SQLite Studio</b>
- <b>Database (Kaggle) </b>


<h2>Program walk-through:</h2>

<h2>What is the average of IMDb ratings on Netflix?</h2>
    <pre><code>SELECT AVG(voted_by) FROM netflix_movies;</code></pre>
<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*KlBNlL8arUT4jmI-gF3NYQ.png" height="80%" width="80%" alt="music Steps"/>
<br />
<br />
<h2>Which genre has the most movies on Netflix?</h2>
    <pre><code>SELECT imdb_rating , COUNT(*) AS movie_count 
FROM movies
GROUP BY imdb_rating 
ORDER BY movie_count DESC 
LIMIT 1;</code></pre>
<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*S8HCSMW1f_h8oJNeJsQ1Vg.png" height="80%" width="80%" alt="music Steps"/>
<br />
<br />
    <h2>How many movies are there in each certificate category?</h2>
    <pre><code>SELECT certificate, COUNT(*) AS movie_count 
FROM movies 
GROUP BY certificate;
</code></pre>
<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*BB8Up9yfvrWoWDXvH1Crag.png" height="80%" width="80%" alt="music Steps"/>
<br />
<br />
    <h2>What are the top 10 movies with the highest number of votes on IMDb?</h2>
    <pre><code>SELECT title, voted_by
FROM movies 
ORDER BY voted_by DESC 
LIMIT 10;</code>
</pre>
<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*f4xIXUtbG-Zng6qrtE9S5g.png" height="80%" width="80%" alt="music Steps"/>
<br />
<br />
    <h2>Which year had the highest number of movie releases on Netflix?</h2>
    <pre><code>SELECT year, COUNT(*) AS movie_count 
FROM movies 
GROUP BY year 
ORDER BY movie_count DESC 
LIMIT 1;</code></pre>
<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*xu2h0Nn9EwmZrOChKTPivg.png" height="80%" width="80%" alt="music Steps"/>
<br />
<br />
    <h2>What is the average duration of movies in each genre?</h2>
   

<pre><code>SELECT genre, AVG(duration) AS average_duration 
FROM movies 
GROUP BY genre;

</code></pre>
<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*p8VEO7aSDjhTxWBjx9bOFA.png" height="80%" width="80%" alt="music Steps"/>
<br />
<br />
    


</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
