This model is used to describe electrons in a strong potential field of ion cores. If the variation of potential is small enough, use [[Nearly free electron model]] to describe. 

# Preparation 
When the interactions between atoms are weak but the interactions between atoms and electrons are strong, the electrons can be regarded as those in an isolated atoms.

When an electron is located within the region of an atom, whose position vector is $\vec R_n$, the electron is described by different functions of orbitals $\varphi_{\alpha}^{a t}\left(\vec{r}-\vec{R}_{n}\right)$ (the explanation of index shows below). The electrons in crystal is **communized** and do not exclusively (专有，排他) belong to a certain atom.  So generally, the electron moves in the composition of the orbits of different atoms $\vec R_n$.

> **orbital function and notation**
> $$\varphi_{\alpha}^{a t}\left(\vec{r}-\vec{R}_{n}\right)$$ represents the orbital function of the electron $\alpha$ at the regime of atom $\vec R_n$

Then the wavefunction of electron $\alpha$ is 
$$\psi_{\alpha}(\vec{k} , \vec{r})=\sum_{n} a_{n} \varphi_{\alpha}^{a t}\left(\vec{r}-\vec R_{n}\right)$$
This wavefunction should satisfy [[Bloch's theorem]],
$$\hat T_{\vec R_m}\psi_{\alpha}(\vec{k} , \vec{r})=e^{i\vec k\cdot \vec R_m}\psi_{\alpha}(\vec{k} , \vec{r})$$  since changing $R_n$ won't change distribution
$$\hat T_{\vec R_m}\psi_{\alpha}(\vec{k} , \vec{r})=\sum_{n} a_{n+m} \varphi_{\alpha}^{a t}\left(\vec{r}-\vec R_{n}+\vec R_m\right)=\psi_{\alpha}(\vec{k} , \vec{r})$$
For $a_n=Ae^{i\vec k\cdot \vec R_n}$  suits the two equation then 

> **wavefunction**(before normalization)
> $$\psi_{\alpha}(\vec{k}, \vec{r})=A \sum_{n} \varphi_{\alpha}^{a t}\left(\vec{r}-\vec{R}_{n}\right) e^{i \vec{k} \cdot \vec{R}_{n}}$$


![[Pasted image 20220523192201.png]]

## Normalization
Write the wavefunction in a compacter form: (eigenvector of energy, or $k$ -vector)
$$|\psi_\alpha\rangle=A\sum_n e^{i \vec{k} \cdot \vec{R}_{n}} |\varphi_\alpha,\vec R_n\rangle$$**approximately** we consider that $\{|\varphi_\alpha,\vec R_n\rangle\}$ is **orthonormal** set of vectors, since $\langle\varphi_\alpha,\vec R_m|\varphi_\alpha,\vec R_n\rangle$ does not significantly equal zero only when two atoms $\vec R_n, \vec R_m$  share their orbits of the electron, which only happens when $n=m$ in this approximation.

> **orthonormal condition of orbital function**
> $$\langle\varphi_\alpha,\vec R_m|\varphi_\alpha,\vec R_n\rangle=\delta_{mn}$$

So because of unitarity, $\langle \psi_\alpha|\psi_\alpha\rangle=1$
$$\begin{align}
\langle \psi_\alpha|\psi_\alpha\rangle&=A^2\sum_n\sum_m\left\langle\varphi_\alpha,\vec R_m\middle| e^{i\vec k\cdot(\vec R_n-\vec R_m)}\middle |\varphi_\alpha,\vec R_n\right\rangle\\
\\
&=A^2\sum_n^N\sum_m^N e^{i\vec k\cdot(\vec R_n-\vec R_m)}\delta_{mn}\\
&=A^2N=1
\end{align}$$
So the coefficient is $A=\frac{1}{\sqrt N}$ 

> **wavefunction**(after normalization) electron at state $s$ 
> $$|\psi_\alpha\rangle=\frac{1}{\sqrt N}\sum_n e^{i \vec{k} \cdot \vec{R}_{n}} |\varphi_s,\vec R_n\rangle$$
> **we will just discuss $s$ band below**

and for electrons from $p$ and $d$ states, the wavefunction is combination of the single wavefunction
$$|\psi\rangle=\sum_\alpha|\psi_\alpha\rangle$$


# Energy band $E(\vec k)$
In this section, we gonna solve the eigenvalue of $\hat H$==**of $s$ state** ==

with respect to electron,  $$\hat H= \frac{\hat P^2}{2m_e}+\hat V(r)$$
notice the term of potential energy is the whole potential field, but we need component form to put inside the summation. 
$$\hat H= \frac{\hat P^2}{2m_e}+\hat V^{at}(r-\vec R_m)+\hat{V}(r) -\hat V^{at}(r-\vec R_m)$$
the first two terms are Hamiltonian of a single electron in the field of a single atom
![[Pasted image 20220523205527.png]]
$$\left[\frac{\hat P^2}{2m_e}+\hat V^{at}(r-\vec R_m)\right]\left|\varphi_s,\vec R_n\right\rangle=E^{at}\left|\varphi_s,\vec R_n\right\rangle$$

then the **eigenvalue**:
$$\begin{align}
\left\langle\psi_s\middle |\hat H\middle|\psi_s\right\rangle&=\left\langle\psi_s\middle |\frac{\hat P^2}{2m_e}+\hat V(r)\middle|\psi_s\right\rangle\\

&=\frac 1 N \sum_n\sum_m \left\langle\varphi_s,\vec R_m\middle|e^{-i \vec{k} \cdot \vec{R}_{m}}\left[\frac{\hat P^2}{2m_e}+\hat V^{at}(r-\vec R_m)\right]e^{i \vec{k} \cdot \vec{R}_{n}}\middle|\varphi_s,\vec R_n\right\rangle \\
&+\frac 1 N \sum_n\sum_m \left\langle\varphi_s,\vec R_m\middle|\left[\hat V(r)-\hat V^{at}(r-\vec R_m)\right]e^{i \vec{k} \cdot (\vec{R}_{n}-\vec R_m)}\middle|\varphi_s,\vec R_n\right\rangle
\end{align}$$
the first term equals $\sum\sum\frac 1 N NE^{at}_s\delta_{nm}=E^{at}_s$  then the second term can be separated into two parts. before we do that, we first introduce an approximation. Because the range of the interaction between atoms is short, we just consider the interaction of the nearest atoms. so summation $\sum_n$ becomes a summation with respect to the nearest atoms, and denoted by 
$$\sum_n^N\to\sum_n^{N.N}$$

and we can fix $m=0$ to which is $\langle\varphi_s,\vec R_m|\to \langle\varphi_s,0|$   for symmetry 
$$\sum_m^N\to N$$
so the second term can be written by:
- when $n=0$, introduce $C_s$
$$\begin{align}
C_s&=\frac 1 N \sum_n^{N.N}N\left\langle\varphi_s,0\middle|\hat V(r)-\hat V^{at}(r-\vec R_n)\middle|\varphi_s,\vec R_n\right\rangle\\
&= \left\langle\varphi_s,0\middle|\hat V(r)-\hat V^{at}(r)\middle|\varphi_s,0\right\rangle
\end{align}$$
- when $n\neq 0$, introduce $J$
$$\begin{align}
The~second~term&= \sum_n^{N.N}\left\langle\varphi_s,0\middle|\left[\hat V(r)-\hat V^{at}(r-\vec R_n)\right]e^{i \vec{k} \cdot \vec{R}_{n}}\middle|\varphi_s,\vec R_n\right\rangle\\
&=J\sum_n^{N.N}e^{i\vec k\cdot \vec R_n}
\end{align}$$

where $J=\left\langle\varphi_s,0\middle|\hat V(r)-\hat V^{at}(r-\vec R_n)\middle|\varphi_s,\vec R_n\right\rangle$, the validity lies on where eigenvector and $e^{i \vec{k} \cdot \vec{R}_{n}}$(just a number) are commutative, and potential and orbital functions are the same between nearest atoms.

Eventually, we generate the equation of energy  band in tight binding method:
> **energy band**
> $$E(\vec k)=E_{s}^{a t}+C_{s}-J \sum_{R_{n}}^{N.N} e^{i \vec{k} \cdot \vec{R_{n}}}$$

the key of calculation now becomes the summation on nearest atoms, and we have table below for tips.
![[Pasted image 20220524100536.png]]


## band width
we just take **bcc and $s$ band only** as an example
$$\begin{align}
E_{s}(\vec{k}) & = E_{s}^{a t}+C_{s}-J \sum_{n}^{N. N} e^{i \vec{k} \cdot \vec{R}_{n}} \\ & = E_{s}^{a t}+C_{s}-J \sum_{n}^{N .N} e^{i\left(k_{x} \vec{i}+k_{y} \vec{j}+k_{z} \vec{k}\right) \cdot \vec{R}_{n}} \\ & = E_{s}^{a t}+C_{s}-8 J \cos \frac{a}{2} k_{x} \cos \frac{a}{2} k_{y} \cos \frac{a}{2} k_{z}
\end{align}$$
- $E_s(\vec k)$ reaches its **minimum** at $\Gamma$ point (ref: [[Brillouin Zone#Symmetry points and axes]]), where $k_{x}=k_{y}=k_{z}=0$
$$E_{s \min }=E_{s}^{a t}+C_{s}-8 J$$

- $E_s(\vec k)$ reaches its **maximum** at $H$ point $$\begin{array}{l}
k_{x}=\pm \frac{2 \pi}{a}, \quad k_{y}=0, \quad k_{z}=0 \quad \quad(H_1) \\
k_{x}=0, \quad k_{y}=\pm \frac{2 \pi}{a}, \quad k_{z}=0 \quad \quad(H_2) \\
k_{x}=0, \quad k_{y}=0, \quad k_{z}=\pm \frac{2 \pi}{a} \quad \quad(H_3)
\end{array}$$$$E_{s \max }=E_{s}^{a t}+C_{s}+8 J$$
## effective mass
ref: [[Crystal dynamics#^971bd1|definition of effective mass]]
energy band can always can represented by the terms of effective mass.
$$E(\vec k)=E_0+\frac 1 2\hbar ^2k_i\left(\frac{1}{m^*}\right)^{ij}k_j$$