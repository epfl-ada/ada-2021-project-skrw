# Quotations Behind Brexit

The burst of Brexit bubble

Data story link: https://shanci-li.github.io/

# Abstract  (150 words):

Brexit (a portmanteau of "British exit") was the withdrawal of the United Kingdom (UK) from the European Union (EU) at 23:00 GMT on 31 January 2020 (00:00 CET). Actually, the United Kindom was considering about exiting the EU ever since 2016. After several referendums and negotiations between UK-EU, they finally exit the EU in early January, 2020. And the withdrawl aggrement finally came into force on 31 January 2020.

Shortly afterwards, the post-brexit scenario has raised concerns about regional integration and economic security both in the UK and the EU in recent years. Hereby we look forward to shedding some light on these current issues by a full retrospect of Brexit. We'll dive into 95808 quotations talking about the Brexit from 2016 to 2020, summarize characteristics of relevant speakers, extract underlying top topics behind Brexit, and further analyze the changing attitudes of speakers throughout the whole process.

# Research questions : 
1. What are the distribution characteristics of quotations about the Brexit?

Analyzing the distribution characteristics is the elementary problem to be solved when we are trying to analyze quotations talking about the Brexit. This analysis is based on different characteristics of speakers' of these quotations, as this reveals what kind of speaker tends to express their opinions on the Brexit. For example, we can analyze the nationality, the gender, the occupation of these speakers. This helps us sketch the group of people cares about the Brexit. What's more, we can also analyze the change of the number of quotations from 2016 to 2020, which reveals the popularity change of the topic, Brexit, during this time period.

2. What are the topics related to the Brexit during this time period?

Topic detection is also an interesting problem to be solved. We would like to extract the top topics related to the Brexit. This enables us to have a more detailed understanding of what speakers pay attention to when they talk about the Brexit. For example, we may find that top topics related to the Brexit is about people or business. This means that when people talk about the Brexit, they tend to pay attention to what the Brexit may lead to on people's life and the business relationship between the UK and the EU.

3. Do attitudes towards the Brexit vary during this period of time?

People's attitudes towards the Brexit are also worth analyzing. Quotations we have in the database reveal the speakers' attitudes towards the Brexit. What's more, it's also an interesting analysis to find out whether the attitudes towards the Brexit change. For example, people might be negative towards the Brexit in the beginning. But after a period of time, they may change their mind to postive. Maybe they are persuaded that this have more postive effects by other speakers.

# Proposed Database : 
**quotes-2016.json.bz2 - quotes-2020.json.bz2**: To analyze the topic about Brexit, we use the Quotation-centric version of the dataset from 2016 to 2020. The quotation-centric version of the dataset is an aggregated set of unique quotations, which is minimal but sufficient for us. We will extract all the quotations containing Brexit to analyse the Brexit.

**speaker_attributes.parquet**: Additional metadata about the speakers in the Quotebank dataset. This dataset gives us additional information about speakers we are interested in to help us analyze the distribution characteristics of quotations about the Brexit

**wikidata_labels_descriptions_quotebank.csv.bz2**： This dataset helps us to extract the aforementioned information about speakers from the Wikidata knowledge base.
 
# Methods : 
### Data Cleaning and Preprocessing:

### Enrich dataset:
After data cleaning and preprocessing, we can get all quotations related to the Brexit in this period of time. As the original dataset only contains very limited information about the speaker, we need to enrich the original dataset with the speaker_attributes.parquet based on the QID of the speaker. What's more, as we need to analyze the distribution of speakers' age range, we need to convert the special format of date of birth into age. With this step, it helps us to accomplish future steps easier.


### Hot Topic extraction and Analysis:
To find the hottest topic during the selected time period, we need to extract the key topics in different documents. We will use Latent Dirichlet Allocation (LDA) for topic modeling. Latent Dirichlet Allocation (LDA) is a generative statistical model that allows sets of observations to be explained by unobserved groups that explain why some parts of the data are similar. For example, our observations are words collected into quotations, it posits that each quotation is a mixture of a small number of topics and that each word's presence is attributable to one of the quotation's topics. After extracting hot topics, we can classify different quotations related to the hot topics. This result can be applied to further analysis on hot topics and data visualization.  

### Sentiment Analysis
Since the quotation data has no label information, we cannot adopt the supervised machine learning techniques. Here we apply the pretrained model from Transformers to finish the sentiment analysis task.Transformers provides thousands of pretrained models to perform tasks on different modalities such as text, vision, and audio. Transformers provides APIs to quickly download and use those pretrained models on a given text, fine-tune them on your own datasets. To immediately use a model on a given input (text, image, audio, ...), Transformers provides the pipeline API. Pipelines group together a pretrained model with the preprocessing that was used during that model's training. Using the pretrained model, we obtain the positive or negative label of each quotations. This method is a time-consuming task. Therefore, we only do this part toward UK people and save the output so that it is easier for us to load it later.
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
