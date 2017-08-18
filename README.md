# svm1
利用电压数据来处理预测间隙大小
首先从问题定义出发，要知道就要得知所有和间隙有关的量，比如浓度，电压，电流，压力，各种传感器得来的数据。但这里有必要用折磨多的传感器吗
从现有的知识可以知道间隙在某个范围内是与电压成线性关系的，那么就利用电压数据来作为模型的输入，这样特征就被选定了，不需要再去提取特征
既然选择电压就要看看电压与间隙的关系。
从图中可以看出一个间隙对应着不同的电压值，当然这是万用表测出来，是一种平均电压，
这种电压变动并不是因为噪声，而是因为项目中添加的静电驱动结构，
![image](https://github.com/chenglu66/svm1/blob/master/1123.jpg)
从图中可以看出电压和间隙应该是一中非线性的关系，从下面一幅图中可以明显看出整个电压信号是呈周期过来的。因为采样10w个信号不同的信号仅有128个
![image](https://github.com/chenglu66/svm1/blob/master/正常加工电压.jpg)
下面是该波形的还原，因为电源的频率较高所以采样失真比较严重。
![image](https://github.com/chenglu66/svm1/blob/master/%E7%94%B5%E5%8E%8B%E8%BF%98%E5%8E%9F%E5%9B%BE.png)

