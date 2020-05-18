---
title: "用語 : 不偏推定量/ Terminology : Unbiased Estimator"
collection: publications
permalink: /:collection/terminology_02_unbiased_estimator.html
excerpt: '用語をまとめています。'
date: 9999-09-29
venue:
paperurl:
citation:
---

Table of contents
===
- [1. 平均の2乗の不偏推定量 / Unbiased Estimator of $\mu^2$](#1-%e5%b9%b3%e5%9d%87%e3%81%ae2%e4%b9%97%e3%81%ae%e4%b8%8d%e5%81%8f%e6%8e%a8%e5%ae%9a%e9%87%8f--unbiased-estimator-of-math-xmlns%22httpwwww3org1998mathmathml%22semanticsmrowmsupmi%ce%bcmimn2mnmsupmrowannotation-encoding%22applicationx-tex%22mu2annotationsemanticsmath%ce%bc2)
  - [1.1. $X^2$の期待値を$\sigma$を用いて表すと](#11-math-xmlns%22httpwwww3org1998mathmathml%22semanticsmrowmsupmixmimn2mnmsupmrowannotation-encoding%22applicationx-tex%22x2annotationsemanticsmathx2%e3%81%ae%e6%9c%9f%e5%be%85%e5%80%a4%e3%82%92math-xmlns%22httpwwww3org1998mathmathml%22semanticsmrowmi%cf%83mimrowannotation-encoding%22applicationx-tex%22sigmaannotationsemanticsmath%cf%83%e3%82%92%e7%94%a8%e3%81%84%e3%81%a6%e8%a1%a8%e3%81%99%e3%81%a8)
  - [1.2. $\sigma^2$の不偏推定量(不偏分散)は](#12-math-xmlns%22httpwwww3org1998mathmathml%22semanticsmrowmsupmi%cf%83mimn2mnmsupmrowannotation-encoding%22applicationx-tex%22sigma2annotationsemanticsmath%cf%832%e3%81%ae%e4%b8%8d%e5%81%8f%e6%8e%a8%e5%ae%9a%e9%87%8f%e4%b8%8d%e5%81%8f%e5%88%86%e6%95%a3%e3%81%af)
  - [1.3. RSSの期待値を計算](#13-rss%e3%81%ae%e6%9c%9f%e5%be%85%e5%80%a4%e3%82%92%e8%a8%88%e7%ae%97)
  - [1.4. $E\left(\bar{X^2}\right)$を$\mu$と$\sigma$を用いて表す事を考える](#14-math-xmlns%22httpwwww3org1998mathmathml%22semanticsmrowmiemimrowmo-fence%22true%22momover-accent%22true%22msupmixmimn2mnmsupmomomovermo-fence%22true%22momrowmrowannotation-encoding%22applicationx-tex%22eleftbarx2rightannotationsemanticsmathex2%e3%82%92math-xmlns%22httpwwww3org1998mathmathml%22semanticsmrowmi%ce%bcmimrowannotation-encoding%22applicationx-tex%22muannotationsemanticsmath%ce%bc%e3%81%a8math-xmlns%22httpwwww3org1998mathmathml%22semanticsmrowmi%cf%83mimrowannotation-encoding%22applicationx-tex%22sigmaannotationsemanticsmath%cf%83%e3%82%92%e7%94%a8%e3%81%84%e3%81%a6%e8%a1%a8%e3%81%99%e4%ba%8b%e3%82%92%e8%80%83%e3%81%88%e3%82%8b)
  - [1.5. 平均の2乗の不偏推定量を考える](#15-%e5%b9%b3%e5%9d%87%e3%81%ae2%e4%b9%97%e3%81%ae%e4%b8%8d%e5%81%8f%e6%8e%a8%e5%ae%9a%e9%87%8f%e3%82%92%e8%80%83%e3%81%88%e3%82%8b)


Contents.
===

<a id="unbiased_extimator_of_mu_squared"></a>
## 1. 平均の2乗の不偏推定量 / Unbiased Estimator of $\mu^2$

確率件数$X_1, X_2, ...X_n$が平均$\mu$、分散$\sigma^2$に独立に従うとき、$\mu^2$の不偏推定量（不偏分散）は以下の式になることを証明。

$$
  E\left( \bar{X^2} - \frac{ \hat{\sigma}^2}{n} \right) = \mu^2
$$


### 1.1. $X^2$の期待値を$\sigma$を用いて表すと

\begin{align}
    V\left( X\right) &= E\left(X^2\right) - \bigl(E(X)\bigr)^2 \nonumber \\\\\\\\
    E\left( X^2\right) &= V\left( X\right) + \bigl(E(X)\bigr)^2 \nonumber \\\\\\\\
    \label{form1}
    &= \sigma^2 + \mu^2 
\end{align}

### 1.2. $\sigma^2$の不偏推定量(不偏分散)は
この式の証明は別途。

\begin{aligned}
  \hat{\sigma}^2 = \frac{1}{n-1} \sum{ \left(X-\bar{X}\right)^2} 
\end{aligned}

つまり

$$
  \label{form2}
  \sum{ \left(X-\bar{X}\right)^2} = \left( n -1 \right)\hat{\sigma}^2
$$

### 1.3. RSSの期待値を計算

\begin{aligned}
    E\bigl( \sum\left( X_i-\bar{X} \right)^2 \bigr) &= E\bigl( \sum\left(X_i^2  -2\bar{X}X_i + \bar{X}^2 \right)\bigr) \\\\\\\\
    &= E\bigl( \sum\left(X_i^2\right) - 2\bar{X}\sum X_i  + n\bar{X}^2 \bigr) \\\\\\\\
    &= E\bigl( \sum\left(X_i^2\right) - 2\bar{X} \cdot n \cdot\frac{\sum X_i}{n} + n\bar{X}^2 \bigr) \\\\\\\\
    &= E\bigl( \sum\left(X_i^2\right) - 2\bar{X} \cdot n \cdot \bar{X} + n\bar{X}^2 \bigr) \\\\\\\\
    &= E\bigl( \sum\left(X_i^2\right) - 2n\bar{X}^2 + n\bar{X}^2 \bigr) \\\\\\\\
    &= E\bigl( \sum\left(X_i^2\right) - n\bar{X}^2\bigr) \\\\\\\\
    &= \sum{E\left(X_i^2\right)} - nE\left(\bar{X^2}\right)
\end{aligned}

よって

$$
    \label{form3}
    E\left(\bar{X^2}\right) = \frac{1}{n}\biggl(\sum{E\left(X_i^2\right)} - E\bigl( \sum\left( X_i-\bar{X} \right)^2 \bigr) \biggr)
$$

### 1.4. $E\left(\bar{X^2}\right)$を$\mu$と$\sigma$を用いて表す事を考える

ここで、$\left( \ref{form1} \right)$と$\left( \ref{form2} \right)$を用いて$\left( \ref{form3} \right)$を書き換えると

\begin{aligned}
    E\left(\bar{X^2}\right) &= 
    \frac{1}{n} \biggl( \sum{\left(\sigma^2 + \mu^2\right)}  - E\bigl( \left( n-1 \right) \hat{\sigma}^2 \bigr) \biggr) \\\\\\\\
    &= 
    \frac{1}{n} \biggl( n\left(\sigma^2 + \mu^2\right)  - \left( n-1 \right) E\left(\hat{\sigma}^2 \right)  \biggr) \\\\\\\\
    &= 
    \left(\sigma^2 + \mu^2\right)  - \frac{n-1}{n} E\left(\hat{\sigma}^2 \right) \\\\\\\\
\end{aligned}

$\hat{\sigma}^2$は不偏分散なので$E\left(\hat{\sigma}^2\right) = \hat{\sigma}^2 = \sigma^2$とできる。つまり平均の期待値は、以下で表すことが出来る。

\begin{aligned}
    E\left(\bar{X^2}\right) = 
    \left(\sigma^2 + \mu^2\right)  - \frac{n-1}{n}\sigma^2 \\\\\\\\
    = \frac{n\sigma^2}{n} + \mu^2 -  \frac{n\sigma^2-\sigma^2}{n} \\\\\\\\
    =  \mu^2 + \frac{n\sigma^2 - n\sigma^2 + \sigma^2}{n} \\\\\\\\
    = \mu^2 + \frac{\sigma^2}{n}
\end{aligned}

### 1.5. 平均の2乗の不偏推定量を考える

この$\mu^2 + \frac{\sigma^2}{n}$が$\mu^2$に等しくなるような不偏推定量を求めることになる。ある定数$k$を用いて$\bar{X}^2$と$\hat{\sigma}^2$の和の期待値を作ると。**<font color="##ff0000">(なぜ$\hat{\sigma}^2$?)</font>**

\begin{aligned}
  E\left( \bar{X}^2 + k\hat{\sigma}^2 \right) = \mu^2 + \frac{\sigma^2}{n} + k\sigma^2
\end{aligned}

これが、$\mu^2$と等しくなるような$k$の値を求めると

\begin{aligned}
  \frac{\sigma^2}{n} + \mu^2 + k\sigma^2 &= \mu^2 \\\\\\\\
  k &= -\frac{1}{n}
\end{aligned}

$$
  \therefore
  E \left( \bar{X}^2 - \frac{\hat{\sigma}^2}{n} \right) = \mu^2 //
$$
