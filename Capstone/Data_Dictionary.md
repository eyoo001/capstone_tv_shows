# OMDB

| Feature 	| Description 	|  	
|---	|---	|
| title 	| title of the show/movie 	|  	
| year 	  	| start/end year as a range |
| rated 	| the FCC parental ratings 	|  	
| released 	| air date formatted: [DD] [3-letter Month] [Year] 	|  	
| runtime 	| length of time of an episode/movie 	|  	
| genre 	| genre as a list 	|  	
| director 	| Director of the series or movie. Most of these appear to show "N/A" unless the same director handled the whole show 	|  	
| writer 	| Writer for th series. Same as Director, "N/A" if different writers handled the show during it's course 	|  	
| actors 	| Main cast 	|  	
| plot 	  	| 1 to 3 sentence "logline" type synopses 	|
| language 	| Language the show was aired in 	|  	
| country 	| Country the show was aired in 	|  	
| awards 	| Awards or nominations the show was eligible for/won 	|  	
| poster 	| Link to the poster image 	|  	
| ratings 	| Dictionary of rating(s) and where from 	|  	
| metascore 	| Metacritic score 	|  	
| imdb_rating 	| Rating for the whole series on IMDB 	|  	
| imdb_votes 	| Number of votes for the whole series on IMDB 	|  	
| imdb_id 	| IMDB id 	|  	
| type 	| series, movie 	|  	
| total_seasons 	| Number of total seasons 	|  	
| tomato_meter 	| RottenTomatoes 	|  	
| tomato_image 	| RottenTomatoes 	|  	
| tomato_rating 	| RottenTomatoes 	|  	
| tomato_reviews 	| RottenTomatoes 	|  	
| tomato_fresh 	  	| RottenTomatoes 	|
| tomato_rotten 	| RottenTomatoes 	|  	
| tomato_consensus 	| RottenTomatoes 	|  	
| tomato_user_meter 	| RottenTomatoes 	|  	
| tomato_user_rating 	| RottenTomatoes 	|  	
| tomato_user_reviews 	| RottenTomatoes 	|  	
| dvd 	| N/A 	|  	
| box_office 	| N/A 	|  	
| production 	|  N/A	|  	
| website 	| N/A 	|  	
| response 	| I wasn't able to find out what this was 	|  	



# TMDB

| Feature | Description |
| --- | --- |
| 'created_by' | gives a dict of the director/producer/writer and their TMDB ID |
| 'episode_run_time' | either a single value or a range of values, separated by brackets |
| 'first_air_date' | date first aired YYYY-MM-DD | 
| 'genres' | dict of genres and their TMDB ID |
| 'id' | TMDB ID |
| 'in_production' | True/False, currently airing or not |
| 'languages' | language show aired in, list |
| 'last_air_date' | date of the most recent episode | 
| 'last_episode_to_air' | may be the ID for the last episode? |
| 'name' | name of the show | 
| 'networks' | dict of network the show aired and its ID |
| 'next_episode_to_air' | possible ID as well? |
| 'number_of_episodes' | number of episodes in the series | 
| 'number_of_seasons' | number of seasons in th series |
| 'origin_country' | where the show was made |
| 'original_language' | language the show was made in |
| 'original_name' | original name |
| 'overview' | synopsis |
| 'popularity' | TMDB internal popularity, determined by clicks/views and votes |
| 'poster_path' | link to poster/ID |
| 'production_companies' | has an ID, not clear what for |
| 'seasons' | dict of air date, ID and episode count of seasons |
| 'status' | returning, ended, or cancelled |
| 'type' | series or movie | 
| 'vote_average' | TMDB internal voting average score |
| 'vote_count' | TMDB internal voting number of votes |



# TVDB

| Feature | Description |
| --- | --- |
| 'airsDayOfWeek' | string - day of week show airs/ed |
| 'airsTime' | also string - what time of week the show airs/ed |
| 'firstAired' | first airing date |
| 'genre'| list of genres |
| 'id' | TVDB ID |
| 'imdbId' | IMDB ID |
| 'network' | airing network |
| 'overview' | synopses |
| 'rating' | FCC's parental guidance ratings |
| 'runtime' | range of ints |
| 'seriesId' | IMDB ID |
| 'seriesName' | name of series |
| 'siteRating' | TVDB's rating system is proprietary | 
| 'siteRatingCount' | TVDB's voting numbers | 
| 'status' | Continuing or Ended | 





