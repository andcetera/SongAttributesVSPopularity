# Song Attributes vs. Popularity

Project Structure:

Completed Project Dashboard can be found HERE

Files:
-
-
-
-
-

Background:
What truly makes a song popular? To answer this, analyzed the impact a song's attributes have on it's popularity. In order to do this, we looked at an dataset from Kaggle, Spotify Weekly Top 200, which is a dataset that contains songs from Spotify's 'Weekly Top Songs' for each country between 2021 to 2022. 


Part 1: Exploratory Data Analysis and creating Data Frames

The initial data set required cleaning and filtering in order for it to be used for the future steps. Certain columns were removed due the the size,     which impacted the CSV being read. The columns that were used in the CSV were artist name, track name, rank, weeks on chart, streams, danceability, energy, loudness, speechiness, acousticness, valence, tempo, duration and country. The cleaned data set was then divided into different data frames which would then be used to make different tables. These tables were 'country_attributes', which look at the songs and their attributes, and then groups them together by the country. Another table was 'top_fifty_genres' which showed the top 50 genres based on the number of artists. The table 'max_weeks_on_chart' looks at the length of time a song is on the charts. The table 'coolness' looks at the how popular a song is with it's rank, streams, weeks on the chart, and popularity score. The 'all_countries_top_fifty' looks at the top fifty songs for each country based on it's popularity.  These tables were then all exported to CSVs.


Part 2: Converting the data to sqlite Database
After all the data frames were created, we imported sqlite3 to create our database. Once sqlite was running, the dataframes were then converted into sql files, and tested to see if the file was working. The tables for the database, songs_complete_db_sqlite, were coolness, country_attributes, fiftygenre. all_countries_top_50. Afterwards, primary keys were added to the table. (have image of ERD?) The primary key for country_attributes was 'country', the primary key for coolness were artist_names and track_name. The primary key for fiftygenre was artist_genre. The primary keys for top_50_by_country were artist_name, track_name, and country. 

Part 3: Flask


Part 4: Work on json to create html dashboard


Resources:
https://www.kaggle.com/datasets/yelexa/spotify200
