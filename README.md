# Sentiment Analysis and Social Network Analysis
R Sentiment Analysis project about hashtag #pride2020 on Twitter, excluding retweets. Data have been extract from 24th June 2020 to 10th July 2020 (19354 tweets in English). 
A non-bernoullian sample of 10000 units has been extracted. The first step was data-cleaning: removal of URLs, emoticons, hashtags, non-ASCII charachters.
After creating the corpus next step has been pre-processing. This phase coincided with: 1 - word normalisation (all words in lowercase); 2 - numbers removal; 3 - stopwords removal; 
4 - tags removal; 5 - other corrections; 6 - stemming through the library "SnowballC".
Term-Doc matrix has been created. Since text data like this are sparse a core task was sparseness reduction. A dataframe with 192 words in a decreasing order of frequency has been 
created. Sentiment analysis has been carried out through the library "syuzhet". The output was a dataframe, where rows were documents and columns were the "sentiments" such as: 
anger, anticipation, disgust, fear, disgust, joy, sadness, surprise, trust, negative and positive. For each tweet the frequency of each sentiment has been specified.
In order to provide more information Social Network Analysis techniques have been employed. First, high frequency words have been excluded because they do not provide so much 
information. Therefore, a new corpus has been created and all the operations made on the first corpus have been replicated on this second corpus as well.
The second Ter-Doc matrix is composed of 184 words and it has been used to determine the adjacency matrix. The latter is important in order to create graphs and to highlight 
relationships among the words. Finally, in order to improve graph interpretation community detection has been employed. The main goal was to identify tight groups in the network. 
"Fast greedy" algorithm has been used to find out 6 communities. The main network and the 6 communities were represented through the software "Gephi".
The last phase of the whole analysis was bigrams and trigrams creation, i.e., the most frequent sequences of 2-3 words.
