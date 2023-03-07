# List of Dataset Links for Project 4

The following list of links should serve as a great starting point for putting together problems and/or ideas for your Project 4:

https://www.drivendata.org/competitions/  
https://www.kaggle.com/  (One of the best places for data sets)  
https://data.world/  
https://www.challenge.gov  
https://archive.ics.uci.edu/ml/index.php  
http://www.stat.ufl.edu/~winner/datasets.html  
https://www.reddit.com/r/datasets/  
http://exploresara-sara-tx.opendata.arcgis.com/  
http://nowdata.cinow.info/indicators/local-open-data-portals  
https://data.fivethirtyeight.com/  
https://toolbox.google.com/datasetsearch  
https://github.com/brohrer/academic_advisory/blob/master/use_cases.md  
https://explore.openaire.eu/  
https://blog.datasciencedojo.com/30-datasets-to-uplift-your-skills-in-data-science/ (Would recommend going for Intermediate or Advanced Datasets here)  
https://developer.ibm.com/exchanges/data/  
https://github.com/awesomedata/awesome-public-datasets  
https://mran.microsoft.com/web/packages/fivethirtyeight/vignettes/fivethirtyeight.html  
https://data.worldbank.org/  
https://www.imf.org/en/Data  
https://www.transit.dot.gov/ntd/ntd-data  
https://gosa.georgia.gov/downloadable-data  
https://www.usaspending.gov/#/download_center/custom_award_data  

## Sports Related Data
Many of the cooler Sports Play-by-Play date scraping packages are done in R (nflfastR, hoopR, etc.), but thankfully the creators of those projects set up a data repository in Github that you can read directly into your notebook.

### NFL Data from nflfastR/nflverse
The nflfastR package scrapes nfl data from several sources, and the play-by-play data is stored in several different formats at the following link: [nflverse Data](https://github.com/nflverse/nflverse-data/).  

From there, you can click on the data you want. For play-by-play data, click on load_pbp tag in the table.  You'll see a repo of all play-by-play data for the NFL from 1999-Present.  If you wanted to access the 2022 play-by-play data with Python, you can run the following in your Jupyter Notebook.

```python
pbp = pd.read_parquet('https://github.com/nflverse/nflverse-data/releases/download/pbp/play_by_play_2022.parquet', engine='auto')
pbp.head()
```
You can also install the [nfl_data_py](https://github.com/cooperdff/nfl_data_py) library and use it to obtain NFL data.

### NBA and College Basketball Data from hoopR

Similar to nflfastR, the [hoopR Data](https://github.com/sportsdataverse/hoopR-data) is in Github.  At that link, you can click on either the nba or mbb folders for the NBA or Men's College Basketball data respectively.
From that folder tree, you can then click on the pbp folder for play-by-play data, the player_box folder for player specific box scores, schedules for Team schedules, or team_box for Team Box Scores.  Each folder has four different types of files.

As above, if you wanted Team Box Scores for the 2021-2022 Men's Basketball Season using the parquet file format, you can click on the github file folders in order from mbb, team_box, then parquet.  Click on the team_box_2022.parquet file, then right click on View Raw and Copy Link Address.

```python
mbb_pbp = pd.read_parquet('https://github.com/sportsdataverse/hoopR-data/blob/main/mbb/team_box/parquet/team_box_2022.parquet?raw=true')
mbb_pbp.head()
```

### Other Sports

[PySport](https://opensource.pysport.org/) keeps a list of various sports packages to use to scrape/get data as well including Soccer, Hockey, Baseball, and more.  Code and packages are updated frequently so there may be different ways of getting data than what was demonstrated above.

Keep in mind that the data scraped, while cleaned up by the scraping process, still require a great deal of cleaning for analysis.  There are a few python-related tutorials on the NFL data.
