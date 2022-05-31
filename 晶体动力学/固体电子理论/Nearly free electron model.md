The band structure of a crystal can often be explained by the nearly free electron model for which the band electrons are treated as perturbed only weakly by the periodic potential of the ion cores.

Following we will discuss the case in **one-dimension**
# Preparation
Since the potential is periodic $V(x)=V(x+na)$ then, we can do [DFT](https://en.wikipedia.org/wiki/Discrete_Fourier_transform) of it 
$$V(x)=V_{0}+\sum_{m}' V_{m} e^{i \frac{2 \pi}{a} m x}$$
Regard the latter term as a **perturbance**, denoted by $H'$ 

Then the Hamiltonian of the electron becomes:
$$H=H_0+H'=(\frac {P^2}{2m}+V_0)+\sum_{m}' V_{m} e^{i \frac{2 \pi}{a} m x}$$
For convenience, let $V_0=0$ 

# Non-degenerate case
Without the perturbance, the electron acts the same as **free electron**, so the eigenvector in position representation is 
$$\langle x|0n\rangle=\frac{1}{\sqrt{L}} e^{i k_n x}$$
Where $k_n=\frac{2\pi}{L}n$, revealed in [[Free electron theory#^001c3e|wave function of 'free' electron]]
According to [[Method of Perturbation]], the relations of non-perturbance and perturbance systems follows
The matrix equation:
$$HU=UE$$
And transition between the eigenvector of perturbance system $|n\rangle$ and of non-perturbance system $|0n\rangle$ is represented by
$$ |n\rangle=U |0n\rangle$$
## the zero approx
- 0th energy is the energy of free electron
$$E^{(0)}_n=\frac{\hbar ^2k_n^2}{2m_e}$$
- 0th transition matrix
$$U^{(0)}=\mathbb 1$$
- 0th eigenvector
$$ |n\rangle^{(0)}=|0n\rangle$$

## the first approx
- 1th energy is revealed in [[Method of Perturbation#The first-order approx|method of perturbance]] 
$$E^{(1)}_{n}=H'_{nn}=\langle 0n|~H'~|0n\rangle=\langle 0n|~\sum_{m}' V_{m} e^{i \frac{2 \pi}{a} m x}~|0n\rangle$$
Then write in position representation
$$\int _0^L \frac{1}{\sqrt L} e^{ik(x-x')}\delta(x-x')\sum_{m}' V_{m}e^{i \frac{2 \pi}{a} m x}\mathrm d x\mathrm d x'$$
Since [[Bloch's theorem|PBC]], $e^{i2\pi/a nL}=e^0=1$, then 
$$E^{(1)}_n=0$$

- 1th transition matrix
According the calculation below:
$$U^{(1)}_{nl}=\frac{H'_{nl}}{E^{(0)}_l-E^{(0)}_n}=\sum_{m}' \frac{2 m_e V_{n} }{\hbar^{2}\left(k_n-\frac{2 \pi}{a} m\right)^{2}-\hbar^{2} k_n^{2}}$$
$H'_{nl}=V_m$  where $n$ satisfies $k_l=k_n-\frac{2\pi} a n$ 
 ^dd6873
- 1th eigenvector
$$|n\rangle^{(1)}=\sum_l U_{nl}^{(1)}|0l\rangle$$
That is 
$$\langle x|n\rangle^{(1)}=\frac{1}{\sqrt{L}} \sum_{m}'\frac{2 m_e V_{n} }{\hbar^{2} k_n^{2}-\hbar^{2}\left(k_n-\frac{2 \pi}{a} m\right)^{2}}e^{i (k_n-\frac{2\pi} a n) x}$$ ^3bc59b

## The second approx
- 2th energy (revealed in [[Method of Perturbation#^eb8dfa|method of perturbance]])
$$E^{(2)}_n=\sum_{l}' \frac{H_{n l}' H_{l n}'}{E_{n}^{(0)}-E_{l}^{(0)}},~~~~~~(l\ne n)$$
Then write in position representation
$$\begin{align}
H'_{nl}&=\langle 0n|~\sum_{m}' V_{m} e^{i \frac{2 \pi}{a} m x}~|0l\rangle\\
&=\int_0^L e^{i(k_n-k_l)x}\sum_m V_m e ^{i\frac{2 \pi}{a} m x} \mathrm d x\\
&=\sum_mV_m\int_0^L e^{i(k_l-k_n+\frac{2\pi} a m)x}\mathrm d x\\
&=\sum _mV_m\delta(k_l-k_n+\frac{2\pi} a m)
\end{align}$$
So $H'_{nl}=V_m$  where $m$ satisfies $k_l=k_n-\frac{2\pi} a m$ then 
$$E^{(2)}_n=\sum_{m}' \frac{2 m_e\left|V_{m}\right|^{2}}{\hbar^{2} k_n^{2}-\hbar^{2}\left(k_n-\frac{2 \pi}{a} m\right)^{2}}$$ ^af6c18
- 2-th transition matrix 
Too small, just remain the 1th approx of eigenvector

## Conclusion
- Energy 
$$E_n=E_n^{(0)}+E^{(2)}=\frac{\hbar ^2k_n^2}{2m_e}+\sum_{m}' \frac{2 m_e\left|V_{m}\right|^{2}}{\hbar^{2} k_n^{2}-\hbar^{2}\left(k_n-\frac{2 \pi}{a} m\right)^{2}}$$ ^591150
- Eigenvector
$$\begin{align}
\langle x|n\rangle&=\langle x|n\rangle^{(0)}+\langle x|n\rangle^{(1)}\\
&=\frac{1}{\sqrt{L}} e^{i k x}\left[1+\sum_{m}'\frac{2 m V_{n}^{*} e^{-i \frac{2 \pi}{a} n x}}{\hbar^{2} k_n^{2}-\hbar^{2}\left(k_n-\frac{2 \pi}{a} m\right)^{2}}\right]
\end{align}$$

# Failure of non-degenerate perturbation theory
When the difference between $k_n$ and $k_l$ is too small, the non-degenerate theory fails.


- At the boundary of [[Brillouin Zone|BZ]], and we can always pick $k_l$ satisfies the following relationship:
$$k_n=\frac{K_{n}}{2}=\frac{\pi n}{a}, \quad k_l=k_n-\frac{2 \pi}{a} n=-\frac{\pi n}{a}$$
Then $E^{(0)}_n=E^{(0)}_l$ , then [[#^af6c18|the second approx of energy]], and [[#^3bc59b|the first approx of eigenvector]] approach to infinity
$$E_{n}^{(2)} \rightarrow \infty, \quad \psi_{n}^{(1)} \rightarrow \infty$$
So the theory fails at the boundary of BZ


# Degenerate case
Since non-degenerate theory can not handle the boundary of BZ, we apply degenerate theory for it and it's neighborhood.

we know from above, energy of the two boundary $\pm \frac {\pi} n$ of BZ degenerates to one. for convenience, denote the point on the neighborhood of each boundaries by $k,k'$ 
![[Pasted image 20220509224713.png|300]]
so for $|\Delta|<<1$ , we have
$$k=\frac{n\pi}{a}(1+\Delta), \quad k^{\prime}=-\frac{n\pi}{a}(1-\Delta)$$
clear that the system at the boundary of BZ is a two-degree degeneracy. ^0878da

according to [[Method of Perturbation#Degeneracy case|degenerate theory]]: 
- 0th approx of eigenvector
$$|\psi\rangle^0=A|k\rangle+B|k'\rangle$$
$$\psi^{0}=A \psi_{k}^{0}+B \psi_{k^{\prime}}^{0}=A \frac{1}{\sqrt{L}} e^{i k x}+B \frac{1}{\sqrt{L}} e^{i k^{\prime} x}$$
subs to Schrodinger eq and gain 
$$ \left(H^{\prime}-E_{n}^{(1)} I\right)\left[\begin{matrix}A\\B \end{matrix}\right]=0$$

the matrix equation induce det = 0
$$\det \left(H^{\prime}-E_{n}^{(1)} I\right) =0$$
from calculate [[#^af6c18|above]], $H'_{nl}=\sum _mV_m\delta(k_l-k_n+\frac{2\pi} a m)$, notice that 
the first column of the matrix is labeled by $k$, the second one by $k'$ 
$$H'_{kk'}=V_n,\quad H'_{k'k}=V_{-n},\quad H'_{kk}=H'_{k'k'}=0$$
for $E_{n}^{(1)}=E-E_{n}^{(0)}$
$$\left|\begin{array}{cc}
-E+E^{0}(k) & V_{-n} \\
V_{n} & -E+E^{0}\left(k^{\prime}\right)
\end{array}\right|=0$$
then 
$$E(k)=\frac{1}{2}\left[E^{0}(k)+E^{0}\left(k^{\prime}\right)\right] \pm\left\{\left[E^{0}(k)-E^{0}\left(k^{\prime}\right)\right]^{2}+\left|V_{n}\right|^{2}\right\}^{1 / 2}$$
for [[#^0878da|the relation]] of $k$, $E(k)=\frac{\hbar^2k^2}{2m}$ then expression above can be simplified to 
$$E(k)=T_{n}\left(1+\Delta^{2}\right) \pm\left\{\left|V_{n}\right|^{2}+4 T_{n}^{2} \Delta^{2}\right\}^{1 / 2}$$
where $$T_{n}=\frac{\hbar^{2}}{2 m}\left(n \frac{\pi}{a}\right)^{2}$$
- simplify 
![[Pasted image 20220510094509.png|400]]

so the two split energy near the boundary of BZ are $$\left\{\begin{array}{l}
E(k)=E(k)_{+}=T_{n}+\left|V_{n}\right|+T_{n}\left(1+\frac{2 T_{n}}{\left|V_{n}\right|}\right) \Delta^{2} \\
E(k)=E(k)_{-}=T_{n}-\left|V_{n}\right|-T_{n}\left(\frac{2 T_{n}}{\left|V_{n}\right|}-1\right) \Delta^{2}
\end{array}\right.$$it's a parabola approximately
![[Pasted image 20220510094758.png|400]] ^d4fc28


# conclusion 
integrate all cases 
then the **dispersion relation**
![[Pasted image 20220510095434.png]]

- $\Delta=0$ 
$$\begin{array}{l}
k=\frac{K_{n}}{2}=\frac{n \pi}{a}, \quad k^{\prime}=-\frac{K_{n}}{2}=-\frac{n \pi}{a} \\
E_{+}=T_{n}+\left|V_{n}\right|, \quad E_{-}=T_{n}-\left|V_{n}\right|
\end{array}$$
then the width of the energy gap $E_g=2|V_n|$ 