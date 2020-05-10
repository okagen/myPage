---
title: "基本公式 / Basic formulas"
collection: publications
permalink: /:collection/basic_formulas
excerpt: '基本公式をまとめています。'
date: 9999-12-30
venue:
paperurl:
citation:
---

Table of contents.
===
- [1. 平均（Mean）](#1-%e5%b9%b3%e5%9d%87mean)
- [2. 期待値（Expectation value）](#2-%e6%9c%9f%e5%be%85%e5%80%a4expectation-value)
  - [2.1. Xが離散型確率変数 / discrete random variable](#21-x%e3%81%8c%e9%9b%a2%e6%95%a3%e5%9e%8b%e7%a2%ba%e7%8e%87%e5%a4%89%e6%95%b0--discrete-random-variable)
  - [2.2. Xが連続型確率変数 / continuous random variable](#22-x%e3%81%8c%e9%80%a3%e7%b6%9a%e5%9e%8b%e7%a2%ba%e7%8e%87%e5%a4%89%e6%95%b0--continuous-random-variable)
- [3. 母分散 (Population variance)](#3-%e6%af%8d%e5%88%86%e6%95%a3-population-variance)
- [4. 標本の分散](#4-%e6%a8%99%e6%9c%ac%e3%81%ae%e5%88%86%e6%95%a3)
  - [4.1. 標本分散 (Sample variance)](#41-%e6%a8%99%e6%9c%ac%e5%88%86%e6%95%a3-sample-variance)
  - [4.2. 不偏分散 (Unviased variance)](#42-%e4%b8%8d%e5%81%8f%e5%88%86%e6%95%a3-unviased-variance)
- [5. 標準偏差 (SD : Standard Deviation)](#5-%e6%a8%99%e6%ba%96%e5%81%8f%e5%b7%ae-sd--standard-deviation)
- [6. 変動係数 (CV : Coefficient of variation)](#6-%e5%a4%89%e5%8b%95%e4%bf%82%e6%95%b0-cv--coefficient-of-variation)
- [7. 標準誤差（Standard Error）](#7-%e6%a8%99%e6%ba%96%e8%aa%a4%e5%b7%aestandard-error)

Contents.
===

## 1. 平均（Mean）


$$
\mu = \frac{1}{n}\sum\limits_{i = 1}^n {x_i}
$$


## 2. 期待値（Expectation value）

### 2.1. Xが離散型確率変数 / discrete random variable
  - *p(x)* : 確率質量関数 / probability mass function (pmf) 


$$
E \left( X \right) = \sum\limits_{i = 1}^n {x_i P \left(X = x_i \right)}
                   = \sum\limits_{i = 1}^n {x_i \cdot p \left( x \right)}
$$

### 2.2. Xが連続型確率変数 / continuous random variable
  - *f(x)* : 確率密度関数 / Probability density function (pdf) 


$$
E \ \left( X \right) = \int^{\infty}_{-\infty}x\cdot f(x)\:dx
$$

## 3. 母分散 (Population variance)


$$
\sigma^2  = V \left( X \right)
          =  \frac{1}{n}\sum\limits_{i=1}^n{\left( {x_i - \mu } \right)^2}
          =  \sum\limits_{i=1}^n{\left( {x_i - \mu } \right)^2p_i}
$$

$$
V(X) = E \left( X^2 \right) - \bigl( E \left( X \right) \bigr)^2
$$

## 4. 標本の分散

### 4.1. 標本分散 (Sample variance)


$$
s^2  =  \frac{1}{n}\sum\limits_{i=1}^n{\left( {x_i - \bar x } \right)^2}
$$

<a id="unviased_variance"></a>
### 4.2. 不偏分散 (Unviased variance)
  - DoF : 自由度 / degree of freedom
  - RSS : 偏差平方和 / residual sum of squares


$$
\hat{\sigma}^2  = u^2
 =  \frac{1}{n -1}\sum\limits_{i=1}^n{\left( {x_i - \bar x } \right)^2}
 = \frac{RSS}{DoF}
$$

  - 不偏分散の期待値は母分散（推定したいもの）と一致する ⇒ 母分散の不偏推定量である。


$$
E(\hat{\sigma}^2)  = E(u^2) = \sigma^2
$$


## 5. 標準偏差 (SD : Standard Deviation)


$$
\sigma  = \sqrt {\sigma_2 }
$$

<a id="coefficient_of_variation"></a>
## 6. 変動係数 (CV : Coefficient of variation)

量の散らばり具合を表す統計量。本来比較が難しい2種類以上の比較することが出来る。例えば、人の身長の散らばり具合と体重の散らばり具合の比較とか。

$$
CV  = \frac {\sigma} {\mu}
$$

$$
CV  = \frac {s} {\bar x}
$$


## 7. 標準誤差（Standard Error）



$$
\frac{\sigma}{\sqrt n}
$$







