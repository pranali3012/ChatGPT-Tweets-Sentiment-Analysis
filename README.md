# ChatGPT-Tweets-Sentiment-Analysis
This project aims to investigate the sentiments of users towards ChatGPT, a language model developed by OpenAI. By analyzing user sentiments and considering demographic variables, we aim to gain a deeper understanding of user perceptions towards ChatGPT over time. 

# Dataset
https://www.kaggle.com/datasets/manishabhatt22/tweets-onchatgpt-chatgpt

The dataset used in our analysis was obtained from Kaggle after reviewing multiple datasets. We specifically selected this dataset because it covered tweets from December to April, providing us with the longest time period compilation available. The dataset included the location of the user, which added an important demographic aspect to our analysis. The dataset comprised the following columns:

This dataset contains tweets starting from November 2022 to 8th April, 2023 containing the keywords keywords #ChatGPT The dataset contains 12 columns which are:

Date - Date of the tweet
Tweet - Contents of the tweet
Url - Link for the original tweet
User - UserName of the person who tweeted.
UserCreated - Account creation date
UserVerified - Boolean field for verified user or not.
UserFollowers - Follower count of user.
UserFriends - Friends count of user.
Retweet - Count of retweets
Likes - Count of Likes
Location - Location of User
UserDescription - Description of user



# Approach 
We have used VADER (Valence Aware Dictionary for Sentiment Reasoning) for performing sentiment analysis on the dataset. VADER is a lexicon and rule-based sentiment analysis tool that uses a predefined dictionary to assign valence scores to various lexical features. It considers emoticons, acronyms, and slang words. VADER's lexicon encompasses a wide range of sentiment-bearing words, and it also takes into account emoticons such as the laughing emoji, popular acronyms like LOL, TTYL, IKR, and TMI that are commonly used in online communication, making it an ideal choice for tweet analysis.
VADER's analysis captures both the polarity and intensity of emotions, using heuristics to determine the overall sentiment score. VADER employs a set of heuristics like punctuation, capitalization, degree modifiers, negations, and conjunctions like ‘but’. It is able to understand and capture the change in magnitude of intensity or shift in polarity caused by these heuristics.

How is the overall sentiment of an input text determined?
Each lexical feature within the input text is assigned an individual valence score ranging from -4 to 4, where -4 denotes the most negative sentiment and 4 denotes the most positive. These individual scores are then combined to derive an overall sentiment score which is then normalized to ensure a standardized measure of sentiment ranging between -1 and 1. 

If overall valence score < 0, then the text is classified as ‘Negative’
If overall valence score = 0, then the text is classified as ‘Neutral’
If overall valence score < 0, then the text is classified as ‘Positive’
