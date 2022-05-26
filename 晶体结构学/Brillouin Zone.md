# Brillouin zone (布里渊区)
> **Definition:** Brillouin zone
> 在能带论中，固体的各种电子态按照它们的波矢分类。在倒易格子中取某一**倒易阵点**为原点，作所有倒格矢的**垂直平分面**，倒易格子被这些面划分为一系列的区域，这些区域就是**布里渊区**。
> (The region enclosed by the perpendicular bisector of lines (planes) connecting the nearest reciprocal lattice points.)
> 其中最靠近原点的一组面所围的闭合区称为第一布里渊区；在第一布里渊区之外，由另一组平面所包围的波矢区叫第二布里渊区；依次类推可得第三、四、…等布里渊区。

^41b39d

$$\vec{k}=\tau_{1} \vec{b}_{1}+\tau_{2} \vec{b}_{2}+\tau_{3} \vec{b}_{3}$$
Where $\tau_{j}=\frac{l_{j}}{N_{j}}, \quad-\frac{N_{j}}{2}<l_{j} \leq \frac{N_{j}}{2}$ $N_j$ 为原胞数。


## One-dimension
第一布里渊区就是倒易格子的维格纳-塞茨原胞，如果对每一倒易格子作此元胞，它们会毫无缝隙的填满整个波矢空间。

如一维单原子链，晶格常数为 $a$，reciprocal vector 是 $2\pi/a$, 那么第一布里渊区就是 $[-\pi/a,\pi/a]$ 



## Two-dimension
- 二维六角 
	- 格点
	 ![[Pasted image 20220524094528.png]]
- 布里渊区
![[Pasted image 20220524094456.png]]

## Confirmed BZ
我们有一个非常好用的判定标准来判定第几布里渊区。
> **determination** 从 reciprocal 原点出发，经过 $n-1$ 个垂直平分面可以到达的为第 $n$ 布里渊区

## Properties
- 第二，第三... 布里渊区可以通过沿着 reciprocal vectors 的平移整数倍而填满第一布里渊区
- 布里渊区面积（体积）等于 reciprocal 原胞的面积（体积）
- 每个布里渊区中间不含有其他的垂直平分线

# examples 
![[Pasted image 20220524095312.png]]
- bcc 倒空间原胞体积
$$\Omega^{*}=2 \frac{(2 \pi)^{3}}{a^{3}}$$
- fcc 倒空间原胞体积
$$\Omega^{*}=4 \frac{(2 \pi)^{3}}{a^{3}}$$


# Symmetry points and axes
上面一行是点，下面一行是轴
![[Pasted image 20220524095742.png]]
比较重要的是 $\Gamma$ 点，也就是倒空间原点