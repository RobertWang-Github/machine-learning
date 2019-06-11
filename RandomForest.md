
核心思想就是bagging:通过在不同训练集（由有放回抽样得到）上训练分类器,最后对这些分类器的结果进行投票(分类)或者取平均(回归),可以降低噪音,获取规律  

&emsp;&emsp;1.bootstrap sample  
&emsp;&emsp;&emsp;&emsp;设训练集大小(样本数)为N，随机且有放回地从训练集中的抽取N个训练样本（这种采样方式称为bootstrap sample方法）,如此构造M个训练集;  

&emsp;&emsp;2.
&emsp;&emsp;&emsp;&emsp;在每个构造的训练集(共M个)上,随机选择K个特征,用这K个特征生成一个Cart-Tree,不进行剪枝,让每个树最大生长至指定深度h.  

&emsp;&emsp;3.  
&emsp;&emsp;&emsp;&emsp;对这M个Cart-Tree的结果进行投票或者取平均,作为预测结果.  

tips:  
&emsp;&emsp;所谓“包外估计”(out of bag estimate)即构造训练集时,进行N次有放回抽样,某个样本不进入该构造样本集的概率.
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;<a href="https://www.codecogs.com/eqnedit.php?latex=$\lim_{N&space;\to&space;\infty}(1-1/N)^N=1/e\approx36.8\%$" target="_blank"><img src="https://latex.codecogs.com/gif.latex?$\lim_{N&space;\to&space;\infty}(1-1/N)^N=1/e\approx36.8\%$" title="$\lim_{N \to \infty}(1-1/N)^N=1/e\approx36.8\%$" /></a>  






