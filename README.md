# Disney-Plus-Porject

Downlad link : [Paper](https://github.com/Yeni-Hwang/DisneyPlus_Project/raw/main/Paper_OTT(Over-the-top)%20Content%20Textual%20Clustering%20and%20Dissimilarity%20.pdf) (English)

## Revisiting Genre Classification Through NLP: Topic Modeling and Dissimilarity Measurement with Textual Data

A noticeable consumer behavior in this industry is that many OTT platform users multihome, which means that they use multiple OTT platforms simultaneously. In the United States for example, a survey from Reelgood revealed that Netflix had the most subscribers and that the vast majority of users were multi-homing (Stoll). Multi-homing behavior was consistent in other OTT service platforms such as Disney Plus, Hulu, Amazon Prime, HBO Max, etc. Such statistics show that users are in demand of filling in the gaps between the range of content that different platforms provide. This is an opportunity for platforms to appeal to users by promoting the variety of content they provide. However, there is no uniform measure of the level of variety in the OTT service industry. 

In this paper, we utilize topic modeling, an NLP method, with Disney Plus film data and incorporate textual data of the films, such as plot, title, and genre to create a new classification of films. Using the created topics, we aim to quantify the level of variety of films in Disney Plus and compare them with Hulu.

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

The graph compares topic proportion of each films. '10 Things I Hate About You' and 'Stargirl' are conventionally classified in same genre, however, Topic modeling noticed a difference and distinguished them. Both of them are teen, romantic, comedy-drama but mysterious and fantasy stroy lines are added in 'Stargirl'. 

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
Comparing 3,700 words data from disney plus's and Hulu shows all title, plot and genre, It is interesting that Hulu tends to have higher distances between clusters. It indicates that the contents data extracted from title, plot, and genre has more diversity than Disney Plus does. 

## Conclusion
### Business Impact and conclusion
By applying topic modeling to the corpus of Disney Plus film data containing textual information, we were able to extract latent topics and see the distribution of words within topics as well as the distribution of topics within documents. Incorporating such text-mined information into classifying films is a more advanced and micro-level approach. Much more detailed and descriptive information about films is required  in order to have an in-depth understanding of the films. This is a fundamental knowledge to run any business. Moreover, results of our analysis can be utilized in many areas of business such as product management, product development, marketing, and brand analysis, which all are essential aspects of strategic management.

On the other hand, the dissimilarity measure based on heights score of hierarchical clustering takes into account the latent and dimensional information of the film’s content. In addition, establishing the dissimilarity measure allows for a comparison across different OTT platforms, which was not possible before. In this paper, we compared the dissimilarity measures of Disney Plus and Hulu and identified that Hulu has more variety in its film offerings. 
