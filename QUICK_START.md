# 🚀 Quick Start Guide

**Your portfolio is ready! Follow these steps to deploy it.**

---

## Step 1: Clean First Notebook (30 min)

Open: `01_Situation_Awareness_Prediction/situation_awareness_prediction.ipynb`

**Find and delete:**
```python
from google.colab import drive
drive.mount('/content/drive')
```

**Change file paths:**
```python
# FROM:
file_path = '/content/drive/MyDrive/SAdata_allMeasures.csv'

# TO:
# Note: Dataset from academic coursework, available upon request
file_path = './data/SAdata_allMeasures.csv'  # Local path
```

**Add at top (first cell):**
```markdown
# Situation Awareness Prediction using XGBoost & LightGBM

**Author**: Andre de Carvalho  
**Course**: CS5079 - Applied Artificial Intelligence  
**University**: University of Aberdeen (2025)

## Executive Summary

This notebook implements gradient boosting models (XGBoost and LightGBM) to predict driver situation awareness from physiological and behavioral data.

**Key Results:**
- Implemented and compared XGBoost vs LightGBM
- Performed hyperparameter optimization
- Analyzed feature importance

**Technologies**: XGBoost, LightGBM, Scikit-learn, Pandas
```

**Save and test** - Run all cells to ensure it works

---

## Step 2: Repeat for Other Notebooks (2-3 hours)

Same process for:
- `01_Situation_Awareness_Prediction/exploratory_analysis.ipynb`
- `02_EV_Battery_Health_Prediction/rnn_time_series_approach.ipynb`
- `02_EV_Battery_Health_Prediction/knn_baseline_approach.ipynb`
- `03_Reinforcement_Learning_Optimization/dqn_frozenlake.ipynb`
- `04_Music_Recommendation_System/recommendation_system.ipynb`

---

## Step 3: Push to GitHub (15 min)

```bash
cd /home/andre/portfolio/machine-learning-portfolio-clean

git init
git add .
git commit -m "Initial commit: ML Portfolio - XGBoost, Time-Series, Deep Learning, RL"

# Go to github.com/andercodder and create new repo:
# Name: machine-learning-portfolio
# Description: Machine Learning & AI projects from MSc at University of Aberdeen
# Public repo

git remote add origin https://github.com/andercodder/machine-learning-portfolio.git
git branch -M main
git push -u origin main
```

---

## Step 4: Verify on GitHub (5 min)

Check:
- [ ] README displays correctly
- [ ] All projects visible
- [ ] Links work
- [ ] Professional appearance

---

## Step 5: Update Your CV (10 min)

Add under Projects or Technical Skills:

```
Machine Learning Portfolio
github.com/andercodder/machine-learning-portfolio

• Implemented XGBoost and LightGBM for situation awareness prediction
• Developed RNN time-series models for EV battery health forecasting  
• Built Deep Q-Network for sequential optimization
• Created content-based recommendation system

Technologies: Python, XGBoost, LightGBM, PyTorch, TensorFlow, Scikit-learn
```

---

## Step 6: Apply to TotalEnergies (30 min)

**Use cover letter template from:** `TOTALENERGIES_REFERENCE.md`

**Key points:**
- Mention XGBoost/LightGBM experience
- Highlight time-series forecasting (RNN)
- Reference energy sector project (EV battery)
- Include portfolio link

**Application link:**
https://jobs.totalenergies.com/en_US/careers/JobDetail/Machine-Learning-Data-Science-and-Software-Development-Internship/70026

---

## 📋 Today's Checklist

- [ ] Clean situation_awareness_prediction.ipynb
- [ ] Clean exploratory_analysis.ipynb
- [ ] Test both notebooks run without errors
- [ ] Commit progress to Git

## This Week's Checklist

- [ ] Clean all 6 notebooks
- [ ] Push to GitHub
- [ ] Update CV with portfolio link
- [ ] Apply to TotalEnergies
- [ ] Apply to 2-3 similar roles

---

## 🆘 Need Help?

- **Detailed instructions**: See `SETUP_GUIDE.md`
- **TotalEnergies specific**: See `TOTALENERGIES_REFERENCE.md`
- **Overview**: See `PORTFOLIO_COMPLETE_SUMMARY.md`

---

## 🎯 Success Criteria

Your portfolio is ready when:
✅ All notebooks run without Colab dependencies  
✅ Professional README displays on GitHub  
✅ All links work  
✅ No typos or errors  
✅ Portfolio link in your CV  

---

**You've got this! Start with Step 1 now! 🚀**
