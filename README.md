# RandomMap
游戏地图是许多游戏不可或缺的一部分，而能够自我变化的游戏地图则更丰富了游戏的内容，例如《挺进地牢》、《以撒的结合》、《死亡细胞》等游戏都采用了随机地图这一机制，给游戏带来丰富多样的变化,也使得游戏延长了寿命。

我自己很喜欢玩，并且之后也打算制作一款利用这种机制的游戏，所以我这次就尝试用Unity制作一下生成地图的这个功能。
![思路](http://img.mcatin.com/202008031ERP3XOMPKE56R5ZB4UMNTZ.png)
1. 首先随机在地图上创建一些房间
2. 然后将他们重叠的部分进行移动并调整到合适的位置
3. 筛选出符合条件的房间，然后以每个房间的中心点为结点进行三角剖分运算后，生成最小生成树以确定连通关系
4. 最后将路径转换成曼哈顿距离的路径来完成道路的样貌。
