# NHL-Classification
This project utilizes K-means clustering algorithm to label the NHL players and use decision trees to predict and classify the NHL players. 

# Player Data Analysis

## Overview
This project involves analysis of player data using machine learning techniques including K-Means clustering and decision trees. It provides insights into player performances by clustering them based on their points per game and goal difference per game, and predicting player clusters using a decision tree model.

## Features
- **Data Loading**: Load player data from a CSV file.
- **Data Preprocessing**: Normalize and encode features for clustering and classification.
- **Clustering**: Group players using K-Means based on performance metrics.
- **Classification**: Predict the cluster of players using a Decision Tree Classifier.
- **Visualization**: Visualize clusters and decision tree to interpret the models.
### Clustering with K-Means

**Objective**: To identify patterns in player performance by grouping similar players into clusters.

**Methodology**:
- **Feature Selection**: Two key performance indicators are chosen: 'Point per Game' and 'Goal Difference per Game'.
- **Data Scaling**: Features are scaled using `StandardScaler` to normalize the data, ensuring that each feature contributes equally to the distance calculations in the clustering process.
- **Model Training**: A K-Means model is initialized with `n_clusters=3` to partition players into three distinct groups. The model is trained on the scaled data.
- **Interpretation**: Cluster labels are assigned back to the original data, allowing for analysis of common characteristics within each cluster.

**Visualization**:
- The clustering results are visualized in a scatter plot, using different colors to represent each cluster. This visualization helps in understanding the distribution and separation of clusters based on the selected features.

### Classification with Decision Tree

**Objective**: To predict the cluster classification of players based on their attributes.

**Methodology**:
- **Data Preparation**: Non-relevant columns and target cluster labels are removed from the feature set used to train the decision tree.
- **Model Training**: A `DecisionTreeClassifier` is used, with a random state for reproducibility. The model is trained on a training dataset and validated on a separate validation set to evaluate its performance.
- **Performance Evaluation**: The accuracy of the decision tree in predicting the correct cluster is calculated and used as the primary metric to assess the model's effectiveness.

**Visualization**:
- The structure of the trained decision tree is visualized, showing the decision paths and splits that the model uses to classify players. This visualization helps in interpreting the model's decision-making process and understanding which features are most influential in predicting player clusters.

**Feature Importance**:
- After training, the model provides insights into which features are most important for predicting the player clusters, allowing for a better understanding of the factors that influence player grouping.

**Future plans**:
- I wish this project can be used to evaluate players in real life. 
