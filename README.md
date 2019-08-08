# Customer-dispute-analysis

## 目的
將未經分類的消保投訴資料整理分群並且可以為新進的資料快速歸類

## 作法
1. 利用 cosine similarity 對資料本身做相似度分群,比對方式為

EX : 中國信託商業銀行 , 中國信託  => ['中國','信託','商業銀行'] , ['中國','信託']

將兩個list串接起來 => ['中國','信託','商業銀行']

利用 vector 表示成 [ 1  1  1 ] ,  [ 1  1  0 ]

然後在做 cosine similarity , 算出來 >= 0.5 即分為同一群

最後得到的初步分群結果除了可以拿來用作 k-means 的 k 外, 還可以大致理解資料分布情形

Cosine Similarity :
![](https://i.imgur.com/jEGbGyG.png)

## 工具

1. Code with jupyter notebook (python 3.7)
2. pandas
3. jieba
4. Math
