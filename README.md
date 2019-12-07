# NLP-text-summarization-GloVe
Text summarization using GloVe algorithm

Hereby, I am building a "News Briefer" using GloVe algorithm by scrapping TimesOfIndia RSS feeds to get news article text. This text is further passed to GloVe algorithm to create a brief summary of N sentences. 

Below is the basic data flow:
1. Get RSS feed for a topic. RSS feed contains news headline, link and published-date. 
2. Fetch the link HTML which contains the actual news article. Extract news text from it. 
3. Perform basic text pre-processing such as cleanup/normalization
4. Generate sentence vectors using GloVe algorithm.
5. Rank the sentences using pagerank algorithm. 
6. Take top N sentences which forms the summary of the news article.

Text is cleaned/normalized for html-stripping, accented, contraction, lowercase, lemmatization, special-char, stopwords. Normalized text is then passed to GloVe algorithm. I am using pre-trained Wikipedia 2014 + Gigaword 5 GloVe vectors available [here](https://nlp.stanford.edu/projects/glove/). Heads up – the size of these word embeddings is 822 MB.

