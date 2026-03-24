# factfulness
IE data project
# Factfulness Clustering Project

## Project Overview  
This project analyzes whether the world can be divided into simple categories such as developed vs developing countries using clustering techniques on UN Development Indicators data.

The goal is to test the idea presented in Factfulness by Hans Rosling, which argues that the world is better understood as multiple groups rather than a binary classification.

---

## Dataset  
- Name: UN Development Indicators  
- File included: `UN.csv`  
- Source: https://github.com/manoelgadi/PSDMA/blob/main/datasets/UN.csv  

---

## Research Questions and Answers  

- Can the world be meaningfully divided into only two clusters (developed vs developing)?  
  No  

- How many clusters are suggested by the data (Elbow Rule)?  
  5  

- How much of the data structure is explained by two clusters compared to the optimal number of clusters?  
  36%  

- Does the evidence support the claim in Factfulness that the world cannot be divided into only two groups but into more (e.g., 4)?  
  Yes  

---

## Methodology  

### 1. Data Exploration  
- Loaded the dataset  
- Inspected variables  
- Selected numeric indicators  

### 2. Missing Values  
- Replaced missing values with the median  

### 3. Feature Scaling  
- Applied StandardScaler  

Why scaling is required:  
K-Means clustering uses distance calculations. Without scaling, variables with larger ranges would dominate the results.

---

### 4. Determine the Number of Clusters  
- Applied K-Means clustering  
- Tested multiple values of k  
- Used the Elbow Rule  

Result: Optimal number of clusters = 5

---

### 5. Compare Models  
- Ran clustering with k = 2  
- Ran clustering with k = 5 (optimal)  

---

### 6. Evaluation  
- The 2-cluster model explains only 36% of the data structure  
- The 5-cluster model provides a better representation  

---

## Conclusion  

The analysis shows that the world cannot be meaningfully divided into only two groups.  

Instead, the data supports multiple clusters (around 5), aligning with the idea that global development exists on a spectrum rather than a binary classification.

---

## Project Structure  
