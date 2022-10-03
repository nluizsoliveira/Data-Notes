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


Proximity Measures allow generating a real number in `[0,1]` that represents the similarity (or dissimilarity) of instances in a dataset. This allow a wide number of statistical and DS techniques.

For example, it's possible to group items in **clusters**, a set of similar items that have internal cohesion and external separation. 


