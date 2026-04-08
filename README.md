**Exploratory Data Analysis on Amazon Prime Video**
--
## Project Overview

This project focuses on cleaning and analyzing the Amazon Prime Video dataset to extract meaningful insights about content diversity, regional distribution, trends over time, and IMDb ratings.

---



## Dataset Information

The project uses two datasets:

* `titles.csv` → Contains information about movies and TV shows
* `credits.csv` → Contains cast and crew details

**title dataset*

1.person_ID: The person ID on JustWatch.

2.id: The title ID on JustWatch.

3.name: The actor or director's name.

4.character_name: The character name.

5.role: ACTOR or DIRECTOR.



**credit dataset**

1.id: The title ID on JustWatch.

2.title: The name of the title.

3.show_type: TV show or movie.

4.description: A brief description.

5.release_year: The release year.

6.age_certification: The age certification.

7.runtime: The length of the episode (SHOW) or movie.

8.genres: A list of genres.

9.production_countries: A list of countries that produced the title.

10.seasons: Number of seasons if it's a SHOW.

11.imdb_id: The title ID on IMDB.

12.imdb_score: Score on IMDB.

13.imdb_votes: Votes on IMDB.

14.tmdb_popularity: Popularity on TMDB.

15.tmdb_score: Score on TMDB.


Libraries used: Numpy, Pandas, Matplotlib, Seaborn


##  Data Wrangling Steps

* Loaded datasets using Pandas
* Checked dataset shape and missing values
* check how many duplicated values present in both dataset and remove duplicate records
* Check count of missing value,In title dataset 8 columns have missing value ,some column has large quantity , some has less and in credit column only 1 column has large missing value.

so we dropped null columns in `credits` and dropped large quantity of null value containing columns:`age_certification`, `seasons`, `tmdb_score`, `imdb_votes` and replace rest columns with 0 and 'unknown'.
* Reset index for consistency
* Merged datasets using `id`
* Saved cleaned dataset

---

##  Exploratory Data Analysis & Visualizations

###1. Content Diversity (Genres)
* Majority of content is movies
* Drama, Comedy, and Action dominate the platform
* Drama is most consuming content.


###2. Regional Availability (Countries)

* USA contribute most content.
* High concentration of content  in some region and some region have very less content.

###3. Trends Over Time

* Significant growth after 2015,1980 to 2015 there is not much growth.
* Streaming platforms are increasing original content production

###4. IMDb Ratings Analysis
* Highest-rated shows have IMDb ratings above 8.5
* Popular shows have high IMDb votes
* Some shows are highly rated but not widely popular

---



##  Conclusion

The analysis reveals that Amazon Prime Video has a large and growing content library dominated by movies and popular genres like Drama and Action. While most content has average ratings, a small portion of high-rated content plays a crucial role in driving user engagement. Strategic focus on quality and regional content can further enhance platform growth.
