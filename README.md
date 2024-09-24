# Product Demand Prediction using Decision Support System (DSS) with Fuzzy Inference System (FIS) Tsukamoto

This project involves developing a Decision Support System (DSS) that uses the Fuzzy Inference System (FIS) Tsukamoto method to measure and predict product demand for an e-commerce platform. The system helps businesses estimate the demand for various products by considering multiple variables such as total sales, product ratings, views, and total comments.

## Table of Contents

1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Methodology](#methodology)
4. [Fuzzy Rules](#fuzzy-rules)
5. [Results](#results)
6. [Conclusion](#conclusion)
7. [References](#references)

## Introduction

E-commerce companies need effective methods to assess the viability of their products for future production. Traditionally, only best-selling products were used as indicators to estimate future demand. However, several criteria must be considered to predict market trends more accurately.

In this project, a Decision Support System (DSS) is implemented using the Fuzzy Inference System (FIS) Tsukamoto method to consider multiple variables and predict product demand. The system helps businesses make informed decisions regarding production and inventory management.

## Dataset

The input variables used in this system include:
- **Total Sales (TS)**: The number of units sold for each product.
- **Rating (R)**: The average rating of the product.
- **Views (V)**: The total number of views for the product.
- **Total Comments (TC)**: The total number of comments left by customers.

The output variable is:
- **Product Demand (PD)**: The predicted demand for the product.

The dataset spans one year and includes data from the e-commerce website Orebae.com.

## Methodology

The Tsukamoto method of Fuzzy Inference System (FIS) is used in this research. The steps involved are:

1. **Fuzzification**: Converts input variables (TS, R, V, TC) into fuzzy sets using membership functions.
2. **Fuzzy Rule Creation**: A total of 81 fuzzy rules were created, of which 17 correspond to high product demand.
3. **Defuzzification**: Transforms the fuzzy output into a crisp value representing the predicted product demand. This is achieved using the Center Average Defuzzifier (CAD) method.

### Fuzzy Membership Functions

- **Total Sales (TS)**: Categorized as Low, Medium, or High.
- **Rating (R)**: Categorized as Bad, Medium, or Good.
- **Views (V)**: Categorized as Low, Medium, or High.
- **Total Comments (TC)**: Categorized as Low, Medium, or High.
- **Product Demand (PD)**: Categorized as Low, Medium, or High.

## Fuzzy Rules

Example of fuzzy rules used in the system:
1. If Total Sales is High and Rating is Good and Views are High and Total Comments are High, then Product Demand is High.
2. If Total Sales is Medium and Rating is Medium and Views are Medium and Total Comments are Low, then Product Demand is Medium.

A total of 81 rules are applied to model various scenarios.

## Results

The system was tested with a sample dataset consisting of product data from the e-commerce platform Orebae.com. The results showed that the system could accurately classify product demand into high, medium, or low categories.

### Sample Results:

| No | Product                      | Total Sales | Rating | Views     | Total Comments | Predicted Demand |
|----|------------------------------|-------------|--------|-----------|----------------|------------------|
| 1  | Gantungan Kunci Baduy         | 2,257,891   | 4      | 3,258,175 | 1,420          | High             |
| 2  | Miniatur Badak Bercula Satu   | 1,768,313   | 4      | 5,353,782 | 1,003          | High             |
| 3  | Tenun Baduy Sarung            | 167,342     | 4      | 807,372   | 522            | High             |
| 4  | Oblong Banten                 | 532,162     | 4      | 851,548   | 198            | Low              |
| 5  | Pashmina Tenun Baduy          | 80,642      | 4      | 303,789   | 156            | Medium           |

## Conclusion

The Decision Support System built using the Fuzzy Inference System (FIS) Tsukamoto method successfully predicts product demand by considering multiple factors. It increases efficiency in decision-making and helps businesses optimize product production based on real-time market trends. The system provides a useful tool for e-commerce platforms to forecast demand and maximize profit.

## References

The project is based on the research published in the following paper:
- Fadil Indra Sanjaya, Dadang Heksaputra, Muhammad Fachrie, Sulistyo Dwi Sancoko, Nuzula Afini, Zahra Septa Hati. "Sistem Pendukung Keputusan Untuk Mengukur Permintaan Produk Pada E-Commerce dengan Fuzzy Inference System: (Studi Kasus Orebae.com)." *JIMP : Jurnal Informatika Merdeka Pasuruan*, Vol.7 No.1, Maret 2022. DOI: [http://dx.doi.org/10.37438/jimp.v7i1.404](http://dx.doi.org/10.37438/jimp.v7i1.404)
