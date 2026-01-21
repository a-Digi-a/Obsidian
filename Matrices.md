#semester-2 #maths #problem-solving-for-engineers

# Matrices

## What is a matrix?

A **matrix** is a **rectangular array** of numbers, symbols or expressions organised into **rows** and **columns**:

**Example** **Matrix**:

$\begin{bmatrix}1 & 2 & 3 \\ 4 & 5 & 6\end{bmatrix}$

**Matrix** **columns** and **rows** can be **infinitely big**, and are typically denoted by *n* and *m*

$m\times n=\begin{bmatrix}a_{1,1}&a_{1,2}&\dots &a_{1,n} \\ a_{2,1}&a_{2,2}&\dots &a_{2,n} \\\dots&\dots&\dots &\dots \\a_{i,1}&\dots&a_{i,j} &\dots  \\\dots&\dots&\dots &\dots  \\a_{m,1}&a_{m,2}&\dots &a_{m,n} \\ \end{bmatrix}$

## Turning Simultaneous Equations into Matrices

Consider the **simultaneous** **equation**:

$2x+3y=8$
$4x-5y=-6$

We can **rewrite** this as:

$\begin{bmatrix}2 & 3 \\ 4 & -5\end{bmatrix}\begin{bmatrix}x \\ y\end{bmatrix}=\begin{bmatrix}8 \\ -6\end{bmatrix}$

$A=\begin{bmatrix}2 & 3 \\ 4 & -5\end{bmatrix},~~B=\begin{bmatrix}x \\ y\end{bmatrix},~~C=\begin{bmatrix}8 \\ -6\end{bmatrix}$

This means we can write the equation as:

$Ax=B$

### Why is This Useful?

Imagine a equation had more than 10 variables. That would be very difficult to solve by hand. By **turning the equation into a matrix**, we can use **computer programs** such as **python** to solve them.

## Matrix Equality 

**Matrices** are **only equal** if they have the **same dimension** and **every element is the same**:

$A=\begin{bmatrix}1&2 \\ 3&2\end{bmatrix},~~B=\begin{bmatrix}1&2 \\ 3&2\end{bmatrix},~~C=\begin{bmatrix}1&1 \\ 3&1\end{bmatrix},~~D=\begin{bmatrix}1&1&1&1\end{bmatrix}$

$A=B,~~~ A\neq C, ~~~ A\neq D$

## Matrix Addition

**Matrices** can be **added** **only** if they have the **same dimensions**

$C_{i,j}=A_{i,j}+B_{i,j}$

$\begin{bmatrix}1&2&3 \\ 4&5&6\end{bmatrix}+\begin{bmatrix}7&8&9 \\ 10&11&12\end{bmatrix}=\begin{bmatrix}1+7&2+8&3+9 \\ 4+10&5+11&6+12\end{bmatrix}$

## Matrix Subtraction

**Matrices** can be **subtracted** **only** if they have the **same dimensions**

$C_{i,j}=A_{i,j}-B_{i,j}$

$\begin{bmatrix}1&2&3 \\ 4&5&6\end{bmatrix}-\begin{bmatrix}7&8&9 \\ 10&11&12\end{bmatrix}=\begin{bmatrix}1-7&2-8&3-9 \\ 4-10&5-11&6-12\end{bmatrix}$

## Matrix Scalar Multiplication

**Matrices** can be **multiplied** by **scalars** too:

$\begin{bmatrix}1&2&3 \\ 4&5&6\end{bmatrix}\times k=\begin{bmatrix}1k&2k&3k \\ 4k&5k&6k\end{bmatrix}$

## Matrix Multiplication

