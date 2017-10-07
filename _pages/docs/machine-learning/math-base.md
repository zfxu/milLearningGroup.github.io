---
title: 数学基础
layout: single
permalink: /docs/machine-learning/math-base/
author: Accepted Doge
sidebar:
  nav: "docs"
---

{% include toc %}

**本文来自知乎问题 [机器学习应该准备哪些数学预备知识？](https://www.zhihu.com/question/36324957) 下 [机器之心](https://www.zhihu.com/org/ji-qi-zhi-xin-65) 的回答。**

机器之心整理

> 本文作者依据自身经验给出了一套快速上手的可行方法及学习资源的分类汇总，机器之心在其基础上做了增益，希望对读者有所帮助。

## 先决条件

机器学习的基础是数学。数学并非是一个可选可不选的理论方法，而是不可或缺的支柱。如果你是一名计算机工程师，每天使用 UML、ORM、设计模式及其他软件工程工具／技术，那么请闭眼一秒钟，忘掉一切。这并不是说这些概念不重要，绝不是！但是机器学习需要一种不同的方法。如今 Python 如此流行的原因之一是其「原型设计速度」。在机器学习中，一种使用几行代码即可建模算法的语言绝对是必要的。

微积分、线性代数、概率论在机器学习几乎所有算法中不可或缺。如果你的数学背景很扎实，请跳过这一章节。如若不然，那么重新温习一下这些重要概念也不错。考虑到理论的数量，我并不建议大家从大部头开始。尽管一开始可以用它查询具体概念，但是初学者先关注简单的话题比较好。网上有很多好的在线资源（比如 Coursera、可汗学院或优达学城），实用且适合各种背景的人群。但是我建议从提纲之类的简明书籍上手，其中所有核心概念均被涉及，次要概念可在需要的时候自行查询。这种方法虽然不够系统，但却避免了这样的缺陷：大量晦涩概念使得没有扎实理论背景的人望而却步。

初学者最好先学习下列内容：

### 概率论

- 离散型和连续型随机变量
- 主要分布（伯努利分布、二项式分布、正态分布、 指数分布、 泊松分布、Beta 和 Gamma 分布）
- 矩估计和最大似然估计
- 贝叶斯统计
- 相关性系数和协方差（Correlation and Covariance）

### 线性代数

- 向量和矩阵
- 矩阵的行列式
- 特征向量和特征值
- 矩阵分解（如 SVD）

### 微积分

- 极限与导数
- 微分和积分
- 数值计算与最优化方法

网上有很多免费资源，比如

- 《[概率论入门](http://www.dartmouth.edu/~chance/teaching_aids/books_articles/probability_book/amsbook.mac.pdf)》，Grinstead、Snell 著
- 《[线性代数入门](http://www.stat.columbia.edu/~liam/teaching/4315-spr06/LinAlg.pdf)》，Wise、Gallagher 著
- 《[微积分入门](http://www.math.odu.edu/~jhh/Volume-1.PDF)》，Heinbockel 著

### 其它资源

维基百科上也有很多好资源，对方程、定理等进行了清晰易懂的解释。

机器之心也介绍过许多数学基础与概念：

- [基础入门：深度学习矩阵运算的概念和代码实现](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650729690&idx=2&sn=5e90776562550c882af34c5424c3bb2c&chksm=871b28a4b06ca1b2ffa71d2dbacffdecc2c2a710474f3972f3e02ec677055417a674851c3267&scene=21#wechat_redirect)
- [想了解概率图模型？你要先理解图论的基本定义与形式](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650725041&idx=1&sn=0c57ba70e2613e6af80c4ab61c996d44&chksm=871b1ecfb06c97d9547e50705d3e74a2b8c41254f0efc2dd88d2e89eec3bfac5da089f28c398&scene=21#wechat_redirect)
- [深度神经网络中的数学，对你来说会不会太难？](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650729055&idx=1&sn=2a4cf2be611cb32da5d245cb17389c1a&chksm=871b2e21b06ca73793c6e61e2eddf079711115ba9b6b232efcd31a1f191eafd22187806ab877&scene=21#wechat_redirect)
- [Reddit 热门话题：如何阅读并理解论文中的数学内容？](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650729640&idx=4&sn=947ac4fb6765797bac76ae6c6c395c14&chksm=871b28d6b06ca1c02db2790f5dae76a27c45e06ed4327779a340fbeffa9b99e08f10794716de&scene=21#wechat_redirect)

机器学习主要需要的数学基础就是微积分、线性代数、概率论，我们感觉只需要掌握大学中常见的高数、线性代数、概率论与数理统计三门课程，基本上概念的理解就没什么问题了。如果再学一点数值计算和最优化等，我们基本上就能理解机器学习的学习过程推导。

## 机器学习方法建议（面向初学者）

### 特征工程

开始机器学习的第一步是理解如何评估和改进数据集的质量。管理特征的类别和缺失、归一化和降维（PCA、ICA、NMF）是大幅提高算法性能的基本技术，而且还有助于研究如何将数据集分割成训练集和测试集、如何采取交叉验证来取代传统的测试方法。

机器之心也曾详解过特征工程如 PCA 降维算法的详细理论与推导，当然我们还介绍了其它有关特征的概念：

- [从特征分解到协方差矩阵：详细剖析和实现PCA算法](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650728723&idx=4&sn=f6277ef6c72ab3744a3915c38f372796&chksm=871b2d6db06ca47b9b8ea490627849215f7e755a5e49e55f9b7dfa9fcae78714ac9ba207f565&scene=21#wechat_redirect)
- [基于TensorFlow理解三大降维技术：PCA、t-SNE 和自编码器](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650728960&idx=1&sn=8b9e10a0c4170a136658262253c7b993&chksm=871b2e7eb06ca7681edd3243ade430853a4b83c94b323f903aa925e3a7b8a53a17bb7e69238a&scene=21#wechat_redirect) 
- [似乎没区别，但你混淆过验证集和测试集吗？](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650729251&idx=3&sn=c700055d6f78cd60c5df87bb20a1ed59&chksm=871b2f5db06ca64b94a89bcfcd91705e58be8343a79fdaf045a94a00f1184cf5d543eabe54f0&scene=21#wechat_redirect)

### Numpy：Python 数值计算之王！

使用 Python 时，Numpy 不仅仅是一个库。它是几乎所有机器学习实现的基础，因此了解它的工作原理、关注向量化和广播（broadcasting）是非常必要的。这些技术可以帮助加速大多数算法的学习过程，利用多线程和 SIMD、MIMD 架构的力量。

官方文档已经很完整了，不过，我还建议大家看一下以下资源：

- 《Python 数据科学手册：数据使用的核心工具》，VanderPlas J. 著
- 《Python 科学编程入门书》，LangTangen P. H. 著
- [维度、广播操作与可视化：如何高效使用TensorFlow](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650729714&idx=2&sn=8aac55a04ca9aabd774c8b813ea50494&chksm=871b288cb06ca19a424d929d32fd54e462dc62d3a0353960a25825f00587721d78af1640792b&scene=21#wechat_redirect)

### 数据可视化

Matplotlib 即使不是纯粹的机器学习话题，了解如何可视化数据集也很重要。Matplotlib 可能是最广泛使用的解决方案：Matplotlib 易用，允许绘制不同种类的图表。Bokeh 和 Seaborne 提供了有趣的替代方案。不必要彻底了解所有包，但是了解每一个包的优点和弱点还是很有用的，可以帮助你选择合适的包。

了解 Matplotlib 细节的资源：《掌握 Matplotlib》，McGreggor D. 著

### 线性回归

线性回归是最简单的模型之一，可以把它作为一个优化问题来研究，该问题可通过最小化均方误差而得到求解。该方法虽然有效，但是限制了可利用的可能性。我建议还可以把它当作贝叶斯问题，使用之前的可能性展示参数（比如，高斯分布），优化变成了最大似然估计（Maximum Likelihood Estimation，MLE）。即使这看起来更加复杂，但该方法提供了一个可供几十个其他复杂模型共享的新方法。

Coursera 上介绍贝叶斯统计的课程：

- 《[贝叶斯统计：从概念到数据分析](https://www.coursera.org/learn/bayesian-statistics/)》
- 《[贝叶斯统计：技术与模型](https://www.coursera.org/learn/mcmc-bayesian-statistics)》

以及这两本书：

- 《思考贝叶斯》，Downey B. A. 著
- 《黑客的贝叶斯方法》Davidson-Pilon C. 著

包括线性回归在内，机器之心曾介绍了一些解决回归问题的方法（后文提供了 CART 算法进行回归分析）：

- [初学TensorFlow机器学习：如何实现线性回归？](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650726606&idx=1&sn=c26b56e320e8abab053ad24bd73e52b6&chksm=871b24b0b06cada6da34fd3a0240acbc5614d69439bd9b5499ab3b20eb60753a7b69b9388012&scene=21#wechat_redirect) 
- [回归、分类与聚类：三大方向剖解机器学习算法的优缺点（附Python和R实现）](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650726814&idx=1&sn=7b5efae26f862b286cfc462eae133c75&chksm=871b25e0b06cacf68cf70b171e63f2373990cb7a8766e85088be2275b61262e5b185853b551b&scene=21#wechat_redirect)

### 线性分类

通常情况下，Logistic 回归是最佳起始点，也是研究信息论进而了解信息熵、交叉熵和互信息的好机会。类别交叉熵（Categorical cross-entropy）是深度学习分类中最稳定、使用最广泛的代价函数，一个简单的 logistic 回归可以展示它是如何加速学习过程的（与均方差相比）。另一个重要的话题是正则化（Ridge、Lasso 和 ElasticNet）。很多情况下，人们认为它是一种提高模型准确率的深奥方式，但是它的真实意义是更准确，在具体实例的帮助下变得易于理解。我还建议刚开始的时候，把 logistic 回归当作一个简单的神经网络，可视化（以 2D 实例为例）权重向量在学习过程中的移动轨迹。

我还建议本节应包括超参数网格搜索。网格搜索不在没有完整了解的情况下尝试不同的值，而是评估不同的超参数集的性能。因此，工程师可以将注意力集中在可达到最高准确率的组合上。当然还有更加强大的贝叶斯优化方法，即利用先验知识逼近未知目标函数的后验分布从而调节超参数的方法。

- [从头开始：用Python实现带随机梯度下降的Logistic回归](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650729997&idx=3&sn=557c6978fa2cdf1af2420d68d48edbf7&chksm=871b2a73b06ca36535713c6b5646b3e451b49fe64484e133ffaea1ac4513b2c4905aabaca34a&scene=21#wechat_redirect) 
- [如何通过牛顿法解决Logistic回归问题](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650729725&idx=3&sn=842cdf4afb9c1c6c8b0fa935b576ff41&chksm=871b2883b06ca1955bee87dcd09faef6b89088acfccd8aa10a404ad572e63de24296b709038d&scene=21#wechat_redirect)
- [拟合目标函数后验分布的调参利器：贝叶斯优化](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650729915&idx=2&sn=5da6789719cdc3785cae0034ea950934&chksm=871b29c5b06ca0d3e09f00691c0eff7f4989ed628d609c64fd9ef08266a78eedf19b8fc0d739&scene=21#wechat_redirect)

### 支持向量机（SVM）

支持向量机提供了不同的分类方法（包括线性和非线性方法）。该算法非常简单，具备基础几何知识的人也可以学会。不过，了解核支持向量机的工作原理非常有用，因为它会在线性方法失败的时候展示出其真正实力。

一些有用的免费资源：

- 《支持向量机简明教程》，Law 著
- 核函数方法，维基百科词条
- [详解支持向量机SVM：快速可靠的分类算法](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650728330&idx=2&sn=dadc2ac166249dbb600014c44077ae87&chksm=871b23f4b06caae2c1eaf4c2b81af316bb194d153d3bcb8fafb768bd04d41159922aba2efd95&scene=21#wechat_redirect)
- [详解支持向量机（附学习资源）](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650722941&idx=2&sn=328ba8aa2657217c1d90304018ba3bc6&chksm=871b1603b06c9f155faf0f1e6d6a62f9d014bcaa85f57abc9f0f9ff0ab0ac608b1749f12c170&scene=21#wechat_redirect)

### 决策树

决策树提供了另一种分类和回归的方法。通常，它们不是解决复杂问题的首选，但它们提供了完全不同的方法，即使是非技术人员也可以很容易理解，该方法还可以在会议或演示中可视化。

- [教程 | 从头开始：用Python实现决策树算法](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650723438&idx=4&sn=cf3902a9933afe08ac3c38452044cddd&chksm=871b1010b06c99062809133f3ad6279bccd64768a761a2aa6495367048069bc13788929b276a&scene=21#wechat_redirect)
- [从决策树到随机森林：树型算法的原理与实现](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650729423&idx=1&sn=7d78fbddbd79cb864e64516744224212&chksm=871b2fb1b06ca6a7dbc4f8f057f17e737d7dbc7d7ced78a2e12dcef0616f830bd50cdd1973f0&scene=21#wechat_redirect) 

### 集成学习一览

在理解了决策树的动态特性以后，研究集成训练树的集（集成）来提高整体准确率的方法很有用。随机森林、梯度树提升和 AdaBoost 都是强大的算法，且复杂度较低。对比简单的树和提升方法与 bagging 方法采用的树的学习过程挺有趣的。Scikit-Learn 提供了最常见的实现方法，但是如果你想更好地驾驭这些方法，我还是建议你在 XGBoost 上多花些时间，XGBoost 是一个既适用于 CPU 又适用于 GPU 的分布式框架，即使在较大的数据集上也能加速学习过程。

- [从Boosting到Stacking，概览集成学习的方法与性能](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650730238&idx=2&sn=18239d7ea90de70c939d704f3f8482d8&chksm=871b2a80b06ca396e3a71fdfdf9574886a776ef99971bf0be4e818c568424c2a337c6e1cd14b&scene=21#wechat_redirect)

### 聚类

当开始聚类方法的学习时，我的建议是从高斯混合算法（基于期望最大化/EM）学起。虽然 K-均值聚类要更加简单易懂（也是必须要学习的），但是高斯混合算法为我们提供了纯粹的贝叶斯方法，在其他类似任务中也十分实用。其它必学的算法还有层次聚类（Hierarchical Clustering）、谱聚类（Spectral Clustering）和 DBSCAN。这对你了解基于实例的学习或研究 K-近邻算法（既适用于有监督又适用于无监督任务）也是有帮助的。谱聚类的一个有用的免费资源是：

- 《谱聚类教程》，Von Luxburg U 著

聚类算法是无监督学习中的代表，机器之心也曾详细地介绍过各种聚类方法与实现：

- [机器理解大数据的秘密：聚类算法深度详解](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650725078&idx=1&sn=db7b6f92466bdf146ac9b0163880e42c&chksm=871b1ea8b06c97be5256dd45e14ec50c7ac984b68045e869dab44bd11cfa411fab0e954860f9&scene=21#wechat_redirect)
- [综述分类、聚类和信息提取算法在文本挖掘领域内的应用](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650729406&idx=4&sn=d7b61123116dbffa22e553ad47f0233a&chksm=871b2fc0b06ca6d6a36968dc8af17ff662ea3a71004fe7490e5fcd35d989b39494f362c3290e&scene=21#wechat_redirect) 
- [如何用Python和机器学习炒股赚钱？](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2650728678&idx=3&sn=7df9c0cb6abddb724e7e589ad5d0ea96&chksm=871b2c98b06ca58ec4b2461bf3d2be31c40943973242868e98451d623c8d361095c536bff446&scene=21#wechat_redirect)
