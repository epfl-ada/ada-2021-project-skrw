# Quotations Behind Brexit

# Abstract  (150 words):

Brexit (a portmanteau of "British exit") was the withdrawal of the United Kingdom (UK) from the European Union (EU) at 23:00 GMT on 31 January 2020 (00:00 CET). The UK is the first and so far the only member state to have left the EU, after 47 years of having been a part of the union — the EU and its predecessor the European Communities (EC), which included the European Economic Community — since 1 January 1973. Actually, the United Kindom was considering about exiting the EU ever since 2016. After several referendums and negotiations between UK-EU, they finally exit the EU in early January, 2020. And the withdrawl aggrement finally came into force on 31 January 2020.

In our project, we would like to dive into quotations talking about the Brexit and analyze information behind these quotations to learn about people's attitude through the whole event.

# Research questions : 
1. What are the distribution characteristics of quotations about the Brexit?

Analyzing the distribution characteristics is the elementary problem to be solved when we are trying to analyze quotations talking about the Brexit. This analysis is based on different characteristics of speakers' of these quotations, as this reveals what kind of speaker tends to express their opinions on the Brexit. For example, we can analyze the nationality, the gender, the occupation of these speakers. This helps us sketch the group of people cares about the Brexit. What's more, we can also analysis the change of the number of quotations from 2016 to 2020, which reveals the popularity change of the topic, Brexit, during this time period.

2. What are the topics related to the Brexit during this time period?

Topic detection is also an interesting problem to be solved. We would like to extract the top topics related to the Brexit. This enables us to have a more detailed understanding of what speakers pay attention to when they talk about the Brexit. For example, we may find that top topics related to the Brexit is about people or business. This means that when people talk about the Brexit, they tend to pay attention to what the Brexit may lead to on people's life and the business relationship between the UK and the EU.

3. Do attitudes towards the Brexit vary during this period of time?
People's attitudes towards the Brexit are also worth analyzing. Quotations we have in the database reveal the speakers' attitudes towards the Brexit. What's more, it's also an interesting analysis to find out whether the attitudes towards the Brexit change. For example, people might be negative towards the Brexit in the beginning. But after a period of time, they may change their mind to postive. Maybe they are persuaded that this have more postive effects by other speakers.

# Proposed Database : 
quotes-2019.json.bz2: To analyze the hot topics in 2019, we use the Quotation-centric version of the dataset for the year 2019. The quotation-centric version of the dataset is an aggregated set of unique quotations, which is minimal but sufficient for us to find the hot topics of the year as we don't need the information of the context. 

**speaker_attributes.parquet**: Additional metadata about the speakers in the Quotebank dataset. This dataset gives us additional information about speakers we are interested in to help us analyze the distribution characteristics of quotations about the Brexit

**wikidata_labels_descriptions_quotebank.csv.bz2**： This dataset helps us to extract the aforementioned information about speakers from the Wikidata knowledge base.
 
# Methods : 
### Data Cleaning and Preprocessing:

### Enrich dataset:
After data cleaning and preprocessing, we can get all quotations related to the Brexit in this period of time. As the original dataset only contains very limited information about the speaker, we need to enrich the original dataset with the speaker_attributes.parquet based on the QID of the speaker. What's more, as we need to analyze the distribution of speakers' age range, we need to convert the special format of date of birth into age. With this step, it helps us to accomplish future steps easier.


### Hot Topic extraction and Analysis:
To find the hottest topic during the selected time period, we need to extract the key topics in different documents. We will use Latent Semantic Analysis(LSA) and Latent Dirichlet Allocation (LDA) for topic modeling. Latent Semantic Analysis is based on a principle called the distributional hypothesis: words and expressions that occur in similar pieces of text will have similar meanings. We also use Latent Dirichlet Allocation (LDA) to model all the documents to topics in a way such that the words in each document are mostly captured by those topics. After extracting hot topics, we can classify different quotations related to the hot topics. This result can be applied to further analysis on hot topics and data visualization.  

### Sentiment Analysis
After classifying quotations into different topics, we will apply sentiment analysis on different quotations related to the same topic. Sentiment analysis is an NLP technique performed on textual data to determine whether the data is Positive, Negative, or Neutral. In this project, we will apply a machine learning technique to classify texts into different sentiment categories. By applying text extraction or text vectorization techniques, we can get bag-of-words for the original text. Then we can use support vector machines to classify these texts into different categories. Then we can accomplish further analysis on attitudes and the change of attitudes related to different topics.
# Proposed timeline :
- Week 8: Finished initial data cleaning, preprocessing. Implement initial analysis on processed data.
- Week 9: Finish Hot topic extraction with LSA and LDA.
- Week 10: Finish hot topic analysis on topics we extracted.
- Week 11: Implement sentiment analysis on topics we extracted.
- Week 12: Finalize the conclusion on research questions and make visualization towards these questions.
- Week 13: Sort out the notebook and READme file. Finish the data story.

# Team Organization:
Shanci Li: Initial data preprocessing and analysis, analyze topic extraction result, finalize the conclusion

Wanting Li: Topic extraction, sentiment analysis, analyze sentiment analysis result, write data story

Kang Fu: Initial data preprocessing and analysis, analyze topic extraction result, data visualization

Runke Zhou: Writing READme for Milestone2, topic extraction, sentiment analysis, data visualization

# Questions for TAs
1. When doing the lemmatization, what kind of words should we keep, like verb, noun, adjective? Can we remove adverbs?
2. When using the phrase detection(bigram or trigram), should removing stopwords before this process or after?
