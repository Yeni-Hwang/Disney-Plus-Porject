# Disney-Plus-Porject

Downlad link

## Revisiting Genre Classification Through NLP: Topic Modeling and Dissimilarity Measurement with Textual Data

A noticeable consumer behavior in this industry is that many OTT platform users multihome, which means that they use multiple OTT platforms simultaneously. In the United States for example, a survey from Reelgood revealed that Netflix had the most subscribers and that the vast majority of users were multi-homing (Stoll). Multi-homing behavior was consistent in other OTT service platforms such as Disney Plus, Hulu, Amazon Prime, HBO Max, etc. Such statistics show that users are in demand of filling in the gaps between the range of content that different platforms provide. This is an opportunity for platforms to appeal to users by promoting the variety of content they provide. However, there is no uniform measure of the level of variety in the OTT service industry. 

In this paper, we utilize topic modeling, an NLP method, with Disney Plus film data and incorporate textual data of the films, such as plot, title, and genre to create a new classification of films. Using the created topics, we aim to quantify the level of variety of films in Disney Plus and compare them with Hulu.

- LDA topic modeling
- K means Clustering
- Hierarchical Clustering

Raw data from https://www.kaggle.com/unanimad/disney-plus-shows


## Application
### 1) Generate Topics through LDA topic modeling
The model generated five topics based on textual data : title, plot, genre
![image](https://user-images.githubusercontent.com/78137937/152575073-d1b65e31-6440-4516-bdc3-578af6a53515.png)

### 2) K means clustering and Analytic

#### Result example: 
| **Title** | **Genre** | **Cluster** |
|:--------:|:--------:|:--------:|
| 10 Things I Hate About You | Comedy, Drama, Romance | 3 |
| Stargirl | Comedy, Drama, Romance | 1 | 

#### Comparison of topic proportion
![image](https://user-images.githubusercontent.com/78137937/152579001-9f7cc45a-98a0-4812-8c74-bca2a734fb45.png)

### 3) Hierarchical clustering and compare dissimilarity
#### : Disney Plus VS Hulu

#### Hulu Dendogram
![image](https://user-images.githubusercontent.com/78137937/152580732-db20d78e-7e1a-4dc0-854c-6436af45c129.png)

#### Dinsey Dendogram
![image](https://user-images.githubusercontent.com/78137937/152581201-e564d24d-1034-4f83-8ec6-a62e0e84abf6.png)

| **Number of clusters** | **Disney** | **Hulu** |
|:--------:|:--------:|:--------:|
2 |	1.3589344	|1.3903432
3 |	1.3560568	|1.3871417
4 |	1.3523074	|1.3813330
5 |	1.3483776	|1.3746192
6 |	0.8610793	|0.5345073

#### Results:
Comparing 3,700 words data from disney plus's and Hulu shows all title, plot and genre, It is interesting that Hulu tends to have higher distances between clusters. It indicates that the contents data extracted from title, plot, and genre has more diversity than Disney Plus does. 
