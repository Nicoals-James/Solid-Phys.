After classical theory of free electron (valence electrons are treated as classical particles, like ideal gas) by P. Drude and H. A. Lorentz, Sommerfeld found the quantum theory of free electron.

# Sommerfeld model
> **model**  Sommerfeld model (索莫菲模型)
> Quantum free electron gas, no-interaction, obeys [[近独立子系#F-D 分布|FD statistics]].

![[Pasted image 20220426085818.png|400]]

The potential of field of the crystal (infinity potential well):
$$\left\{ \begin{array}{l}
V(x, y, z)=0, \quad 0<x, y, z<L \\
V(x, y, z)=\infty, \quad x, y, z \geq L
\end{array} \right.$$
Then [[stationary Schrodinger eq]] under position representation:
$$\nabla^{2} \psi+\frac{2 m}{\hbar^{2}} E \psi=0$$
After separating variables, solve the equation and gain wave function under position representation:
$$\psi(\vec{r})=\frac{1}{\sqrt{V}} e^{i \vec{k} \cdot \vec r}$$
Where $k_i=\frac{2\pi}{L}n_i,\quad n_i\in \mathbb Z$.
The eigenvalue (energy) is $E=\frac{\hbar^2k^2}{2m}$  ^001c3e

- Periodic boundary condition:
Wave function is totally the same in different crystal block, that is
$$\begin{array}{l}
\psi(x+L, y, z)=\psi(x, y, z) \\
\psi(x, y+L, z)=\psi(x, y, z) \\
\psi(x, y, z+L)=\psi(x, y, z)
\end{array}$$
## State in $\vec k$ space
In fact, $\vec k$ space is a momentum space and a [[倒易点阵（Reciprocal lattice）|reciprocal space]], vectors in $\vec k$ space can be represented by $\vec{k}=k_{x} \vec{i}+k_{y} \vec{j}+k_{z} \vec{k}$ 

Then the density of representative points in $\vec k$ space (the point satisfying the quantum number of the system) is 
$$\rho(\vec k)=\frac V {(2\pi)^3}$$
- Derivation:
Total number of representative points: $N=n_x\cdot n_y\cdot n_z$ 
So $$\rho=\frac{N}{\vec k_x\cdot (\vec k_y\times \vec k_z)}=\frac{n_x\cdot n_y\cdot n_z}{\frac{(2\pi)^3}{L^3}n_x\cdot n_y\cdot n_z}=\frac V {(2\pi)^3}$$



## DOS
The DOS $g(E)$ satisfies:
$$g(E)\mathrm d E=2\int_{\mathrm dE}\rho(k)\mathrm d k\quad \text{or}\quad g(E)=\frac{\mathrm d Z}{\mathrm d E}$$
Attention that coefficient $2$ comes from the state of electron spin.
(ref: [[经典晶体振动#The density of states DOS]])
Where $\mathrm d Z$ is the number of states


The equi-energy surface within free electron approximation is a sphere with radius $k=\sqrt{2mE}/\hbar$ 

then the density of $k$, (3-dimension)
$$\rho(k)=\frac{V}{(2\pi)^3}$$

Then the DOS of free electron approximation
$$g(E)=4 \pi V_{c}\left(\frac{2 m}{h^{2}}\right)^{3 / 2} E^{1 / 2}$$ ^a1e5fd

![[Pasted image 20220426094636.png|300]]

## Fermi energy of electron gas
Ref: [[Fermi gas]]

We will derivate the energy of electron gas in another way.

### Prepare
- Total distribution
$$f(E)=\frac{g_l}{e^{(E-E_F)/kT}+1}$$
Where $E_F$ is [[Fermi gas#^4f01a7|Fermi energy]]

![[Pasted image 20220428113211.png|300]]
In different cases
- $T=0K$
$$f(E)=\left\{\begin{array}{ll}
1, & E<E_F^0 \\
0, & E>E_F^0
\end{array}\right.$$

- $T\neq 0K$
$$f(E)=\left\{\begin{array}{ll}
1, & E-E_F^0< \text{several} ~~kT\\
1/2 &E=E_F^0\\
0, & E-E_F^0>\text{several} ~~kT
\end{array}\right.$$

Some parameters
- Fermi temperature $T_F=E_F/k_B$
- Fermi wave vector $k_F=\sqrt{2mE_F}/\hbar$ 

### Fermi energy in different cases
We usually calculate Fermi energy via the relation between it and particle number
$$\begin{align}
N&=\sum_E f(E)\\
&=\int f(E)g(E)\mathrm dE
\end{align}$$
Where $g(E)$ is [[#^a1e5fd|DOS above]]

#### $T=0K$

$$N=\int_0^{E_F^0} f(E)g(E)\mathrm dE$$
Then 
$$E_F^0=\frac{h^{2}}{2 m}\left(\frac{3 n}{8 \pi}\right)^{2 / 3}$$
(ref: [[Fermi gas#T 0]]  where $g=2$)

And **average energy at $T=0$ **:
$$\bar E=\frac E N=\frac{3}{5}  E^0_{\mathrm{F}}$$ ^09b9db

#### $T\neq 0$
- Prerequisite: $-\frac{\partial f}{\partial E}$ is a $\delta$ - like function at $E_F$
![[Pasted image 20220430094138.png|200]]

According to the expression above 
$$N=\int_0^{\infty} f(E)g(E)\mathrm dE$$
Where  
$$f(E)= \frac{1}{\exp \left(\frac{E-E_{F}}{k T}\right)+1} ,\quad\quad\quad g(E) =C E^{1 / 2}$$
Where $C$ represents the coefficient of $g(E)$. Integral by parts then 
$$N=\left. f(E)(\int_0^E g(E)\mathrm dE) \right|_{0} ^{\infty}+\int_{0}^{\infty} (\int_0^E g(E)\mathrm dE)\left(-\frac{\partial f}{\partial E}\right) d E$$
Let
$$H(E)=\int_0^E g(E)\mathrm dE$$
Then 
$$\left.N=f(E)H(E)\right|_{0}^{\infty} + \int_{0}^{\infty} H(E)\left(-\frac{\partial f}{\partial E}\right) \mathrm d E$$
Since the first term equals zero ($E\to \infty,f(E)=0$). Then we come to discuss the expression of the latter one. ^297c4e

Since $-\frac{\partial f}{\partial E}$ is $\delta$ -like, the integral does not equal zero only in the neighbourhood of $E_F$, do Taylor expansion on $H(E)$
$$H(E)=H(E_F)+H^{\prime}(E_F)(E-E_F)+\frac{1}{2} H^{\prime \prime}(E_F)(E-E_F)^{2}+o(E^2)$$

Then the total number
$$\begin{aligned}
N=& H(E_F) \int_{0}^{\infty}\left(-\frac{\partial f}{\partial E}\right) \mathrm{d} E+H^{\prime}(E_F) \int_{0}^{\infty}(E-E_F)\left(-\frac{\partial f}{\partial E}\right) \mathrm{d} E \\
&+\frac{1}{2} H^{\prime \prime}(E_F) \int_{0}^{\infty}(E-E_F)^{2}\left(-\frac{\partial f}{\partial E}\right) \mathrm{d} E\\
&=N_1+N_2+N_3
\end{aligned}$$
#### The first term 
For $-\frac{\partial f}{\partial E}$ is $\delta$ -like, 
$$N_1=H(E_F)$$
#### The second term
Also for $\delta$ -like,
$$N_2=E_F-E_F=0$$
It can also be deducted precisely by include a new variable $\eta$ (see discussion below)
#### The third term 
It's little bit different for the term of the second order, because this $\delta$ -like is too rough here.

Include a new variable $\eta$
$$\eta=\frac{E-E_F}{kT}$$
Then the third term:
$$N_3=\frac 1 2 (kT)^2 H''(E_F)\int^{\infty}_{-E_F/kT}\frac{\eta^2e^{-\eta}}{(1+e^{-\eta})^2}\mathrm d \eta$$
([[#^297c4e|expression of f]]) since $-E_F/kT$ is small enough (in room temperature) to regard it as negative infinity then calculate the integral in _mathematica_ 
$$\int^{\infty}_{-\infty}\frac{\eta^2e^{-\eta}}{(1+e^{-\eta})^2}\mathrm d \eta=\frac {\pi^2} 3$$
That is 
$$N_3=\frac{\pi^2} 6 (kT)^2H''(E_F)$$

--------
After all 
$$N=H(E_F)+\frac{\pi^{2}}{6}\left(k T\right)^{2} H^{\prime \prime}(E_F)$$

For 
$$H(E_F)=\frac{2}{3} C E_F^{3 / 2}, H^{\prime \prime}(E_F)=\frac{1}{2} C E_F^{-1 / 2}$$
Where $C=4 \pi\left(\frac{2 m}{\hbar^{2}}\right)^{3 / 2}$

Then the **Fermi energy at $T\neq 0$ ** is 
$$\begin{align}
E_F&=E^0_{\mathrm{F}}\left[1+\frac{\pi^{2}}{8}\left(\frac{k_{\mathrm{B}} T}{E_F}\right)^{2}\right]^{-2 / 3}\\
&\approx E^0_{\mathrm{F}}\left[1-\frac{\pi^{2}}{12}\left(\frac{k_{\mathrm{B}} T}{E_F}\right)^{2}\right]
\end{align}$$
Actually the expression is a equation which we don't expect. Do a **trick**: for $kT$ is small and $E_F,E^0_F$ are so big, substituting $E_F$ for $E_F^0$ makes little difference, then
$$E_F\approx E^0_{\mathrm{F}}\left[1-\frac{\pi^{2}}{12}\left(\frac{k_{\mathrm{B}} T}{E^0_F}\right)^{2}\right]$$
- The total energy of the system is showed below. 
![[Fermi gas#^a30cba]]
- Since average energy at $T=0$ is $\bar E_0 =3/5 N E_F^0$  (ref: [[#^09b9db]]), then the **average energy** is 
$$\bar E=\frac 3 5 N E^0_F\left[1+\frac{5}{12} \pi^{2}\left(\frac{k_{B} T}{E_{F}^{0}}\right)^{2}\right]=\bar{E}_{0}\left[1+\frac{5}{12} \pi^{2}\left(\frac{k_{B} T}{E_{F}^{0}}\right)^{2}\right]$$


# Heat capacity of electron gas
$$C_{v}^{e}=\left(\frac{\partial \bar{E}_{e}}{\partial T}\right)_{V}=\frac{\pi^{2}}{2}N_e k_{B} \frac{k_{B} T}{E_{F}^{0}}$$
Used the first equal sign of the average energy expression. and where $N$ is the number of electrons.

Since the  phonon ([[固体热容理论(固物)#Debye Model|Debye model]]) distributes the $T^3$ term for [[Solid heat capacity theory#^475c50|the empirical formula]], now the electron gas distributes the $T$ term.
