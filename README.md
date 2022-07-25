# WeRateDog-Udacity-Data-Analyst-Project-2
This repository contains the codes used to extract, wrangle and analyse the WeRateDog Dataset. It also contains the visualization and insights derived from the analysis.

## Gathering Data
The dataset was gather through:

1. File on hand twitter_archive_enhanced.csv
2. File hosted on Udacity server image_predictions.tsv
3. Query of Twitter API tweet_json.txt

## Assessing Data
The data were assessed both visually and programmatically to look for quality and tidiness issues. 
Programmatic Methods: 
```
data.head() 
data.describe() 
data.info() 
data.duplicated() 
data.value_counts()
```
## Cleaning
This section contains the cleaning process performed on the datasets.

### Tidiness issue
Simplify 3 tables to 2 by joining (inner) archived_tweet_copy with img_dataframe_copy to create one tweet observation table.
Convert doggo, flooter, pupper, puppo columns into one stage column in the tweet_combined, then drop the four columns

### Quality issue
1. Retweets rows and 'retweeted_status_id', 'retweeted_status_user_id', 'retweeted_status_timestamp' columns were removed.
2. The source was Stripped to remove the HTML link.
3. Dog names were replaced with 'None', and lowercase dog names were also replaced. Names that were not found were replaced with not a number(NaN).
4. Rows where all predictions of dog breed is not a dog were dropped.
5. I removed the jpg_url, in_reply_to_status_id, in_reply_to_user_id and expanded_urls column from img_dataframe and archived_tweet dataframe.
6. Timestamp were converted to datetime.
7. Rows with missing values were removed.
8. Variable types were change to appropriate.

## Questions(5) were formulated and 4 visualization were generated

__Questions__

1. Are retweets and replies correlated?
2. Statistics of Dog Stage and Ratings
3. Which dogs are the top favorite dog?
4. Which are the top dogs according to retweets?
5. What's the distribution for the retweet count?
 __Visualization__
1. Heatmap of correlation between favorite count and retweet count
2. Distribution of ratings
3. Top favorite dog
4. Distribution of Source
Check out the insights and visualization (here)[https://github.com/OluKennie/WeRateDog-Udacity-Data-Analyst-Project-2/blob/main/act_report.ipynb]
