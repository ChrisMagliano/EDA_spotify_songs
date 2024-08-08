# Most streamed Spotify songs Analysis

## Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning & Preparation](#data-cleaning-and-preparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Results and findings](#results-and-findings)
- [Recommendations and Insights](#recommendations-and-insights)
- [Limitations](#limitations)
- [References](#references)
 

### Project Overview
In this project I have performed a complete Data Exploration of the most streamed Spotify songs up to 2024. By analyzing several metrics of Spotify tracks, I aim at identifying trends, records and gain a deeper understanding of the music market's logic.

### Data Sources
The dataset used in this project "Spotify_Refined_Explicity_classifed.csv" was retrieved on [Kaggle](https://www.kaggle.com/datasets/pragyantiwari/spotify-refined-explicity-classified-1). It contains 4600 different tracks and a total of 30 columns that provide with important information per each track, e.g. the release date, the artist, the track score, number of streams etc.

### Tools
The whole data preprocessing and visualization has been performed by means of [Python](https://www.python.org/downloads/) programming language and [Jupyter Notebook](https://jupyter.org/install) platform. It is accessible throughout the "Most Streamed Spotify Songs 2024.ipynb" file.

### Data Cleaning and Preparation
The first step of this project regards the data loading and preprocessing. I performed the following taks:
1. **Data loading and inspection**;
2. **Handling missing values**;
3. **Data cleaning** (drop useless columns and duplicated) and **formatting**.

### Exploratory Data Analysis
Exploratory Data Analysis (EDA) process consists of exploring the dataset to answer key questions, such as:
- How has the number of released tracks changed over the years?
- Does a preferred release month exist?
- What are the most streamed songs and artists on Spotify? What about YouTube and TikTok?
- Do explicit songs have higher "track score" with respect to friendly ones?
- What are the main factors that affect the *track score* ?

## Results and findings
Firstly, I investigated how the number of released songs has changed over the years till 2023 since at the moment of analysis 2024 is not finished yet.
![num_tracks_year](https://github.com/user-attachments/assets/c0a73bac-ff4a-4433-b2aa-a993b99637d5)
We notice an exponential growth of the number of songs released from 2015. Moreover, while during 2015-2020 nearly 50 songs per year were released, in the last three years 2021-2023, the release rate nearly reaches 400 songs per year. The growing number of released songs each year can be attributed to several factors. The rise of digital platforms and streaming services has made it easier for artists to distribute their music globally without the need for traditional record labels. Advances in technology have lowered the cost and complexity of music production, allowing more independent artists to create and release their work. Additionally, the increasing demand for diverse and niche music genres has encouraged more frequent releases to satisfy varied audience preferences.

The plot below shows the number of tracks per months till 2023. 
![months](https://github.com/user-attachments/assets/b325e110-08f2-47c6-98b9-e5ae585100b9)
It evidences that January is the preferred release month by the artists with 431 songs (9.3% from total), followed by October with 384 songs (8.3% from total). On the contrary, April turns out to be the least preferred with 257 tracks (5.5% from total) alongside with February with 267 tracks (5.8%).

- **January** follows the holiday season, a period when fewer new releases are scheduled due to the focus on holiday music and end-of-year festivities. Being the first month of the year, people and media are looking for innovation. Thus, January becomes a strategic time to release new material when competition is lower, and audiences are looking for new content.
- **October** is strategically important for releasing new music ahead of the holiday season. This timing allows albums and singles to gain traction and popularity in time for holiday gift-giving.
- After the flurry of releases in November and December, followed by the New Year releases in January, **February** can experience a lull as the industry catches its breath. Moreover, with fewer days in February, there might be a slight impact on the number of releases simply due to the shorter timeframe.
- **April** might be seen as a transitional period, with some artists and labels holding off releases until late spring or early summer when people are preparing for summer activities and vacations.

I here stress that these are only possible explanations of the found results. However the music industry often follows specific marketing cycles, and these cycles can influence the timing of releases. In some markets, the eligibility periods for music awards can influence release dates. Artists might align their release schedules with touring and festival seasons. Certain months are influenced by cultural events and holidays, which can either encourage or discourage new releases. All these factors contribute to prevent the consolidation of a dominant release month over the others. In fact, despite January being the top month for song releases, its percentage difference with respect to April (the worst month) corresponds to 3.8%.

I examined which are the most streamed songs and artists on the three major platforms (Spotify, YouTube and TikTok).
![most_streamed_tracks](https://github.com/user-attachments/assets/d767cfe0-08c2-49f9-ac65-283d48d545f1)
**Blinding Lights** (*The Weekend*) is the most streamed song on Spotify with more than 8 billions streams, immediately followed by **Shape of You** (*Ed Sheeran*) with little less than 8 billions streams. **Baby Shark**, instead, results to be the most streamed on YouTube with more than 17 billions of views, almost doubling **Despacito** (*Luis Fonsi*) at the second position with nearly 9 billions of views. We also notice that the third position is occupied by Shape of You that reaches almost 8 billions visualizations. The most streamed song on TikTok, and the most streamed overall, is **Monkeys Spinning Monkeys** (*Kevin MacLeod*) which has achieved more than 250 billions of streams! This result indicates that TikTok is nowadays the most used platform to stream video and songs. It is important to highlight that Monkeys Spinning Monkeys is a soundtrack which fits very well with the most viral videos on TikTok. In fact it has only a few millions views on YouTube and nearly 10 millions streams on Spotify (ten thousands times less than TikTok streams!). A similar argument could be made for **Love You So** (*The King Khan & BBQ Show*) that outperformed TikTok ranks with more than 200 billions of streams but a few ten millions on the other two platforms.

The most streamed artist on Spotify is Bad Bunny together with The Weekend with more than 35 billions ratings. Immediately after there is Drake with more than 30 billions streams. Regarding YouTube, the most rated artist is Ed Sheeran with more than 25 billions of listenings, followed by Bad Bunny. Taylor Swift, instead, is the third most streamed artits on YouTube reaching 20 billions plays. As already discussed for the track, also the most streamed artists on TikTok are not the most popular on the other two platforms. In fact, Kevin MacLeod and The King Khan & BBQ Show occupy the first and the second rank in this ranking thanks to their extremely viral soundtracks.
![most_streamed_artists](https://github.com/user-attachments/assets/4f5a18b0-803f-4bec-a0d9-71342bc74eab)

![artists_tracks](https://github.com/user-attachments/assets/5f18f2f7-0aba-4894-8890-6ec2c14fd76f)


The dataset under exam also provides information whether the track contains or not curse words or language deemed sexual, violent, or offensive in general. In particular each track has been classified according to a binary classification: explicit or friendly. As shown in figure below, the sample is highly unbalanced towards friendly tracks (76%) against the explicit content songs (24%).
![class_pie](https://github.com/user-attachments/assets/11168980-6044-44e3-a591-172c237c1eed)

However, no statistical significant difference arose between the mean track score of the two classes.
![track_score_class](https://github.com/user-attachments/assets/05e5596b-5183-4a95-9eee-92c2ffa262c5)


In addition, I also investigated how the number of explicit and friendly songs changed during the years. What we learn from the figure below is that, while friendly songs experienced an approximately constant growth from early 2000s, the same does not stand for explicit tracks. In fact, after the initial growth in the early 2000s, from 2002 to 2006 explicit songs underwent a rapid decrease. Possible factors might be attributed to the sudden decrease in explicit tracks from 2002 to 2006. For example, in the early 2000s, particularly after the 2004 Super Bowl halftime show controversy, the Federal Communications Commission in the United States increased its scrutiny and fines for indecent content on public airwaves. This led to a more cautious approach by record labels and artists regarding explicit content to avoid potential fines and censorship. Moreover, these years saw a surge in pop music’s popularity, which generally leans towards more radio-friendly and less explicit content. Artists like Britney Spears, NSYNC, and Christina Aguilera dominated the charts with music that was more commercially viable and less explicit. Eventually, after the 2001 recession and the impacts of events like 9/11, there might have been a shift towards more conservative content as the nation focused on healing and unity, influencing the type of music that was produced and promoted. From the mid-2000s onwards, hip-hop and rap genres, which often contain more explicit content, became increasingly mainstream. Artists like Kanye West, Jay-Z, and later on, artists like Drake and Kendrick Lamar, gained massive popularity, bringing explicit content back into the forefront of popular music. As societal norms evolved, there was a greater acceptance and normalization of explicit content in media, including music. This shift allowed artists more freedom to express themselves without facing the same level of backlash as in the early 2000s. The rise of digital music platforms provided artists with new distribution channels that were less regulated compared to traditional radio and TV. These platforms allowed for greater artistic freedom, including the release of explicit content without fear of censorship. Streaming services use algorithms to recommend music to users based on their listening habits, which can sometimes favor more provocative or explicit content that generates engagement and streams.
![expl_friend_years](https://github.com/user-attachments/assets/51ff3985-04ee-4b19-95ff-4cff39c4a10f)

Eventually, I concluded this project by analyzing possible correlations between the variables available per each track by means of the correlation heatmap. This plot shows the Spearman rank between two features per each track. I chose the Spearman coefficient rather than the Pearson’s one because not all the variables were normally distributed. The Spearman coefficient is a float number comprised between -1 and +1 and expresses the monotonic relationship between the two variables (negative if -1, positive if +1 and null if 0). Of particular interest is to understand what are the most important (statistically speaking) factors that correlate with the Track Score. Looking at the first row of the correlation matrix we see that there is not a dominant feature monotonically correlated with the track score, but a weak dependence on Spotify Playlist Reach and Spotify Popularity. This is in line with what expected since the most liked songs are also those more popular. It is interesting to note the high values of the Spearman coefficient for the three sub-matrices:

- 4x4 sub-matrix formed by Spotify Streams, Spotify Playlist Count, Spotify Plalyst Reach and Spotify Popularity;
- 2x2 sub-matrix formed by YouTube Views and YouTube Likes;
- 3x3 sub-matrix formed by TikTok Posts, TikTok Likes and TikTok Views.
These three matrices stress how the algorithm behind the three platforms works: likes and views are highly correlated in a vicious cycle where the former’s growth leads the latter’s increase and viceversa.
![df_corr](https://github.com/user-attachments/assets/f59aab19-1845-4a46-8ec4-b1e020a8832a)
Another important result we retrieve from the heatmap chart is that the number of Spotify streams is quite strongly positive correlated with the number of Shazam counts. Thus, if people use Shazam to find the name of an unknown song then it is probably they will listen it again on Spotify. Moreover Spotify streams are negatively correlated with the release year thus suggesting the most streamed songs are also the newest one.

## Recommendations and Insights
- Nowadays the music market is more accessible due to the existence of many technologies and platforms that allow users to communicate with public. This leads to an exponential growth of the number of tracks released every year;
- There is not a clear and inequivocable ideal month to release a new track. However months like January and October seem to be slightly preferred;
- The top 3 streamed songs on Spotify are: **Blinding Lights, Shape of You** and **As It Was**. The top 3 viewed songs on YouTube are: **Baby Shark, Despacito** and **Shape of You**. Thus, *Shape of You* is the only song that is contained in both top 3 ranks. TikTok most reproduced songs are typically soundtracks that well fit with viral videos. The top 3 listened artists on Spotify are: **Bad Bunny, The Weekend** and **Drake**. The top 3 listened artists on YouTube are: **Ed Sheeran, Bad Bunny** and **Taylor Swift**. Finally, the top 3 listened artists on TikTok are **Kevin MacLeod, The King Khan & BBQ Show** and **Kreepa**;
- There is not a statistical significant difference in *Track Score* between explicit and friendly songs;
- The *Track Score* is a complex feature that poorly correlates with all the factors taken into account. However it is slightly positive correlated with the `Spotify Playlist Reach` and the `Spotify Popularity`.

## Limitations
1. The dataset used in this project does not contain all the tracks on Spotify but just the *most streamed ones*. This means that there is a threshold value for the Spotify Streams. In fact, `df['Spotify Streams'].max()` is equale to 1071. Thus we are considering all Spotify track with more than 1071 streams.
2. The datset contains many NaN values, even for columns of interest. We handled these values by replacing them with the median value of each column. We opted to use the median because more robust against the outliers. However, this always constitutes an approximation of the genuine dataset. 


## References
