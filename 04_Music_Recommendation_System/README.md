# Music Recommendation System

**Course**: CS5079 – Applied Artificial Intelligence, University of Aberdeen (2025)

---

## 📋 Overview

This project develops a content-based music recommendation system using similarity metrics and feature engineering. The system analyzes user listening patterns and song characteristics to generate personalized recommendations, demonstrating core machine learning techniques for recommendation engines.

**Real-World Applications:**
- **Personalization Systems**: Content discovery and user engagement
- **E-commerce**: Product recommendation engines
- **Streaming Platforms**: Music, video, and content suggestions
- **Marketing**: Targeted content delivery
- **Data Analysis**: Pattern discovery in user behavior

---

## 🎯 Objectives

1. Build content-based recommendation system using song features
2. Perform comprehensive exploratory data analysis (EDA)
3. Engineer features from user-song interaction data
4. Implement similarity-based recommendation algorithms
5. Evaluate recommendation quality and diversity

---

## 📊 Dataset

**Source**: Music listening dataset with user-song interactions  
**Size**: 102,627 listening records  
**Features**: User ID, Song ID, Play Count, Title, Release, Artist, Year

**Key Statistics:**
- **Users**: Multiple users with varying listening patterns
- **Songs**: Diverse catalog across artists and years
- **Interactions**: Play count as implicit feedback signal
- **Temporal**: Release year for temporal analysis

**Note**: Dataset is from academic coursework and not included in this repository.

---

## 🔧 Technical Approach

### Exploratory Data Analysis

**Data Quality:**
- Missing value analysis
- Duplicate detection and handling
- Distribution analysis of play counts
- Temporal trends in music consumption

**Key Insights:**
- Most listened songs identification
- Popular artists ranking
- User listening behavior patterns
- Song count distribution across users
- Year-wise music trends

### Feature Engineering

**User Features:**
- Total play count per user
- Unique songs per user
- Artist diversity metrics
- Temporal listening patterns

**Song Features:**
- Popularity metrics (total plays)
- Artist popularity
- Release year encoding
- Genre indicators (if available)

### Recommendation Algorithm

**Approach**: Content-Based Filtering

1. **Feature Representation**: Create feature vectors for songs
2. **Similarity Computation**: Calculate cosine similarity between songs
3. **Recommendation Generation**: Find k-most similar songs
4. **Ranking**: Order by similarity score and popularity

**Similarity Metrics:**
- Cosine Similarity: Measures angle between feature vectors
- Weighted by user preferences and play counts

---

## 📈 Key Results

### System Performance

**Recommendation Quality:**
- Generated diverse recommendations based on song features
- Balanced popularity and similarity in rankings
- Captured user preferences from listening history

**Insights:**

1. **Popular artists** dominate listening patterns but niche preferences exist
2. **Play count distribution** is highly skewed (power law)
3. **Temporal trends** show evolution of music preferences
4. **Feature engineering** significantly impacts recommendation quality

### Visualizations

- Play count distributions (histograms, box plots)
- Top songs and artists (bar charts)
- User behavior patterns (scatter plots)
- Correlation heatmaps for features
- Recommendation diversity analysis

---

## 🛠️ Technologies Used

**Core Libraries:**
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Scikit-learn**: Cosine similarity, preprocessing
- **Matplotlib/Seaborn**: Data visualization
- **PCA**: Dimensionality reduction for visualization

**Key Techniques:**
- Content-Based Filtering
- Cosine Similarity
- Feature Engineering
- Exploratory Data Analysis
- Statistical Analysis

---

## 📁 Project Structure

```
04_Music_Recommendation_System/
├── README.md
├── recommendation_system.ipynb    # Complete implementation
├── requirements.txt               # Python dependencies
└── images/                        # Visualizations and results
```

---

## 💡 Key Takeaways

### Machine Learning Concepts

1. **Content-based filtering** works well when item features are available
2. **Similarity metrics** (cosine similarity) effectively capture feature relationships
3. **Feature engineering** is crucial for recommendation quality
4. **Exploratory analysis** reveals patterns that inform algorithm design
5. **Implicit feedback** (play counts) provides valuable preference signals

### System Design

1. **Scalability**: Similarity computation can be pre-computed and cached
2. **Cold Start**: Content-based approach handles new songs with features
3. **Diversity**: Balance between similar and diverse recommendations
4. **Evaluation**: Metrics beyond accuracy (diversity, novelty, serendipity)

---

## 🔮 Future Enhancements

### Algorithm Improvements

- **Collaborative Filtering**: Leverage user-user or item-item similarities
- **Hybrid Systems**: Combine content-based and collaborative approaches
- **Matrix Factorization**: Latent factor models (SVD, NMF)
- **Deep Learning**: Neural collaborative filtering, autoencoders

### Feature Engineering

- **Audio Features**: Tempo, key, energy, danceability (from Spotify API)
- **Lyrics Analysis**: NLP features from song lyrics
- **Genre Classification**: Multi-label genre prediction
- **Temporal Dynamics**: Time-aware recommendations

### Production Deployment

- **Real-Time System**: Streaming recommendation updates
- **A/B Testing**: Compare recommendation strategies
- **Personalization**: User-specific recommendation tuning
- **Scalability**: Distributed similarity computation (Spark, Dask)

### Evaluation Metrics

- **Precision@K**: Accuracy of top-K recommendations
- **Recall@K**: Coverage of user preferences
- **Diversity**: Variety in recommended items
- **Novelty**: Recommending less-known items
- **Serendipity**: Surprising but relevant recommendations

---

## 🌍 Industry Applications

This project demonstrates skills applicable to:

✅ **Recommendation Systems**: Core ML application across industries  
✅ **Feature Engineering**: Creating meaningful representations from raw data  
✅ **Similarity Metrics**: Foundation for many ML algorithms  
✅ **Data Analysis**: Extracting insights from user behavior data  
✅ **Scalable Design**: Considerations for production systems

---

## 📚 References

- Ricci, F., et al. (2011). Recommender Systems Handbook
- Aggarwal, C. C. (2016). Recommender Systems: The Textbook
- Koren, Y., et al. (2009). Matrix Factorization Techniques for Recommender Systems

---

## 📝 Academic Context

This project was completed as part of CS5079 (Applied Artificial Intelligence) coursework at the University of Aberdeen, demonstrating practical implementation of recommendation algorithms and data analysis techniques.

---

[← Back to Portfolio](../README.md)
