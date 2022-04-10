# Capstone - What is US lawmakers' sentiment on Cryptocurrencies

### Background
Many people became rich by investing in cryptocurrencies. I would like to be rich too but I don't want to invest in cryptocurrencies blindly. I am willing to take (calculated) risk and that's the objective of this project, i.e. to analyse the sentiment of US congressman towards cryptocurrecies and deduce whether cryptocurrencies will be accepted/regulated in US. To analyse US congressman sentiment, I analyse the hearing related to cryptocurrencies, this hearing involved 42 congressmen and 6 CEOs of Cryptocurrencies company. 


### Problem Statement
Assume cryptocurrencies will be accepted by the US if majority of the sentiment towards cryptocurrencies is positive. This project aims to detect US lawmakers' sentiment on Cryptocurrencies. 

### Data collection

Use beautiful soup to scrap transcript of US House on Financial Services hearing: https://www.rev.com/blog/transcripts/crypto-ceos-testify-before-house-financial-services-hearing-transcript



### Data Dictionary

|Feature|Type|Description|
|---|---|---|
|Time|*datetime64*|timestamp of speech|
|speaker|*object*|Name of speaker|
|speech|*object*|Sppech|

### EDA and cleaning data

**crypto_dic.csv**: This cleaned dataframe contains 645 rows (i.e. paragraphs) and 3 columns 

1. Standardize name of the same speaker
2. Label speaker's role, i.e. congress or CEO
3. Count number of words by each speaker


### Preprocessing and Modeling

1. Tokenise paragraphs into sentences
2. Use KeyBERT to extract keywords from each sentence
3. Use Hugging Face to analyse sentiment of each sentence


### Evaluation 

1. Use CountVectoriser to identifiy top 10 words from positive and negative sentiment sentences
2. Identify the main topics discussed for positive sentiment and negative sentiment respectively
3. Summarise the proportion of positive/neutral/negative sentiments from the whole hearing
4. Analyse the proportion of positive/neutral/negative sentiments by congress and CEO respectively

### Conclusion and Recommendation

1. Overall, the hearing has more positive comments than negative comments. 
2. However, when analyse based on roles, congressmen have more negative comments than positive comments; while CEOs have more positive comments than negative comments. 

### Reference
https://www.rev.com/blog/transcripts/crypto-ceos-testify-before-house-financial-services-hearing-transcript
