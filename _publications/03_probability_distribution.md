---
title: "確率分布 / Probability distribution"
collection: publications
permalink: /:collection/probability_distribution
excerpt: '確率分布についてまとめています。'
date: 9999-10-30
venue:
paperurl:
citation:
---


Table of contents.
===
- [1. 離散分布（Discrete probability distribution）](#1-%e9%9b%a2%e6%95%a3%e5%88%86%e5%b8%83discrete-probability-distribution)
  - [1.1. 一様分布（Discrete uniform distribution）](#11-%e4%b8%80%e6%a7%98%e5%88%86%e5%b8%83discrete-uniform-distribution)
  - [1.2. 二項分布（Binomial distribution）](#12-%e4%ba%8c%e9%a0%85%e5%88%86%e5%b8%83binomial-distribution)
  - [1.3. 幾何分布（Geometric distribution）](#13-%e5%b9%be%e4%bd%95%e5%88%86%e5%b8%83geometric-distribution)
  - [1.4. 負の二項分布（Negative binomial distribution）](#14-%e8%b2%a0%e3%81%ae%e4%ba%8c%e9%a0%85%e5%88%86%e5%b8%83negative-binomial-distribution)
  - [1.5. ポアソン分布（Poisson distribution）](#15-%e3%83%9d%e3%82%a2%e3%82%bd%e3%83%b3%e5%88%86%e5%b8%83poisson-distribution)
- [2. 連続分布（Continuous probability distribution）](#2-%e9%80%a3%e7%b6%9a%e5%88%86%e5%b8%83continuous-probability-distribution)
  - [2.1. 一様分布（Continuous uniform distribution）](#21-%e4%b8%80%e6%a7%98%e5%88%86%e5%b8%83continuous-uniform-distribution)
  - [2.2. 指数分布（Exponential distribution）](#22-%e6%8c%87%e6%95%b0%e5%88%86%e5%b8%83exponential-distribution)
  - [2.3. 正規分布（Normal distribution）](#23-%e6%ad%a3%e8%a6%8f%e5%88%86%e5%b8%83normal-distribution)

Contents.
===

## 1. 離散分布（Discrete probability distribution）

### 1.1. 一様分布（Discrete uniform distribution）

### 1.2. 二項分布（Binomial distribution）

#### 1.2.1. 二項係数（binomial coefficient）


$$
\binom{n}{k} = \frac{n!}{k!(n-k)!}
$$


#### 1.2.2. 二項分布の平均（Mean of Binomial Distributuion）

$$
M_b  = np
$$

#### 1.2.3. 二項分布の分散（Variance of Binomial Distribution）


$$
\sigma^2 _b  = npq
$$


#### 1.2.4. 二項係数（Binomial Coefficient）

$$
 P(X)  = \binom{n}{k} \cdot p^kq^{n-k}
$$


### 1.3. 幾何分布（Geometric distribution）

### 1.4. 負の二項分布（Negative binomial distribution）

<a id="poisson"></a>
### 1.5. ポアソン分布（Poisson distribution）


$$
    X \sim Po\left( \lambda \right) \\
    E\left( X \right) = \lambda \\
    V\left( X \right) = \lambda \\
    P\left( x \right) = \frac{ e^{-\lambda}  \lambda^x }{x!}
$$



## 2. 連続分布（Continuous probability distribution）

### 2.1. 一様分布（Continuous uniform distribution）

### 2.2. 指数分布（Exponential distribution）

### 2.3. 正規分布（Normal distribution）

確率変数Xが正規分布に従うとき、以下のように表現する。  

$$
    X \sim N\left(\mu, \sigma^2\right) \\
    \mu : 平均 \\
    \sigma^2 : 分散 \\
$$

<a id="zscore"></a>
Xを線形変換した（標準化した）z値は、標準正規分布に従う。  

$$
    z = \frac{X - \mu }{\sigma} \sim N\left(0, 1\right)
$$
