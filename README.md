# NLP_frequency_-_Polarity_using_Scispacy-
Problem Statement:

• Objective 1: Get the most frequent entities from the tweets.

• Objective 2: Find out the sentiment/polarity of each author towards each of the entities.

Technology/Tools used:

• Spacy for tokenization, stop words removal, named entity recognition.

• Scispacy (“en_ner_bc5cdr_md” module having labels “Entity” for named entity recognition. (medical or bi medical named entities)

• “en_core_sci_lg” module is used to cater to clinical dataset i.e; “tweets.json”

• Pandas for analyzing the dataset.

• Json to reads the dataset to Dataframe.

• Natural Language Processing library “SentimentIntensityAnalyzer”, Valence Aware Dictionary or Vader for sentiment Reasoning.

Approach followed:

Step 1: Installed spacy.

Step 2: Imported and loaded scispacy and its biomedical module “en_ner_bc5cdr_md”.

Step 3: “Json” format read to Dataframe using orientation “index”

Step 4: Cleaned “tweet_text” column.

• No duplicates or missing values in the Dataframe.

• Removed punctuations, emoji s and digits,

• Removed hyper link and hashtags,

• Removed words less than 2 characters

• Changed to lower case,

• Removed extra trailing spaces,

• Created tokens,

• Removed stop words

Step 5: Extracted entity from “cleaned_tweet_text” column.

Step 6: Frequency of entities (solution to problem statement 1)

Step 7: Calculated polarity on each entity.

Step 8: Authors' sentiment analysis (solution to problem statement 2)

Approach to solve the problem :

• Spacy module “en_core_web_sm” did not recognise context related entity, tried few clinical module but “en_ner_bc5cdr_md” biomedical module of scispacy solved this problem.

Conclusion:

• Data Cleansing and Entities Extraction were a crucial parts of the solution. Removing unnecessary elements from “tweet_text” consumed most of the time.

• Entities Extraction is a key point in the solution. Finding the right entities defines extracting the right phrases from the tweets on which the core meaning of tweets relies on.

• Then, there comes extracting the sentiments of each entities from the tweets with the help of "NLTK package SentimentIntensityAnalyzer" .
