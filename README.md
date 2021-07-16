# ETL-mini-project


## What Are The Makings of a Great Seinfeld Episode? 

### Overview

I started by browsing Kaggle for interesting data sets, and happened across a .csv containing the script of every episode of Seinfeld. It also offered a second .csv with episode info such as Title, Writer, and Release Date. I decided to use all this information to determine what it takes to make a great episode of Seinfeld. However, the dataset did include rating. So I decided to scrape IMDb to fill in that information.

### The Data Sources

* [Kaggle Datasets](https://www.kaggle.com/thec03u5/seinfeld-chronicles/activity)
  * Episode Information (csv)
  * All show dialogue (csv) 

* [IMDb Episode List](https://www.imdb.com/title/tt0098904/episodes)

---  

### The Process

I started by scraping ratings from IMDb, along with some supporting data. Then I loaded the two .csv's into pandas DataFrames and began to merge my data.

Immediately I noticed that I was dropping rows on an inner merge. After spending far too long pulling my hair out looking for these errors the *wrong* way, I finally remembered how to inspect and clean data effectively using pandas.

The mismatch between the two datasets turned out to be mostly 2-part episodes, title punctuation, special anniversary episodes that were not included in both sources, and a few errors in the source data. Some errors were easily fixed with a list of replace commands, but others were far better suited to a manual solution (i.e. fixing a cascading typo in the source csv).

In the end, the data was merged successfully to create one large dataframe containing every line of dialogue from the show along with all information on the corresponding episode.

---

### Where To Go Next

I loaded the dataframe to MongoDB, but my real goal is to disect the data using python and create visualizations with matplotlib. 

The data I'm most interested in investigating:
* **Rating vs Character Lines** --- Who speaks the most in highly rated episodes?
* **Rating vs Writer / Director** --- Who created the most well loved episodes?
* **Character Lines vs Writer** --- Did different writers tend to favor certain characters?
* **Rating vs Release Date** --- Did the show get better with time?


The possibilities are endless and I can't wait to dig in!
