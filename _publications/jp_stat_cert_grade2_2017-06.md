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


# 問11 / [23]
## Point
  1. 「ある精度で母平均を推定する為に、十分な量の標本の数を求めよ」という問題。
  2. 母集団の[変動係数](basic_formulas.html#coefficient_of_variation){:target="_blank"}が与えられている為、母平均と母分散（標準偏差）の関係が分かる。
  3. ```95%の確率で○○を±5%以下に抑える```という条件を満たすにあたり、標準正規分布にあてはめて確率を求めることを考える。つまり、まずはz値を計算することを考える。

## Slution
問題文の通りに式を組み立てると以下になる。  

$$
P\left( \left| \frac{\bar X - \mu}{\mu} \right| \leq \pm 00.5 \right) = 0.95
$$

()の中を式変換し、z値の式を作る。

$$
P\left( \left| \bar X - \mu \right| \leq \pm 00.5 \mu \right) = 0.95
$$

$$
P\left( \left| z \right| = \left| \frac{\bar X - \mu}{ \frac{\sigma}{\sqrt n}} \right| \leq \pm \frac{00.5 \mu}{\frac{\sigma}{\sqrt n}} \right) = 0.95
$$

ここで```95%の確率で・・・```は、信頼区間95%の両側検定を意味するので、標準正規分布表より以下が言える。

$$
P\left( \left| z \right| \leq 1.96 \right) = 0.95
$$

つまり

$$
\frac{00.5 \mu}{\frac{\sigma}{\sqrt n}} = 1.96
$$

$$
\sqrt n = \frac{1.96\sigma }{0.05 \mu}
$$


ここで```母変動係数が0.4```なので

$$
\frac{\sigma}{\mu} = 0.4
$$

$$
\sigma = 0.4 \mu
$$

これを代入して

$$
\sqrt n =  \frac{1.96 \times 0.4 \mu}{00.5 \mu}
$$

$$
\sqrt n =  15.68
$$

$$
n = 245.86
$$

∴ 少なくとも、n = 245.86が必要ということになる。//

## Memo