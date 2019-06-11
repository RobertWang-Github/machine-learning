核心思想就是bagging:通过在不同训练集上训练分类器,最后对这些分类器的结果进行投票(分类)或者取平均(回归),可以降低噪音,获取规律
&emsp;&emsp;1.bootstrap sample 
&emsp;&emsp;&emsp;&emsp;设训练集大小为N，对于每棵树而言，随机且有放回地从训练集中的抽取N个训练样本（这种采样方式称为bootstrap sample方法）,作为该树的训练集;  
&emsp;&emsp;2.
