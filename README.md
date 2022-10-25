# WeRateDog-Dataset-Exploration-
# Gathering Data
### I imported the Libraries needed for this analysis
> Pandas
> Numpy
> Matplotlib
> Json
> Seaborn
> Tweepy
###  Next, imported files needed for analysis which are listed below and also scraped data from WeRateDogs twitter account using tweepy tools;
> twitter_archive_enhanced.csv
> tweet_json.txt
> image_predictions.tsv
## Assessing Data
> Programmatical Assessment
    Methods like info(), duplicated(), describe(), value_count(), isna(), query() was used to assess the data loaded into a dataframe,
    different visuals was used to depict the assessement procedure. Quality Issues and Tidiness issues was identified which are listed below;
    > inconsistent ratings
    > Missing row in retweet_count
    > outliers in rating
    > wrong rating calculation for grouped dog picture.
    > Rating that was not related to the project study.
    
>  Virtual Assessment
    The dataframe of each of the three files were loaded and assessed by scrolling horizontally and vertically.
## Cleaning 
    In this section, all identified issues were cleaned programmatically using line codes, user-defined-functions, iterations etc.
    > Created a copy of all dataframe using copy() method
    > kept only rows without retweets using either 'retweeted_status_id' or 'retweeted_status_user_id' that had values in it to avoid duplicated rating.
    > missing field in clean_twitter_archive table was solved by extracting the data again from the scrapped twitter data and any missing field was set to nan
    > incosistent dog name was replaced with none using replace() method.
    > incorrect ratings; extracted ratings again then set rating denominator to 10, corrected some rating numerator by cross checking affected tweet using tweet_id.
    > used drop() method for outliers carefully crossed checked using tweet_id.
    >  used rename() method to rename columns.
    > used merge() to join  the different dataframe into one .
    > used a Code-Based-Test to effect changes on the cleaning process
    
  ## Merging and storing
    The cleaned and merged DataFrame was stored in a master file.
