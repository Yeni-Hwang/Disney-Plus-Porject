# Disney-Plus-Project

Downlad link : [Paper](https://github.com/Yeni-Hwang/DisneyPlus_Project/raw/main/Paper_OTT(Over-the-top)%20Content%20Textual%20Clustering%20and%20Dissimilarity%20.pdf) (English)

## Revisiting Genre Classification Through NLP: Topic Modeling and Dissimilarity Measurement with Textual Data

A noticeable consumer behavior in this industry is that many OTT streaming platform users multihome, which means that they are subscribing to mutiples streaming services. Multi-homing behavior is consistent in OTT service platforms such as Netflix, Disney Plus, Hulu, Amazon Prime, HBO Max, etc. Such trend shows that users are in demand of filling in the gaps between the range of contents that different platforms provide. This is an opportunity for platforms to appeal to users by promoting the variety of content they provide. However, there is no uniform measure that tracks the level of variety in the OTT service industry. 

In this paper, we utilize topic modeling with Disney Plus film data and incorporate textual data of the films, such as plot, title, and genre to create a new classification of the films. Using the created topics, we aim to quantify the level of variety of films on Disney Plus and compare it with that of Hulu.

- LDA topic modeling
- K means Clustering
- Hierarchical Clustering

Raw data from https://www.kaggle.com/unanimad/disney-plus-shows

## Application
### 1) Generate Topics through LDA topic modeling
The model generated five topics based on textual data : Title, Plot and Genre

![image](https://user-images.githubusercontent.com/78137937/152575073-d1b65e31-6440-4516-bdc3-578af6a53515.png)

### 2) K means clustering and Analytic

### Result example: 
| **Title** | **Genre** | **Cluster** |
|:--------:|:--------:|:--------:|
| 10 Things I Hate About You | Comedy, Drama, Romance | 3 |
| Stargirl | Comedy, Drama, Romance | 1 | 


![image](https://user-images.githubusercontent.com/78137937/152579001-9f7cc45a-98a0-4812-8c74-bca2a734fb45.png)

The graph compares topic proportion of each films. '10 Things I Hate About You' and 'Stargirl' are conventionally classified in the same genre -Comedy, Drama, Romance. However, Topic modeling noticed a difference and distinguished them. Both of them are teen-romantic, but Stargirl has mysterious and fantasy stroy lines. In addition, music played a crucial role in providing narratives in Stargirl. Interestingly, according to wordcloud at step 1, topic 4 demonstartes these characters quite well.

### 3) Hierarchical clustering and compare dissimilarity: Disney Plus VS Hulu

#### Hulu Dendogram

![image](https://user-images.githubusercontent.com/78137937/152580732-db20d78e-7e1a-4dc0-854c-6436af45c129.png)

#### Dinsey Dendogram

![image](https://user-images.githubusercontent.com/78137937/152581201-e564d24d-1034-4f83-8ec6-a62e0e84abf6.png)

The below graph shows the maximum heights scores on each number of clusters which indicates dissimilarities.

| **Number of clusters** | **Disney** | **Hulu** |
|:--------:|:--------:|:--------:|
2 |	1.3589344	|1.3903432
3 |	1.3560568	|1.3871417
4 |	1.3523074	|1.3813330
5 |	1.3483776	|1.3746192
6 |	0.8610793	|0.5345073

#### Results:
Hulu tends to have higher distances between clusters. This indicates that the textual data extracted from title, plot, and genre of Hulu's contents is more diverse than data from Disney Plus. 

## Conclusion
### Business Impact and conclusion
By applying topic modeling to the corpus of Disney Plus film data containing textual information, we were able to extract latent topics and see the distribution of words within each topic, as well as the distribution of topics within documents. 

Incorporating such text-mined information into classifying films is a more advanced and micro-level approach. Much more detailed and descriptive information about films is required  in order to have an in-depth understanding of them. This is a fundamental knowledge to run any business. Moreover, results of our analysis can be utilized in essential aspects of strategic management, such as product management, product development, marketing, and brand analysis.

On the other hand, the dissimilarity measure based on heights score of hierarchical clustering takes into account the latent and dimensional information of the film’s content. In addition, establishing the dissimilarity measure allows for a comparison across different OTT platforms, which was not possible before. In this paper, we compared the dissimilarity measures of Disney Plus and Hulu and identified that Hulu has more variety in its films. 
