# llms_projects
List of self-developed LLM based projects

1. Zero-Shot Unsupervised Text Classification using Sentence Transformers
In this work, we address the task of sentiment analysis on the Rotten Tomatoes dataset in an unsupervised setting, without utilizing its provided labels. This approach is motivated by scenarios where the text data lacks annotations, and the objective is to classify the data into predefined categories.

Methodology
Our methodology involves the following steps:

Text Embedding Generation
We use Sentence Transformers to compute embeddings for the text samples, capturing their semantic representations.

Clustering
We apply the K-Means++ clustering algorithm to partition the embeddings into two clusters, corresponding to the two sentiment categories (positive and negative).

Cluster Identification
To identify the sentiment associated with each cluster, we calculate the cosine similarity between the cluster centroids and the embeddings of predefined reference sentences:

"A positive movie review"
"A negative movie review"
This allows us to assign sentiment labels to the clusters.
Classification
For test data, we compute the cosine similarity between their embeddings and the identified cluster centroids. Based on the highest similarity, each test sample is classified into the corresponding sentiment.

This approach demonstrates an application of unsupervised techniques for sentiment analysis, leveraging semantic embeddings and clustering to achieve meaningful classification without reliance on labeled data.


