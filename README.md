# Spotify-Track-Analysis

**Author**: Yoatam Gebremicael

This project analyzes the relationship between song popularity and various musical attributes, such as energy, danceability, and mood, using data from Spotify. The main objective is to answer two key questions regarding Spotify tracks:

- **How does the presence of one or more highly popular songs in an album affect the popularity and listener engagement of other tracks within the same album?**
- **How do the musical attributes of tracks change when artists collaborate compared to when they work solo?**

## Research Questions

### Main Questions:
1. How does the presence of one or more highly popular songs in an album affect the popularity and listener engagement of other tracks within the same album?
2. How do the musical attributes of tracks change when artists collaborate compared to when they work solo?

### Sub-questions:
- Do high-popularity albums show higher listener retention for less popular tracks?
- Do features that make tracks popular, such as high energy or danceability, lead to more interaction with other tracks on the same album that have those qualities?
- Do collaborations cause noticeable changes in musical qualities like tempo, loudness, and energy versus solo tracks?
- Does the popularity of collaborations vary by genre?

## Dataset

- **Dataset Size**: 114,000 tracks across 114 genres.
- **Data Source**: Spotify Web API.
- **Data Cleaning**: Missing values, especially for artist, album name, and track name, were handled. Track duration was converted from milliseconds to minutes.
- **Key Variables**: Popularity, energy, danceability, tempo, loudness, and valence.

## Methods

### 1. Data Cleaning and Transformation:
- Handling missing values.
- Conversion of duration from milliseconds to minutes.
- Setting a popularity threshold (above the 80th percentile) to distinguish highly popular tracks.

### 2. Exploratory Data Analysis (EDA):
- **Box Plots**: Used to compare popularity distributions for albums with and without highly popular tracks. Also used to analyze the difference in musical attributes between solo and collaborative tracks.
- **Scatter Plots**: Examined how the popularity of popular tracks influences other tracks within the same album.
   
### 3. Hypothesis Testing:
- T-tests were conducted to assess whether the presence of highly popular tracks leads to higher popularity for other tracks on the same album and to analyze genre-based differences in solo vs. collaborative tracks.

## Main Results

- **Impact of Highly Popular Tracks on Album Popularity**: Albums containing highly popular tracks have significantly higher overall popularity. The statistical significance was confirmed through a t-test (p-value < 0.0001).
  
- **Musical Qualities of Collaborative vs. Solo Tracks**:
  - Solo tracks tend to be more energetic and faster, with a louder and more upbeat sound.
  - Collaborative tracks, in contrast, tend to have more subtle, acoustic qualities, often with a more relaxed sound.
  
- **Genre-based Differences in Collaborations**:
  - **Blues**: Collaborative tracks are more acoustic and slower.
  - **Disco**: Collaborative tracks are more danceable and upbeat.
  - **Emo**: Collaborative tracks tend to be slightly more energetic, although often slower in tempo.
  - **Jazz**: Collaborative tracks show higher energy and danceability, but are less acoustic than solo tracks.

## Conclusion

The analysis shows that collaborations tend to change the mood and style of music, making it more varied and sometimes more accessible to a wider audience. The influence of collaborations on musical attributes varies significantly across genres, with genres like Jazz and Disco showing notable shifts in energy, tempo, and danceability.

## Limitations

- **Missing Data**: Key attributes like artist gender and release year were not included in the dataset, which could have provided additional insights.
- **Outliers**: Some key attributes such as loudness had minor outliers, but these were retained as their influence on the analysis was negligible.
- **Generalization**: The analysis may not be fully representative of all music genres or collaborations, particularly genres like Classical or Hip-Hop.
- **External Factors**: Social media trends and promotional activities by artists were not considered, which could affect track popularity.

## How to Replicate

### Prerequisites

- Python 3.x
- Necessary Python libraries: `pandas`, `matplotlib`, `seaborn`, `scipy`, `numpy`

### Steps to Run the Analysis

1. Clone this repository.
   ```bash
   git clone https://github.com/yourusername/spotify-track-analysis.git
   cd spotify-track-analysis
