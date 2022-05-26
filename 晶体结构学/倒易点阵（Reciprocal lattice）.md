

- Derive: 
	[[Fourier Transform in Vector Space#DFT in periodic system|DFT in periodic system]] 
	![[Pasted image 20220308204613.png|500]]
	Call $\vec{K_h} = n \vec{k_n}$ **reciprocal vector** (same conception: lattice vector)
	由这个矢量张开的空间为**倒空间 (reciprocal space)** 
	>**Definition:** reciprocal vector
	>The periodic vector in reciprocal space. Denoted as $\vec K_h=h_1\vec{b_1}+h_2\vec{b_2}+h_3\vec{b_3}$ 

	- The relation of $\vec{R_l}$ and $\vec{K_h}$ 
	From the derivation above: $$\vec{R_l}\cdot\vec{K_h}=2\pi \mu,\quad \mu=0, \pm 1,\pm2,\dots $$ ^e29275


# Construction of Reciprocal Space
Based on [[#^e29275|the fundamental condition]], the relation of the bases of this two space can be derive:
$$\vec{a_i}\cdot\vec{b_j}=2\pi \delta_{ij}$$
Then, constructure the reciprocal space:
$$\begin{array}{l}
\vec{b}_{1}=2 \pi \frac{\vec{a}_{2} \times \vec{a}_{3}}{\Omega} \\
\vec{b}_{2}=2 \pi \frac{\vec{a}_{3} \times \vec{a}_{1}}{\Omega} \\
\vec{b}_{3}=2 \pi \frac{\vec{a}_{1} \times \vec{a}_{2}}{\Omega}
\end{array}$$
or
$$\vec b_i=\frac{2\pi}\Omega\varepsilon_{ijk}\vec a_j \times \vec{a_k}$$
	
# Relationship of Reciprocal Space
- 倒空间与原空间基矢互为傅里叶变换 (互为倒数)

- 倒格矢量的方向是晶面**法线**方向(ref: [[晶体参数(指数)#^c25b44|proof]] )，模是面间距的倒数乘个因子 ($2\pi$) [[晶体参数(指数)#^8a9317|晶面方向]]
> **Definition**: reciprocal lattice vector $$|\vec{K_h}|=|OP|=\frac{2\pi}{d_{h_1h_2h_3}}$$
> Where $P$ call reciprocal point and $\vec K_h=h_1\vec b_1+h_2\vec b_2+h_3\vec b_3$  
 ^d118b9
- The reciprocal lattice does not depend on the configuration of basis vectors of crystal lattice.
It only depends on the crystal structure ( the repeat vector $R_l$ )

- Reciprocal of the volume：$\Omega^{*}=(2 \pi)^{3} / \Omega$ 

- Have the same point group

- The lattice vector $R_l$ and the reciprocal vector $K_l$ : 
$$\vec{R_l}\cdot\vec{K_h}=2\pi \mu,\quad \mu=0, \pm 1,\pm2,\dots$$ or$$\vec a_{i} \cdot \vec b_{j}=2 \pi \delta_{i j}$$

