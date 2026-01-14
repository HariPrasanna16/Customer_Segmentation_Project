Customer Segmentation using RFM Analysis & K-Means Clustering
Project Overview

This project focuses on customer segmentation using RFM (Recency, Frequency, Monetary) analysis combined with K-Means clustering, an unsupervised machine learning technique.
The goal is to segment customers based on their purchasing behavior and extract actionable business insights from real-world retail transaction data.

Objective

To analyze customer purchasing patterns and group customers into meaningful segments such as VIP, Regular, and At-risk customers using unsupervised learning.

Dataset

The dataset contains retail transaction records with the following columns:

InvoiceNo – Unique transaction identifier

StockCode – Product code

Description – Product description

Quantity – Number of items purchased

InvoiceDate – Date & time of transaction

UnitPrice – Price per unit

CustomerID – Unique customer identifier

Country – Customer location

The dataset represents real-world e-commerce transactions, making the analysis realistic and industry-relevant.

Methodology
1️) Data Cleaning & Preprocessing

Removed transactions with missing CustomerID

Converted InvoiceDate to datetime format

Removed cancelled transactions (negative quantity)

Created TotalPrice = Quantity × UnitPrice

2️)Feature Engineering – RFM Analysis

Customer behavior was summarized using:

Recency: Days since the last purchase

Frequency: Number of unique purchases

Monetary: Total spending by the customer

This transformed transaction-level data into customer-level behavioral features.

3️)Feature Scaling

Standardized RFM features using StandardScaler

Required for distance-based clustering algorithms like K-Means

4️)Clustering (Unsupervised Learning)

Applied K-Means clustering

Used the Elbow Method to determine the optimal number of clusters (K = 3)

Assigned cluster labels to each customer

5️)Cluster Interpretation

Each cluster was analyzed using average RFM values to identify customer segments:

Cluster Type	Description
VIP / Loyal Customers	Recent, frequent, high-spending customers
Regular Customers	Moderate purchase frequency and spending
At-Risk Customers	Inactive customers with low engagement

Visualizations

Elbow Method plot to select optimal K

2D and 3D scatter plots to visualize customer clusters

Cluster-wise RFM comparison for interpretation

These visualizations help validate clustering quality and improve business understanding.

Key Learnings

Importance of feature engineering over raw data

Difference between supervised vs unsupervised learning

Why scaling is critical for K-Means clustering

How to interpret ML results from a business perspective

Handling real-world, messy datasets effectively

Future Improvements

Experiment with Hierarchical Clustering or DBSCAN

Perform cluster profiling by country or product category

Build a recommendation or retention strategy based on clusters

Automate customer segmentation for real-time data

Technologies Used

Python
Pandas
NumPy

Matplotlib

Scikit-learn
