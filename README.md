# multi-label-classification-on-sound-track
machine learing practice

## Goal
the task is to annotate or tag a sound with descriptive (semantic) keywords.  This kind of content-based tagging system could be useful to musicians and sound engineers who want to automatically organize their sound library, or search for sounds by keyword.

## Evaluation of Tagging
For evaluation, you will predict the presence/absence of tags for each test sound. The evaluation metric is "Mean column-wise AUC".  AUC is the area under the ROC curve, which plots FPR vs TPR.  "Mean column-wise" computes the average of the AUCs for the tags.  To compute AUC, you will need to predict the score of each label (e.g., decision function value, probability, etc.) rather than the label.


1、前置知识： 多标签分类----每个数据可能同时被分到多个类别

2、对声波的梅尔倒频谱mfcc进行聚类处理（多少种声音） 并对每种聚类进行词袋处理生成bag-of-sound（类似于处理文本）再用tfidf进行特征提取，最后训练多标签分类器进行分类

3、聚类尝试了 kmeans、gmm、dbscan等，分类器使用了nn、cnn、lstm、rnn、mlp及随机森林

