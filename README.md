# Abstractive text summarization using CNN/DailyMail dataset

Abstractive text summarization summarizes the text maintaining coherent information in a similar amount of words as human generated summary. In the report, briefly describe the abstractive text summarization task and several methods used to predict the summary in a concise way. Notebook file fine-tunes T5 transfer learning model on CNN/DailyMail dataset and achieve a strong ROUGE-1 unigram measure of 44% and ROUGE-2 bigram of 14%.


## Dataset

[CNN, Daily Mail Dataset](https://www.kaggle.com/gowrishankarp/newspaper-text-summarization-cnn-dailymail)

An English-language dataset containing over 300k unique news articles as written by journalists at CNN and the Daily Mail. 

The dataset has the following columns: 
1. id: a string containing the url
2. article: the body of the news article 
3. highlights: the highlight of the article as written by the article author 

Article and highlights features are used as a 'source_text' and 'target_text' respectively as a training data.The target_text feature is used to test the model generated summarization vs the author generated summarization of the source_text.

## Pre-processing

Following pre-processing of the data is conducted. 
1. General contractions in the English language are expanded for consistency of each type of word. 
2. All the text converted to lowercase and all the unwanted characters, stopwords are removed from the dataset. 
3. Frequency of each word in the vocabulary calculated. 
4. Final vocabulary of size 58, 2734 words are obtained.

## Results

| CNN/DailyMail Summary Text | T5 Fine tuned predicted summary text |
| :------------: |:---------------:| 
| Aluko nets winner with ten minutes remaining at KC Stadium. Tomas Marek put visitors into shock lead after two minutes. Ahmed Elmohamady equalised for the hosts .Steve Bruce's side now await Europa League play-off. | Ahmed Elmohamady gave AS Trencin the lead early on in the first half. Sone Aluko doubled the lead with a stunning free-kick from six yards. Hull's European adventure was extended by a minute-long penalty.|

ROUGE 1: 0.11, ROUGE 2: 0.02


