# NLP-on-Twitter-for-Mid-term-Elections

## Problem Statement
According to CNBC, the 2022 midterm elections are estimated to have cost more than $16.7 billion in campaign expenditure, making them the most “expensive” midterm elections in history. All involved parties spent lots of resources in terms of money, time, and people in the race to control the House and the Senate. One of the main campaign tools that candidates utilized to influence and understand public opinion was social media, particularly Twitter. What if political parties could utilize Twitter data to forecast election results and understand the public's main concerns? 

## Proposed Solution
Our team proposes an “Election outcome forecasting model” which utilizes Twitter data such as candidates’ tweets during campaigning, the public’s replies to those tweets, and other Twitter metadata such as the number of shares, likes, comments, and followers of each candidate, in an attempt to predict the winner for the Senate Elections in each of the 33 states where midterm elections took place. To achieve this, we leverage various Machine Learning techniques such as Topic Modelling, Sentiment Analysis, and Regression Models.

## Methodology
Using Twitter Developer API, we scraped the tweets of all 93 candidate senators that maintain a Twitter account for one month before the elections and the general public's replies to those tweets for 7 days. Thus, we have two datasets: one that includes ~9K tweets from senate candidates and another one of ~41K replies from the general population to those candidates' tweets.
We implemented a Natural Language Processing technique, namely Latent Dirichlet Allocation, to identify the topics most frequently talked about by the candidates during campaigning. We came up with 7 broad election issues: Election Campaigns, Inflation/ Economy, Healthcare, Abortion, Crime/ Race, Students/ Schools, and Current Events (such as Hurricane Ian/ Ukraine War/ Iran Protests).
We further leveraged another Natural Language Processing technique, Sentiment Analysis, utilizing three models: TextBlob, Flair, and DistilBert, to understand the public’s response (positive/ negative/ neutral) to the candidates’ tweets.
We applied extensive feature engineering to combine the topic data with public sentiments and relevant metadata such as the number of followers, likes, and retweets to generate our final dataset at a candidate level. We then used various Linear and Ensemble methods to forecast candidates' vote share in their respective states and identify the Senate winners.


## Key Results
Our Random Forest Bert-based model correctly predicted the winning party in 31 out of the 33 states and the winning candidate in 30 out of 33 states. The incorrectly predicted states (party-level) were Nevada and Pennsylvania, both of which had a cutting-throat battle. Our model characterized Inflation, Abortion, and Healthcare as the most important predictors, controversial issues that have polarized the general public over the last few months.


## Conclusion
Political parties could utilize such a model to identify the public's perspective on their candidates and the key election issues, which can give them a significant lead in future elections. It is also important to mention that such a technique could easily be reused for any election with social media campaigns. Finally, this model can be extended to other critical domains such as public policy, humanitarian decision-making, and product feedback. 
