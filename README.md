# Extractive-summarization-using-K-means
Selecting key phrases from the entire text is referred to as extractive summarization.

To extract specific sentences from the original text, the clustering (K-means) technique is employed.

![image](https://github.com/Hemasundher/Extractive-summarization-using-K-means/assets/89529752/5963a5ad-6b72-4e0a-881c-e1ea9f7e8ced)

* Split the text into sentences using the Spacy module.
* Generate a sentence vector for each sentence using the SBERT model.
* The sentence vectors are of shape (768,), making them high-dimensional.
* Utilize the UMAP algorithm to reduce the dimensionality.
* Apply k-means clustering to the dimension-reduced vectors.
* Experiment with different values of k within a range(5-10) and assess them using silhouette scores.
* **Cluster centers are not the data points themselves, so the point closest to each cluster center is selected as the representative point for that cluster.**
* Once the optimal k value and k-means model are obtained, select one sentence from each cluster to represent that cluster.
