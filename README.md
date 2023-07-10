# Sentiment Analysis for Beauty Product Reviews on Amazon

# Problem and Approach

E-commerce has become popular in the last decade. Thousands of products are sold through platforms like Amazon, eBay, etc. One of the biggest advantages of e-commerce platforms for both customers and sellers alike is an option to rate and review the products. These reviews can be used by businesses to make major business decisions based on price optimization, demand forecasts, product comparison with the competition. In the real world situation, businesses don’t have access to the sentiment label of the reviews provided by the customers. Through this project, we would like to explore different ways of unsupervised sentiment analysis for luxury beauty products sold on Amazon and find insights for the features that work for the brand.

Today Luxury Beauty Products globally is 126 Billion USD Market with 18.8 Billion USD in US alone. More than 2000 products are sold on Amazon with wide range of brands, price and categories.

# Data Structure and Dictionary 
*Data is not uploaded to the repository because of the large size* 

Data Credit : Jianmo Ni, J. L. (2019). Justifying recommendations using distantly-labeled reviews and fined-grained aspects. . Empirical Methods in Natural Language Processing (EMNLP).

**Some important variables**

reviews.json

reviewerID - ID of the reviewer, e.g. A2SUAM1J3GNN3B
asin - ID of the product, e.g. 0000013714
reviewerName - name of the reviewer
vote - helpful votes of the review
style - a dictionary of the product metadata, e.g., "Format" is "Hardcover"
reviewText - text of the review
overall - rating of the product
summary - summary of the review
meta_data.json

asin - ID of the product, e.g. 0000031852
title - name of the product
description - description of the product
price - price in US dollars (at time of crawl)

# Models 
We tested 3 models:
- VADER
- KMeans with Word2Vec
- KMeans with Self Organzing Maps

# Conclusion, Recommendation and Future Steps

## Business Recommendation
- From our analysis we found that there is an exponentital relation between the price and number of reviews. More the reviews can also be correlated with the popularity of the product

- For Luxury Brands to make their ranking on amazon and get more positive sentiments they need to create strong descriptions as well as use the sentiments from these products for price optimization

- For market researchers, different unsupervised sentiment analysis techniques can go a long way rather than just abiding by the rule based or corpus based approach.

## Data Science Recommendations
- If the decision makers care about recall and F-1 Score, VADER is a good model. If they care about Precision alone, they can use K-Means with Word2Vec

- The models we used are not very optimized. Especially SOM which requires more data as well as computationally faster infrastructure. We can fine-tune them to create as good results as VADER.

- More expertise from Beauty Product experts can help us decide more ways to prepare the text and remove/modify tokens accordingly

