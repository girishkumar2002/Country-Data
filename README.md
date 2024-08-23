Country Data Analysis for NGO Funding
Overview
This repository contains a Python-based analysis of country-level data to help an NGO allocate approximately $100 million in funds to countries that need it most. The goal is to identify and group countries based on various socioeconomic metrics, and to determine which groups of countries would benefit most from the funding.

Data
The dataset includes the following columns:

country: Name of the country
child_mort: Child mortality rate
exports: Exports as a percentage of GDP
health: Health expenditure as a percentage of GDP
imports: Imports as a percentage of GDP
income: Gross national income per capita
inflation: Inflation rate
life_expec: Life expectancy
total_fer: Total fertility rate
gdpp: GDP per capita
The dataset was obtained from this source.

Analysis
Data Preprocessing:

The data was scaled using MinMaxScaler to bring all metrics to a common scale. This is essential for clustering algorithms that rely on distance measures.
Clustering:

K-Means clustering was used to group countries into clusters based on the scaled features.
The optimal number of clusters was determined using the Elbow Method, which identified 4 clusters as the best fit.
Cluster Analysis:

Countries were assigned to clusters based on their features.
Cluster centers were analyzed to understand the characteristics of each group.
Results:

Cluster 1: Includes countries with high child mortality rates and lower income levels, indicating a need for substantial aid.
Cluster 2: Contains countries with moderate metrics across various features.
Cluster 3: Includes countries with moderate child mortality rates and relatively better income levels.
Cluster 4: Countries in this group have lower child mortality rates and higher income levels.
Recommendations:

Group of Countries Needing Help: The NGO should focus on Cluster 1, as it includes countries with high child mortality rates and lower income levels. These countries are likely to benefit most from additional support.
Code
The analysis was performed using the following libraries:

pandas
numpy
matplotlib
sklearn
Key code snippets:

Data loading and preprocessing
Feature scaling with MinMaxScaler
Clustering with KMeans
Evaluation of clustering performance using the Elbow Method
Usage
To replicate the analysis:

Clone this repository.
Install the required Python packages using pip install -r requirements.txt.
Run the analysis.py script to perform the analysis and view results.
