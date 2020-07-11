# Pakistan Twitter Analysis

This repository of code analyzes Twitter data in Pakistan from 2007-2020.  It was written for the World Bank Report "The Social Contract in Pakistan's Former Tribal Areas." 

## Files

* 000. Determining Location of Users with Geocoordinates.ipynb
Uses Twitter generated geocoordinates to assign mean latitude and longitude values to users in the dataset and retains only users with mean locations in Pakistan.

* 002. Assigning Provinces to users.ipynb
Merges city-level user data with file that matches cities to provinces.  Output is that all users have both city and province data in Pakistan.

* 003. Descriptive Statistics on all Tweets.ipynb
Generates descriptive plots such as number of tweets over time, number of unique users over time, languages in the dataset, and language distribution among users in the dataset.

* 004. Plotting User Locations.ipynb
Generates bar charts of users per province, users per city in each province, and cloropleth maps of numbers and percentages of users per city.

* 005. Separate Tweets inside and outside of KP.ipynb
Separates data into two dataframes - one for users based in Khyber Pakhtunkhwa (former tribal areas) and one for users based in the rest of Pakistan.

* 006. Cleaning KP Tweet Text.ipynb
Cleans tweet text including putting to lowercase, moving punctuation and emojis to their own columns, removing retweet and @ signs, removing line breaks, and removing urls (which are not functional in this dataset).

* 007. Extracting and Plotting Hashtags in KP.ipynb
Extracts hashtags into their own column. Joins into a list and value-counts to produce hashtag frequency plot.

* 008. Separating KP Tweets by Language.ipynb
Separates tweets into five different categories based on language.  English, Urdu, and Pashto language tweets are determined by Twitter-generated language labels and stopword searches for each respective language. Tweets with fewer than three words and no hashtags are moved to a "low-data" dataframe and tweets not in English, Urdu, or Pashto are moved to a "unidentified language" dataframe.

* 009. Downloading KP Urdu Arabic Tweets for Translation.ipynb
Opens pickle file of Urdu language tweets in Arabic script and downloads 50K at a time for translation to English via google translate. 

* 010. Uploading and merging Urdu Translated Tweets.ipynb
Uploads and merges translated Urdu tweets. 

* 011. Downloading Pashto Tweets for Translation.ipynb
Opens pickle file of Pashto language tweets and downloads 50K at a time for translation to English via google translate. 

* 012. Uploading and merging Pashto translated tweets.ipynb
Uploads and merges translated Pashto tweets. 

* 013. Finding Pashtun Diaspora Tweets .ipynb
Identifies probable members of Pashtun diaspora throughout Pakistan by identifying users outside of former tribal areas who have written at least one tweet in Pashto. Saves file of users.

* 014. Plotting Percent of Pashtun users Per City outside KP.ipynb
Plots total numbers and percentage per population of probable Pashtun diaspora in Pakistan in barchars and chloropleth maps. 

* 015. Combining English, Urdu, Pashto KP Tweets.ipynb
Merges English language tweets in KP with translated Urdu and Pashto tweets. 

* 016. Descriptive Statistics For KP Users.ipynb
Generates descriptive plots such as number of tweets over time, number of unique users over time, languages in the dataset, and language distribution among users in KP. 

* 017. Bot Detection - Calculating SD of Tweet Intervals and Average Tweets Per Day for KP users.ipynb
Uses formula to determine the standard deviation of the distribution of each user's tweet frequency.  SD's close to zero suggest uniform tweeting intervals and suggests the user might be a bot. Users with SD's less than 60 minutes are saved in a "potential bots" dataframe. Uses formula to determine average tweets per day per user.  Users with average tweets per day greater than 25 are suspected bots and saved in a "potential bots" dataframe.

* 018. KP Topic Modeling.ipynb
Users Short Text Topic Modeling (STTM) on KP tweets with k=25. Saves a dataframe with the 8 most important words in each topic as well as the frequency of those topics in the data. Assigns a topic to each tweet and a percentage fit for each tweet in each topic and saves the dataframe.

* 019. Plotting Distribution of Topics in KP.ipynb
Creates pie chart showing distribution of topics in the data. 

* 020. Plotting Change in Topics Over Time.ipynb
Creates stacked area plot to show changes in topic distribution over time.

* 021. English Sentiment Analysis - Inside and Outside of KP.ipynb
Uses hedonometer dictionary (hedonometer.org) to calculate the sentiment of English-language tweets in the data on a scale of 1-9.  Saves sentiment score, standard deviation of the score estimate, and words that contributed to the score in columns in the dataframe for each tweet.

* 022. Urdu and Pashto Sentiment Analysis - Inside and Outside KP.ipynb
Uses a hedonometers trandlated into Urdu and Pashto respectively (via Google Translate) to calculate the sentiment of Urdu and Pashto language tweets in their original un-translated form. Saves sentiment score, standard deviation of the score estimate, and words that contributed to the score in columns in the dataframe for each tweet.

* 023. Combining Sentiment Score Results in Different Languages.ipynb
Merges dataframes with sentiment scores from English, Urdu, and Pashto.

* 024. Plotting Sentiment Analysis in Pakistan versus KP.ipynb
Plots timeseries of sentiment in KP, in Pakistan versus KP, and excess sentiment of KP compared to Pakistan.

* 025. Combining Topic and Sentiment Data in KP Tweets.ipynb
Merges main tweets dataframe with topics and sentiment dataframes.

* 026. Assigning sub-categories in Municipal Issues Topic.ipynb
Uses keyword analysis to assign sub-categories in the topic and generates a dataframe of only these tweets categorized by sub-topic.

* 027. Assigning sub-categories in Corruption Topic.ipynb
Uses keyword analysis to assign sub-categories in the topic and generates a dataframe of only these tweets categorized by sub-topic.

* 028. Assigning sub-categories in Economy Topic.ipynb
Uses keyword analysis to assign sub-categories in the topic and generates a dataframe of only these tweets categorized by sub-topic.

* 029. Assigning sub-categories in Violent Conflict Topic.ipynb
Uses keyword analysis to assign sub-categories in the topic and generates a dataframe of only these tweets categorized by sub-topic.

* 030. Assigning sub-categories in Political Debate.ipynb
Uses keyword analysis to assign sub-categories in the topic and generates a dataframe of only these tweets categorized by sub-topic.

* 031. Assigning sub-categories in Party Politics.ipynb
Uses keyword analysis to assign sub-categories in the topic and generates a dataframe of only these tweets categorized by sub-topic.

* 032. Assigning sub-categories in Family and Gender .ipynb
Uses keyword analysis to assign sub-categories in the topic and generates a dataframe of only these tweets categorized by sub-topic.

* 033. Assigning sub-categories in Supreme Court Nawaz Sharif.ipynb
Uses keyword analysis to assign sub-categories in the topic and generates a dataframe of only these tweets categorized by sub-topic.

* 034. Plotting Subtopic Data for Each Topic from Topic Modeling.ipynb
For each dataframe generated in 026-033, generates stacked timeseries representing the percentage of tweets on each topic over time, barcharts showing the percentage difference between subtopic sentiment and median sentiment for all tweets, barchart of most common bigrams in the topic, barcharts of most common words in the topic, barcharts of most common hashtags in the topic, chloropleth map showing percentage of users tweeting about the topic per city, and a stacked barchart showing the percentage of users tweeting about each sub-topic within each city. 

* 035. Removing Suspected Bots from KP Dataframe.ipynb
Loads the user id's of potential bots identified by standard deviation of tweet intervals and tweet frequency.  Determines users who started tweeting after 2019 and adds them to list of potential bots (as bot detection may not have had time to catch them). Removes all users identified as potential bots. 

036. Assigning KP Tweets since 2018 to Categories based on Keywords.ipynb
Uses keyword search analysis to group data into categories of interest based on the primary research question.  Outputs eight dataframes on different categories of interest with dummy variable columns identifying sub-categories in each category.

037. Analysis of Keyword Categorized Tweet Categories in KP.ipynb
For each dataframe generated in 036, generates stacked timeseries representing the percentage of tweets on each category over time, barcharts showing the percentage difference between sub-category sentiment and median sentiment for all tweets, barchart of most common bigrams in each category, barcharts of most common words in each category, barcharts of most common hashtags in each category, chloropleth map showing percentage of users tweeting about each category per city, and a stacked barchart showing the percentage of users tweeting about each sub-category within each city. 
