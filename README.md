# Hot Topic Detection and Analysis

# Abstract  (150 words):

Nowadays, the media is full of overwhelming information in different topics and different areas. Although large amount of data is helpful in big data mining, most of data is not meaningful to us. In order to extract meaningful information from a large dataset which contains millions of quotations, trending topic analysis is a Natural Language Processing (NLP) technique that allows us to automatically extract meaningful information from text by identifying recurrent themes or topics. Hot topic analysis can help providing many meaningful information to be used in many recommendataion system, for example, social media monitoring tools and marketing.

# Research questions : 

1. What are the most hot topics during the selected time period?
2. How does the clout of these hot topic vary during the period of time?
3. What are the attitudes of different media towards these topics?
4. Do attitudes towards these topics vary between different press?
5. Do attitudes towards these topics change during the period of time for specific press or speaker? 


# Additional database : 

 
# Methods : 

### Data Cleaning, Preprocessing and Initial Analysis:
The first step of data cleaning and preprocessing is to group quotations in the dataset according to date. As our main task is to find hot topics in the Quotebank Dataset, combining the quotations on the same day will not affect the occurrence of different topics. Non-ascii characters are removed and texts are standardized to facilitate the tokenization process of the dataset. Tokenization and lemmatization are accomplished to facilitate the Tfidf vectorization.

### Hot Topic extraction and Analysis:
To find the most hot topic during the selected time period, we need to extract the key topics in different documents. We use Latent Dirichlet Allocation (LDA) to model all the documents to topics in a way such that the words in each document are mostly captured by those topics. After extracting hot topics, we can classify different quotations related to the hot topics. This result can be applied to further analysis on the hot topics and data visualization.  

### Sentiment Analysis
After classifying quotations into different topics, we will apply sentiment analysis on different quotations related to the same topic. Then we can accomplish further analysis on attitudes and the change of attitudes related to differents topics.
# Proposed timeline :
- Week 8 : 
- Week 9 : 
- Week 10 : 
- Week 11 :
- Week 12 :
- Week 13 : 

# Team Organization:
# Questions for TAs

