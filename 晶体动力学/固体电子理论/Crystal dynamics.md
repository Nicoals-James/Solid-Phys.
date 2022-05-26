Here we talk about the quasi-classical dynamics

# Average velocity of electrons
Although [[Translation operator(空间平移算符)|translation operator]] and Hamiltonian is commutative ([[Bloch's theorem#^1d6bef|proof]]), the momentum operator is not commutative with Hamiltonian (reason is translation operator operates in translation direction). 

Since the eigenvector of electrons is the [[Bloch's theorem|Bloch wave]] (in position representation)
$$\hat H|k,r\rangle=E(k)|k,r\rangle$$

Where $\langle x|k,r\rangle=\psi(\boldsymbol r)=e^{i\boldsymbol k\cdot \boldsymbol r}u(\boldsymbol r)$ . So there is no definite value of momentum under these eigenvectors but average value.  ^b6b2d4

So the we define velocity operator
$$\hat v=\frac {\hat P} m$$
Notice that apply $\hat v$ to the Bloch wave
$$\hat v|k,r\rangle=\frac 1 m e^{i\boldsymbol k\cdot \boldsymbol r}(\hbar\boldsymbol k+\hat P)|r\rangle$$
Where $\langle x|r\rangle=u(\boldsymbol r)$ is the plane wave
[[Pasted image 20220514211748.png|derivation]]

Then the average velocity:
$$\begin{align}
\bar {\boldsymbol v}&=\langle k,r|\hat v|k,r\rangle\\
&=\langle r|\left[e^{-i\boldsymbol k\cdot \boldsymbol r}\frac 1 m e^{i\boldsymbol k\cdot \boldsymbol r}(\hbar\boldsymbol k+\hat P)\right]|r\rangle\\
&=\langle r| \frac 1 m  (\hbar\boldsymbol k+\hat P)|r\rangle
\end{align}$$

^aac388

Now the problem becomes to solve out the matrix element of $\frac 1 m  (\hbar\boldsymbol k+\hat P)$. We know the [[#^b6b2d4|Schrodinger Eq.]], then
$$\hat P^2|k,r\rangle=e^{i\boldsymbol k\cdot \boldsymbol r}(\hbar\boldsymbol k+\hat P)^2|r\rangle $$
(since we show above $\hat P e^{i\boldsymbol k\cdot \boldsymbol r}=e^{i\boldsymbol k\cdot \boldsymbol r}(\hbar\boldsymbol k+\hat P)$ ), so the Schrodinger eq becomes:
$$\frac 1 {2m}(\hbar\boldsymbol k+\hat P)^2|r\rangle=E(\boldsymbol k)|r\rangle$$
If we give a quasi-momentum perturbance $\delta \hbar \boldsymbol k$ to $\hbar\boldsymbol k$ then we have 
$$\begin{align}
LHS&=\frac 1 {2m}(\hbar\boldsymbol k+\hbar\delta \boldsymbol k+\hat P)^2|r\rangle\\
\\
&=\left[\frac 1 {2m}(\hbar\boldsymbol k+\hat P)^2+\frac \hbar {m}(\hbar\boldsymbol k+\hat P)\delta \boldsymbol k \right]|r\rangle
\end{align}$$
(2nd-order perturbance is omitted)
And 
$$\begin{align}
RHS&=E(\boldsymbol k+\delta \boldsymbol k)|r\rangle\\
&=[E(\boldsymbol k) +\nabla_kE(\boldsymbol k)\delta \boldsymbol k]|r\rangle
\end{align}$$
Both sides is written into expansion form, and each order is corresponding. So we have
$$\frac \hbar {m}(\hbar\boldsymbol k+\hat P)\delta \boldsymbol k=\nabla_kE(\boldsymbol k)\delta \boldsymbol k$$
Compare with [[#^aac388|the expression of average velocity]], then 

> **expression** Average velocity of electron motion
> $$\bar {\boldsymbol v}=\frac 1 \hbar \nabla_kE(\boldsymbol k)$$

^b6e6dc


# Equation of motion
For an external field $\boldsymbol f=-\nabla U$ , work done by the force equals the difference of energy
$$\boldsymbol f\cdot \bar{\boldsymbol v}~\mathrm dt=\boldsymbol f\cdot\frac 1 \hbar \nabla_kE(\boldsymbol k)\mathrm dt=\mathrm d E(\boldsymbol k)=\nabla_kE(\boldsymbol k)\cdot\mathrm d\boldsymbol k$$
So by the second and the last equal sign, we have
> **expression**  Equation of motion
> $$\boldsymbol f=\hbar \frac{\mathrm d \boldsymbol k}{\mathrm d t}$$
> Then we call the $\hbar \boldsymbol k$ **the quasi-momentum**.

^733cfd

Like the second law of Newton. $\boldsymbol f=\frac{\mathrm d \boldsymbol p}{\mathrm d t}$

## Quasi-momentum
Here we discuss why $\hbar \boldsymbol k$ is called the quasi-momentum. Obviously, $\hbar \boldsymbol k$ has the same dimension (量纲) of momentum but it's not the real momentum of anything.

The quasi-momentum is the eigenvalue of momentum operator $\hat P$ on Bloch wave

Proof in position representation 
![[Pasted image 20220514222036.png]]


# Acceleration and effective mass
since we obtain the [[#^b6e6dc|average velocity]] above, then the acceleration is 
$$\begin{align}
\bar{a}^i&=\frac{\mathrm d\bar {v}^i}{\mathrm d t}=\frac 1 {\hbar}\frac {\mathrm d }{\mathrm d t}\frac{\partial E(\boldsymbol k)}{\partial k_i}\\
&=\frac 1 {\hbar}\frac{\mathrm d k_j}{\mathrm d t} ~\frac{\partial } {\partial k_j}\frac{\partial E(\boldsymbol k)}{\partial k_i}\\
&=\frac 1 {\hbar^2}~\frac{\partial^2 E(\boldsymbol k)}{\partial k_i\partial k_j}f_j\\
&=\left(\frac{1}{m^*}\right)^{ij} f_j
\end{align}$$

^744259

where we define the effective mass tensor as $m^*$. (Einstein summation notation has been used)

> **expression**  effective mass
> $$\left(\frac{1}{m^*}\right)^{ij}=\frac 1 {\hbar^2}~\frac{\partial^2 E(\boldsymbol k)}{\partial k_i\partial k_j}$$
we can choose proper axes then $\left(\frac{1}{m^*}\right)^{ij}$ becomes a diagonal matrix:$$\left(\begin{array}{l}
a_{x} \\
a_{y} \\
a_{z}
\end{array}\right)=\left(\begin{array}{ccc}
\frac{1}{m_{x x}} & \\
& \frac{1}{m_{y y}} & \\
& & \frac{1}{m_{z x}}
\end{array}\right)\left(\begin{array}{l}
F_{x} \\
F_{y} \\
F_{z}
\end{array}\right)$$

^971bd1


mostly, we are in 1-dimension case(1-D dispersion relation is clear), so  
$$\frac{1}{m^*}=\frac 1 {\hbar^2}\frac{\partial^2 E(k)}{\partial k^2}$$
we discuss the 1D case below.

## the relation of effective mass and dispersion relation
### the value of effective mass
here comes a question which effective mass is larger of the two energy bands below
![[Pasted image 20220515174857.png]]
since the 2nd order derivative of the curve is positive, we know the gentler the energy band changes, the smaller $\frac{\partial^2 E(k)}{\partial k^2}$ would be. then
$$m_{2}^{*}>m^{*}_1>0$$
another case:
![[Pasted image 20220515195030.png|400]]
since the 2nd order derivative of the curve is negative, so $$m_{2}^{*}<m^{*}_1<0$$ ^635cb2
- conclusion
> **theorem** the flatter the $E(k)$ curve is, the larger the absolute value of effective mass.
> (越平绝对值越大)

### energy in terms of effective mass
write [[Nearly free electron model#^d4fc28|energy near the boundary of BZ]]($E(k)_{\pm}=T_{n}\pm\left|V_{n}\right|+T_{n}\left(1\pm\frac{2 T_{n}}{\left|V_{n}\right|}\right) (\delta k)^{2}$ ) in terms of effective mass 
$$\begin{align}
E_+&=E_{min}+\frac{\hbar^2}{2m^*_{bottom}}(\delta k )^2\\
E_-&=E_{max}+\frac{\hbar^2}{2m^*_{top}}(\delta k )^2
\end{align}$$
- here is how it comes:
Taylor expand the energy near the boundary of BZ
$$E(k)=E_0+\frac{\partial E}{\partial k}\delta k+\frac 1 2 \frac{\partial^2 E}{\partial k^2}(\delta k)^2$$
the first term is $E_{min}$ for $E_+$ and $E_{max}$ for $E_-$ (see the fig); the second term equals zero; then the third term can be written in effective mass
![[Pasted image 20220510094758.png|400]]

- 结论
$m^*$ 不同于电子质量$m_e$, 它记录了周期性势能的影响; 电子受外场作用, 能量动量都发生变化, 而且要于晶格交换能量动量(与声子碰撞), 如果从外场得到动量大于交给声子动量, 则电子动量增加($m^*>0$) 反则, 电子动量减少($m^*<0$)


# Holes(空穴)
when a $\boldsymbol k$ state is empty, the total current of energy bands is as if caused by a positive charge $e$ with velocity the same as that of electron in the $\boldsymbol k$ state. Such empty state is called **hole**.

In short, a hole = a positive electron. when electrons jump to the higher energy band by thermal excitation, holes are generated

the intensity of current of a hole 
$$\vec j=e \vec v(\vec k)$$

## hole motion
for a electron $-e$ moving in an external field:
$$\frac{d \vec{v}}{d t}=\frac{-e}{m_{e}^{*}}(\vec{\varepsilon}+\vec{v} \times \vec{B})$$
then if this electron is gone and replace by a hole, the hole would move in the same path as the electron did
$$\frac{d \vec{v}}{d t}=\frac{e}{-m_{e}^{*}}(\vec{\varepsilon}+\vec{v} \times \vec{B})$$
by this equation, we can regard a hole is a positive electron $e$ with effective mass $-m_e^*$. we define $m_h^*=-m_e^*$ as the **effective mass of a hole** 

since it's easier for a electron at the top of a energy band(maximum energy) to be exited to higher band, holes is mostly generated at the top of the band where $m_e^*<0$ (ref:[[#^635cb2|effective mass at top and bottom]]), so the effective mass of a hole is mostly positive $m_h^*>0$. 

### momentum and energy 
![[Pasted image 20220517095942.png]]