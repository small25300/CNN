# 1. Einstein约定
## 哑标
- 哑标：☞在一个单项式中，若一个脚标重复出现两次（重复小于或大于两次都不是哑标），则表示该项关于这一脚标对1、2、3求和，而无须再写出求和记号$\sum$，而求和约定中重复两次的脚标称为哑标。
- 哑标可以用其他任意字母代替，只要该字母没有在该项中出现过就可以。见如下几个公式：
$$a=a_ie_i=a_je_j$$
$$a_jb_jc_k=a_mb_mc_k$$
- 矢量的代数运算法则：
$$\mathbf{c}=\mathbf{a}+\mathbf{b}=a_ie_i+b_ie_i=(a_i+b_i)e_i=c_ie_i$$
$$\mathbf{a}=\alpha\mathbf{b}=\alpha(b_je_j)=(\alpha b_j)e_j$$
\begin{equation}
  \mathbf{a}\cdot\mathbf{b}=(a_ie_i)\dot(b_je_j)=a_ib_j(e_i\cdot e_j)=a_ib_j\delta_{ij}=a_ib_i
\end{equation}
其中$e_i\cdot e_j=e_i^Te_j$在线性代数中表示向量$e_i$与$e_j$的内积，而此处$e_i$与$e_j$表示标准基，因此当$i=j$时，$e_i\cdot e_j=1$，此处用：
\begin{equation}
  \delta_{ij}=e_i\cdot e_j=
  \begin{cases}
    1\qquad x=y\\\\
    0 \qquad x\neq y
  \end{cases}
\end{equation}
- 根据以上分析可知：
\begin{equation}
  \begin{cases}
    \delta_{ij}a_j=a_i\\\\
    \delta_{ij}a_i=a_j
  \end{cases}
\end{equation}
(3)式中第一个式子，因为$\delta_{ij}a_j$中，$j$ 是哑标，所以$j$ 可以被任意替代，而$\delta_{ij}$当$i=j$ 时为1，其余为0，所以结果为$a_i$。同理，第二个式子中$i$ 为哑标，可以用$j$ 来替换，最终结果为$a_j$。
## 自由标
- 自由标：☞在一个单项式中仅出现一次的脚标，称为自由标。自由标顾名思义相当于变量，可以遍历所有可能取值，在所有张量的课程中默认为1、2、3（为什么不是1~N，具体原因不详）。
例如：$\delta_{ij}a_j$的含义表示3个式子
\begin{equation}
  \begin{cases}
    \delta_{1j}a_j\\\\
    \delta_{2j}a_j\\\\
    \delta_{3j}a_j
  \end{cases}
\end{equation}
  - 对于多项式而言，每一项的自由标必须是相同的。
  - 若一个表达式中有$n$个自由标，则表示有$3^n$个表达式，如有2个自由标，则共有9个表达式。
## 置换符号
- 矢积也叫叉乘运算，即：$mathbf{c}=\mathbf{a}\times\mathbf{b}$，叉乘的结果表示有向量$\mathbf{a}$和$\mathbf{b}$张成的平行四边形的面积，符合右手法则。
- 右手法则：即$\mathbf{a}\times\mathbf{b}$的结果是四指指向向量$\mathbf{a}$的方向，然后向向量$\mathbf{b}$的方向弯曲，大拇指的方向就是向量$\mathbf{c}$的方向，向量$\mathbf{c}$的大小就是$\mathbf{a}$和$\mathbf{b}$张成的平行四边形的面积。
- 叉乘与行列式的关系：
  - 在线性代数中$2\times2$行列式的几何意义是由2个列向量所张成的平行四边形的面积，而如果是$3\times3$行列式，则表示由这3个列向量张成的平行六面体的体积。
  - 但是在此处如果向量$\mathbf{a}$和$\mathbf{b}$都$\in\mathbb{R^3}$，但是却只有两个向量，按照道理应该是三维空间中某一平面中有向量$\mathbf{a}$和$\mathbf{b}$张成的平行四边形的面积，为了符合行列式，我们引入$\mathbf{a}$和$\mathbf{b}$的单位向量$e$，使得$3\times3$的行列式计算出的是面积不是体积。如(5)式所示：
\begin{equation} 
  \begin{array}
      \mathbf{c}&=\mathbf{a\times b}\\\\
      &=\begin{vmatrix}
        e_1 & e_2 & e_3\\\\
        a_1 & a_2 & a_3\\\\
        b_1 & b_2 & b_3\\\\
      \end{vmatrix}\\\\
      &=a_1b_2e_3+a_2b_3e_1+a_3b_1e_2-a_1b_3e_2-a_2b_1e_3-a_3b_2e_1
   \end{array}
\end{equation}
观察(5)式：脚标无论怎么循环移位，都可以形成1、2、3顺序的，这样的排列称为偶排列（正向排列），其项前面为+1。脚标无论怎么循环移位，都可以形成3、2、1顺序的，这样的排列称为奇排列（反向排列），其项前面都为-1。为了表示行列式脚标与符号之间的关系，因此我们定义一个新的符号$\rightarrow$置换符号。  
- 置换符号定义如下：
\begin{equation}
  \xi_{ijk}=\begin{cases}
  \ 1\qquad & ijk为偶排列（正向排列）\\\\
  -1\qquad & ijk为奇排列（反向排列）\\\\
  \ 0\qquad  & ijk中有两个的值相等时
  \end{cases}
\end{equation}
$\xi_{ijk}$有27中可能的式子，其中 $ijk$ 有两个值相等的情况有21个。
  - 如果将置换符号的脚标$ijk$看作正向，$kji$看作反向，则：
  $$\xi_{ijk}=\xi_{jki}=\xi_{kij}$$
  $$\xi_{ijk}=-\xi_{kji}=-\xi_{jik}=-\xi_{ikj}$$
  根据以上分析：
  \begin{equation}
    \mathbf{c=a\times b}=\xi_{ijk}a_ib_je_k
  \end{equation}
  \begin{equation}
    \begin{array}
      \mathbf{c}&=\mathbf{a\times b}\\\\
     &=(a_ie_i)\times (b_je_j)\\\\
     &=(a_ib_j)(e_i\times e_j)
    \end{array}
  \end{equation}
  对比上面(7)式和(8)式：$a_ib_j(e_i\times e_j)=\xi_{ijk}a_ib_je_k$，可得出：
  $$e_i\times e_j=\xi_{ijk}e_k$$
 - 混合积
 $$[\mathbf{a,b,c}]=\mathbf{a\cdot (b\times c)}$$
 它表示由$\mathbf{a,b,c}$所张成的平行六面体的体积，这个与$3\times 3$行列式的几何意义完全相同。
    - 直觉上可以这样理解：$\mathbf{b\times c}$表示由$\mathbf{b}$和$\mathbf{c}$张成的底面积，则$\mathbf{a}$表示高，底面积点乘高最后是体积。
    - 接下来推理混合积的表示：
      - 首先定义脚标：$\mathbf{a}=a_ie_i$，$\mathbf{b}=b_je_j$，$\mathbf{c}=c_ke_k$
      \begin{eqnarray*}
          \mathbf{[a,b,c]}&=&\mathbf{a\cdot (b\times c)}\\\\
          &=&a_ie_i\cdot (b_je_j\times c_ke_k)\\\\
          &=&a_ie_i\cdot b_jc_k(e_j\times e_k)\\\\
          &=&a_ie_i\cdot b_jc_k\xi_{jkl}e_l\\\\
          &=&a_ie_i\cdot b_jc_k\xi_{jkl}e_l\\\\
          &=&a_ib_jc_k\xi_{jkl}(e_i\cdot e_l)\\\\
          &=&a_ib_jc_k\xi_{jkl}\delta_{il}\\\\
          &=&a_lb_jc_k\xi_{jkl}\\\\
          &=&\xi_{ljk}a_lb_jc_k
      \end{eqnarray*}
      其中：因为$e_i\times e_j=\xi_{ijk}e_k$，所以$e_j\times e_k=\xi_{jkl}e_l$，由于前面有$a_ie_i$,所以不能用 $i$ 符号，选择 $l$ 符号。
      - 通过以上方式可以证明：
      $$\mathbf{[a,b,c]=[c,a,b]=[b,c,a]}\qquad 注意：是正向排序$$
      $$\mathbf{[a,b,c]=-[c,b,a]=-[b,a,c]=-[a,c,b]}\qquad 注意：是反向排序$$
## Kronecker($\delta$)符号与置换符号之间的关系
$$
\begin{vmatrix}
  \delta_{11} & \delta_{12} & \delta_{13}\\\\
  \delta_{21} & \delta_{22} & \delta_{23}\\\\
  \delta_{31} & \delta_{32} & \delta_{33}\\\\
\end{vmatrix}=
\begin{vmatrix}
  \delta_{11} & 0 & 0\\\\
  0 & \delta_{22} & 0\\\\
  0 & 0 & \delta_{33}\\\\
\end{vmatrix}=
\begin{vmatrix}
1 & 0 & 0\\\\
0 & 1 & 0\\\\
0 & 0 & 1\\\\
\end{vmatrix}=1
$$
  - 行列式的性质是交换行或列一次，行列式变号，该性质与置换符号相同，所以置换符号可以用下列式子来表示：
  $$
  \xi_{ijk}=
  \begin{vmatrix}
    \delta_{1i} & \delta_{1j} & \delta_{1k}\\\\
    \delta_{2i} & \delta_{2j} & \delta_{2k}\\\\
    \delta_{3i} & \delta_{3j} & \delta_{3k}\\\\
  \end{vmatrix}
  $$
  所以：
  $$
  \xi_{ijk}=-
  \begin{vmatrix}
    \delta_{1j} & \delta_{1i} & \delta_{1k}\\\\
    \delta_{2j} & \delta_{2i} & \delta_{2k}\\\\
    \delta_{3j} & \delta_{3i} & \delta_{3k}\\\\
  \end{vmatrix}
  $$
  这样可以推出：
  $$
  \xi_{pqr}\xi_{ijk}=-
  \begin{vmatrix}
    \delta_{pi} & \delta_{pj} & \delta_{pk}\\\\
    \delta_{qi} & \delta_{qj} & \delta_{qk}\\\\
    \delta_{ri} & \delta_{rj} & \delta_{rk}\\\\
  \end{vmatrix}
  $$
  具体推导思路：将$\xi_{pqr}$写成同$\xi_{ijk}$相同的模式，由于这两个置换符号用$\delta$符号表示的行列式中仅有对角线元素是为1的，其他元素都为0，所以就是对应对角线元素的乘积(**但是该乘积以点乘表示才能推导出，具体原因不详**)，仅以$\delta_{1p}\cdot\delta_{1i}$为例：
  $$
  \delta_{1p}\cdot\delta_{1i}=(e_1\cdot e_p)\cdot (e_1\cdot e_i)=(e_1e_p)^T(e_1e_i)=e_p^Te_1^Te_1e_i=e_p^Te_i=e_p\cdot e_i=\delta_{pi}
  $$
  上面的这个推导思路压根计算不出来，具体怎么推理也不清楚。暂时放在这儿！
- 证明$\xi_{ijk}\xi_{mnk}=\delta_{im}\delta_{jn}-\delta_{in}\delta_{jm}$
\begin{eqnarray*}
  \xi_{ijk}\xi_{mnk} &=& \begin{vmatrix}
    \delta_{im} & \delta_{in} & \delta_{ik}\\\\
    \delta_{jm} & \delta_{jn} & \delta_{jk}\\\\
    \delta_{km} & \delta_{kn} & \delta_{kk}\\\\
  \end{vmatrix}\\\\
  &=&\delta_{im}\delta_{jn}\delta_{kk}+\delta_{in}\delta_{jk}\delta_{km}+\delta_{ik}\delta_{jm}\delta_{kn}
  -\delta_{ik}\delta_{jn}\delta_{km}-\delta_{im}\delta_{jk}\delta_{kn}-\delta_{in}\delta_{jm}\delta_{kk}\\\\
  &=&3\delta_{im}\delta_{jn}+\delta_{in}\delta_{jm}+\delta_{in}\delta_{jm}-\delta_{im}\delta_{jn}-\delta_{im}\delta_{jn}-3\delta_{in}\delta_{jm}\\\\
  &=&3\delta_{im}\delta_{jn}+2\delta_{in}\delta_{jm}-2\delta_{im}\delta_{jn}-3\delta_{in}\delta_{jm}\\\\
  &=&\delta_{im}\delta_{jn}-\delta_{in}\delta_{jm}
\end{eqnarray*}
根据：$\delta_{kk}=\delta_{11}+\delta_{22}+\delta_{33}$且$\delta_{ik}\delta_{jm}\delta_{kn}中当i=k时\delta_{ik}=1$，且  $k$是哑标可以将 $k$ 替换为 $i$。
# 2. 与场有关的物理量
## 场的定义
- 如果一种物理量在某个空间区域中的每一个点都有确定的值，就称这个空间区域上定义着（存在着）该物理量的场。
  - 数量（标量）场：温度场、电位场、密度场等。
  - 矢量场：速度场、力场、磁场等。
- 场可以用一个函数来描述，且这个函数值即场的大小与“空间位置”、“时间”一定是相关的(空间位置、时间是变量)。
## 梯度（gradient）
- 方向导数：一个物理量沿着空间某一方向变化的快慢，称为方向导数。梯度是所有方向导数最大的那个方向和值。
- 梯度：若在数量场中的一点$M$处存在着矢量 $g$ ，其方向为$M$点处函数变化最大的方向，其模为这个最大变化率的值，则称 $g$ 为这个函数在$M$点处的梯度。（即：$M$点处方向导数最大的方向为梯度方向，梯度值为方向导数最大值或该方向导数的模）。
- 梯度的表示：
\begin{equation}
  g = grad \ \varphi = \nabla\ \varphi
\end{equation}
其中：$\nabla$称为Hamilton算符，其本身就是一个矢量，可以用下式表示：
$$\nabla=\frac{\partial}{\partial x_1}\mathbf{e_1}+\frac{\partial}{\partial x_2}\mathbf{e_2}+\frac{\partial}{\partial x_3}\mathbf{e_3}=\frac{\partial}{\partial x_i}\mathbf{e_i}$$
若某个函数对坐标$x_i$取偏微分，则记为$(.),i$，如下所示：
$$g=\nabla\ \varphi=\varphi_{,i}e_i$$
也就是说：$\varphi_{,i}\equiv \frac{\partial\varphi}{\partial x_i}$
- 方向导数与梯度的关系：
\begin{eqnarray*}
    \frac{\partial\varphi}{\partial\mathbf{n}}&=&\nabla\varphi\cdot\mathbf{n}\\\\
    &=&\frac{\partial\varphi}{\partial x_1}\cos\alpha_1+\frac{\partial\varphi}{\partial x_2}\cos\alpha_2+\frac{\partial\varphi}{\partial x_3}\cos\alpha_3\\\\
\end{eqnarray*}
其中：$\mathbf{n}$是方向向量(注意：它不是单位向量)，$\mathbf{n}=(\cos\alpha_1,\cos\alpha_2,\cos\alpha_3)^T$，它实际上表示的是$\mathbf{n}$在标准基$e_1,e_2,e_3$三个方向上的投影。  
本质上：$\nabla\varphi\cdot\mathbf{n}=(\varphi_{,i}e_i)\cdot(n_je_j)=\varphi_{,i}n_j(e_i\cdot e_j)=\varphi_{,i}n_j\delta_{ij}=\varphi_{,i}n_i$
## 散度
- 通量（类似磁通量）：☞穿过空间某个任意曲面的物理量的总量称为通量。
  - 由上面通量定义可知，能形成通量的物理量一定是矢量。
  - 对于一个曲面，真正意义上的通量是与该曲面法线（垂直与该曲面某点切面的直线）方向向平行的物理量，但实际情况不是所有物理量都沿法线方向，因此是该物理量在法线方向上的投影，才是真正的通量。
  - 物理量用向量$\mathbf{v}$表示，法线用向量$\mathbf{n}$表示，注意此处的法向量是一个单位向量，因此：
  $$\mathbf{v\cdot n}=\lVert\mathbf{v}\rVert\cdot\lVert\mathbf{n}\rVert\cos\alpha=\lVert\mathbf{v}\rVert\cos\alpha$$
  由于$\mathbf{v}$与$\mathbf{n}$的夹角为$\alpha$，则$\lVert\mathbf{v}\rVert\cos\alpha$表示$\mathbf{v}$在$\mathbf{n}$方向上的投影，因此$\mathbf{v\cdot n}$就是该投影。
- 穿过曲面通量的公式表示：
$$\int_s\mathbf{v\cdot n}\ ds=\int_s v_in_i\ ds=\int_s(v_1\cos\alpha_1+v_2\cos\alpha_2+v_3\cos\alpha_3)\ ds$$
$\mathbf{v\cdot n}$表示单位面积内通量的大小，所以$\int_s\mathbf{v\cdot n}\ ds$表示该曲面的通量大小。
$\int_s(v_1\cos\alpha_1+v_2\cos\alpha_2+v_3\cos\alpha_3)\ ds=\int_s v_1\cos\alpha_1\ ds+\int_s v_2\cos\alpha_2\ ds+\int_s v_3\cos\alpha_3\ ds$，其中$\cos\alpha \ ds$可以看成是$ds$这个小面积在某个方向上的投影。
- Gauss公式：
$$\oint_s \mathbf{u\cdot n}\ ds=\int_s div\ \mathbf{u}\ dv$$
高斯公式表明：针对一个物理量封闭曲面的面积积分可以变成针对它的体积积分（**此处完全忘记了，如果以后可能用到，再查高数**）  
其中：$\oint_s \mathbf{u\cdot n}\ ds$表示封闭曲面的通量，而$div\ \mathbf{u}$就是我们此处要定义的散度。
$$div\ \mathbf{u}=\nabla\cdot \mathbf{u}=u_{i,i}=\frac{\partial u_1}{\partial x_1}+\frac{\partial u_2}{\partial x_2}+\frac{\partial u_3}{\partial x_3}$$
- 散度的物理意义：
  - 若$div\ \mathbf{u}>0$，则表示在该点有源。
  - 若$div\ \mathbf{u}<0$，则表示在该点有汇。
  - 若$div\ \mathbf{u}=0$，则表示在该点无源无汇。
    - $div\ \mathbf{u}=0$的大小表示“源”和“汇”的强度，与坐标系无关。
  - “源”与“汇”的概念：以一个水池为例进行说明：
    - 源：☞一个封闭水池中的水流入口
    - 汇：☞一个封闭水池中的水流出口
  - 若是一个完全封闭的空间，这对某一物理量与外界没有任何的交换，则其散度必然为0，因为该空间无源无汇。
## 旋度rotation
- 定义：设$\Gamma$为分段光滑的空间有向闭曲线，$\sum$是以$\Gamma$为边界的分片光滑有向曲面。$\Gamma$的方向与$\sum$曲面的法线之间是符合右手定则的，函数$P(x,y,z),Q(x,y,z),R(x,y,z)$在包含曲面$\sum$在内的一个空间区域内具有一阶连续偏导数。（**这个定义感觉没有说完，也不明白**）
- 我们用Stokes公式(斯托克斯)来描述旋度：
$$\iint_\sum (\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z})\ dydz+(\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x})\ dzdx+(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y})\ dxdy=\oint_\Gamma P\ dx+Q\ dy+R\ dz$$
令：
$$
rot\ \mathbf{u}=\nabla\times\mathbf{u}=\begin{vmatrix}
e_1 & e_2 & e_3\\\\
\frac{\partial}{\partial x_1} & \frac{\partial}{\partial x_2} & \frac{\partial}{\partial x_3}\\\\
u_1 & u_2 & u_3\\\\
\end{vmatrix}
$$
- 旋度物理意义：旋度是用来描述一个漩涡源的漩涡流强度的物理量，而所谓的漩涡源就是一个能在其周围造成一个“环(封闭有向曲线)”的流源，因此为了描述此漩涡的强度，定义：单位面积的最大环量称为旋度，其方向为此环所围的面的法向量。
- 实际意义：就是一个局部微圆转动变化的快慢，我们称之为旋度。
- 旋度的特性：
  - 旋度是一个矢量，是空间坐标点的函数。
  - 一点旋度的大小是该点**环量面密度**的最大值（不懂）。
  - 旋度的方向是与该点**最大环量面密度**对应的法线方向（有点与梯度相同的感觉）。
  - 如果矢量场有一点的段都$\neq$0，则是旋度场，如果矢量场中旋度处处=0，则称为无旋度场。
  - 一点有旋度，则处处有旋度。
# 3. 张量（tensor）
## 坐标变换
- 坐标变换的本质是基的变换，而且是标准基的变换。
- 由于坐标系是正交基，所以坐标系的变换一定对应一个正交矩阵。
- 若$det\ M = 1>0$，则坐标变换是绕原点的某轴的一个旋转。
- 若$det\ M=-1<0$:
  - 绕过远点的某轴的一个旋转。
  - 对某个轴的反射，右手系的原坐标系改为左手系。
- $Scalar\Longrightarrow Vector\Longrightarrow Tensor$
- 标量$\Longrightarrow$标量+方向$\Longrightarrow$矢量+方向
- 坐标变换-可以看成基变换的特殊情况，特殊在基是正交基。
  - 基变换的表示：
  \begin{equation}
    \begin{pmatrix}e_1^\prime\\\\e_2^\prime\\\\e_3^\prime\\\\ \end{pmatrix}=M\begin{pmatrix}e_1\\\\e_2\\\\e_3\\\\ \end{pmatrix}
  \end{equation}
