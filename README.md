# 🎮 Anomaly Detection in Steam User Profiles

> Final Project – CSE 575: Statistical Machine Learning  
> Arizona State University: Spring 2025
> Team: Deepanshu Jain, Rishit Puri, Shreya Sett, Mounusha Metti

---

## 🔍 Overview

This project builds a **multi-model anomaly detection system** to flag suspicious user behavior on the Steam gaming platform. With a dataset of over **470,000 user profiles**, we explored behavioral, historical, and engagement patterns to detect **cheaters, bots, and fraudulent accounts**.

Using a blend of **statistical methods**, **clustering**, and **machine learning algorithms**, we detect abnormal patterns in features like playtime, ban history, and game ownership. The goal is to support fairness and integrity in online gaming ecosystems.

---

## 🎯 Objectives

- Analyze Steam player profiles and detect suspicious patterns
- Engineer behavioral features (e.g., playtime consistency, ban density)
- Implement multiple anomaly detection techniques:
  - Rule-based
  - Statistical
  - Clustering (KMeans, HDBSCAN, LOF)
  - Machine Learning (Isolation Forest, One-Class SVM, Autoencoders)
- Build an ensemble voting system for robust anomaly flagging
- Recommend improvements for real-world deployment

---

## 📁 Dataset

- **Source**: Steam user data (476,694 profiles)
- **Key Features**:
  - Ban metrics: VAC bans, game bans, economy bans, last ban date
  - Engagement: Steam level, total playtime, cs2 playtime, number of games/friends
  - Metadata: Account age, profile visibility
- **Engineered Features**:
  - Ban density (bans normalized by account age)
  - Playtime per game
  - CS2 concentration
  - Engagement score (friends + games + playtime)

---

## ⚙️ Models Used

| Category            | Techniques                               |
|---------------------|-------------------------------------------|
| 📏 Rule-Based        | Custom heuristics (e.g., CS2 > total playtime) |
| 📊 Statistical       | Z-score, IQR, Mahalanobis Distance        |
| 📦 Clustering        | KMeans, HDBSCAN, LOF                      |
| 🧠 Machine Learning  | Isolation Forest, One-Class SVM, Autoencoder |

---

## 🧪 Results Summary

| Model            | Total Anomalies | Consensus Overlap | Overlap (%) |
|------------------|------------------|--------------------|-------------|
| HDBSCAN          | 152,055           | 12,365             | 8.13%       |
| Isolation Forest | 92,024            | 17,606             | 19.13%      |
| OCSVM            | 23,814            | 12,164             | 51.08%      |
| Autoencoder      | 23,835            | 6,187              | 25.96%      |
| KMeans           | 15,812            | 8,637              | 54.62%      |
| LOF              | 27,550            | 3,820              | 13.87%      |

✅ **Consensus Voting**: Users flagged by ≥3 models were selected as final anomalies for improved robustness and reduced false positives.

---

## 🔍 Key Visualizations

- Feature importance from Isolation Forest
- Cluster visualizations (KMeans, HDBSCAN)
- Anomaly score distributions

---

## 📚 Technologies Used

- **Python**, **Jupyter Notebook**
- `pandas`, `numpy`, `scikit-learn`, `pyod`, `seaborn`, `matplotlib`
- `tensorflow` / `keras` (for autoencoders)
- `hdbscan`,  `IsolationForest`, `Oneclass SVM`, `Kmeans Clustering`

---

## 🧠 Learnings & Impact

- An ensemble of anomaly detection models is more robust than a single approach.
- Rule-based methods provide baseline interpretability but lack flexibility.
- Advanced ML models (e.g., Autoencoders, Isolation Forests) capture subtle anomalies missed by traditional models.
- Clustering-based models like HDBSCAN can uncover complex groupings but may overflag dense regions.
- This work has practical implications for building cheat detection systems in real-world gaming environments.

---

## 📈 Future Enhancements

- Integrate Explainable AI (XAI) for Autoencoder decisions
- Add real-time detection capabilities
- Perform demographic fairness audits (if data available)
- Use graph-based features (e.g., friend networks)

---

## 📑 Report

Full report available here: [`FourML Ensemble_Report.pdf`](FourML Ensemble_Report.pdf)

---

## 👥 Contributors

- **Deepanshu Jain** 
- **Rishit Puri** 
- **Shreya Sett** 
- **Mounusha Metti** 
---

## 📬 Contact

For questions or collaborations, reach out via [LinkedIn](https://www.linkedin.com/in/mounusha-ram-metti/) or [Github](https://github.com/Mounusha25)
