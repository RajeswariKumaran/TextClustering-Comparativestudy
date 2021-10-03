# TextClustering-Comparativestudy
Compared Spherical KMeans clustering and HDBSCAN clustering - both with and without embeddings

I have always found text clustering very challenging. In my professional experience I have tried many different metrics to find out the quality of cluster and none of them gave a satisfactory output to figure out what are the good clusters vs. bad clusters. The issue was that every document was forced into any one of the clusters and this leads to a lot of bad clusters where unrelated documents are clustered together.

In this project, I used HDBScan on a dataset of 10,000 support tickets and found that the clustering is improved. The tickets which cannot be clustered with the others are not clustered at all giving a label of -1 which makes it easier for us to pick the good clusters. The downside ofcourse is that the count of tickets with label of -1 is very high, but atleast they dont get in the way of good clusters.

I also added BERT embedding to both Spherical KMeans and HDBSCAN and surprisingly found very little impact of embedding on both. It is possibly because the description of the ticket which I used for clustering is already preprocessed and do not have stop words.

Comparison of Spherical KMeans Vs. HDBScan:

![Screenshot 2021-10-03 at 8 20 13 PM](https://user-images.githubusercontent.com/52888997/135759406-9b085333-2bbe-4f80-ae3b-070084b75a9c.png)

Comparison of Spherical KMeans with and without BERT embedding:

![Screenshot 2021-10-03 at 8 33 19 PM](https://user-images.githubusercontent.com/52888997/135759855-9be48511-f18b-463d-9f66-160f5965bb64.png)

Comparison of HDBSCAN with and without BERT embedding:

![Screenshot 2021-10-03 at 9 49 39 PM](https://user-images.githubusercontent.com/52888997/135762672-9df12bdf-9f03-4dab-91b9-8a75d400c4b7.png)

