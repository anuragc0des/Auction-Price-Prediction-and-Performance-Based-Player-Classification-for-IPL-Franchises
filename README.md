# AI-Driven Decision Intelligence for IPL Player Auction Analytics and Team Strategy Optimization

> A data-driven framework for IPL auction price prediction, player performance ranking, quantile-based classification, and head-to-head player comparison.

---

## 📌 Overview

The Indian Premier League (IPL) auction is a complex decision-making environment where franchises evaluate players using a combination of historical performance, player characteristics, previous-season statistics, and auction-specific factors.

This project develops an **AI-driven decision-support framework for IPL player and auction analytics**.

The study is divided into two complementary analytical components:

1. **IPL Auction Price Prediction**
   - Predicts player auction prices using XGBoost regression.
   - Uses player statistics and historical performance attributes.
   - Compares random and time-based validation.
   - Investigates overfitting and the bias-variance trade-off.
   - Uses feature importance and prediction-error analysis.

2. **IPL Player Performance Ranking and Classification**
   - Uses detailed ball-by-ball IPL data.
   - Builds a multi-dimensional player performance matrix.
   - Calculates batting and bowling performance metrics.
   - Uses standardized Z-scores to combine metrics.
   - Ranks players using a weighted Composite Z-Score.
   - Classifies players using quantile-based performance tiers.
   - Provides pairwise head-to-head comparisons.

The two studies are complementary:

> **Study 1 asks: "What auction price can be expected for a player?"**

> **Study 2 asks: "How does the player's actual performance compare with other players?"**

Together, they provide a broader analytical framework for supporting IPL player evaluation and auction decision-making.

---

# 🎯 Objectives

The major objectives of the project are:

- Predict IPL player auction prices using machine learning.
- Identify the player attributes that contribute to auction-price prediction.
- Evaluate model generalization using different train-test strategies.
- Investigate the effect of regularization on model variance and overfitting.
- Identify limitations of season-level auction datasets.
- Use detailed ball-by-ball data for deeper player-performance analysis.
- Construct a comprehensive batting and bowling performance matrix.
- Standardize different performance metrics using Z-scores.
- Generate a composite player performance score.
- Rank players based on multiple performance dimensions.
- Classify players into meaningful performance tiers using quantiles.
- Compare players directly using head-to-head performance matrices.
- Develop a decision-support framework that can be extended with additional auction and team-level information.

---

# 🏏 Study Architecture

The project follows two major studies.

```text
                         IPL Analytics Framework
                                  │
                 ┌────────────────┴────────────────┐
                 │                                 │
                 ▼                                 ▼
       STUDY 1: AUCTION PRICE             STUDY 2: PLAYER
             PREDICTION                    PERFORMANCE ANALYSIS
                 │                                 │
                 ▼                                 ▼
       Season-level auction data          Ball-by-ball IPL data
                 │                                 │
                 ▼                                 ▼
          Data Cleaning                  Player Identification
                 │                                 │
                 ▼                                 ▼
       Feature Engineering              Performance Aggregation
                 │                                 │
                 ▼                                 ▼
          XGBoost Model                 Performance Matrix
                 │                                 │
                 ▼                                 ▼
       Model Evaluation                   Z-Score Standardization
                 │                                 │
                 ▼                                 ▼
     Feature Importance                 Composite Performance Score
                 │                                 │
                 ▼                                 ▼
       Error Analysis                    Player Ranking
                 │                                 │
                 │                                 ▼
                 │                         Quantile Classification
                 │                                 │
                 │                                 ▼
                 └──────────────────────► Head-to-Head Comparison
