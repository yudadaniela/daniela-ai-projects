# Clustering U.S. Congressional Voting Patterns

## Problem
Applied unsupervised learning to U.S. congressional voting records 
(435 representatives, 16 votes) to see whether voting patterns alone 
— without knowing party affiliation — could reveal the underlying 
political groupings, and to compare two different clustering approaches.

## Tools & Approach
- Python: Pandas for data cleaning, scikit-learn for modeling
- Data cleaning: converted categorical votes (yes/no) to binary, 
  handled missing values by imputing the mode
- K-Means clustering (k=2) to group representatives by voting similarity
- PCA (Principal Component Analysis) to reduce 16 voting dimensions 
  down to 2 for visualization
- DBSCAN clustering to compare a density-based approach against K-Means, 
  including outlier/noise detection
- Seaborn/Matplotlib for visualizing clusters and centroids

## My Contribution
Individual project — full pipeline from data cleaning through both 
clustering methods and comparative analysis.

## Key Findings
- K-Means correctly grouped representatives matching their real party 
  affiliation in **88% of cases**, based purely on voting patterns
- DBSCAN identified only one dense cluster, but flagged **35 
  representatives as outliers** — legislators whose voting behavior 
  didn't clearly align with either party bloc
- K-Means outperformed DBSCAN here specifically because the number of 
  expected groups (2 parties) was known in advance — DBSCAN's strength 
  is in discovering unknown structure and identifying atypical cases, 
  not in matching a predefined number of groups

## What I'd Do Differently
Tune DBSCAN's parameters (eps and min_samples) further to see if a 
better-separated result was possible, rather than relying on a single 
configuration.

## Course
Machine Learning
