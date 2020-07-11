# Pakistan Twitter Analysis

This repository of code analyzes Twitter data in Pakistan from 2007-2020.  It was written for the World Bank Report "The Social Contract in Pakistan's Former Tribal Areas." 

## Files

#000. Determining Location of Users with Geocoordinates.ipynb
Uses Twitter generated geocoordinates to assign mean latitude and longitude values to users in the dataset and retains only users with mean locations in Pakistan.

#002. Assigning Provinces to users.ipynb
Merges city-level user data with file that matches cities to provinces.  Output is that all users have both city and province data in Pakistan.

#003. Descriptive Statistics on all Tweets.ipynb
Generates descriptive plots such as number of tweets over time, number of unique users over time, languages in the dataset, and language distribution among users in the dataset.

#004. Plotting User Locations.ipynb
Generates bar charts of users per province, users per city in each province, and cloropleth maps of numbers and percentages of users per city.

#005. Separate Tweets inside and outside of KP.ipynb
Separates data into two dataframes - one for users based in Khyber Pakhtunkhwa (former tribal areas) and one for users based in the rest of Pakistan.

#006. Cleaning KP Tweet Text.ipynb
Cleans tweet text including putting to lowercase, moving punctuation and emojis to their own columns, removing retweet and @ signs, removing line breaks, and removing urls (which are not functional in this dataset).

#007. Extracting and Plotting Hashtags in KP.ipynb
Extracts hashtags into their own column. Joins into a list and value-counts to produce hashtag frequency plot.

#008. Separating KP Tweets by Language.ipynb
Separates tweets into five different categories based on language.  English, Urdu, and Pashto language tweets are determined by Twitter-generated language labels and stopword searches for each respective language. Tweets with fewer than three words and no hashtags are moved to a "low-data" dataframe and tweets not in English, Urdu, or Pashto are moved to a "unidentified language" dataframe.

#009. Downloading KP Urdu Arabic Tweets for Translation.ipynb
Opens pickle file of Urdu language tweets in Arabic script and downloads 50K at a time for translation to English via google translate. 

#010. Uploading and merging Urdu Translated Tweets.ipynb
Uploads and merges translated Urdu tweets. 

#011. Downloading Pashto Tweets for Translation.ipynb
Opens pickle file of Pashto language tweets and downloads 50K at a time for translation to English via google translate. 

#012. Uploading and merging Pashto translated tweets.ipynb
Uploads and merges translated Pashto tweets. 

#013. Finding Pashtun Diaspora Tweets .ipynb
Identifies probable members of Pashtun diaspora throughout Pakistan by identifying users outside of former tribal areas who have written at least one tweet in Pashto. Saves file of users.

#014. Plotting Percent of Pashtun users Per City outside KP.ipynb
Plots total numbers and percentage per population of probable Pashtun diaspora in Pakistan in barchars and chloropleth maps. 

#015. Combining English, Urdu, Pashto KP Tweets.ipynb
Merges English language tweets in KP with translated Urdu and Pashto tweets. 

#016. Descriptive Statistics For KP Users.ipynb
Generates descriptive plots such as number of tweets over time, number of unique users over time, languages in the dataset, and language distribution among users in KP. 

#017. Pie Charts of Tweets Manually Designated to Topics of Interest in KP.ipynb
Generates pie charts based on 

018. Analysis of Manually Categorized Service Delivery Tweets in KP.ipynb
2 days ago512 kB
019. Bot Detection - Calculating SD of Tweet Intervals and Average Tweets Per Day for KP users.ipynb
2 days ago412 kB
020. KP Topic Modeling.ipynb
4 hours ago10.2 kB
021. English Sentiment Analysis - Inside and Outside of KP.ipynb
2 days ago10.7 kB
022. Urdu and Pashto Sentiment Analysis - Inside and Outside KP.ipynb
2 days ago7.71 kB
023. Plotting Distribution of Topics in KP.ipynb
4 hours ago3.91 kB
024. Combining Sentiment Score Results in Different Languages.ipynb
4 hours ago4.22 kB
025. Plotting Sentiment Analysis in Pakistan versus KP.ipynb
4 hours ago468 kB
026. Plotting Change in Topics Over Time.ipynb
4 hours ago526 kB
027. Combining Topic and Sentiment Data in KP Tweets.ipynb
4 hours ago3.8 kB
028. Assigning sub-categories in Municipal Issues Topic.ipynb
4 hours ago26.3 kB
029. Assigning sub-categories in Corruption Topic.ipynb
4 hours ago16.5 kB
030. Assigning sub-categories in Economy Topic.ipynb
4 hours ago17.4 kB
031. Assigning sub-categories in Violent Conflict Topic.ipynb
4 hours ago18.3 kB
032. Assigning sub-categories in Political Debate.ipynb
4 hours ago14.9 kB
033. Assigning sub-categories in Party Politics.ipynb
3 hours ago25.4 kB
034. Assigning sub-categories in Family and Gender .ipynb
3 hours ago15.4 kB
035. Assigning sub-categories in Supreme Court Nawaz Sharif.ipynb
3 hours ago15.4 kB
036. Plotting Subtopic Data for Each Topic from Topic Modeling.ipynb
an hour ago960 kB
037. Removing Suspected Bots from KP Dataframe.ipynb
2 hours ago3.14 kB
038. Assigning KP Tweets since 2018 to Categories based on Keywords.ipynb
2 hours ago84 kB
039. Plotting Subtopic Data for Each Topic from Topic Modeling.ipynb

