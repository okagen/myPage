---
title: "統計検定 2級 2016年11月"
collection: publications
permalink: /:collection/jp_stat_cert_grade2_2016-11.html
excerpt: 1,2,3,4,5,6,7,8,9,10,11,12,13,【14】,【15】,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35 /【】は記載あり。
date: 2016-11-27
venue:
paperurl:
citation:
---

# Table of contents
- [問8 / [14]](#%e5%95%8f8--14)
- [問8 / [15]](#%e5%95%8f8--15)
- [問9 / [17]](#%e5%95%8f9--17)

-------------------------
# 解き方

問8 / [14]
---
#### Point
  1. ```標準化```という言葉から「平均=0」「分散=1」を連想する。
  2. ```無相関```という言葉から「共分散=0」を連想する。

#### Slution
[相関係数](basic_formulas.html#correlation_coefficient)の式に$ Y=\left(X_1 + X_2 + X_3 \right)/3 $ を代入する。

$$
  \label{corr}
  Corr\left( X_1, Y \right) = \frac{Cov \bigl( X_1, \left(X_1 + X_2 + X_3 \right)/3\bigr)}{\sqrt{ V\left( X_1 \right) \cdot  V\bigl( \left(X_1 + X_2 + X_3 \right)/3 \bigr)} }
$$

分子の[共分散](basic_formulas.html#covariance)を展開する。

\begin{aligned}
    & Cov \bigl( X_1, \left(X_1 + X_2 + X_3 \right)/ 3 \bigr) \\\\\\\\
    &= E \bigl( X_1 \cdot \left(X_1 + X_2 + X_3 \right)/ 3 \bigr) - E\left( X_1 \right) E\bigl( \left(X_1 + X_2 + X_3 \right)/3 \bigr) \\\\\\\\
    &= 1/3 \cdot E\left(X_1^2 + X_1 X_2 + X_1 X_3 \right) - 1/3 \cdot \bigl( E\left(X_1\right)^2 + E\left(X_1\right)E\left(X_2\right) + E\left(X_1\right)E\left(X_3\right) \bigl) \\\\\\\\
    &= 1/3 \cdot \bigl( E\left( X_1^2 \right) + E\left( X_1 X_2 \right) + E\left( X_1 X_3 \right) - E\left( X_1 \right)^2 - E\left( X_1 \right)E\left( X_2 \right) - E\left( X_1 \right) E\left( X_3 \right) \bigr) \\\\\\\\
    &= 1/3 \cdot \bigl( V\left( X_1 \right) + Cov \left( X_1, X_2 \right) + Cov \left( X_1, X_3 \right) \bigr) 
\end{aligned}

ここで、$ X_1, X_2, X_3 $は無相関なので、それぞれの「共分散=0」となる。また、標準化されているので$ \bigl( V\left( X_1 \right) \bigr) = 1 $となる。つまり分子は

$$
  \label{numerator}
  = 1/3 \cdot \bigl( V\left( X_1 \right) \bigr) = 1/3 \times 1 = 1/3
$$

分母を展開する。

\begin{align}
  & \sqrt{ V\left( X_1 \right) \cdot  V\bigl( \left(X_1 + X_2 + X_3 \right)/3 \bigr)} \nonumber \\\\\\\\
  &= \sqrt{1 \times \frac{1}{9} \bigl( V\left( X_1 \right) + V\left( X_2 \right) + V\left( X_3 \right)\bigr)} \nonumber \\\\\\\\
  \label{denominator}
  &= \sqrt{1 \times \frac{3}{9}} = \sqrt{\frac{1}{3}}
\end{align}

$\left( \ref{numerator} \right)$と$\left( \ref{denominator} \right)$を用いて$\left( \ref{corr} \right)$を計算する。

\begin{aligned}
  \frac{1}{3} \div \sqrt{\frac{1}{3}} = \frac{\sqrt{3}}{3} = 0.58 //
\end{aligned}

#### Memo

  - [相関係数](basic_formulas.html#correlation_coefficient)
  - [共分散](basic_formulas.html#covariance)
  - [分散の公式](basic_formulas.html#formula_for_variance)


問8 / [15]
---
#### Point

  1. 標準化された2つの確率変数XとYは、それぞれ分散=1になる。よってXとYが独立でない場合、それらの相関係数と共分散が同じ値になる。(独立の場合は、相関係数も共分散も0)
  2. 独立でない確率変数の和の分散V(X+Y)を展開した式はどうなるか。 

#### Slution
まず、Pointの1を考える。

$$
  Corr\left( X_1, X_2 \right) = \frac{Cov \left( X_1, X_2 \right)}{\sqrt{ V\left( X_1 \right) V \left( X_2 \right)}}\\
  Corr\left( X_1, X_3 \right) = \frac{Cov \left( X_1, X_3 \right)}{\sqrt{ V\left( X_1 \right) V \left( X_3 \right)}}
$$

$X_1$も$X_2$も$X_3$も標準化さてているため、分散=1になる。また、相関係数=0.5なので、以下の式が成り立つ。

$$
  \label{corr_eq_cov}
  Corr\left( X_1, X_2 \right) = Cov \left( X_1, X_2 \right) = 0.5\\
  Corr\left( X_1, X_3 \right) = Cov \left( X_1, X_3 \right) = 0.5
$$

[14]より、$Corr\left( X_1, Y \right)$の分子を$\left( \ref{corr_eq_cov} \right)$を用いて計算すると以下になる。

\begin{align}
  Cov\left( X_1, Y \right) &= 1/3 \cdot \bigl( V\left( X_1 \right) + Cov \left( X_1, X_2 \right) + Cov \left( X_1, X_3 \right) \bigr) \nonumber \\\\\\\\
  &= 1/3 \cdot \left( 1 + 0.5 + 0.5 \right) \nonumber \\\\\\\\
  \label{numerator2}
  &= \frac{2}{3}  
\end{align}

[14]より、$Corr\left( X_1, Y \right)$の分母を展開する。その際、$X_1,X_2,X_3$は独立でない事に注意する。[分散の公式](basic_formulas.html#formula_for_variance)を参照。

\begin{align}
  & \sqrt{ V\left( X_1 \right) \cdot  V\bigl( \left(X_1 + X_2 + X_3 \right)/3 \bigr)} \nonumber \\\\\\\\
  &= \sqrt{1 \times \frac{1}{9} \bigl( V\left( X_1 \right) + V\left( X_2 \right) + V\left( X_3 \right) + 2Cov\left(X_1,X_2\right) + 2Cov\left(X_1,X_3\right)+ 2Cov\left(X_2,X_3\right)\bigr)} \nonumber \\\\\\\\
  &= \sqrt{\frac{1}{9} \left( 1 + 1 + 1 + 2 \times 0.5 + 2 \times 0.5 + 2 \times 0.5\right)} \nonumber \\\\\\\\
  \label{denominator2}
  &= \sqrt{\frac{2}{3}}
\end{align}


$\left( \ref{numerator2} \right)$と$\left( \ref{denominator2} \right)$を用いて$\left( \ref{corr} \right)$を計算する。

\begin{aligned}
  \frac{2}{3} \div \sqrt{\frac{2}{3}} = 0.82 //
\end{aligned}

#### Memo
  - [分散の公式](basic_formulas.html#formula_for_variance)


問9 / [17]
---
#### Point

  1. ```平均λが20以上のポアソン分布は、正規分布で近似```より、正規分布の確率を求める。
  2. [ポアソン分布](probability_distribution.html#poisson)の期待値と分散を思い出す。
  3. [z値](probability_distribution.html#zscore) $\sim N\left(0,1\right)$を用いて、確率を求める。


#### Slution

```参加者は平均50（人）のポアソン分布に従う```とあるので、参加者数をXとすると、条件よりXは$\mu=50$の正規分布に近似できる。  

$$
  E\left( X \right) = \lambda \\
  \color{red} V\left( X \right) = \lambda \color{black} \\
   X \sim Po\left( \lambda \right) \sim N\left(\mu, \sigma^2 \right) = N\left(50, 50 \right) \\
$$

$\overline{X}>60$の確率を求める。

$$
  p\left( \overline{X} > 60 \right) = p\left( z = \frac{60 - 50}{\sqrt{50}} > 0 \right) = p\left( z>1.42 \right) = 0.0793 //
$$

#### Memo
  - [ポアソン分布](probability_distribution.html#poisson)
  - [z値](probability_distribution.html#zscore) 
