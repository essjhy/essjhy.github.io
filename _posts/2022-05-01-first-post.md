---
title: Post test
author: Chris
layout: post
---
## 多元函数微分学

1. 对于一元函数 $y=f(x)$,它在一点$x_0$有导数，则意味着它在该点一定是连续的。对于二元函数，在一点 $(x_0,y_0)$ 对于$x$和$y$的偏导数存在不能推出它在该点连续，例如$u=sgn(xy)$在$(0,0)$处。（偏导数存在并不代表可微）

同样，连续并不代表偏导数存在，这点是显然的。例如$y=\begin{cases}\displaystyle\frac{x^2+y^2}{\abs{x}+\abs{y}}\ (x,y)\neq(0,0)
\\ 0 \ (x,y)=(0,0)
\end{cases}$

2. 若函数$f(x,y)$在$(x_0,y_0)$点可微，则该函数在 $(x_0,y_0)$点连续，且在$(x_0,y_0)$点的两个偏导数存在

注意记号$\Delta z=A\Delta x+B\Delta y+o(\rho),dz=A\Delta x+B\Delta y$,能写成这样的形式说明可微：等价命题，$\exist A,B$使得$o(\rho)=\Delta z-A\Delta x-B\Delta y$

3. **可微的充分条件** 若函数 $z=f(x,y)$ 的偏导数 $f_x(x,y)$ 和 $f_y(x,y)$ 在点 $(x_0,y_0)$ 的某个临域内存在，且这两偏导数在 $(x_0,y_0)$ 处连续，则函数$f(x,y)$在$(x_0,y_0)$点可微

若$D$是$\bold{R}^2$中的一个区域，而$f\in C^1(D)$ ,则 $f$ 在 $D$ 内可微

注意以下例子：
$f(x,y)=\sqrt{\abs{xy}}$在$(0,0)$连续， $f_x(0,0)$ 和 $f_y(0,0)$存在，但在此点不可微

**证明不可微的方法**：
1.若两个偏导数不存在，那显然不可微（当然首先要验证函数是连续的）

2.若两个偏导数存在，则$o(\rho)=\Delta z-f_x(x_0,y_0)\Delta x-f_y(x_0,y_0)\Delta y$验证此式可知是否可微（验证是否是$o(\rho)$）

（**但是只要偏导数在此点连续就必定可微**）

对于初等函数来说，偏导数存在就必定可微

4. 若函数$f(x,y)$的两个混合偏导数$f_{xy}(x,y)$和$f_{yx}(x,y)$在区间$D$内连续，则在该区域内这两个二阶偏导数必相等，即：$f_{xy}(x,y)=f_{yx}(x,y),\ \forall(x,y)\in D$

混合偏导数不相等的例子：$f(x,y)=\begin{cases}\displaystyle\frac{(x^2-y^2)xy}{x^2+y^2}\ (x,y)\neq(0,0)
\\ 0 \ (x,y)=(0,0)
\end{cases}$

5. 偏微分链式法则的要求：$z=f(u,v)$在相应的点$(u,v)$处对$u,v$的偏导数存在且连续，且$u=\phi(x,y)$和$v=\rho(x,y)$在点$(x,y)$处偏导数存在
6. 高阶微分概念理解：$\text{d}f=f_x(x,y)\text{d}x+f_y(x,y)\text{d}y$

$\text{d}(\text{d}f)=\displaystyle\frac{\partial}{\partial x}(f_x(x,y)\text{d}x+f_y(x,y)\text{d}y)dx+\displaystyle\frac{\partial}{\partial y}(f_x(x,y)\text{d}x+f_y(x,y)\text{d}y)dy$

于是有$\text{d}(\text{d}f)=f_{xx}(x,y)\text{d}x^2+f_{xy}(x,y)\text{d}x\text{d}y+f_{yx}(x,y)\text{d}y\text{d}x+f_{yy}(x,y)\text{d}y^2$

如果$f\in C^n(D)$,则$f$在区域$D$内的$n$阶微分可以写为：$\text{d}^nf=(\displaystyle\text{d}x\frac{\partial}{\displaystyle\partial x}+\text{d}y\frac{\partial}{\partial y})^nf$并且微分算子$\text{d}$可以作二项式展开

7. <img src="img/截屏2021-12-22 下午8.33.13.png" alt="截屏2021-12-22 下午8.33.13"  />

8. 二元函数的泰勒公式：设$D\subset\bold{R}^2$为一区域，而函数$f(x,y)\in C^{n+1}(D)$。又设$P_0(x_0,y_0)\in D,P_1(x_0+\Delta x,y_0+\Delta y)\in D$，且$P_0$至$P_1$的连线$\overline{P_0P_1}\subset D$，则有**二元函数的带拉格朗日余项的泰勒公式**

$f(x_0+\Delta x,y_0+\Delta y)=\displaystyle{f(x_0,y_0)+\frac{1}{1!}\text{d}f(x_0,y_0)+\frac{1}{2!}\text{d}^2f(x_0,y_0)+\cdots+\frac{1}{n!}\text{d}^nf(x_0,y_0)+\frac{1}{(n+1)!}\text{d}^{n+1}f(x_0+\theta \Delta x,y_0+\theta \Delta y)}$

最后一项$R_n=\displaystyle\frac{1}{(n+1)!}\text{d}^{n+1}f(x_0+\theta \Delta x,y_0+\theta \Delta y)$被称为拉格朗日余项，它可以用n+1阶的偏导数估计

**注意**:一元函数泰勒公式只要求$f$的$n+1$阶导数存在，不要求$n+1$阶导数连续。二元函数泰勒公式要求$f$的$n+1$阶偏导数存在且连续，即要求$n+1$阶可微。

另外，当泰勒公式中的项数固定而$\rho=\sqrt{\Delta x^2+\Delta y^2}\rightarrow0$,这时有$R_n=o(\rho^n)$便得到**二元函数的带佩亚诺余项的泰勒公式**（条件可放松至n阶偏导数连续）

$f(x_0+\Delta x,y_0+\Delta y)=\displaystyle{f(x_0,y_0)+\frac{1}{1!}\text{d}f(x_0,y_0)+\frac{1}{2!}\text{d}^2f(x_0,y_0)+\cdots+\frac{1}{n!}\text{d}^nf(x_0,y_0)+o(\rho^n)}$

根据高阶微分的定义，称多项式$\displaystyle{f(x_0,y_0)+\frac{1}{1!}\text{d}f(x_0,y_0)+\frac{1}{2!}\text{d}^2f(x_0,y_0)+\cdots+\frac{1}{n!}\text{d}^nf(x_0,y_0)}$为**泰勒多项式**（作为$\Delta x=(x-x_0)$和$\Delta y=(y-y_0)$的多项式）

9. **隐函数存在性定理**（对多元函数可以类推，要求点函数值为0和领域偏导数连续以及因变量偏导数不为0）

设函数$F(x,y)$在一点$P_(x_0,y_0)$的领域内有定义，且满足下列条件：（1）$F(x_0,y_0)=0$；（2）$F_x(x,y)$及$F_y(x,y)$连续，且$F_y(x_0,y_0)\neq0$。则在$x_0$的某领域$(x_0-\delta,x_0+\delta)$内存在一个函数$y=f(x)$，使得$y_0=f(x_0)$且$F(x,f(x))\equiv0,\forall x\in(x_0-\delta,x_0+\delta)$，并且$y=f(x)$在$(x_0-\delta,x_0+\delta)$内有连续的导函数，其导数可由$F_x$和$F_y$表示：$f'(x)=-\displaystyle\frac{F_x(x,y)}{F_y(x,y)}$

10. 另一种求隐函数偏导数的方法:将$F(x,y,z)=0$中的$z$视作$(x,y)$的函数，对$x$（或者$y$）求偏导，再从所得式中解出$z_x$和$z_y$
11. 对于多元函数求隐函数的方法:将因变量视作自变量的函数求偏导即可，只要偏导数可解出即存在（分母不为0:雅可比行列式不为0）
12. **逆映射的存在性定理**：设函数$x=x(u,v)$和$y=y(u,v)$在$(u_0,v_0)$的一个领域内有连续的一阶偏导数，且其雅可比行列式$\displaystyle\frac{D(x,y)}{D(u,v)}\Bigg|_{(u_0,v_0)}=\left|\begin{matrix}x_u(u_0,v_0) &x_v(u_0,v_0)\\y_u(u_0,v_0) &y_v(u_0,v_0)\end{matrix}\right|\neq0$.又设$x_0=x(u_0,v_0)，y_0=y(u_0,v_0)$，则在$(x_0,y_0)$的一个邻域内存在函数$u=u(x,y)$和$v=v(x,y)$且映射$(x,y)\rightarrow(u(x,y),v(x,y))$是$(u,v)\rightarrow(x(u,v),y(u,v))$的逆映射。

**推论：**一个连续可微映射的雅可比行列式若在一点不为0，则映射在该点附近是一一映射.

13. 对于雅可比行列式，有关系：$\displaystyle\frac{D(x,y)}{D(u,v)}\Bigg|_{(u_0,v_0)}=\displaystyle{1\Big/\frac{D(u,v)}{D(x,y)}\Bigg|_{(x_0,y_0)}}$证明方法是对$(x,y)\rightarrow(u(x,y),v(x,y))$的转换关系求偏导

14. 一阶全微分的形式不变性的应用：设由$x=u+v,y=u^2+v^2,z=u^3+v^3$确定函数$z=z(x,y)$，求当$x=0,y=u=\displaystyle\frac{1}{2},v=-\displaystyle\frac{1}{2}$时，$\displaystyle\frac{\partial z}{\displaystyle\partial x}$和$\displaystyle\frac{\partial z}{\partial x}$的值。（提示：利用$\text{d}z=z_x\text dx+z_y\text dy$求解）

15. 函数极值的必要条件：若$f(x,y)$在点$(x_0,y_0)$处达到极值，且$f_x(x_0,y_0)$和$f_y(x_0,y_0)$存在，则必有$f_x(x_0,y_0)=f_y(x_0,y_0)=0$.

16. 函数极值的充分条件：设$z=f(x,y)$在$(x_0,y_0)$的一个领域内有**连续的二阶偏导数**（二阶可微），且有$f_x(x_0,y_0)=f_y(x_0,y_0)=0$.令$A=\displaystyle{\frac{\partial^2f}{\partial x^2}(x_0,y_0)},B=\displaystyle{\frac{\partial^2f}{\partial x\partial y}(x_0,y_0)},C=\displaystyle{\frac{\partial^2f}{\partial y^2}(x_0,y_0)}$。若$B^2<AC$,则当$A>0$时，$f(x_0,y_0)$是极小值；而当$A<0$时，$f(x_0,y_0)$是极大值

    （注记：假定设$z=f(x,y)$在$(x_0,y_0)$的一个领域内有**连续的二阶偏导数**，且有$f_x(x_0,y_0)=f_y(x_0,y_0)=0$（是稳定点）.若$B^2>AC$,则$f(x_0,y_0)$一定不是极值；若$B^2=AC$,则$f(x_0,y_0)$可能是极值，也可能不是。)

17. **拉格朗日乘数法 or $\lambda$乘子法** 求函数$z=f(x,y)$在约束条件$\phi(x,y)=0$下的极值点，做辅助函数$F(x,y,\lambda)=f(x,y)+\lambda\phi(x,y)$。然后解方程组$\begin{cases}F_x(x,y,\lambda)=f_x(x,y)+\lambda\phi_x(x,y)=0\\F_y(x,y,\lambda)=f_y(x,y)+\lambda\phi_y(x,y)=0\\F_\lambda(x,y,\lambda)=\phi(x,y)=0\end{cases}$,设法消去$\lambda$而得到$(x,y)$的解，它们便是条件极值的稳定点，再判断此稳定点是否是条件极值点。

    （注记：对于多限制条件推广，设多个$\lambda_i$即可）

18. **曲面的参数方程**：若在一个平面区域$D$上有三个连续函数$x(u,v),y(u,v),z(u,v)$，其中$(u,v)$在$D$中变动，那么由$\begin{cases}x=x(u,v)\\y=y(u,v)\\z=z(u,v)\end{cases},(u,v)\in D$所确定的点$(x,y,z)$的集合称作一张曲面。这个方程称作曲面的**参数方程**，而$(u,v)$称为相应点的参数

19. **正则曲面**要求参数与曲面上的点一一对应，以及$x(u,v),y(u,v),z(u,v)$有连续偏导数，并且$\bold{r}_u=(x_u(u,v)+y_u(u,v)+z_u(u,v))$与$\bold{r}_v=(x_v(u,v)+y_v(u,v)+z_v(u,v))$不共线，也即$\bold{r}_u\times\bold{r}_v\neq0$.后面的条件实际上相当于保证了曲面处处有切平面，且切平面连续变动。

20. 对曲面$F(x,y,z)=0$在$(x_0,y_0,z_0)$处的**切平面**的法向量为$\bold{n}=(F_x(x_0,y_0,z_0),F_y(x_0,y_0,z_0),F_z(x_0,y_0,z_0))$（证明：将过此点的任意一条光滑曲线写为参数方程代入曲面方程，并求微分，得到所有曲线的切线均与$\bold{n}$垂直

    切平面方程为：$F_x(x_0,y_0,z_0)(x-x_0)+F_y(x_0,y_0,z_0)(y-y_0)+F_z(x_0,y_0,z_0)(z-z_0)=0$

    法线方程为：$\displaystyle\frac{x-x_0}{F_x(x_0,y_0,z_0)}=\displaystyle\frac{y-y_0}{F_y(x_0,y_0,z_0)}=\displaystyle\frac{z-z_0}{F_z(x_0,y_0,z_0)}$

21. 对于由参数方程表达出来的曲面$S：\begin{cases}x=x(u,v)\\y=y(u,v)\\z=z(u,v)\end{cases},(u,v)\in D$，

    只需考虑$S$上过$P_0(x(u_0,v_0),y(u_0,v_0,z(u_0,v_0))$的两条特殊曲线$l_1：\begin{cases}x=x(u,v_0)\\y=y(u,v_0)\\z=z(u,v_0)\end{cases},l_2：\begin{cases}x=x(u_0,v)\\y=y(u_0,v)\\z=z(u_0,v)\end{cases}$的切向量，

    法向量$\bold{n}$与它们都垂直，于是$\bold{n}|_{(u_0,v_0)}=\bold{r}_u\times\bold{r}_v|_{(u_0,v_0)}=\left|\begin{matrix}\bold{i}&\bold{j}&\bold{k}\\x_u&y_u&z_u\\x_v&y_v&z_v\end{matrix}\right|_{(u_0,v_0)}$.

    若用雅可比行列式书写，法向量为$\bold{n}=\displaystyle{\left(\frac{D(y,z)}{D(u,v)},\frac{D(z,x)}{D(u,v)},\frac{D(x,y)}{D(u,v)}\right)\Bigg|_{(u_0,v_0)}}$.

    切平面方程$(\bold{r}-\bold{r}_0)\bold\cdot\bold n=0$,用行列式表达即是：$\left|\begin{matrix}x-x_0&y-y_0&z-z_0\\x_u&y_u&z_u\\x_v&y_v&z_v\end{matrix}\right|=0$.

### ppt补充内容

1. **多元函数的极限定义**(扩充)

$f$是集合$E$上的函数，$P_0$是$E$的聚点。若对$\forall\epsilon>0,\exist\delta>0$使得当$P\in D$且满足$0<d(P,P_0)<\delta$时，有$|f(P)-A|<\epsilon$，则称$P\rightarrow P_0$时，$f(P)$以$A$为极限，记为$\lim_{P\rightarrow P_0}f(P)=A$

2. **一元复合函数的极限**的细节(注意定义域问题)

设$\lim_{x\rightarrow x_0}g(x)=y_0,$且$x\neq x_0$时，$g(x)\neq y_0$,若$\lim_{y\rightarrow y_0}f(y)=A$,则有$\lim_{x\rightarrow x_0}f(g(x))=A$

设$\lim_{x\rightarrow x_0}g(x)=y_0,$若$\lim_{y\rightarrow y_0}f(y)=A=f(y_0)$,则有$\lim_{x\rightarrow x_0}f(g(x))=A$（对$f$要求连续，对$g$要求有极限）

3. **夹逼定理**例

$f(x,y)=\displaystyle\frac{x^m\cdot y^n}{(x^2+y^2)^{\frac{k}{2}}},m+n>k$时，极限$lim_{(x,y)\rightarrow(0,0)}f(x,y)$存在（极限为0）。$m+n\leq k$时上述极限不存在（反例取$y=ax$即可）

4. 二元初等函数：从$x,y$出发进行有限次的加、减、乘、除、与一元初等函数复合得到的函数。

定理：二元初等函数在其定义域内连续（定义域的内点都是连续点）

5. **有界闭区域上的连续函数有界**：设$\overline{D}$是有界闭区域，$f\in C(\overline{D})$，则$f$在$\overline D$上有界，即存在$M>0$,使得$|f(P)|\leq M,\forall P\in D$.（且最大最小值存在且介值定理成立）
6. 若$f(x,y)$的两个混合偏导数$f_{xy}$和$f_{yx}$在区域$D$内连续，则$f_{xy}(x,y)=f_{yx}(x,y),\forall(x,y)\in D$.（记$C^n(D)$为$D$上所有$k(k\le n)$阶偏导数连续的函数构成的集合，类似的可交换性质可推广到更高阶导数）

证明：考虑$H=(\Delta x,\Delta y)=f(x_0+\Delta x,y_0+\Delta y)-f(x_0,y_0+\Delta y)-f(x_0+\Delta x,y_0)+f(x_0,y_0)$（排除$\Delta x,\Delta y,(\Delta x)^2,(\Delta y)^2$的影响）考虑两种不同的一元函数展开方式

7. **可微函数偏导数不一定连续**(与一元函数类似)如对：$f(x,y)=\begin{cases}(x^2+y^2)\sin{\displaystyle{\frac{1}{x^2+y^2}}},(x,y\neq(0,0)\\0,(x,y)=(0,0)\end{cases}$

   偏导数为$f_x(x,y)=\begin{cases}2x\sin{\displaystyle{\frac{1}{x^2+y^2}}}-\displaystyle\frac{2x}{x^2+y^2}\cos{\displaystyle{\frac{1}{x^2+y^2}}},(x,y)\neq(0,0)\\0,(x,y)=(0,0)\end{cases}$

   **某点连续的函数在此点偏导数不一定存在**：如$f(x,y)=\sqrt{x^2+y^2}$

8. **二元函数的微分中值定理**：设$z=f(x,y)\in C^1(D),P_0(x_0,y_0),P_1(x_0+\Delta x,y_0+\Delta y)\in D$且$\overline{P_0P_1}\subset D$.则存在$\theta\in(0,1)$,使得$\displaystyle{f(x_0+\Delta x,y_0+\Delta y)=f(x_0,y_0)+\frac{\partial f}{\partial x}(x_0+\theta \Delta x,y_0+\theta\Delta y)\Delta x+\frac{\partial f}{\partial y}(x_0+\theta \Delta x,y_0+\theta\Delta y)\Delta y}$

注：设$\overline{\Delta P}=\overline{P_0P_1}$，中值公式可以写为$f(P_1)=f(P_0)+\grad f|_{P_0+\theta\overline{\Delta P}}\cdot\overline{\Delta P}$或者$f(P_1)=f(P_0)+\displaystyle\frac{\partial f}{\partial \overline{\Delta P}}\Bigg|_{P_0+\theta\overline{\Delta P}}\cdot\big|\overline{\Delta P}\big|$

### 解题指南补充内容

1. 已知函数$\text dz=P\text dx+Q\text dy$求$z$

方法1:凑全微分法；

方法2:不定积分法：由$\displaystyle{\frac{\part z}{\part x}=P(x,y)}$对$x$积分得到$z=\int P(x,y)\text dx+C(y)$,再由$\displaystyle{\frac{\part z}{\part y}=Q(x,y)}$求得$C'(y)$,最后求得$C(y)$即求得$z(x,y)$.

## 向量代数与空间解析几何

1. **点到平面的距离方程**:平面$Ax+By+Cz+D=0$,点$P(x_1.y_1,z_1)$

$d=\displaystyle\frac{|\overrightarrow{P_0P_1}\cdot\bold{n}|}{|\bold{n}|}=\displaystyle\frac{|Ax_1+By_1+Cz_1+D|}{|\sqrt{x^2+y^2+z^2}|}$（平行平面距离类似）

2. 平面：

**一般式方程**$Ax+By+Cz+D=0$;

**点法式方程**$A(x-x_0)+B(y-y_0)+C(z-z_0)=0$

**截距式方程**$\displaystyle{\frac{x}{-\frac{D}{A}}+\frac{y}{-\frac{D}{B}}+\frac{z}{-\frac{D}{C}}}=1$（要求$D\neq0$且补充定义$A$或$B$或$C$为0的情况)

**三点式方程**：$P_1(x_1,y_1,z_1),P_2(x_2,y_2,z_2),P_3(x_3,y_3,z_3)$,平面上的点$P$需满足：$\overrightarrow{P_1P}\cdot(\overrightarrow{P_1P_2}\times\overrightarrow{P_1P_3})=0$

把混合积写成坐标形式：$\left|\begin{matrix}x-x_1&y-y_1&z-z_1\\x_2-x_1&y_2-y_1&z_2-z_1\\x_3-x_1&y_3-y_1&z_3-z_1\end{matrix}\right|=0$,能张成平面的充要条件：$\overrightarrow{P_1P_2}\times\overrightarrow{P_1P_3}\neq0$

3. 直线：

**两面式方程**或**一般方程**由两个平面方程联立给出（交线）

**参数方程**$\begin{cases}x-x_0=ta\\y-y_0=tb\\z-z_0=tc\end{cases},(-\infty<t<+\infty)$,方向向量$\bold{e}=(a,b,c)$

**标准方程**$\displaystyle{\frac{x-x_0}{a}=\frac{y-y_0}{b}=\frac{z-z_0}{c}}$,注意补充定义$A$或$B$或$C$为0的情况

由一般方程推导参数方程或者标准方程：$\bold{e}=\bold{n}_1\times\bold{n_2}$,再由两平面方程联立的解中的任意一点得到$(x_0,y_0,z_0)$（通解与特解）

4. 过两直线的平面方程：首先要求两直线有唯一交点（不异面，不共线），再由两直线推出平面法向量即可获得平面的点法式方程

5. **点到直线距离方程**：点$P(x_1,y_1,z_1)$到直线$\displaystyle{\frac{x-x_0}{a}=\frac{y-y_0}{b}=\frac{z-z_0}{c}}$

$d=\displaystyle{\frac{|(x_1-x_0,y_1-y_0,z_1-z_0)\times(a,b,c)|}{\sqrt{a^2+b^2+c^2}}}$（平行直线距离类似）

6. **异面直线距离方程**：直线$\displaystyle{\frac{x-x_0}{a}=\frac{y-y_0}{b}=\frac{z-z_0}{c}}$到直线$\displaystyle{\frac{x-x_1}{a_1}=\frac{y-y_1}{b_1}=\frac{z-z_1}{c_1}}$

记$\bold{n}=(a_1,b_1,c_1)\times(a_2,b_2,c_2)$:距离$d=\displaystyle{\frac{|(x_1-x_0,y_1-y_0,z_1-z_0)\cdot\bold{n}|}{|\bold{n}|}}$

7. **三元二次方程形成曲面典型形式**

$\displaystyle{\frac{x^2}{a^2}+\frac{y^2}{b^2}-\frac{z^2}{c^2}}=0$ 椭圆锥面（考虑$z=z_0$的截面：椭圆、曲面上任意一点与原点的连线：锥面）

$\displaystyle{\frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2}}=1$ 椭球面 （考虑平行于坐标平面的截面）

$\displaystyle{\frac{x^2}{a^2}+\frac{y^2}{b^2}-\frac{z^2}{c^2}}=1$ 单叶双曲面 （考虑$z=z_0$的截面：椭圆、$x=x_0或y=y_0$的截面：双曲线-直线、一个平面：单叶）

$\displaystyle{\frac{x^2}{a^2}+\frac{y^2}{b^2}-\frac{z^2}{c^2}}=-1$ 双叶双曲面  （考虑$z=z_0$的截面：椭圆-点、$x=x_0或y=y_0$的截面：双曲线、两个平面：双叶）

$\displaystyle{\frac{x^2}{a^2}+\frac{y^2}{b^2}=1}$ 椭圆柱面 

$\displaystyle{\frac{x^2}{a^2}-\frac{y^2}{b^2}=1}$ 双曲柱面

$\displaystyle{\frac{x^2}{a^2}-y=0}$ 抛物柱面

$\displaystyle{\frac{x^2}{a^2}+\frac{y^2}{b^2}=z}$ 椭圆抛物面（考虑$z=z_0$的截面：椭圆-点、$x=x_0或y=y_0$的截面：抛物线）

$\displaystyle{\frac{x^2}{a^2}-\frac{y^2}{b^2}=z}$ 双曲抛物面（考虑$z=z_0$的截面：双曲线-直线、$x=x_0或y=y_0$​的截面：抛物线）

### ppt补充内容

1. 一般二次曲面方程$Ax^2+By^2+Cz^2+Dxy+Eyz+Fzx+Gx+Hy+Iz+J=0$，其中$A,B,C,D,E,F$不能全为0

一些特殊情形不是曲面，如：$(A_1x+B_1y+C_1z+D_1)^2+(A_2x+B_2y+C_2z+D_2)^2=0$表示一条直线

对于实对称矩阵，可以进行正交化化为一个对角矩阵：于是可将一般二次曲面方程化为$Ax^2+By^2+Cz^2+Gx+Hy+Iz+J=0$

当$A,B,C$均不为0时方程可通过坐标平移化为$Ax^2+By^2+Cz^2+J=0$,并根据$A,B,C$的正负号区分椭圆锥面，椭球面，单叶双曲面，双叶双曲面

当$A,B,C$中有一个为0时，方程可化为$Ax^2+By^2+Iz+J=0$.若$I=0$：椭圆柱面和双曲柱面（与$z$无关）；若$I\neq0$，可进一步简化为$Ax^2+By^2+Iz=0$：椭圆抛物面与双曲抛物面

当$A,B,C$中有两个为0时，方程可化为$Ax^2+Hy+Iz+J=0$.若$H=I=0$曲面退化为两个平面；若$H,I$不全为0，通过平移可化为$Ax^2+Hy+Iz=0$再旋转得到抛物柱面$Ax^2+y=0$

### 解题指南补充内容

1. 判断直线间位置关系：检验两直线的方向向量，若同向则为平行或重合（判断两直线方程是否成比例区分），反之则为异面或相交（判断两直线间的距离是否为0区分，或者直接联立求解交点）
2. 已知两直线方程求公垂线方程：公垂线方向已知，且与两直线均共面，所以可以用两面式方程表示
3. 直线投影至平面的投影方程：过直线作平面的垂面（直线的方向向量$\times$平面的法向量）与平面的交线，用两面式方程表示

## 微分中值定理与泰勒公式

注意，对于一元函数，可导与可微是相互等价的

1. **罗尔定理**：设$y=f(x)$在闭区间$[a,b]$上连续，且$f(a)=f(b)$.又设$y=f(x)$在$(a,b)$内可导，则必存在一点$c\in(a,b)$使得$f'(c)=0$.

证明：对常值函数显然。对非常值函数，闭区间内最大值和最小值必有一个在$(a,b)$内取到，对于这个点，因为导数存在，由导数的定义其导数值必为0。

2. **微分中值定理**/**拉格朗日中值定理**：设$y=f(x)$在$[a,b]$连续，在$(a,b)$可导，则必存在一点$c\in(a,b)$使得$f'(c)=\displaystyle\frac{f(b)-f(a)}{b-a}$.

证明：令$g(x)=f(x)-\displaystyle\frac{f(b)-f(a)}{b-a}(x-a)$,对$g(x)$应用罗尔定理

3. 导函数大于零的函数严格递增，严格递增函数的导函数可以在有限个点处取到0
4. **达布中值定理**：设$y=f(x)$在$(A,B)$区间中可导，又设$[a,b]\subset(A,B)$,且$f'(a)<f'(b)$.证明：对任意给定的$\eta$：$f'(a)<\eta<f'(b)$,都存在一点$c\in(a,b)$使得$f'(c)=\eta$

先证明$f'(a)<0,f'(b)>0,\eta=0$的情况成立：由于$f'(a)<0,f'(b)>0$，闭区间$[a,b]$的最小值点必定在$(a,b)$内取到（因为对于$a,b$附近的点，均有其函数值小于$f(a)或f(b)$）由$y=f(x)$存在导函数，所以必然在最小值点$c$，$f'(c)=\eta=0$

对于一般情况，令$g(x)=f(x)-\eta x$,问题就转化到了先前已证明的形式

5. **柯西中值定理**：设$f(x)$与$g(x)$在$[a,b]$上连续，在$(a,b)$上可导，且$g'(x)\neq0$，必存在一点$c\in(a,b)$，使得$\displaystyle{\frac{f(b)-f(a)}{g(b)-g(a)}=\frac{f'(c)}{g'(c)}}$.

证明：令$h(x)=f(x)-\displaystyle\frac{f(b)-f(a)}{g(b)-g(a)}[g(x)-g(a)]$,对$h(x)$应用罗尔定理

6. 柯西中值定理补充习题（来自zcf）

设函数$f(x)$在闭区间$[a,b]$内连续，开区间$(a,b)$内可导且$f(x)\neq0$，$f(a)=0,f(b)=2$，证明在$(a,b)$中存在两个不同的点$\eta,\zeta$使得：$f'(\eta)[f(\zeta)+\zeta f'(\zeta)]=f'(\zeta)[bf'(\eta)-1]$

选取使得$f'(\eta)和f'(\zeta)$不为0，原式相当于$\displaystyle{\frac{bf'(\eta)-1}{f'(\eta)}=\frac{f(\zeta)+\zeta f'(\zeta)}{f'(\zeta)}}$，由柯西中值定理可知

$\exists \eta\in(a,b)$,使得$\displaystyle{\frac{bf'(\eta)-1}{f'(\eta)}}=\displaystyle{\frac{[bf(b)-b]-[bf(a)-a]}{f(b)-f(a)}}=\displaystyle{\frac{a+b}{2}}$,

$\exists \zeta\in(a,\displaystyle\frac{a+b}{2})$,使得$\displaystyle{\frac{f(\zeta)+\zeta f'(\zeta)}{f'(\zeta)}=\frac{\frac{a+b}{2}f(\frac{a+b}{2})-af(a)}{f(\frac{a+b}{2})-f(a)}=\frac{a+b}{2}}$

下证此时$\eta和\zeta$不相等(qs十分困难)

另法：设$\displaystyle{\frac{bf'(\eta)-1}{f'(\eta)}=\frac{f(\zeta)+\zeta f'(\zeta)}{f'(\zeta)}}=c$

一者$f'(\eta)=\displaystyle\frac{1}{b-c}$,由连续性可以在$c\in(a,b)$取到$f(c)=1$，由拉格朗日中值定理即可保证$\eta$可以取到

而显然（由柯西中值定理）$\exists \zeta\in(a,c)$,使得$\displaystyle{\frac{f(\zeta)+\zeta f'(\zeta)}{f'(\zeta)}=\frac{cf(c)-af(a)}{f(c)-f(a)}=c}$

7. **局部泰勒公式**:设$y=f(x)$在$x_0$点的某个临域内有定义，并在$x_0$点有$n$阶导数，$n\ge 1$,则在$x_0$附近有下列展式：

$\displaystyle{f(x)=f(x_0)+\frac{f'(x_0)}{1!}(x-x_0)+\cdots+\frac{f^{(n)}(x_0)}{n!}(x-x_0)^n+o((x-x_0)^n)},(x\rightarrow x_0)$

**带拉格朗日余项的泰勒公式**设$y=f(x)$在$(A,B)$内有$n+1$阶导数，则对$(A,B)$中任意取定的一点$x_0$及任意的$x\in(A,B)$,有

$\displaystyle{f(x)=f(x_0)+\frac{f'(x_0)}{1!}(x-x_0)+\cdots+\frac{f^{(n)}(x_0)}{n!}(x-x_0)^{n}+\frac{f^{(n+1)}(\zeta)}{(n+1)!}(x-x_0)^{(n+1)}},(x\rightarrow x_0)$

8. **例题**：设多项式函数$f(x)$在区间$[a,b]$上有$n$个根（一个$k$重根算作$k$个根），且$f^{(n-1)}(x)$存在。证明：$f^{(n-1)}(x)$在$[a,b]$上至少有一个根

**采用递推**：对$n=1$时显然成立

设对$n=k$时命题成立，即函数$f(x)$在区间$[a,b]$上有$k$个根，且$f^{(k-1)}(x)$存在。$f^{(k-1)}(x)$在$[a,b]$上至少有一个根

那么对于$n=k+1$时，只需要证明，$f'(x)=0$有$k$个根即可，由重根的表示方法，$f(x)=(x-x_1)^{k_1}(x-x_2)^{k_2}\cdots(x-x_m)^{k_m}g(x)$,其中$g(x)\neq0,\Sigma k_i=k+1$,于是得到$f'(x)=(x-x_1)^{k_1-1}(x-x_2)^{k_2-1}\cdots(x-x_m)^{k_m-1}r(x)$

其中$r(x)=(x-x_1)(x-x_2)\cdots(x-x_m)g'(x)+\Sigma_i\displaystyle\frac{(x-x_1)(x-x_2)\cdots(x-x_m)}{(x-x_i)}g(x)$

对于$r(x)$:观察可见$r(x_i)=(x_i-x_1)(x_i-x_2)\cdots(x_i-x_m)g(x_i)$可以看到，对于$i=1,2,\cdots,m$的遍历，其值正负相间，至少提供$m-1$个根，再由重根计数的定义可以看到，总根的个数$N_{f'(x)=0}\ge\Sigma_ik_i-m+(m-1)=k$

**罗尔定理法**：证明：函数$f(x)$在区间$[a,b]$上有$n$个根（一个$k$重根算作$k$个根），若$f'(x)$存在，那么$f'(x)=0$在$[a,b]$上至少有$n-1$个根

证明：设单根$r$个，重根$p$个，重根的指数总和为$n-r$，那么$f(x)$共计有$r+p$个零点，由罗尔中值定理可知至少存在不同于这$r+p$个根的$r+p-1$个零点，再有由重根定义直接计算$f(x)=(x-x_i)^{k_1-1}(kg(x_i)+g'(x_i))$,如果$kg(x_i)+g'(x_i)\neq0$那么$x_i$是导函数的$k_i-1$重根，如果$kg(x_i)+g'(x_i)=0$那么$x_i$是导函数的$s$重根且$s>k_i-1$,所以统计所有根的个数和重数，得到$f'(x)=0$在$[a,b]$上至少有$r+p-1+n-r-p=n-1$个根

### 谢惠民补充

1. **Fermat定理**：$x_0$为函数$f(x)$的极值点，且存在$f'(x_0)$，那么$f'(x_0)=0$

证明1:仅对极大值做证明，由极值定义，$\exist \delta$使得$|x-x_0|<\delta$时恒有$f(x_0)>f(x)$，而导数存在，于是它的两个单侧导数存在且相等，即$f'(x_0)=f'_+(x_0)=f'_-(x_0)$。由定义可知$f'(x_0^+)\leq0,f'(x_0^-)\geq0$，于是得到$f'(x_0)=0$

证明2:由小增量的定义，$f(x)-f(x_0)=f'(x_0)(x-x_0)+o(x-x_0)=(f'(x_0)+o(1))(x-x_0)$,若$f'(x_0)\neq0$,当$x、x_0$充分接近时，有$f'(x_0)+o(1)$与$f'(x_0)$同号，于是在$x$经过$x_0$时函数值变号，这与$x_0$是极值矛盾。

注解1：极值点只有可能导数不存在或者导数为0，这两种点统称为**极值可疑点**

注解2：导数存在且为0的点称为驻点，含义是函数值附近几乎不变$o(x-x_0)$,但不一定是极值点（例子易举）

2. **Rolle定理的Samuleson证明**

**罗尔定理**：设$y=f(x)$在闭区间$[a,b]$上连续，且$f(a)=f(b)$.又设$y=f(x)$在$(a,b)$内可导，则必存在一点$c\in(a,b)$使得$f'(c)=0$.

证明：记$F(x)=f(x)-f(x+\frac{b-a}{2})$,由$f(a)=f(b)$易验证得到$F(a)=-F(\frac{a+b}{2})$。因而$\exists a_1\in[a,\frac{a+b}{2}]$，使得$F(a_1)=0$。于是若记$b_1=a_1+\frac{b-a}{2}$就可得到$f(a_1)=f(b_1)$且$a_1-b_1=(b-a)/2$，于是构建闭区间套${[a_n,b_n]}$，它满足$f(a_n)=f(b_n)$且$a_n-b_n=(b-a)/2^n$,于是存在唯一的点$\eta$属于每一个$[a_n,b_n]$，而且有$\lim_{n\rightarrow+\infty}a_n=\lim_{n\rightarrow+\infty}b_n=\eta$.由于$f(x)$在$\eta$点可导，于是$f'(\eta)=\displaystyle{\lim_{n\rightarrow+\infty}\frac{f(b_n)-f(a_n)}{b_n-a_n}=0}$,由于恒有$f(a_n)=f(b_n)$.

注意此处构造的$\eta$点不一定是极值点，因而它是一种完全不同的证明思路。

例如对：$f(x)=\displaystyle{\begin{cases}x^2\sin(\frac{\pi}{x}),x\neq0\\0,x=0\end{cases}}$得到$\eta=0$处$f'(\eta)\ne0$但不为极值点，领域内大于0和小于0的值总存在

3. **Lagrange中值定理的有限增量形式**：

$f(b)=f(a)+f'(\eta)(b-a),a<\eta<b$

$f(b)=f(a)+f'(a+\theta(b-a))(b-a),0<\theta<1$

$\Delta y=f'(x_0+\theta\Delta x)\Delta x,0<\theta<1$

4. **Cauthy定理**：设$f(x)$与$g(x)$在$[a,b]$上连续，在$(a,b)$上可导，且满足条件$g(b)-g(a)\neq0$且$g'^2(x)+f'^2(x)\ne0,\forall x\in(a,b)$，必存在一点$c\in(a,b)$，使得$\displaystyle{\frac{f(b)-f(a)}{g(b)-g(a)}=\frac{f'(c)}{g'(c)}}$.

5. **Darboux定理**：设$f$在区间$I$上可微，则$f'$具有介值性质

另证明：先证明$f'(a)<0,f'(b)>0,\eta=0$的情况成立：若$f(a)=f(b)$，与罗尔定理等同；若$f(a)\ne f(b)$，设若$f(a)>f(b)$，则有$f'(b)>0$，存在$\delta$使得$f(a)>f(b)>f(b-\delta)$，于是由连续函数的介值定理，$\exists \eta\in(a,b-\delta)$,使$f(\eta)=f(b)$,再由罗尔定理即可得证

6. **单侧导数极限定理**：设$[a,b)$上有定义的函数$f$在$(a,b)$上可微，又在点$a$右连续，若导函数$f'(x)$在$a$存在右极限$f'(a^+)=A$,则$f$在点$a$也一定存在右侧导数$f'_+(a)$且成立$f'_+(a)=f'(a^+)=A$,即$f'(x)$在$a$右连续。此外$A$除有限数外，可以为$\pm\infty$

取$\Delta x=x-a,\Delta y=f(x)-f(a)$,差商可写为$\displaystyle{\frac{\Delta y}{\Delta x}=\frac{f(a+\Delta x)-f(a)}{\Delta x}}$，由拉格朗日中值定理$\exist\theta\in(0,1),\Delta y=f'(a+\theta \Delta x)\Delta x$,于是对差商两侧去极限（或者更严谨的用极限的定义可以证明）$f'_+(a)=f'(a^+)=A$，对于无穷情况同理.

思考题：如果证明中的$A$是不具有符号的无穷大量，则单侧导数极限定理不成立

**导数极限定理**：$f$在$a$的某临域$O(a)$连续，在$O(a)-{a}$上可导，$f'(x)$在$a$存在极限，则$f$在$a$处也可导，且$f'$在$a$连续

7. **间断点分类**

第一类间断点：两侧极限存在但不相等或者相等但不等于函数值。若两侧极限相等但不等于此处函数值则为可去间断点

第二类间断点：两侧极限至少有一侧不存在

### 谢惠民例题

1. $f$在$[a,b]$上二阶可微,$f(a)=f(b)=0$。证明：$\forall x\in(a,b),\exist\eta\in(a,b)$,使$f(x)=\displaystyle\frac{f''(\eta)}{2}(x-a)(x-b)$

证明1:固定$x$，令$\lambda =\displaystyle\frac{2f(x)}{(x-a)(x-b)}$,问题即转化为$\exist\eta\in(a,b)$,使$f''(\eta)=\lambda$，构造辅助函数$F(t)=f(t)-\displaystyle\frac{\lambda}{2}(t-a)(t-b)$,显然可以看到$F(a)=F(b)=F(x)=0$,应用两次罗尔定理即可得证

证明2:$f''(\eta)=\displaystyle\frac{2f(x)}{(x-a)(x-b)}$，仍旧固定$x$,若有$f'(\frac{a+b}{2})\ne0$，由柯西中值定理,在子区间$(a,x)和(x,b)$上不会有$f'(t)和g'(t)$同时为0，有$c_1,c_2$满足$\displaystyle\frac{2f(x)}{(x-a)(x-b)}=\displaystyle{\frac{f'(c_1)}{c_1-\frac{a+b}{2}}}=\displaystyle{\frac{f'(c_2)}{c_2-\frac{a+b}{2}}}=\displaystyle{\frac{f'(c_1)-f'(c_2)}{c_1-c_2}}$,于是由拉格朗日中值定理可证得存在$\eta$








