# Portfolio Setup & Deployment Guide

**Author**: Andre de Carvalho  
**Created**: October 2025  
**Purpose**: Guide for finalizing and deploying your ML portfolio

---

## 📁 Current Structure

Your portfolio has been organized into a professional structure:

```
machine-learning-portfolio-clean/
├── README.md                                    # Main portfolio page
├── .gitignore                                   # Git ignore rules
├── SETUP_GUIDE.md                              # This file
│
├── 01_Situation_Awareness_Prediction/
│   ├── README.md                               # Project documentation
│   ├── situation_awareness_prediction.ipynb    # XGBoost/LightGBM model
│   ├── exploratory_analysis.ipynb              # EDA notebook
│   ├── requirements.txt                        # Dependencies
│   └── images/                                 # Visualizations folder
│
├── 02_EV_Battery_Health_Prediction/
│   ├── README.md
│   ├── rnn_time_series_approach.ipynb         # Deep learning approach
│   ├── knn_baseline_approach.ipynb            # Traditional ML baseline
│   ├── requirements.txt
│   └── images/
│
├── 03_Reinforcement_Learning_Optimization/
│   ├── README.md
│   ├── dqn_frozenlake.ipynb                   # DQN implementation
│   ├── requirements.txt
│   └── images/
│
└── 04_Music_Recommendation_System/
    ├── README.md
    ├── recommendation_system.ipynb             # Recommendation engine
    ├── requirements.txt
    └── images/
```

---

## ✅ What's Been Done

### 1. **Professional Structure** ✓
- Clean folder organization
- Descriptive file names
- Consistent naming conventions

### 2. **Comprehensive Documentation** ✓
- Root README with skills showcase
- Project-specific READMEs with:
  - Business context
  - Technical approach
  - Real-world applications
  - Key results
  - Technologies used
  - Future enhancements

### 3. **Dependencies** ✓
- requirements.txt for each project
- Version specifications
- All necessary libraries

### 4. **Git Configuration** ✓
- .gitignore for Python projects
- Excludes data files, checkpoints, cache

---

## 🔧 Next Steps (Manual Cleanup Required)

### Priority 1: Clean Notebooks (Important!)

Each notebook needs these manual edits:

#### **Remove Google Colab Dependencies**

Find and remove/modify these cells:
```python
# REMOVE THESE:
from google.colab import drive
drive.mount('/content/drive')

# CHANGE FILE PATHS FROM:
'/content/drive/MyDrive/...'
# TO:
'./data/filename.csv'  # or '../data/filename.csv'
```

#### **Add Executive Summary Cell**

Add as **first cell** in each notebook:
```markdown
# [Project Title]

**Author**: Andre de Carvalho  
**Course**: [Course Code] - [Course Name]  
**University**: University of Aberdeen (2025)

## Executive Summary

[2-3 sentences about what this notebook does]

**Key Results:**
- [Main finding 1]
- [Main finding 2]
- [Main finding 3]

**Technologies**: [List main libraries used]
```

#### **Add Section Headers**

Ensure notebooks have clear sections:
```markdown
## 1. Data Loading and Exploration
## 2. Data Preprocessing
## 3. Feature Engineering
## 4. Model Training
## 5. Model Evaluation
## 6. Results and Insights
## 7. Conclusions
```

#### **Clean Up Print Statements**

Replace debug prints with meaningful output:
```python
# INSTEAD OF:
print(data.shape)

# USE:
print(f"Dataset shape: {data.shape[0]} rows, {data.shape[1]} columns")
```

---

### Priority 2: Add Visualizations to Images Folders

For each project, save key plots to the `images/` folder:

**Situation Awareness:**
- Feature importance plot
- Model comparison chart
- Correlation heatmap

**EV Battery:**
- ROC curves
- Confusion matrices
- Time-series plots

**Reinforcement Learning:**
- Training reward curves
- Success rate over episodes
- Epsilon decay plot

**Music Recommendation:**
- Top songs/artists bar charts
- Play count distributions
- Correlation heatmap

**How to save plots:**
```python
# Add this after creating each important plot:
plt.savefig('./images/plot_name.png', dpi=300, bbox_inches='tight')
```

---

### Priority 3: Update READMEs with Actual Results

Once notebooks are cleaned, update each project README with:

1. **Actual metrics** from your models
2. **Specific insights** from your analysis
3. **Screenshots** of key visualizations

Example:
```markdown
## Key Results

### Model Performance
- **XGBoost MSE**: 0.0234
- **LightGBM MSE**: 0.0245
- **Best Model**: XGBoost with optimized hyperparameters

![Feature Importance](./images/feature_importance.png)
```

---

## 🚀 GitHub Deployment Steps

### Step 1: Initialize Git Repository

```bash
cd /home/andre/portfolio/machine-learning-portfolio-clean
git init
git add .
git commit -m "Initial commit: Machine Learning Portfolio"
```

### Step 2: Create GitHub Repository

1. Go to https://github.com/andercodder
2. Click "New Repository"
3. Name: `machine-learning-portfolio`
4. Description: "Machine Learning & AI projects from MSc at University of Aberdeen"
5. **Keep it Public** (for recruiters)
6. **Don't** initialize with README (you already have one)

### Step 3: Push to GitHub

```bash
git remote add origin https://github.com/andercodder/machine-learning-portfolio.git
git branch -M main
git push -u origin main
```

### Step 4: Verify on GitHub

- Check all files uploaded correctly
- Verify READMEs render properly
- Test all internal links
- Ensure images display (if added)

---

## 📝 Notebook Cleaning Checklist

Use this checklist for each notebook:

### All Notebooks:
- [ ] Remove `from google.colab import drive`
- [ ] Remove `drive.mount('/content/drive')`
- [ ] Update file paths (remove `/content/drive/MyDrive/`)
- [ ] Add executive summary cell at top
- [ ] Add clear section headers
- [ ] Clean up print statements
- [ ] Add comments to complex code
- [ ] Ensure all cells run sequentially
- [ ] Save key visualizations to images/
- [ ] Add conclusion cell at end

### Situation Awareness Notebooks:
- [ ] Highlight XGBoost and LightGBM usage
- [ ] Show feature importance plots
- [ ] Document hyperparameter tuning process
- [ ] Add model comparison table

### EV Battery Notebooks:
- [ ] Emphasize time-series aspect (RNN)
- [ ] Show comparison between KNN and RNN
- [ ] Highlight SMOTE usage for imbalance
- [ ] Add ROC curves and confusion matrices

### RL Notebook:
- [ ] Document DQN architecture clearly
- [ ] Show training curves
- [ ] Explain epsilon-greedy strategy
- [ ] Add final policy performance

### Music Recommendation Notebook:
- [ ] Show EDA visualizations
- [ ] Document similarity computation
- [ ] Add example recommendations
- [ ] Show top songs/artists

---

## 🎯 TotalEnergies Application Strategy

### Cover Letter Talking Points:

1. **XGBoost/LightGBM Experience**
   - "Implemented gradient boosting models (XGBoost, LightGBM) for situation awareness prediction"
   - Reference: Project 1

2. **Time-Series Forecasting**
   - "Developed RNN-based time-series models for EV battery health prediction"
   - Reference: Project 2

3. **Energy Sector Relevance**
   - "Applied ML to energy systems (EV battery prediction, optimization)"
   - Reference: Project 2

4. **Sequential Decision-Making**
   - "Implemented Deep Q-Network for sequential optimization problems"
   - Reference: Project 3

5. **Production-Ready Code**
   - "Developed modular, well-documented code with comprehensive evaluation"
   - Reference: All projects

### Portfolio Link in Application:

**In your CV/Resume:**
```
GitHub Portfolio: github.com/andercodder/machine-learning-portfolio
```

**In your cover letter:**
```
"I have developed a portfolio of machine learning projects demonstrating 
experience with gradient boosting (XGBoost, LightGBM), time-series 
forecasting, and deep learning. My work on EV battery prediction and 
situation awareness systems directly relates to energy sector applications. 
Portfolio: github.com/andercodder/machine-learning-portfolio"
```

---

## 🔍 Quality Checklist Before Submission

### Technical Quality:
- [ ] All notebooks run without errors
- [ ] No Google Colab dependencies
- [ ] Clear, commented code
- [ ] Professional visualizations
- [ ] Comprehensive documentation

### Professional Presentation:
- [ ] No typos in READMEs
- [ ] Consistent formatting
- [ ] Professional language
- [ ] Clear project descriptions
- [ ] Working links

### GitHub Repository:
- [ ] Repository is public
- [ ] README displays correctly
- [ ] All links work
- [ ] Professional repository name
- [ ] Good commit messages

---

## 📊 Estimated Time to Complete

- **Notebook Cleaning**: 3-4 hours (30-45 min per notebook)
- **Adding Visualizations**: 1-2 hours
- **Final Review**: 1 hour
- **GitHub Setup**: 30 minutes

**Total**: ~6-8 hours of focused work

---

## 💡 Pro Tips

1. **Clean one project at a time** - Don't try to do everything at once
2. **Test notebooks after cleaning** - Run all cells to ensure they work
3. **Save progress frequently** - Commit to Git after each project
4. **Get feedback** - Ask a friend to review before applying
5. **Keep original files** - Don't delete your original notebooks yet

---

## 🆘 Common Issues & Solutions

### Issue: "File not found" errors after removing Colab paths
**Solution**: Add note in notebook about data availability:
```markdown
**Note**: This notebook requires the dataset `filename.csv`. 
Data is from academic coursework and available upon request.
```

### Issue: Notebooks take too long to run
**Solution**: Consider clearing output before committing:
```bash
jupyter nbconvert --clear-output --inplace notebook.ipynb
```

### Issue: Images not displaying on GitHub
**Solution**: Use relative paths:
```markdown
![Description](./images/plot.png)
# NOT: ![Description](images/plot.png)
```

---

## 📧 Questions?

If you encounter issues:
1. Check this guide first
2. Google the specific error
3. Check Stack Overflow
4. Review GitHub documentation

---

## 🎉 You're Almost There!

Your portfolio structure is **professional and ready**. The remaining work is:
1. Clean the notebooks (remove Colab dependencies)
2. Add visualizations to images folders
3. Update READMEs with actual results
4. Push to GitHub
5. Apply to TotalEnergies!

**Good luck with your applications!** 🚀

---

*This guide was created to help you finalize your ML portfolio for job applications.*
