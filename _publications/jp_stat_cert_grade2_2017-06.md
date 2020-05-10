---
title: "統計検定 2級 2017年6月 (完成度 0.5/35)"
collection: publications
permalink: /:collection/jp_stat_cert_grade2_2017-06.html
excerpt: '統計検定 2級 2017年6月実施問題の解き方'
date: 2017-06-17
venue:
paperurl:
citation:
---

# Table of contents

- [問11 / [23]](#%e5%95%8f11--23)
- [問14 / [30]](#%e5%95%8f14--30)

-------------------------
# 解き方

問11 / [23]
---
#### Point
  1. 「ある精度で母平均を推定する為に、十分な量の標本の数を求めよ」という問題。
  2. 母集団の[変動係数](basic_formulas.html#coefficient_of_variation){:target="_blank"}が与えられている為、母平均と母分散（標準偏差）の関係が分かる。
  3. ```95%の確率で○○を±5%以下に抑える```という条件を満たすにあたり、標準正規分布にあてはめて確率を求めることを考える。つまり、まずはz値を計算することを考える。

#### Slution
問題文の通りに式を組み立てると以下になる。  

$$
P\left( \left| \frac{\bar X - \mu}{\mu} \right| \leq \pm 00.5 \right) = 0.95 \nonumber
$$

$\left( \right)$ の中を式変換し、z値の式を作る。

\begin{align}
  P\left( \left| \bar X - \mu \right| \leq \pm 00.5 \mu \right) &= 0.95 \nonumber \\\\\\\\
  \label{zScore1}
  P\left( \left| z \right| = \left| \frac{\bar X - \mu}{ \frac{\sigma}{\sqrt n}} \right| \leq \pm \frac{00.5 \mu}{\frac{\sigma}{\sqrt n}} \right) &= 0.95
\end{align}

ここで```95%の確率で・・・```は、信頼区間95%の両側検定を意味するので、標準正規分布表より以下が言える。

$$
\label{zScore2}
P\left( \left| z \right| \leq 1.96 \right) = 0.95
$$

つまり$\left( \ref{zScore1} \right)$と$\left( \ref{zScore2} \right)$ より

\begin{align}
  \frac{00.5 \mu}{\frac{\sigma}{\sqrt n}} &= 1.96 \nonumber \\\\\\\\
  \label{sqrtN}
  \sqrt n &= \frac{1.96\sigma }{0.05 \mu}
\end{align}

ここで```母変動係数が0.4```なので

\begin{align}
  \frac{\sigma}{\mu} &= 0.4 \nonumber \\\\\\\\
  \label{sigma}
  \sigma &= 0.4 \mu
\end{align}

$(\ref{sigma})を(\ref{sqrtN})$に代入して

\begin{align}
  \sqrt n &= \frac{1.96 \times 0.4 \mu}{00.5 \mu} = 15.68 \nonumber \\\\\\\\
  n &= 245.86
\end{align}

$\therefore$ 少なくとも、n = 245.86が必要ということになる。//

#### Memo
  - [変動係数](basic_formulas.html#coefficient_of_variation){:target="_blank"}
  - 標準化
  - 信頼区間


問14 / [30]
---
#### Point
  - 分散分析表を見て[不偏分散](basic_formulas.html#unviased_variance){:target="_blank"}を求める問題。
  - 母数は```20店舗```であることを念頭に、自由度、平方和を求める。


#### Solution

$$
\begin{align*}
\frac{\partial \theta}{\partial t}= \frac{\partial}{\partial z}
\left[ K(\theta) \left (\frac{\partial \psi}{\partial z} + 1 \right) \right]\ \\

\frac{\partial \theta}{\partial t}= \frac{\partial}{\partial z}
\left[ K(\theta) \left (\frac{\partial \psi}{\partial z} + 1 \right) \right]\

\end{align*}
$$



全体の平方和を求める。。。

$$
\begin{align*}
  全平方和 &= 群間平方和（地域）+ 群内平方和（残差平方和）\ \\
  &= 0.2204 + 0.3370
\end{align*}
$$

不偏分散を求める。

$$
  \frac{0.2204 + 0.3370}{20 - 1} = 0.0293
$$


$\therefore$ 0.0293 //

#### Memo


