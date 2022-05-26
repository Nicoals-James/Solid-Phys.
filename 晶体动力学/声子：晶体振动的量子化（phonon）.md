 > **Prerequisite**: [[Lagrangian Mechanics]], [[equation of vibration]], [[solution of vibration]]

# Vibration in normal coordinate
==we just consider monoatomic chain here==
## represent in generalized coordinate
According to the formulas revealed in [[General Coordinate And General Momentum#Dynamics in Generalized Coordinate|generalized coordinate]], the energy component of lattice wave is showed below:
- Kinetic energy: $T=\frac{1}{2} \sum_{i} m_{i} \dot{u}_{i}^{2}$
- Potential energy: $U=\left.\frac{1}{2} \sum_{i, k} \frac{\partial^{2} U}{\partial u_{i} \partial u_{k}}\right|_{0} u_{i} u_{k}$

Where $u_i$ is the displacement of each atom (generalized coordinate)


## represent in normal coordinate
Then, Lagrangian: $\mathcal L=T-U$. Apply _E-L eq._ and linear transformation to $\mathcal L$  then obtain **canonical equation**: $$\ddot Q(q)+\omega_q^2Q(q)=0$$
And solution:
$$Q_q(t)=A_q e^{-\omega_q t}$$ 

- **note:** the linear transformation above is actually a [[Fourier Transform in Vector Space#Finited dimension case DFT|DFT]]:
$$\mathcal F:u~(\text{generalized coordinate},n a)\to Q~\text{(normal coordinate}, \vec q)$$
从正空间函数变成倒空间函数。
Explicitly: (can be defined, the coefficient is arbitrary and artificial)
$$u(n a)=\frac {1} {\sqrt{m}} \sum_q Q(q)e^{-iq~na}$$
where $m$ is the mass of the atom in the monoatomic chain.
这里定义变换常数 $1/m$ 是为了后面用简正坐标表示动能的时候不含系数。
(ref:[Phonon - Wikipedia](https://en.wikipedia.org/wiki/Phonon#Quantum_treatment))


After the conversion above, we can represent the energy in terms of $Q_j$
- Kinetic energy: $T=\frac 1 2 \sum_j \dot Q_j^2$ 
- Potential energy: $U=\frac 1 2 \sum \omega_j^2Q_j^2$ 

we can derivate the conclusion as follows:
- **Derivation1**: 
> $T=\frac{1}{2} \sum_{i} m_{i} \dot{u}_{i}^{2},\quad u(n a)=\frac {1} {\sqrt{m}}\sum_q Q(q)e^{-iq~na}\quad \Rightarrow\quad  T=\frac 1 2 \sum_j \dot Q_j^2$ 
> ![[Pasted image 20220405202629.png|500]]
> then 
> ![[Pasted image 20220405203658.png|500]]

- **derivation2**:
> $U=\frac{1}{2} \beta \sum_{n} (u_n-u_{n-1})^2, \quad u(n a)=\frac {1} {\sqrt{m}}\sum_q Q(q)e^{-iq~na}\quad \Rightarrow\quad$ 
> $U=\frac 1 2 \sum_j w_j^2\dot Q_j^2$
> ![[Pasted image 20220405210719.png|500]]
>ref: [[经典晶体振动#Solution|dispersion relation]]: $4\sin \frac{qa}2= \frac{m}{\beta}\omega^2$ 



# phonon(声子)
since canonical equation are
$$\ddot Q(q)+\omega_q^2Q(q)=0$$
then by quantitation (构建产生消灭算符), energy can be represented by :
$$\varepsilon_q=(n_q+\frac1 2)\hbar \omega_q$$ The quantum of energy ( $\hbar\omega_q$ ) is called a **phonon** in analogy with the photon of the electromagnetic wave. 
- Note phonon is not real particle!

- remarks
> The crystal vibrations can be described by a collection of various phonons. Two phonons do not interact within the harmonic theory(**harmonic approximation**). When the anharmonic terms are included, the phonons are interacting. ^f52abe


## properties of  phonon
- Phonon is Boson
	1. obey B-E distribution (ref: [[近独立子系#B-E 分布]])			
	2. number of phonons is not conserved 

- Quasi momentum(准动量) of phonon: $\hbar \vec q$ 

- Phonon is non-local particle 


## measurement of phonon
or say inelastic scattering
所谓 measurement 就是测定声子频率，即测定色散关系 (dispersion relation)。 格波波长与中子波长相近，与中子发生较明显的相互作用 
![[Pasted image 20220408214241.png|400]]
这里是准动量守恒(conservation of quasi-momentum)

加号为放出声子, 减号为吸收声子

