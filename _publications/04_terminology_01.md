---
title: "用語 / Terminology"
collection: publications
permalink: /:collection/terminology_01
excerpt: '用語をまとめています。'
date: 9999-09-30
venue:
paperurl:
citation:
---

分散分析表 / Analysis of variance table (ANOVA table)
---
### 一元分散分析 / One-Factor Analysis of Variance


| 要員<br>Factors | 平方和<br>SS| 自由度<br>DF| 不偏分散<br>U| F値<br>F-statistic| p値<br>p-value|
|:---:|:---:|:---:|:---:|:---:|:---:|
|群（Factor）|$SS_F$|$DoF_F = \mbox{群数} - 1$|$U_F = \frac{S_F}{DoF_F}$|$F = \frac{U_F}{U_E}$|
|残差（Error）|$SS_E$|$DoF_E = \mbox{全データ数} - \mbox{群数}$|$U_E = \frac{S_E}{DoF_E}$||
|全体（Total）|$SS_T = SS_F + SS_E$||||


