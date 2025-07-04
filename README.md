# ML-Projects

Customer Segmentation with K-Means Clustering
📋 Project Overview
Apply unsupervised learning to segment mall customers into distinct groups based on their annual income and spending habits. This enables targeted marketing and personalized promotions.

🗃️ Dataset
Source: Mall_Customers.csv (200 records, 5 columns)

Features used:

Annual Income (k$)

Spending Score (1–100)

🔍 Methodology
Data Preparation
• Loaded 200 customer records into a NumPy array X of shape (200, 2).
• No missing values; features on comparable scales.

Elbow Method for k-Selection
• Computed Within-Cluster Sum of Squares (WCSS) for k = 1…10 using scikit-learn’s KMeans.inertia_.
• Observed WCSS drop from 269,981 (k=1) to 44,448 (k=5), an 83.5% reduction, indicating an “elbow” at k=5.

K-Means Clustering
• Trained KMeans(n_clusters=5, init='k-means++', random_state=0) on X.
• Assigned each customer to one of 5 clusters; cluster sizes = [35, 81, 39, 22, 23].

Visualization & Insights
• Plotted clusters in 2D, highlighting centroids in yellow.
• Identified five actionable segments (e.g., high-income high-spender vs. budget-conscious low-spender).
• Enables tailored marketing campaigns and resource allocation.
