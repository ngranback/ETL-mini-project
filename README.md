# ETL-mini-project



Realized that I had pulled too many columns from IMDB,
so I removed Episode, Season, and Title
and only kept SEID to later merge with other tables

Then, realized that the episode numbers were not matching with other source episode #s
After pulling my hair out for a wihle, I realized that the Episode Info csv had unreliable SEIDs.
My scraped SEIDs were actually more accurate.

Using innerjoins knocked out 20 episodes
Can't identify the problem between the datasets....