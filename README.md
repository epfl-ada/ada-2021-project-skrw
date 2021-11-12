# Hot Topic Detection and Analysis

# Abstract  (150 words):

Nowadays, the media is full of overwhelming information in different topics and different areas. Although large amount of data is helpful in big data mining, most of data is not meaningful to us. In order to extract meaningful information from a large dataset which contains millions of quotations, trending topic analysis is a Natural Language Processing (NLP) technique that allows us to automatically extract meaningful information from text by identifying recurrent themes or topics. Hot topic analysis can help providing many meaningful information to be used in many recommendataion system, for example, social media monitoring tools and marketing.

# Research questions : 

1. What are the most hot topics during the selected time period?
This is the key problem of our project. We would like to extract the most hot topics during the selected period of time. This enables us to have a more direct understanding on what topics are more prevalent, as this reveals what are people focusing. A possible hot topic in 2019 might be global climate change, as Greta Thunberg had continuously taken action to propel activities to fight against global climate change. 
2. How does the clout of these hot topics vary during the period of time?
It's obvious that the clout of these hot topics would change countinuously. This analysis can also be interesting because we can have a direct visualization on how people's interest on different topics vary.
3. Do attitudes towards these topics vary between different press?
People's attitudes towards these topics are also an interesting task. Quotations we have in the database reveals the speakers' attitudes towards the specific topic. What's more, it's also an interesting analysis to find out whether the attitudes towards specific topic change. For example, people's attitude towards global climate change might be negative in the beginning, as people might think this will not be a big problem. But after a period of time, people might feel that global climate change has became a big problem for our human-beings and then their attitudes might change.
4. Do attitudes towards these topics differ between different speaker? 
After analyzing in the scope of time, it can be also interesting to analyze in the scope of people. By analyzing attitudes towards the same topic between different speakers, we can find out whether speakers' attitudes have some difference.


# Proposed Database : 
quotes-2019.json.bz2: To analyze the hot topics in 2019, we use the Quotation-centric version of the dataset for year 2019. The quotation-centric version of the dataset is an aggregated set of unique quotations, which is minimal but sufficient for us to find the hot topics of the year as we don't need information of the context. 

 
# Methods : 
### Data Cleaning, Preprocessing and Initial Analysis:
The first step of data cleaning and preprocessing is to group quotations in the dataset according to date. As our main task is to find hot topics in the Quotebank Dataset, combining the quotations on the same day will not affect the occurrence of different topics. Non-ascii characters are removed and texts are standardized to facilitate the tokenization process of the dataset. Tokenization and lemmatization are accomplished to facilitate the Tfidf vectorization.

### Hot Topic extraction and Analysis:
To find the most hot topic during the selected time period, we need to extract the key topics in different documents.We will use Latent Semantic Analysis(LSA) and Latent Dirichlet Allocation (LDA) for topic modeling. Latent Semantic Analysis is based on a principle called the distributional hypothesis: words and expressions that occur in similar pieces of text will have similar meanings. We also use Latent Dirichlet Allocation (LDA) to model all the documents to topics in a way such that the words in each document are mostly captured by those topics. After extracting hot topics, we can classify different quotations related to the hot topics. This result can be applied to further analysis on the hot topics and data visualization.  

### Sentiment Analysis
After classifying quotations into different topics, we will apply sentiment analysis on different quotations related to the same topic. Sentiment analysis is a NLP technique to perform on textual data to determine whether the data is Postive, Negative or Neutral. In this project, we will apply machine learning technique to classify texts to different sentiment categories. By applying text extraction or text vectorization techniques, we can get bag-of-words for the original text. Then we can use support vector machines to classify these texts into different categories. Then we can accomplish further analysis on attitudes and the change of attitudes related to differents topics.
# Proposed timeline :
- Week 8 : Finished initial data cleaning, preprocessing. Implement initial analysis on processed data.
- Week 9 : Finish Hot topic extraction with LSA and LDA.
- Week 10 : Finish hot topic analysis on topics we extracted.
- Week 11 : Implement sentiment analysis on topics we extracted.
- Week 12 : Finalize the conclusion on research questions and make visualization towards these questions.
- Week 13 : Sort out the notebook and READme file. Finish the data story.

# Team Organization:
Shanci Li: Initial data preprocessing and analysis, analyze topic extraction result, finalize the conclusion
Wanting Li: Topic extraction, sentiment analysis, analyze sentiment analysis result, write data story
Kang Fu: Initial data preprocessing and analysis, analyze topic extraction result, data visualization
Runke Zhou: Writing READme for Milestone2, topic extraction, sentiment analysis, data visualization
# Questions for TAs

