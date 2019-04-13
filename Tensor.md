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
\begin{eqnarray} 
  \begin{gathered}
      \mathbf{c}&=&\mathbf{a\times b}\\\\
      &=&\begin{vmatrix}
        e_1 & e_2 & e_3\\\\
        a_1 & a_2 & a_3\\\\
        b_1 & b_2 & b_3\\\\
      \end{vmatrix}\\\\
      &=& a_1b_2e_3+a_2b_3e_1+a_3b_1e_2-a_1b_3e_2-a_2b_1e_3-a_3b_2e_1
   \end{gathered}
\end{eqnarray}
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
  \begin{eqnarray}
    \begin{gathered}
      \mathbf{c}&=&\mathbf{a\times b}\\\\
     &=&(a_ie_i)\times (b_je_j)\\\\
     &=&(a_ib_j)(e_i\times e_j)
    \end{gathered}
  \end{eqnarray}
  对比上面(7)式和(8)式：$a_ib_j(e_i\times e_j)=\xi_{ijk}a_ib_je_k$，可得出：
  $$e_i\times e_j=\xi_{ijk}e_k$$
 - 混合积
 $$[\mathbf{a,b,c}]=\mathbf{a\cdot (b\times c)}$$
 它表示由$\mathbf{a,b,c}$所张成的平行六面体的体积，这个与$3\times 3$行列式的几何意义完全相同。
    - 直觉上可以这样理解：$\mathbf{b\times c}$表示由$\mathbf{b}$和$\mathbf{c}$张成的底面积，则$\mathbf{a}$表示高，底面积点乘高最后是体积。
    - 接下来推理混合积的表示：
      - 首先定义脚标：$\mathbf{a}=a_ie_i$，$\mathbf{b}=b_je_j$，$\mathbf{c}=c_ke_k$
      \begin{eqnarray*}
        \begin{gathered}
          \mathbf{[a,b,c]}&=&\mathbf{a\cdot (b\times c)}\\\\
          &=&a_ie_i\cdot (b_je_j\times c_ke_k)\\\\
          &=&a_ie_i\cdot b_jc_k(e_j\times e_k)\\\\
          &=&a_ie_i\cdot b_jc_k\xi_{jkl}e_l\\\\
          &=&a_ie_i\cdot b_jc_k\xi_{jkl}e_l\\\\
          &=&a_ib_jc_k\xi_{jkl}(e_i\cdot e_l)\\\\
          &=&a_ib_jc_k\xi_{jkl}\delta_{il}\\\\
          &=&a_lb_jc_k\xi_{jkl}\\\\
          &=&\xi_{ljk}a_lb_jc_k
        \end{gathered}
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
  具体推导思路：将$\xi_{pqr}$写成同$\xi_{ijk}$相同的模式，由于这两个置换符号用$\delta$符号表示的行列式中仅有对角线元素是为1的，其他元素都为0，所以就是对应对角线元素的乘积**(但是该乘积以点乘表示才能推导出，具体原因不详)**，仅以$\delta_{1p}\cdot\delta_{1i}$为例：
  $$
  \delta_{1p}\cdot\delta_{1i}=(e_1e_p)\cdot (e_1e_i)=(e_1e_p)^T(e_1e_i)=e_p^Te_1^Te_1e_i=e_pe_i=\delta_{pi}
  $$
