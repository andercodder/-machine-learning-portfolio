# EV Battery Health Prediction

**Course**: CS5062 – Machine Learning, University of Aberdeen (2025)

---

## 📋 Overview

This project develops predictive models for electric vehicle (EV) battery status classification, comparing traditional machine learning with deep learning approaches. The system predicts battery health status from vehicle operational data, critical for energy management and predictive maintenance in electric vehicle fleets.

**Real-World Applications:**
- **Energy Management**: Optimizing charging schedules and grid integration
- **Fleet Operations**: Predictive maintenance for EV fleets
- **Battery Storage**: Forecasting battery degradation for energy storage systems
- **Smart Grids**: Demand prediction and load balancing
- **Trading & Optimization**: Energy trading strategies based on battery status forecasts

---

## 🎯 Objectives

1. Predict binary battery status (charging/discharging) from vehicle speed data
2. Compare traditional ML (KNN) vs. deep learning (RNN) approaches
3. Handle imbalanced class distribution effectively
4. Develop time-series aware models for sequential data
5. Evaluate model performance with comprehensive metrics

---

## 📊 Dataset

**Source**: Electric vehicle operational data  
**Size**: ~60,000+ observations  
**Features**: Trip ID, Vehicle Speed (km/h), Battery Status (binary)

**Characteristics:**
- **Temporal Structure**: Sequential trip data with time dependencies
- **Class Imbalance**: Unequal distribution of charging/discharging states
- **Real-World Noise**: Operational data with natural variability

**Note**: Dataset is from academic coursework and not included in this repository.

---

## 🔧 Technical Approaches

### Approach 1: K-Nearest Neighbors (Baseline)

**Preprocessing:**
- Feature scaling with StandardScaler
- SMOTE (Synthetic Minority Over-sampling Technique) for class imbalance
- Train-test split with stratification

**Model:**
- K-Nearest Neighbors classifier
- Hyperparameter tuning for optimal k value
- Distance-based classification

**Advantages:**
- Simple, interpretable baseline
- No assumptions about data distribution
- Fast inference

### Approach 2: Recurrent Neural Network (Advanced)

**Preprocessing:**
- MinMax scaling for neural network optimization
- Sequence reshaping for RNN input (samples, timesteps, features)
- Class weight computation for imbalanced data

**Architecture:**
- SimpleRNN layer for temporal dependencies
- Dense output layer with sigmoid activation
- Binary cross-entropy loss
- RMSprop optimizer

**Advantages:**
- Captures temporal patterns
- Learns sequential dependencies
- Scalable to multivariate time-series

---

## 📈 Key Results

### Model Comparison

| Metric | KNN (Baseline) | RNN (Time-Series) |
|--------|---------------|-------------------|
| Approach | Traditional ML | Deep Learning |
| Temporal Awareness | ❌ No | ✅ Yes |
| Class Imbalance Handling | SMOTE | Class Weights |
| Training Time | Fast | Moderate |
| Scalability | Limited | High |

### Key Insights

1. **Time-series modeling** (RNN) captures temporal dependencies in battery behavior
2. **Class imbalance** significantly impacts model performance - requires careful handling
3. **Sequential patterns** in vehicle speed provide predictive signals for battery status
4. **Model selection** depends on deployment constraints (speed vs. accuracy)

### Performance Metrics
- **ROC-AUC Score**: Evaluated discrimination capability
- **Confusion Matrix**: Analyzed classification errors
- **Precision/Recall**: Assessed class-specific performance
- **F1-Score**: Balanced metric for imbalanced data

---

## 🛠️ Technologies Used

**Machine Learning:**
- **Scikit-learn**: KNN, preprocessing, metrics
- **Imbalanced-learn**: SMOTE for class imbalance
- **TensorFlow/Keras**: RNN implementation
- **Pandas/NumPy**: Data manipulation

**Key Techniques:**
- K-Nearest Neighbors
- Recurrent Neural Networks (RNN)
- SMOTE (Synthetic Minority Over-sampling)
- Class Weight Balancing
- Time-Series Preprocessing

---

## 📁 Project Structure

```
02_EV_Battery_Health_Prediction/
├── README.md
├── knn_baseline_approach.ipynb      # Traditional ML approach
├── rnn_time_series_approach.ipynb   # Deep learning approach
├── requirements.txt                 # Python dependencies
└── images/                          # Visualizations and results
```

---

## 💡 Key Takeaways

### Technical Lessons
1. **Baseline models** (KNN) provide quick insights and performance benchmarks
2. **Deep learning** (RNN) excels when temporal dependencies are important
3. **Class imbalance** requires domain-specific handling strategies
4. **Feature engineering** from time-series data improves both approaches

### Production Considerations
1. **Model selection**: Balance accuracy vs. computational cost
2. **Real-time inference**: KNN for speed, RNN for accuracy
3. **Monitoring**: Track model performance on streaming data
4. **Scalability**: RNN architecture scales to multivariate inputs

---

## 🔮 Future Enhancements

### Model Improvements
- **LSTM/GRU**: More sophisticated RNN architectures
- **Attention Mechanisms**: Focus on relevant time steps
- **Ensemble Methods**: Combine multiple models
- **Feature Engineering**: Add temperature, charging rate, battery age

### Deployment
- **Real-time Pipeline**: Streaming data processing
- **Model Serving**: REST API for predictions
- **Monitoring Dashboard**: Live performance tracking
- **A/B Testing**: Compare model versions in production

### Advanced Applications
- **Remaining Useful Life (RUL)**: Predict battery degradation timeline
- **Anomaly Detection**: Identify unusual battery behavior
- **Multi-step Forecasting**: Predict future battery states
- **Transfer Learning**: Adapt models to different EV models

---

## 🌍 Energy Sector Relevance

This project demonstrates key skills for energy sector applications:

✅ **Time-Series Forecasting**: Critical for energy demand prediction  
✅ **Imbalanced Data**: Common in anomaly detection and fault prediction  
✅ **Model Comparison**: Baseline vs. advanced techniques  
✅ **Production Mindset**: Scalability and deployment considerations  
✅ **Domain Application**: Direct relevance to EV infrastructure and smart grids

---

## 📚 References

- Goodfellow, I., et al. (2016). Deep Learning. MIT Press
- Chawla, N. V., et al. (2002). SMOTE: Synthetic Minority Over-sampling Technique
- Lipu, M. S. H., et al. (2018). A review of state of health and remaining useful life estimation methods for lithium-ion battery

---

## 📝 Academic Context

This project was completed as part of CS5062 (Machine Learning) coursework at the University of Aberdeen, demonstrating both traditional and deep learning approaches to time-series classification.

---

[← Back to Portfolio](../README.md)
