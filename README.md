# 数值分析

##  第一章

##  第二章 插值法 

生成的都是n次多项式形式

### （1）拉格朗日插值

> n次插值条件：n+1个不重合节点 
> 
> Ln(x)=Σyk*lk(x)     大写的L指的是拉格朗日插值多项式   小写的l指的是插值基函数
> 
> 基函数：`lk(x)去掉本身零点作为分子，xk代入本身作为分母`  
>
> 当x = xk时，lk(x) = 1，在其他点处值为0
> 
> 缺点：每次增加新的节点都需要重新计算基函数
> 
> 拉格朗日余项 
>
> ![image](https://user-images.githubusercontent.com/94452452/142720468-f9118cf5-fe52-49ac-b56b-2db8de38ac67.png)


> n = 1 两个点 一次插值（线性插值） `直接求直线方程比较快`
>
> n = 2 三个点 二次插值（抛物线插值）
>
> ![image](https://user-images.githubusercontent.com/94452452/142719821-58ec6224-ccb8-428b-97f3-0a4e3ac32556.png)

> 举例：当 n = 1 时，这时候有两个点 
>
> 一次插值多项式如下
>
> ![image](https://user-images.githubusercontent.com/94452452/142719754-907cd6c8-5aef-42d9-805a-05478857c1a0.png)

> ![image](https://user-images.githubusercontent.com/94452452/142754842-f16c251e-d172-4a82-90c3-0286a6bd6406.png)
> 
> 这个例题说明求解插值函数可以先求误差，反推回去，还要观察函数形式，需要n+1阶导为定值
> 
> 注意：高次插值通常优于低次插值，  高次插值的精度不一定高

### （2）牛顿插值

>![image](https://user-images.githubusercontent.com/94452452/142721793-88040356-22e0-4abc-a389-cbd2d740123d.png)
>
>Nn（x）表达形式如下
>
>![image](https://user-images.githubusercontent.com/94452452/142755072-c52c6f97-69d7-44e4-bbed-3f39c5141770.png)
>
>差商（均差）
>
>![image](https://user-images.githubusercontent.com/94452452/142753597-4dda8ab2-33c5-4ee0-99e8-23bafd169619.png)
>
>![image](https://user-images.githubusercontent.com/94452452/142753632-3328bc41-dd7d-4023-abfe-1576c7d0aa79.png)

>例题
>
>![image](https://user-images.githubusercontent.com/94452452/142753668-6e8050ff-2d2b-4e87-9cf6-fce8c3b99634.png)
>
>![image](https://user-images.githubusercontent.com/94452452/142753687-ea33082e-b98f-4bf3-b02f-13dd9e633544.png)

>待补充
>1牛顿插值差分形式老师上课讲了吗？
>![image](https://user-images.githubusercontent.com/94452452/142756336-53e67a5e-31dd-4093-bb21-f8fd3a181f51.png)

### （3）埃尔米特插值

> n+1个节点 2n+2个条件 P（x）是最高次为2n+1的多项式
> 
> 一般考两点三次
> 
> ![image](https://user-images.githubusercontent.com/94452452/142862526-67a60c81-929c-4120-baba-08e9fbaff5c6.png)
> 
> 余项未看

##  第三章  

### （1）最小二乘法

就考10分，每步骤2分，大题，把雨课堂的12 13 14搞定就行

> 解题步骤
> 
> （1）线性化
> 
> （2）变量代换
> 
> （3）制表
> 
> （4）计算
> 
> （5）反代换

> 例子
> 
> ![image](https://user-images.githubusercontent.com/94452452/143236902-8a41abc2-3f8c-4e4a-bfe6-f4f7d3cc881f.png)
> 
> ![image](https://user-images.githubusercontent.com/94452452/143238315-3ef949b7-00ed-4857-b0e3-ee87c808826f.png)

##  第四章 数值积分

等距节点

### （1）代数精度(必考)

### （2）机械求积公式

### （3）矩形公式

![image](https://user-images.githubusercontent.com/94452452/143246289-b67e6d6d-8802-441c-8a4f-ec429e4e2c9b.png)

### （4）梯形公式T   n=1  m=1  

![image](https://user-images.githubusercontent.com/94452452/143411609-e96b58fc-0ac5-4e4c-a975-4b20b94d8f85.png)

![image](https://user-images.githubusercontent.com/94452452/143246451-b5842ad2-43d9-40e7-aff3-72069072ef1e.png)

### （5）辛普森公式S    n=2  m=3

![image](https://user-images.githubusercontent.com/94452452/143411742-57ca1e29-9be7-4492-ae98-7da97c81918a.png)

### （6）牛顿-科特斯公式C  n=4  m=5   n为偶数时，m=n+1

![image](https://user-images.githubusercontent.com/94452452/143411715-3a32eda4-983a-4f58-8df4-27c12eac319d.png)

> 等距节点 插值型

### （7）插值型求积公式

定理3

### （8）复合梯形公式T  

将区间n等分，每个都看做一个小的梯形，横轴为高，用梯形面积公式求解并求和

每两个点求一次梯形面积，所以头尾只用一次，中间的点用两次

![image](https://user-images.githubusercontent.com/94452452/143434926-11a864a6-2cb6-44bb-9415-c523f568cbb4.png)

![image](https://user-images.githubusercontent.com/94452452/143434903-90959d6e-167b-4d82-8d58-754f8f335301.png)

### （9）复合辛普森公式T  

每个辛普森公式可以计算两个小区间的面积（使用三个节点）

n个辛普森公式可以计算2n个小区间的面积（使用2n+1个节点）

所以需要奇数个点，偶数个小区间才可以使用复合辛普森公式

1 4 1   1 4 1   1 4 1   1 4 1   1 4 1

    1 4 1   1 4 1   1 4 1   1 4 1
    
1 4 2 4 2 4 2 4 2 4 2 4 2 4 2 4 2 4 1

![image](https://user-images.githubusercontent.com/94452452/143438044-1250dafc-16e5-44c5-b550-85cf557c4873.png)

![image](https://user-images.githubusercontent.com/94452452/143438858-69d48221-aa94-41ba-9b84-c05750e45cde.png)

上面这张图片右侧仅仅只是单个小区间的误差，还需要乘以n，得到下面这张图片中的结果

![image](https://user-images.githubusercontent.com/94452452/143551007-cfd9c76e-15ce-4f71-b542-f8217788b34b.png)

### （10）龙贝格求积公式

![image](https://user-images.githubusercontent.com/94452452/143553698-ba85eae9-b56f-42ee-979a-dd0b96a71aeb.png)

梯形变步长计算思路：首先选定初值n和h，计算出Tn，然后步长折半，原本的值取一半，加上现有的步长（或者之前步长的一半）乘以多出来的节点函数值之和

![image](https://user-images.githubusercontent.com/94452452/143568629-39597670-0ef4-4d87-8357-4d0d72a2a4eb.png)

![image](https://user-images.githubusercontent.com/94452452/143570229-690c33e3-c6ab-4165-bc3f-e8fb06db9e7f.png)

> 以上均为等距节点

### （11）高斯型积分 

只会涉及到`定义，非等距节点`

将节点 x0 … xn 以及系数 A0 … An 都作为待定系数。令 f (x) = 1, x, x2, …, x2n+1 代入可求解，得到的公式具有2n+1 次代数精度

总结：关于代数精度，讲到n+1个等距节点时，代数精度为n；n+1个非等距节点，此时节点的横坐标都未知，共计2n+2个未知数，所以代数精度为2n+1

##  第五章 解线性方程组的直接方法（直接法）

第五章和第六章仅仅针对于唯一解的情形

直接法：没有截断误差，不考虑舍入误差的话，得到的是精确解

### （1）高斯消元法  `待定列主元消去法`

> 下三角元素消为0，然后先算xn，再回代算xn-1直到x1，不需要背公式
> 
> 要求：顺序主子式均不为0 <=> 主元均不为0
> 
>       主元不能太小
>       
> 列主元素法：考大题浪费，估计考选择填空，问到第几步时应该交换哪一行和哪一行，交换原则：找到主元值最大的进行交换

行变换相当于左乘初等矩阵

### （2）LU分解（杜利特尔分解）

A=LU   U是上三角矩阵  L是对角线元素为1的下三角矩阵

要求：整个操作中不进行换行操作，分解唯一存在的条件是顺序主子式均不为0 可以参考书本课后习题第11题

Ax=b  ==>   LUx=b  令Ux=y 则Ly=b   这样做是因为LU都是三角矩阵，计算x和y都只需进行回代的操作

> LU的求解过程
> 
> 第一步：L的主对角线元素全部为1
> 
> 第二步：U的第一行为A的第一行
> 
> 第三步：U一行，L一列

示例：

> 1 2 3          1 0 0          1   2    3
> 
> 2 5 2    =     2 1 0      *   0   1   -4
> 
> 3 1 5          3 5 -1         0   0  -24

### （3）平方根法（楚列斯基分解）

分解之后的LU互为转置关系 此时的L并非主对角线元素为1

平方根法是数值稳定的，LU分解不一定

要求：A对称且正定

### （4）追赶法

要求：A为三对角矩阵

生成的L是下二对角矩阵，U是对角线元素为1的上二对角矩阵

### （5）范数 向量范数 矩阵范数



##  第六章 解线性方程组的迭代法（迭代法）















