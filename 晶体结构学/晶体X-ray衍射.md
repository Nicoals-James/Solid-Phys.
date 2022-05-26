# Premise
- Parallel light 
- No Compton effect
- Simplest lattice
- No vibration

# Diffraction Derivation
## Diffraction maximum condition
 ![[Pasted image 20220311155446.png|400]]
 - Derivation:
 ![[Pasted image 20220311155930.png|400]]
 - Condition：
$$\vec{R_l}\cdot (\vec{S}-\vec{S_0})=\mu \lambda,\quad \mu= 1,2,\dots$$
Where $\lambda$ is the wavelength of the incident light.
>**Definition:** Laue equation (劳厄公式)$$\vec{R_l}\cdot (\vec{k}-\vec{k_0})=2\pi\mu,\quad \mu= 1,2,\dots$$ 

Do some substitutions, and gain **Laue Equation** from eq. Above:
$$2\pi\cdot\vec{R_l}\cdot (\vec{S}-\vec{S_0})=\mu \lambda \cdot 2\pi$$
Because wave vector of light satisfies $\vec{k}=\frac{2\pi}{\lambda}\vec{S}$ , then
$$\vec{R_l}\cdot (\vec{k}-\vec{k_0})=2\pi\mu$$
Because [[倒易点阵（Reciprocal lattice）#Relationship of Reciprocal Space|Relationship of Reciprocal Space]]: 
$$\vec{K_h}\cdot\vec{R_l}\cdot (\vec{k}-\vec{k_0})=2\pi\mu\cdot \vec{K_h} \quad \Rightarrow \quad \vec{k}-\vec{k}_{0}=n \vec{K}_{h}$$ ^cb582b


>**Definition:** Bragg law $$2 d_{h_{1} h_{2} h_{3}} \sin \theta=n \lambda$$ where $h_1,h_2,h_3$ is the index of crystal plane.
>Except for derivation in optics, Bragg law can be derivated directly in [[Pasted image 20220313225620.png|here]]

^d302b2



## Scattering factor
Essentially, X-ray diffraction comes from electron scattering. 

>**Definition**: Atomic scattering factor $f$  $$f=\frac{\text { the sum of scattering amplitude from all the electrons within the atom }}{\text { the scattering amplitude from a single electron }}$$ where scattering amplitude is defined in [[Scattering Theory|quantum mechanics]]
>Written in detailed form $$f=\int \mathrm{e}^{\mathrm{i}\left(k-k_{0}\right) \cdot r} \rho(\boldsymbol{r}) \mathrm{d} \tau$$ 

### Derivation
In quantum mechanics,  there is a certain density distribution $\rho(r)$ of electron cloud [[Atom Physics]]. The process of scattering don't modify the module $|A|$ of the amplitude but the **phase**.
认为中心处与电子云处散射能力相同。
![[Pasted image 20220313234056.png]]
- $\vec{k}-\vec{k_0}$ can be replaced by $n\vec{K_h}$ [[#^cb582b]] by choosing a proper coordinate. 
- The factor is related to incident angle and the distribution of electron.
- The [[Pasted image 20220313234432.png|example]] of calculating spherical distribution

## Structure factor 
We always talk about unit cell, so the structure factor represents the characteristic of crystal.
[[Pasted image 20220314093542.png|supplement]], 即结构因子表征晶胞结构，为晶胞内所有原子散射幅度总和（散射幅可以用上面的 scattering factor 求）。
>**Definition**:  Structure factor $F$ 
> $$F=\frac{\text { the sum of scattering amplitude from all the atoms within the unit cell }}{\text { the scattering amplitude from a single electron }}$$ written in detailed form: $$F(\boldsymbol{K})=\sum_{j} f_{j} \mathrm{e}^{\mathrm{i} \mathbf{K} \cdot \boldsymbol{r}_{j}}$$ where $f_i$  is the scattering factor, $r_i$ is the position vector towards the atoms and $\boldsymbol K=\boldsymbol k_1-\boldsymbol k_0=m \vec K_h$. 

It's clear to derivate the detailed form, so derivation is omitted here.

### Calculating total intensity of diffraction
For **the whole** crystal:
- amplitude of each unit cell $F_P$ (structure factor)
- wave vector difference $\vec{k}-\vec{k_0}=\overrightarrow{K_{h'k'l'}}=m\overrightarrow{K_{hkl}}$ 
- position vector of each unit cell $\overrightarrow{R_P}=n\overrightarrow{R_l}$

the total amplitude:$$A(\boldsymbol{k}) \propto \sum_{P=1}^{N} F_{P} \cdot \mathrm{e}^{i \mathbf{K}_{h^{\prime} k^{\prime} l^{\prime}} \cdot \boldsymbol{R}_{P}}$$
for the intensity of light can be written as $I(\boldsymbol{k})\propto\left |A(\boldsymbol{k})\right |^2$   
$$I(\boldsymbol{k})=I_{h^{\prime} k^{\prime} t^{\prime}} \propto F\left(\boldsymbol{K}_{h^{\prime} k^{\prime} l^{\prime}}\right) F^{*}\left(\boldsymbol{K}_{h^{\prime} k^{\prime} l^{\prime}}\right)$$
> **Characteristic**: the total intensity only depends on the structure factor $F(\boldsymbol{k})$ of the crystal, which can be calculated after given the position of atoms in a unit cell.

the formula can be written in scattering factor $f_i$ (structure factor), 
$$\begin{align}
I_{h^{\prime} k^{\prime} l^{\prime}} =I_{m h, m k, m l}
\propto(\operatorname{Re} F)^{2}+(\operatorname{Im} F)^{2}\\
=\left[\sum_{j} f_{j} \cos 2\pi\left(m h u_{j}+m k v_{j}+m l w_{j}\right)\right]^{2} \\
\quad+\left[\sum_{j} f_{j} \sin2\pi \left(m h u_{j}+m k v_{j}+m l w_{j}\right)\right]^{2}
\end{align}$$
where using:
- $\boldsymbol K=\boldsymbol k_1-\boldsymbol k_0=m \vec K_h$
- $\boldsymbol r_j=u_j\boldsymbol a+v_j\boldsymbol b+w_j\boldsymbol c$  is the position vector towards atoms.


