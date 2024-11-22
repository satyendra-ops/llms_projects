# llms_projects
A collection of self-developed LLM-based projects.

## 1. Zero-Shot Unsupervised Text Classification using Sentence Transformers

In this project, we tackle the task of sentiment analysis on the Rotten Tomatoes dataset in an unsupervised setting, without utilizing any predefined labels. This approach is useful in scenarios where the text data lacks annotations, and the objective is to classify the data into predefined categories (e.g., positive or negative sentiment).

### Methodology

The methodology consists of the following key steps:

1. **Text Embedding Generation**  
   We use [Sentence Transformers](https://www.sbert.net/) to generate embeddings for each text sample, capturing their semantic representation in a high-dimensional vector space.

2. **Clustering**  
   We apply the K-Means++ clustering algorithm to partition the embeddings into two clusters, corresponding to the two sentiment categories: positive and negative.

3. **Cluster Identification**  
   To identify the sentiment associated with each cluster, we calculate the cosine similarity between the cluster centroids and the embeddings of predefined reference sentences:
   
   - "A positive movie review"
   - "A negative movie review"
   
   This step allows us to assign sentiment labels to the clusters based on the closest reference sentence.

4. **Classification**  
   For test data, we compute the cosine similarity between their embeddings and the identified cluster centroids. Each test sample is classified into the corresponding sentiment category based on the highest cosine similarity.

### Summary
This approach demonstrates how unsupervised learning techniques can be effectively applied for sentiment analysis, leveraging semantic embeddings and clustering to achieve meaningful classification without relying on labeled data.
