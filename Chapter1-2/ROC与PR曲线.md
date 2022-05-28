### ROC
ROC曲线的**纵轴**是"**真正例率**" (True Positive Rate，简称**TPR**) ，**横轴**是"**假正例率**" (False Positive Rate，简称**FPR**) ，基于表2.1 中的符号

![image](https://user-images.githubusercontent.com/88269254/170818580-7fdc8861-9fc7-41d7-ab1e-c48a7d3d46ca.png)

![image](https://user-images.githubusercontent.com/88269254/170818608-fcffbf78-41c7-40db-aa65-22f159af2693.png)

机器学习中ROC曲线图的画图逻辑？

给定m<sup> + </sup>个正例和m<sup> - </sup>个反例，根据学习器预测结果对样例进行排序，然后把分类阈值设为最大，即把所有样例均预测为反例，此时真正例率和假正例率均为0，在坐标(0,0) 处标记一个点。然后，将分类阈值依次设为每个样例的预测值，即依次将每个样例划分为正例。设前一个标记点坐标为(x,y)，当前若为真正例，则对应标记点的坐标为(x,y+1/m<sup> + </sup>) ;当前若为假正例，则对应标记点的坐标为(x+1/m<sup> - </sup>,y) ，然后用线段连接相邻点即得。


![image](https://user-images.githubusercontent.com/88269254/169699287-08d944ed-b67b-418d-b0f8-b242967eff29.png)

### P-R曲线
**查全率P=TP/(TP+FP)**

**查准率R=TP/(TP+FN)**

P-R曲线则是直观地显示了学习器在样本总体上的查全率和查准率，**横轴是查全率，纵轴是查准率**。有人提出过“**平衡点**”，也就是**查准率=查全率**时的取值，如图，是用来衡量模型的好坏。

![image](https://user-images.githubusercontent.com/88269254/169698791-834f1b3c-cc4d-4683-9afd-8a6fe6392483.png)
