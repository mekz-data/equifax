# Equifax Credit Marketing Segmentation

add equifax logo here

This is a brief description of a project that I worked on for Equifax. Unfortunately, due to signing an NDA, 
I am limited on revealing some aspects of the project. This was an exciting opportunity to work with a big company
on a real-world problem so I wanted to document it for posterity. 

## Project Overview: 
- The project's goal was to optimize credit marketing for Equifax's clients via enhanced targeting.
- Created 4 distinct clusters and developed distinct marketing strategies for each one focusing on accessibility, financial education, and product offerings based on their characteristics.
- Increased focus was placed on whether or not the group contained first time homebuyers for future marketing purposes. 
- Experiments were performed with various forms of dimensionality reduction and clustering. 
- Big dataset consisted of ~2 million rows and ~600 columns.

put diagram here

## Code and Resources used:
- Python 3.12.2
- Google Cloud Platform (GCP) - BigQuery
	
## Data
- Without being too specific, I will just say that the dataset consisted of personal credit data for roughly 2 million people in the United States.
- All of the data is what you would typically find on a credit report. 

## Data Cleaning Process
- This was a large, sparse dataset that we imputed via K-Nearest Neighbors, geo-aggregation, and my domain knowledge of credit data from my days as a loan officer. 

## Model Building
- In order to more easily facilitate clustering, we experimented with various dimensionality reduction methods including Principal Component Analysis and feature selection with Random Forest, LightGBM, and Decision Trees. 
- LightGBM performed the fastest by far and got very similar results to the other methods, so this became our chosen technique to reduce dimensionality. 
- Afterwards, clustering experiments were performed with k means and Gaussian mixture models. 

## Takeaways
- When dealing with large datasets and computationally intensive processes, use the method that gets you 80% of the results at 20% of the cost. In this case, using LightGBM saved us so much time compared to other methods. 
- Real world data is just as dirty as you've been told before. Knowing when to impute and when to just drop rows can be a difficult choice sometimes. 
