 GBDT(Gradient Boosting Decision Tree)(此处讨论的形式针对的是回归问题)  
 1.目标函数:(不妨设样本数有n个,标签值为y_i(每个标签会对应一个特征x_i),模型预测值为\hat{y_i})  
 &emsp;&emsp;&emsp;&emsp;<a href="https://www.codecogs.com/eqnedit.php?latex=(1/n)*\sum_{i=1}^n(\hat{y_i}&space;-&space;y_i)^2" target="_blank"><img src="https://latex.codecogs.com/gif.latex?(1/n)*\sum_{i=1}^n(\hat{y_i}&space;-&space;y_i)^2" title="(1/n)*\sum_{i=1}^n(\hat{y_i} - y_i)^2" /></a>  
 

 2.训练(Boosting):  
 &emsp;&emsp;GBDT采用的是Boosting方法.  
 &emsp;&emsp;&emsp;&emsp;2.1 Boosting思想,即先拿到一个(弱)分类器进行训练最小化1中的目标函数.记作F_1(x).再取一个(弱)分类器去拟合F_1(x_i)-y_i
 (即所有样本的标签值变成了F_1(x_i)-y_i),依次类推.注意,各个分类器的参数是独立训练的.  
 
 3.GBDT独特部分  
 &emsp;&emsp;GBDT中的弱分类器都是Decision Tree（且是Cart-Tree）.  
 
 4.GBDT的分类问题  
 &emsp;&emsp;此时模型输出的值为概率值,即样本为不同类的概率.  
 
 
 5.常用搭配GBDT+LR  
  &emsp;&emsp;基于样本集对GBDT训练->再将样本导入GBDT,拿到所有样本所处的叶子节点编码->将该编码one-hot之后导入LR(logistc regression)再次训练
  ->对数据进行预测
