# 数值分析

##  第一章

##  第二章 插值法 

生成的都是n次多项式形式

### 拉格朗日插值

> n次插值条件：n+1个不重合节点 
> 
> Ln(x)=Σyk*lk(x)     大写的L指的是拉格朗日插值多项式   小写的l指的是插值基函数
> 
> 基函数：`lk(x)去掉本身零点作为分子，xk代入本身作为分母`  
>
> 当x = xk时，lk(x) = 1，在其他点处值为0
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





