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












