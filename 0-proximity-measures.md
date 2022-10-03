# Proximity Measures 

## Motivation
Datasets are often represented as a matrix in which each row is an instance of data and each column represents a feature of that data. 

$$
M = 
\begin{bmatrix}
x11 & x12 & x13 & ... & x1d \\
x21 & x22 & x23 & ... & x2d \\
... & ... & ... & ... & ... \\
xn1 & xn2 & xn3 & ... & xnd 
\end{bmatrix}
$$

For example, the dataset  

<div align="center">
  
| Item | Feature #1 | Feature #1 |
|------|------------|------------|
| x1   | 1.5        | 5055       |
| x2   | 2.3        | 5943       |
| x3   | 5.4        | 7100       |
| x4   | 3.2        | 8590       |
  
</div>

Can be represented as: 

$$
M = 
\begin{bmatrix}
1.5 & 5055 \\
2.3 & 5943 \\
5.4 & 7100 \\
3.2 & 8590
\end{bmatrix}
$$


Proximity Measures allow generating a real number, preferebly but not necessarely in range `[0,1]`,  that represents the similarity (or dissimilarity) of instances in a dataset. This allow a wide number of statistical and DS techniques.

For example, it's possible to group items in **clusters**, a set of similar items that have internal cohesion and external separation. 


Proximity measures are denoted by `d(xi, xj)`, being `x` an instance of a dataset (row of matrix). 

## Dissimilarity Measures

### Properties
There's not a single dissimilarity measures. However, every of them must follow some basic properties: 

1. Simetry: `d(xi, xj) = d (xj, xi)`
2. Positivity: `d(xi, xj) >= 0 for all pair xi, xj`
3. Reflexivity: `d(xi, xj) = 0 if, and only if xi = xj`
4. Triangle Inequality applies 

### Euclidian Distance

Euclidian distance can be applied to **continuous data** (numeric, real numbers). It's calculated as: 

![image](https://user-images.githubusercontent.com/49366837/193611845-6e0f314f-62ec-4b73-89f7-21b3a6c2a547.png)

It is noticable that:
1. features with bigger values/variances can "dominate" the euclidian distance. Therefore it may be interesting to normalize data. 
