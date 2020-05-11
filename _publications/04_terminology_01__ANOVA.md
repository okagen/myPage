---
title: "用語 : 分散分析/ Terminology : ANOVA"
collection: publications
permalink: /:collection/terminology_01_ANOVA.html
excerpt: '用語をまとめています。'
date: 9999-09-30
venue:
paperurl:
citation:
---

Table of contents
===
- [1. 分散分析 / Analysis of variance (ANOVA)](#1-%e5%88%86%e6%95%a3%e5%88%86%e6%9e%90--analysis-of-variance-anova)
  - [1.1. 分散分析表 / Analysis of variance table (ANOVA table)](#11-%e5%88%86%e6%95%a3%e5%88%86%e6%9e%90%e8%a1%a8--analysis-of-variance-table-anova-table)
- [2. 一元配置分散分析 / One-way [One-factor] analysis of variance](#2-%e4%b8%80%e5%85%83%e9%85%8d%e7%bd%ae%e5%88%86%e6%95%a3%e5%88%86%e6%9e%90--one-way-one-factor-analysis-of-variance)
  - [2.1. 分散分析表](#21-%e5%88%86%e6%95%a3%e5%88%86%e6%9e%90%e8%a1%a8)
  - [2.2. 分散分析表作成手順](#22-%e5%88%86%e6%95%a3%e5%88%86%e6%9e%90%e8%a1%a8%e4%bd%9c%e6%88%90%e6%89%8b%e9%a0%86)
- [3. 二元配置分散分析 / Two-way analysis of variance](#3-%e4%ba%8c%e5%85%83%e9%85%8d%e7%bd%ae%e5%88%86%e6%95%a3%e5%88%86%e6%9e%90--two-way-analysis-of-variance)
  - [3.1. 分散分析表](#31-%e5%88%86%e6%95%a3%e5%88%86%e6%9e%90%e8%a1%a8)
  - [3.2. 分散分析表作成手順](#32-%e5%88%86%e6%95%a3%e5%88%86%e6%9e%90%e8%a1%a8%e4%bd%9c%e6%88%90%e6%89%8b%e9%a0%86)


Contents.
===
## 1. 分散分析 / Analysis of variance (ANOVA)

  - 多群に対し多重比較する際は、まず一元配置分散分析を行い、有意性があれば多重比較を行う。2群の検定法を何度も繰り返してはいけない。
  - <font color="#ff000"> $ F = t^2 $ </font>

<a id="anova_table"></a>
### 1.1. 分散分析表 / Analysis of variance table (ANOVA table)

| 因子<br>S | 平方和<br>SS| 自由度<br>DF| 平方和平均<br>MS| F値<br>F| p値<br>P|
|:---:|:---:|:---:|:---:|:---:|:---:|
|群（Factor）or<br>群間（Between samples）|$SS_F$|$DF_F = \mbox{群数} - 1$|$MS_F = \frac{S_F}{DF_F}$|$F = \frac{MS_F}{MS_E}$|F分布表から<br>p値を求める|
|残差（Error）or<br> 郡内（Within samples） |$SS_E$|$DF_E = \mbox{全データ数} - \mbox{群数}$|$MS_E = \frac{S_E}{DF_E}$||
|全体（Total）|$SS_T = SS_F + SS_E$||||

```
S : The source of the variation in the data. 
SS : The sum of squares due to the source.
DF : The degrees of freedom in the source.
MS : The mean sum of squares due to the source.
F : The F-statistic.
P : The P-value.
```

## 2. 一元配置分散分析 / One-way [One-factor] analysis of variance

  - 検定の為の仮説は
    - $ H_0 : \mu_1 = \mu_2...= \mu_i$ 
    - $ H_1 : \mbox{not all of the } \mu_i \mbox{ are equal}$ 
  - つまり対象となった群（の中の標本）の平均に違いがあるということしか分からない。

### 2.1. 分散分析表

| 因子<br>S | 平方和<br>SS| 自由度<br>DF| 平方和平均<br>MS| F値<br>F| p値<br>P|
|:---:|:---:|:---:|:---:|:---:|:---:|
|群（Factor）or<br>群間（Between samples）|$SS_F$|$DF_F = \mbox{群数} - 1$|$U_F = \frac{S_F}{DF_F}$|$F = \frac{MS_F}{MS_E}$|F分布表から<br>p値を求める|
|残差（Error）or<br> 郡内（Within samples） |$SS_E$|$DF_E = \mbox{全データ数} - \mbox{群数}$|$U_E = \frac{S_E}{DF_E}$||
|全体（Total）|$SS_T = SS_F + SS_E$||||

### 2.2. 分散分析表作成手順
#### 2.2.1. 前提
肥料別収穫高。以下のデータが得られとする。

|肥料A|肥料B|肥料C|
|:----:|:----:|:----:|
|6.9|8.3|8.0|
|5.4|6.8|10.5|
|5.8|7.8|8.1|
|4.6|9.2|6.9|
|4.0|6.5|9.3|

#### 2.2.2. 群間の平方和を求める
全体の平均

||肥料A,B,C|
|:----:|:----:|
|平均|$ 7.20667 \fallingdotseq 7.21 $|

肥料毎に平均を求める

||肥料A|肥料B|肥料C|
|:----:|:----:|:----:|:----:|
|平均|5.34|7.72|8.56|

それぞれの群の平方和

||肥料A|肥料B|肥料C|
|:----:|:----:|:----:|:----:|
|SS|$ \left(5.34 - 7.21\right)^2 * 5 = 17.42$|$ \left(7.72 - 7.21\right)^2 * 5 = 1.32$|$ \left(8.56 - 7.21\right)^2 * 5 = 9.16$|

合計：27.897 = SS(肥)

#### 2.2.3. 残差の平方和を求める
全体の平方和を求める

|肥料A|肥料B|肥料C|
|:----:|:----:|:----:|
|$ \left(6.9 - 7.21\right)^2 \times 1 = 0.09$|1.20|0.63|
|3.26|0.17|10.85|
|1.98|0.35|0.80|
|6.79|3.97|0.09|
|10.28|0.50|4.38|

合計：45.349 ＝ SS（全体）

\begin{aligned}
  \mbox{SS(残差)} &= \mbox{SS(全体)} - \mbox{SS(肥料)} \\\\\\
  &= 45.359 - 27.897 \\\\\\
  &= 17.452
\end{aligned}

#### 2.2.4. 自由度を計算する

\begin{aligned}
  & DF\mbox(肥料) = \mbox{3列} - 1 = 2 \\\\\\
  & DF\mbox{(残差)} = DF\mbox{(全)} - DF\mbox{(肥)} = 14 - 2 = 12 \\\\\\
  & DF\mbox(全体) = \mbox{全要素数} - 1 = 15 - 1 = 14
\end{aligned}

#### 2.2.5. 分散分析表を完成

| S | SS | DF | MS| F|
|:---:|:---:|:---:|:---:|:---:|
|肥料| 27.897 | 2 |13.949|$ \frac{MS\mbox{(肥)}}{MS\mbox{(残)}}$ = 9.59|
|残差| 17.452 |12|1.454| - |
|全体|45.249|14| - | - |


## 3. 二元配置分散分析 / Two-way analysis of variance
### 3.1. 分散分析表

| S | SS | DF | MS| F| P|
|:---:|:---:|:---:|:---:|:---:|:---:|
|Factor A| $SS_A$ | $DF_A = r - 1$ | $MS_A = \frac{SS_A}{DF_A}$|$F_A = \frac{MS_A}{MS_E}$|F分布表から<br>p値を求める|
|Factor B| $SS_B$ | $DF_B = c - 1$ | $MS_B = \frac{SS_B}{DF_B}$|$F_B = \frac{MS_B}{MS_E}$|F分布表から<br>p値を求める|
|Interaction| $SS_{AB}$ | $DF_{AB} = \left( r-1 \right) \left(c - 1 \right)$ | $MS_{AB} = \frac{SS_{AB}}{DF_{AB}}$ |$F_{AB} = \frac{MS_{AB}}{MS_E}$|F分布表から<br>p値を求める|
|Error(Within) |$SS_E$|$DF_E = rc \left( n - 1 \right)$|$SS_E = \frac{SS_E}{DF_E}$||
|Total|$SS_T = SS_F + SS_E$|$DF_T = rcn-1$|||



### 3.2. 分散分析表作成手順
#### 3.2.1. 前提
肥料別、土壌別収穫高。以下のデータが得られとする。

|土壌|肥料A|肥料B|肥料C|
|:----:|:----:|:----:|:----:|
|赤土|4.1|3.1|3.5|
| 〃 |3.9|2.8|3.2|
| 〃 |4.3|3.3|3.6|
|黒土|2.7|1.9|2.7|
| 〃 |3.1|2.2|2.3|
| 〃 |2.6|2.3|2.5|

#### 3.2.2. 群間の平方和を求める
全体の平均

|土壌|肥料A,B,C|
|:----:|:----:|
|赤,黒土|$ 3.005555556 \fallingdotseq 3.006 $|

土壌毎に平均を求める

|土壌|肥料A,B,C|
|:----:|:----:|
|赤土|$ 3.533333333 \fallingdotseq 3.533 $|
|黒土|$ 2.477777778 \fallingdotseq 2.478 $|

土壌の平方和

|土壌|肥料A,B,C|
|:----:|:----:|
|赤土|$ \left( 3.533 - 3.006 \right)^2 \times 9 = 2.507 $|
|黒土|$ \left( 2.478 - 3.006 \right)^2 \times 9 = 2.507 $|

合計：5.014 = SS(土壌)

肥料毎に平均を求める

|土壌|肥料A|肥料B|肥料C|
|:----:|:----:|:----:|:----:|
|赤,黒土|3.45|2.6|2.967|

肥料の平方和

|土壌|肥料A|肥料B|肥料C|SS(肥料)|
|:----:|:----:|:----:|:----:|:----:|
|赤,黒土|$ \left(3.45 - 3.006 \right)^2 \times 6 = 1.185 $|$ \left(2.6 - 3.006 \right)^2 \times 6 = 0.986 $|$ \left(2.967 - 3.006 \right)^2 \times 6 = 0.009 $|$ 2.181 $|


#### 3.2.3. 交互作用の平方和を求める

それぞれのブロックの平均を求める

|土壌|肥料A|肥料B|肥料C|
|:----:|:----:|:----:|:----:|
|赤土|4.1|3.067|3.433|
|黒土|2.8|2.133|2.5|

それぞれのブロックの平方和を求める

|土壌|肥料A|肥料B|肥料C|
|:----:|:----:|:----:|:----:|
|赤土|$ \left(4.1 - 3.006\right)^2 \times 3 = 3.593$|$ \left(3.067 - 3.006\right)^2 \times 3 = 0.011$|$ \left(3.433 - 3.006\right)^2 \times 3 = 0.549$|
|黒土|$ \left(2.8 - 3.006\right)^2 \times 3 = 0.127 $|$ \left(2.133 - 3.006\right)^2 \times 3 =2.282 $|$ \left(2.5 - 3.006\right)^2 \times 3 = 0.767 $|

合計：7.329  よって

\begin{aligned}
  \mbox{SS(土壌、肥料)} &= 7.329 - \mbox{SS(土壌)} - \mbox{SS(肥料)} \\\\\\
  &= 7.329 - 5.013 - 2.181 \\\\\\
  &= 0.134
\end{aligned}

#### 3.2.4. 残差の平方和を求める

全体の平方和を求める

|土壌|肥料A|肥料B|肥料C|
|:----:|:----:|:----:|:----:|
|赤土|$ \left(4.1 - 3.006\right)^2 \times 1 = 1.198 $|0.0089|0.2445|
| 〃 |0.8000|0.0423|0.0378|
| 〃 |1.6756|0.0867|0.3534|
|黒土|0.0934|1.2223|0.0934|
| 〃 |0.0089|0.6489|0.4978|
| 〃 |0.1645|0.4978|0.2556|

合計：7.929  よって

\begin{aligned}
  \mbox{SS(残差)} &= \mbox{SS(全体)} - \mbox{SS(肥料、土壌)} - \mbox{SS(土壌)} - \mbox{SS(肥料)} \\\\\\
  &= 7.929 - 0.134 - 5.013 - 2.181 \\\\\\
  &= 0.6
\end{aligned}


#### 3.2.5. 自由度を計算

\begin{aligned}
  & DF\mbox(土壌) = \mbox{2行} - 1 = 1 \\\\\\
  & DF\mbox(肥料) = \mbox{3行} - 1 = 2 \\\\\\
  & DF\mbox(交互) = \left( \mbox{2行} \right) \left( \mbox{3行} - 1 \right) = 2 \\\\\\
  & DF\mbox{(残差)} = DF\mbox{(全)} - DF\mbox{(土)} - DF\mbox{(肥)} - DF\mbox{(交)} = 17 - 1 - 2 - 2 = 12 \\\\\\
  & DF\mbox(全体) = \mbox{全要素数} - 1 = 18 - 1 = 17
\end{aligned}


#### 3.2.6. 分散分析表を完成

| S | SS | DF | MS| F| P|
|:---:|:---:|:---:|:---:|:---:|:---:|
|土壌| 5.013 | 1 |5.013|$ \frac{MS\mbox{(土)}}{MS\mbox{(残)}}$ =  100.28|0|
|肥料| 2.181 | 2 |1.091|$ \frac{MS\mbox{(肥)}}{MS\mbox{(残)}}$ = 21.81| 0.0001|
|交互作用| 0.134 |2|0.672|$ \frac{MS\mbox{(交)}}{MS\mbox{(残)}}$ = 1.34| 0.298|
|残差|0.6|12|0.050| - | - |
|全体|7.929|17| - | - | - |

<font color="#ff0000"> p値の計算方法 </font>

 