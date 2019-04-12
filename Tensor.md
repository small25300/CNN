# Einstein约定
- 在一个单项式中，若一个脚标重复出现两次（重复小于或大于两次都不是哑标），则表示该项关于这一脚标对1、2、3求和，而无须再写出求和记号$\sum$，而求和约定中重复两次的脚标称为哑标。
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
1\qquad x=y  \\

0 \qquad x\neq y
\end{cases}
\end{equation}
f(n) =
\begin{cases} 
n/2,  & \mbox{if }n\mbox{ is even}  

3n+1, & \mbox{if }n\mbox{ is odd}
\end{cases}
