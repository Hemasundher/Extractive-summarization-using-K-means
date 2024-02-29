# Extractive-summarization-using-K-means
Selecting key phrases from the entire text is referred to as extractive summarization.

To extract specific sentences from the original text, the clustering (K-means) technique is employed.


* Split the text into sentences using the Spacy module.
* Generate a sentence vector for each sentence using the SBERT model.
* The sentence vectors are of shape (768,), making them high-dimensional.
* Utilize the UMAP algorithm to reduce the dimensionality.
* Apply k-means clustering to the dimension-reduced vectors.
* Experiment with different values of k and assess them using silhouette scores.
* Once the optimal k value and k-means model are obtained, select one sentence from each cluster to represent that cluster.