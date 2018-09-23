---
layout: post
title:  "General Concept"
date:   2018-07-15 18:11:39 +0430
categories: algebra\chap1
---

#### Goal
- solving a system consists of n equation, n unknowns  
$${a_{11}X_{1}+a_{12}x_{2}+...+a_{1n}x_{n}=b_{1}} $$  
$${a_{21}X_{1}+a_{22}x_{2}+...+a_{2n}x_{n}=b_{2}} $$  
.  
.  
.  
$${a_{n1}X_{1}+a_{n2}x_{2}+...+a_{nn}x_{n}=b_{n}} $$  


#### coefficient matrix
$$A=\begin{pmatrix}a_{11} & a_{12} & ... & a_{1n}\\\ a_{21} & a_{22} & ... & a_{2n} \\\ . \\\ . \\\ . \\\ a_{n1} & a_{n2} & ... &  a_{nn}\end{pmatrix}$$

using this matrix, the equation can write as **AX=b** where **X** is a vector of independant variable and **b** is the vectors of constants  
$$X = \begin{pmatrix}X_{1} \\\ X_{2} \\\ ... \\\ X_{n}\end{pmatrix}$$ , $$b = \begin{pmatrix}b_{1} \\\ b_{2} \\\ ... \\\ b_{n}\end{pmatrix}$$ 

#### Column Representation
`AX` means combination of columns of A  
$$ AX = x_{1}C_{1}+x_{2}C_{2}+...+x_nC_{n} = x_{1}\begin{pmatrix}a_{11} \\\ a_{21} \\\ ... \\\ a_{n1}\end{pmatrix} +  x_{2}\begin{pmatrix}a_{12} \\\ a_{22} \\\ ... \\\ a_{n2}\end{pmatrix} + ... +  x_{n}\begin{pmatrix}a_{1n} \\\ a_{2n} \\\ ... \\\ a_{nn} \end{pmatrix} $$


#### Row Representation of  matrix
$$ X^TA =x_{1}.R_{1}+x_{2}R_{2}+...+x_{n}R_{n} = x_{1}\begin{pmatrix}a_{11} & a_{12} & ... & a_{1n} \end{pmatrix} + x_{2}\begin{pmatrix}a_{21} & a_{22} & ... & a_{2n} \end{pmatrix} + ... +x_{n}\begin{pmatrix}a_{n1} & a_{n2} & ... & a_{nn} \end{pmatrix}  $$


#### Elementary Row Operation
- when solving an equation with form AX=b we can use some operation to convert AX=b to UX=c where U is elementary matrix
- switch places of two rows
- multiply a row to a constant number
- add multiplication of a row to another row
- $$E_{ij}$$ is a matrix which is gained after row operation on A for changing value of element (i,j) of matrix to zero

#### Augmented Matrix
- in AX=b if we add vector b as a column to matrix A, then `[A|b]` is Augmented matrix


