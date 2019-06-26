# Character CNN for Text Classification
## Model Details
This is an implementation of the model presented in the paper [Character-level Convolutional Networks for Text Classification](https://papers.nips.cc/paper/5782-character-level-convolutional-networks-for-text-classification.pdf). There are multiple advantages of using a Char-CNN over word embedding models like word2vec or Glove, some of which are as follows:
- It is very good at handling out-of-vocabulary words as instead of learning individual embeddings for each word we learn embeddings for characters which can be combined to form any word, even those which the model hasn't seen before.
- For the same reason as mentioned above, the model performs fairly well for rare words in the vocabulary.
- Since we have few embeddings to learn, the model's complexity is reduced and the performance increases (in terms of speed).

## Dataset
The dataset used for classification is [BBC news articles](https://www.kaggle.com/yufengdev/bbc-fulltext-and-category) which contains 2226 articles divided into 5 categories. The model is provided only for demonstration purpose and hence no pre-processing is applied to the data. Even then, the model produces an above average classifier with just 5 epochs. Increasing the epochs to 25 gives accuracy up to 75% and further if the data is pre-processed it will increase even more.
