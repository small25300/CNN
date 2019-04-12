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
    \mathbf{c}= \& \mathbf{a\times b}\\\\
    = \&
    \begin{vmatrix}
      e_1 & e_2 & e_3 \\\\
      a_1 & a_2 & a_3 \\\\
      b_1 & b_2 & b_3
    \end{vmatrix}
  \end{equation}
