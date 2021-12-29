# steam_data_science
A collection of data science python utilities for analyzing data from the video game platform Steam



## Features
__build_tag_percentile_data(api_key, steam_ids_list)__
* returns __tag_data__, __percentiles_data__, and __aggregation_data__
  * __tag_data__ - A dataframe of tagid, name, count, appid, proportion
  * __percentiles_data__ - A dataframe of appid, p10, p25, median, p75, p90 percentile playtimes in minutes
  * __aggregation_data__ - A fingerprint dataframe of each user's tag name, and various attribution models like proportional, linear, average, median, etc.

__compute_fan_rating(data)__
* For a given game and its quartiles of playtime data, check the user's playtime against the distribution and compute what percentile the user is compared to the rest of the game's playing population.

__get_review_data(appid)__
* For a given steam app, get its positive and negative review counts for all languages and purchase types.

__get_appid_tags(appid)__
* For a given steam app, get the tag names, the counts of how many times they've been attributed, and what proportion of the total they make up that app's tags.

__get_users_games(api_key, steam_id)__
* Get a user's list of games, playtime data, and other info from the IPlayerService and dump it into a pandas dataframe.

__get_playtime_percentiles_for_app(appid)__
* For a given steam app, gently scrape the howlongis.io site for the app's playtime quartile data. 
