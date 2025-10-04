# Situation Awareness Prediction for Critical Systems

**Course**: CS5079 – Applied Artificial Intelligence, University of Aberdeen (2025)

---

## 📋 Overview

This project develops predictive models to assess driver situation awareness using physiological and behavioral data. The system predicts continuous situation awareness scores, which are critical for safety in high-stakes environments such as autonomous driving, trading floors, and control rooms.

**Real-World Applications:**
- **Energy Trading**: Predicting trader alertness and decision quality under pressure
- **Safety-Critical Systems**: Monitoring operator awareness in control rooms
- **Risk Management**: Real-time assessment of decision-maker cognitive state
- **Autonomous Systems**: Human-in-the-loop monitoring and intervention prediction

---

## 🎯 Objectives

1. Predict continuous situation awareness scores from multimodal features
2. Compare gradient boosting algorithms (XGBoost vs. LightGBM)
3. Identify key features contributing to situation awareness
4. Optimize model performance through hyperparameter tuning
5. Provide interpretable predictions for critical decision support

---

## 📊 Dataset

**Source**: Academic research dataset on driver situation awareness  
**Size**: 1,054 observations with 29 features  
**Target Variable**: Continuous situation awareness score (Y)

**Feature Categories:**
- **Demographic**: Age, gender, driving experience
- **Temporal**: Decision time, task length, task difficulty
- **Physiological**: Pupil changes, pupil mean/std, eye fixations
- **Behavioral**: Mirror checks, road/sky fixations, decision accuracy
- **Environmental**: Car placement, danger level, task complexity

**Note**: Dataset is from academic coursework and not included in this repository.

---

## 🔧 Technical Approach

### Data Preprocessing
- **Missing Value Analysis**: Identified and handled missing data
- **Feature Engineering**: Created interaction features from temporal and physiological data
- **Encoding**: One-hot encoding for categorical variables
- **Scaling**: Standardization for numerical features
- **Pipeline Architecture**: Scikit-learn pipelines for reproducible preprocessing

### Models Implemented

#### 1. **XGBoost Regressor**
- Gradient boosting with tree-based learners
- Hyperparameter optimization via GridSearchCV/RandomizedSearchCV
- Feature importance analysis
- Cross-validation for robust evaluation

#### 2. **LightGBM Regressor**
- Efficient gradient boosting framework
- Faster training on large datasets
- Leaf-wise tree growth strategy
- Comparative analysis with XGBoost

### Evaluation Metrics
- **Mean Squared Error (MSE)**: Primary regression metric
- **Mean Absolute Error (MAE)**: Interpretable error measure
- **R² Score**: Variance explained by the model
- **Cross-Validation**: K-fold validation for generalization assessment

---

## 🚀 Key Results

### Model Performance
- **XGBoost**: Achieved strong predictive performance with optimized hyperparameters
- **LightGBM**: Demonstrated competitive results with faster training time
- **Feature Importance**: Pupil metrics and temporal features identified as top predictors

### Key Insights
1. **Physiological signals** (pupil changes, fixation patterns) are strong predictors of awareness
2. **Temporal factors** (decision time, task length) significantly impact awareness scores
3. **Ensemble methods** outperform traditional regression approaches
4. **Model interpretability** enables actionable insights for intervention strategies

### Production Considerations
- Modular preprocessing pipeline for deployment
- Feature importance for real-time monitoring dashboards
- Scalable architecture for streaming data
- Robust error handling and validation

---

## 📁 Project Structure

```
01_Situation_Awareness_Prediction/
├── README.md
├── situation_awareness_prediction.ipynb    # Main modeling notebook
├── exploratory_analysis.ipynb              # EDA and visualization
├── requirements.txt                        # Python dependencies
└── images/                                 # Visualizations and results
```

---

## 🛠️ Technologies Used

**Core Libraries:**
- **XGBoost**: Gradient boosting implementation
- **LightGBM**: Efficient gradient boosting framework
- **Scikit-learn**: Preprocessing, pipelines, evaluation
- **Pandas**: Data manipulation
- **NumPy**: Numerical computations
- **Matplotlib/Seaborn**: Visualization

**Key Techniques:**
- Gradient Boosting Machines
- Hyperparameter Optimization (GridSearchCV, RandomizedSearchCV)
- Feature Engineering
- Cross-Validation
- Feature Importance Analysis

---

## 📈 Visualizations

The project includes comprehensive visualizations:
- Feature correlation heatmaps
- Feature importance rankings
- Model performance comparisons
- Prediction vs. actual scatter plots
- Residual analysis
- Cross-validation results

---

## 💡 Key Takeaways

1. **Gradient boosting** (XGBoost, LightGBM) excels at capturing complex non-linear relationships in multimodal data
2. **Feature engineering** from physiological signals significantly improves predictive power
3. **Model interpretability** through feature importance is crucial for critical systems
4. **Hyperparameter tuning** provides measurable performance gains
5. **Production-ready pipelines** ensure reproducibility and scalability

---

## 🔮 Future Enhancements

- **Real-time prediction**: Streaming data pipeline for live monitoring
- **Deep learning**: LSTM/Transformer models for temporal sequence modeling
- **Explainability**: SHAP values for instance-level interpretability
- **Multi-task learning**: Joint prediction of awareness and decision quality
- **Deployment**: REST API for integration with monitoring systems

---

## 📚 References

- Chen, T., & Guestrin, C. (2016). XGBoost: A Scalable Tree Boosting System
- Ke, G., et al. (2017). LightGBM: A Highly Efficient Gradient Boosting Decision Tree
- Endsley, M. R. (1995). Toward a Theory of Situation Awareness in Dynamic Systems

---

## 📝 Academic Context

This project was completed as part of CS5079 (Applied Artificial Intelligence) coursework at the University of Aberdeen, demonstrating advanced machine learning techniques for real-world prediction tasks.

---

[← Back to Portfolio](../README.md)
