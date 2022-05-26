The simplest example of [[Electron move in periodic potential]]

The periodic potential is like
![[Pasted image 20220505100700.png]]
势垒势阱交替排布
# System equation
Stationary Schrodinger eq:
$$\frac{d^{2}}{d x^{2}}|\Psi\rangle+\frac{2 m}{\hbar^{2}}(E-V(x))|\Psi\rangle=0$$
For potential 
$$V(x)=\left\{\begin{matrix}
V_0&\quad na-b<x<na &\text{potential barrier}\\
0&\quad na<x<na+c&\text{potential well}
\end{matrix}\right.$$
Apply for [[Bloch's theorem|Bloch wave]]
$$\psi(\boldsymbol r)=e^{i\boldsymbol k\cdot \boldsymbol r}u(\boldsymbol r)$$
Then $$\frac{d^{2} u}{d x^{2}}+2 i k \frac{d u}{d x}+\left[\frac{2 m}{\hbar^{2}}(E-V(x))-k^{2}\right] u=0$$

# Solution
## In the potential well 
$V(x)=0$, let $\alpha=\sqrt{2mE}/\hbar$ 
Eq:
$$\frac{d^{2} u}{d x^{2}}+2 i k \frac{d u}{d x}+\left(\alpha^{2}-k^{2}\right) u=0$$
Then the solution is 
$$u_1(x)=A e^{-i(\alpha+k) x}+B e^{i(\alpha-k) x}$$ ^51ec97

## In the potential barrier
$V(x)=V_0>E$, let $\beta=\sqrt{2m(V_0-E)}/\hbar$ 
Eq:
$$\frac{d^{2} u}{d x^{2}}+2 i k \frac{d u}{d x}-\left(\beta^{2}+k^{2}\right) u=0$$
Subs $\alpha=i\beta$ in the equation [[#^51ec97|above]]
Then the solution is 
$$u_2(x)=C e^{(\beta-i k) x}+D e^{-(\beta+i k) x}$$


## PBC
Choose two boundary to analyse, like:
$$u_1(0)=u_2(0) \quad\quad u_1(c)=u_2(a-b), n=0,1$$
Then solve and obtain (by det=0):
$$\frac{\beta^{2}-\alpha^{2}}{2 \alpha \beta} \sinh \beta b \cdot \sin \alpha c+\cosh \beta b \cdot \cos \alpha c=\cos k a$$

- Include a $\delta$ -like: suppose $V_0\to \infty$ and $b\to 0$ but $V_0 b$ is limited and $\beta b=\sqrt{2m(V_0-E)}/\hbar\cdot b\to 0$ 



Then $$\cosh \beta b\to 1\quad\quad \sinh\beta b\to \beta b$$
Let $\lim \frac{\beta^{2} a b}{2}=P$ 
Then the equation derivated by det=0 becomes:
$$P \frac{\sin \alpha a}{\alpha a}+\cos \alpha a=\cos k a$$
(note: $a=b+c\approx c$) 

## Energy band 
Draw the PBC equation:
![[Pasted image 20220505115846.png]]
- 在图上找到在 $[-1,1]$ 范围内的点 (符合 $\cos \alpha a$ 的要求)，算出对应的 $E$ (一个 $\alpha$ 对应一个 $E$)
- 上述所有点算出对应的 $k$ ($\cos k a$)
- 画出 $E-k$ 图
![[Pasted image 20220505115809.png]]
解析：
![[Pasted image 20220505120724.png]]

这个也叫色散关系 (dispersion relation)，可以看到，同样也是可以限制在第一 [[Brillouin Zone|BZ]] 的
### General features of energy band
- There are energy bands and forbidden bands (能带与禁带)
The forbidden band (energy gap) appears at $k=\frac{n\pi}{a}$ (the boundary of BZ) 
**reason:** 波矢 $k=\frac{n\pi}{a}$ 时，满足[[晶体X-ray衍射#^d302b2|Bragg's law]] 全反射的条件，所以波不能进入晶体内部
![[Pasted image 20220505122250.png]]
- $E\sim k$ is even function
- the width of energy bands: energy $\uparrow$ , the width $\uparrow$
![[Pasted image 20220505122501.png]]
- periodic: the periodicity is $K_h$
since $$\cos ka=\cos(ka+2\pi)=\cos a(k+K_h)$$

- number of electrons: every energy band provide $2N$ electron 'accommodation'
只提供位置，不一定要填满

