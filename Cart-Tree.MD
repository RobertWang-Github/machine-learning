机器学习问题中,有分类与回归两个问题.此时,针对同一个的算法,就会出现两个不同的优化目标(函数),进而有两种形式.Cart-Tree也不例外

1.Cart-Tree生成（基于训练数据）  
&emsp;&emsp;1.1.Cart-Tree是个二叉树  
&emsp;&emsp;1.2.Cart-Tree在所有(可选的)特征中遍历所有（可选的）切分点,选择使得目标函数取最小值的特征和对应的切分点,并依据此特征和切分点进行分裂.  
  
2.Cart-Tree剪枝（基于测试数据）  
&emsp;&emsp;2.1.  


Cart-Tree回归的目标函数  
离散分布p的Gini系数（集合D可以看做是样本集,其中的元素可以计算经验分布,进而可以计算Gini系数）   
<a href="https://www.codecogs.com/eqnedit.php?latex=\inline&space;$Gini(p)&space;=&space;\sum_{k=0}^K{p_k}(1-p_k)=1&space;-&space;\sum_{k=1}^K{p_k^2}$" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\inline&space;$Gini(p)&space;=&space;\sum_{k=0}^K{p_k}(1-p_k)=1&space;-&space;\sum_{k=1}^K{p_k^2}$" title="$Gini(p) = \sum_{k=0}^K{p_k}(1-p_k)=1 - \sum_{k=1}^K{p_k^2}$" /></a>

一个集合按照特征A分裂为两个集合D_1,D_2时Gini系数定义如下    
<a href="https://www.codecogs.com/eqnedit.php?latex=$Gini(D,A)&space;=&space;({D_1}/{D})Gini(D_1)&space;&plus;&space;({D_2}/{D})Gini(D_2)$" target="_blank"><img src="https://latex.codecogs.com/gif.latex?$Gini(D,A)&space;=&space;({D_1}/{D})Gini(D_1)&space;&plus;&space;({D_2}/{D})Gini(D_2)$" title="$Gini(D,A) = ({D_1}/{D})Gini(D_1) + ({D_2}/{D})Gini(D_2)$" /></a>




Cart-Tree分类的目标函数  
