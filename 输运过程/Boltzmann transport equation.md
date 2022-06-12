Boltzmann transport equation bases on the density function in phase space $f(\boldsymbol  r,\boldsymbol  k,t)$ which is defined by 
$$\mathrm d N=f(\boldsymbol  r,\boldsymbol  k,t)\mathrm d\boldsymbol  r\mathrm d\boldsymbol  p$$
Where $\mathrm d N$ is the number of molecules which _all_ have position and momentum lying in $\mathrm d\boldsymbol  r\mathrm d\boldsymbol  p$ about $\boldsymbol  r,\boldsymbol  p$. 

**attention** since transport process is not steady, there are no specify distribution functions to describe it, though this is a system of Fermions (electron). When it becomes steady, the system obeys [[近独立子系#F-D 分布|F-D distribution]].




# Boltzmann transport equation (BTE)
 The BTE is represented by 
 $$\frac{\mathrm d f}{\mathrm d t}=\left.\frac{\partial f}{\partial t}\right|_\text{drift}+\left.\frac{\partial f}{\partial t}\right|_{\text {collision }}+\frac{\partial f}{\partial t}$$
Where
- **drift term** describes the drift of phase space because of external environment, which contents
	- $\boldsymbol  r$ -drift (**diffusion**): $\boldsymbol  r$ (distance of atom) changes because of temperature gradient 
	- $\boldsymbol  k$ -drift (**external force**): $\boldsymbol  k$ (momentum of lattice wave) changes because of external field \[$\hbar \boldsymbol  k =-e(\boldsymbol  \varepsilon+\boldsymbol  v\times \boldsymbol  B)$]
- **collision term** describes the interact between phonons. Some also call it scattering term, caused by defect, impurity etc.
- **time depend term**: actually $\boldsymbol  r,\boldsymbol  p$ includes time implicitly. So the time depend term appears when $f$ includes time explicitly.

Following, we will derivate the explicit form of the BTE.

## Drift term 
![[Pasted image 20220609103642.png]]
Then the drift term is defined by 
$$\left.\frac{\partial f}{\partial t}\right|_{\text{drift}}=\lim_{\mathrm d t \to 0}\frac{f(\boldsymbol  r,\boldsymbol  k ,t)-f(\boldsymbol  r-\boldsymbol  v \mathrm dt ,~\boldsymbol  k-\boldsymbol  v_k\mathrm d t,~t-\mathrm d t)}{\mathrm d t}$$
According to the expansion formula 
$$f(\boldsymbol  u-\boldsymbol  w\mathrm d t)=f(\boldsymbol  u)-\nabla_uf\cdot \boldsymbol  w\mathrm d t+o(w)$$
Then two vector variables is the composition of the one, so 
$$\begin{align}
\left.\frac{\partial f}{\partial t}\right|_{\text{drift}}&=-\boldsymbol  v\cdot\nabla_r f-\boldsymbol  v_k\cdot \nabla_kf\\
&-\boldsymbol  v\cdot\nabla_r f- \dot {\boldsymbol  k}\cdot \nabla_kf
\end{align}$$

## Collision term (simplified)
Usually we use a possibility function of transition to describe scattering/collision process. 

In a word, scattering is a process that change $\boldsymbol  k$ to $\boldsymbol  k'$, but not change position. So we define a possibility function representing the possibility **in per unit time** from $\boldsymbol  k$ to $\boldsymbol  k'$, denoted by $\Theta(\boldsymbol  k, \boldsymbol  k')$, or $\boldsymbol  k'$ to $\boldsymbol  k$ denoted by $\Theta(\boldsymbol  k',\boldsymbol  k)$.
![[Pasted image 20220609161400.png]]
Generally, the collision term is represented by
$$\left.\frac{\partial f}{\partial t}\right|_{\text{collision}}=b-a$$
Where 
- $b$ represents the number of electrons **entering** the phase volume $(\boldsymbol  r, \boldsymbol  k)$  because of collision
$$b=\sum_{\boldsymbol {k}^{\prime}} \Theta\left(\boldsymbol {k}^{\prime}, \boldsymbol {k}\right) f(\boldsymbol {k}^{\prime})[1-f(\boldsymbol {k})]$$

- $a$ represents the number of electrons **escaping** the phase volume $(\boldsymbol  r, \boldsymbol  k)$
$$a=\sum_{\boldsymbol {k}^{\prime}} \Theta\left(\boldsymbol {k}, \boldsymbol {k}^{\prime}\right) f(\boldsymbol {k})[1-f(\boldsymbol {k}^{\prime})]$$

So the explicit form of BTE is 
$$\begin{align}\frac{\mathrm d f}{\mathrm d t}=&-\boldsymbol  v\cdot\nabla_r f- \dot {\boldsymbol  k}\cdot \nabla_kf\\
&+\left\{\sum_{\boldsymbol {k}^{\prime}} \Theta\left(\boldsymbol {k}^{\prime}, \boldsymbol {k}\right) f(\boldsymbol {k}^{\prime})[1-f(\boldsymbol {k})]+ \Theta\left(\boldsymbol {k}, \boldsymbol {k}^{\prime}\right) f(\boldsymbol {k})[1-f(\boldsymbol {k}^{\prime})]\right\}\\
&+\frac{\partial f}{\partial t}
\end{align}$$


# Steady cases
For steady cases, the distribution function $f$ does not depends on $t$ explicitly and stays stable when the time goes:
$$\frac{\mathrm d f}{\mathrm d t}=\frac{\partial f}{\partial t}=0$$
Then BTE becomes:
$$\boldsymbol  v\cdot\nabla_r f+\dot {\boldsymbol  k}\cdot \nabla_kf=b-a$$
One can call equation above BTE either.

# The relaxation time approximation (弛豫近似)
The relaxation time is the average time needed to recover the equilibrium state when the effects of external field or temperature gradient are removed suddenly.

we always assume that the relaxation time is small enough for us to describe differentiation by difference(差分)

> **approximation** relaxation time approximation
> Consider collision only (since the external field and temperature gradient is withdrew, no drift effect remains):
> $$\left.\frac{\partial f}{\partial t}\right|_{\text{collision}}=b-a=\frac{f_0-f}{\tau}$$
> Where $\tau$ is relaxation time, $f_0$ is [[近独立子系#F-D 分布|Fermi distribution function]] for its describing the steady state of electrons.
> 

**attention**:
- $f$ : unsteady state at the moment field or gradient are withdrew (initial state)
- $f_0$ : steady state at the final moment (final state)

So the term is represented in 
$$\text{final - initial}=\frac{f_0-f}{\tau}$$

## Derivation 
The sudden absence of external field or temperature gradient cases the deviation of distribution function $f-f_0$, which means it takes $\tau$ to re-stabilize from a steady state $f_0$ to another steady state $f$ after the environment changed.

And if we consider collision only, by the BTE
$$\begin{align}\frac{\mathrm d f}{\mathrm d t}&=\frac{f_0-f}{\tau}
\\&=b-a=\frac{\partial f}{\partial t}\end{align}$$
Also, by the equation ${\mathrm d f}/{\mathrm d t}={-(f-f_0)}/{\tau}$, solute the equation and gain
$$f=f_0+Ce^{-t/\tau}$$
When $t=0$, $f=f_i$ , the steady function with external field and temperature gradient, so 
$$f=f_0+(f_i-f_0)e^{-t/\tau}$$

## Detail form 
Since $\boldsymbol  v\cdot\nabla_r f+\dot {\boldsymbol  k}\cdot \nabla_kf=b-a$,

### LHS
**The first term**: $\boldsymbol  r$ -shift caused by temperature gradient
- $\boldsymbol  v=\frac 1 \hbar\nabla_{k}E$ (ref: [[Crystal dynamics#^b6e6dc|average velocity of electron]])
- $\nabla_r f=\nabla_rT\frac{\partial f}{\partial T}$
then the first term becomes
$$\frac 1 \hbar\left(\nabla_{k}E\cdot \nabla_rT\right)\frac{\partial f}{\partial T}$$

**The second term**: $\boldsymbol  k$-shift caused by external field
- force of external field $\boldsymbol  F=-e(\boldsymbol  \varepsilon +\boldsymbol  v \times B)$
- momentum: $\hbar \dot{\boldsymbol  k}=\boldsymbol  F$
then the second term becomes
$$-\frac e\hbar(\boldsymbol  \varepsilon +\boldsymbol  v \times B)\cdot \nabla _k f$$

### RHS
according to the relaxation time approximation above 
$$RHS=\frac{f_0-f}{\tau}$$

-----
so the detail form is 
$$\frac 1 \hbar\left(\nabla_{k}E\cdot \nabla_rT\right)\frac{\partial f}{\partial T}-\frac e\hbar(\boldsymbol  \varepsilon +\boldsymbol  v \times \boldsymbol B)\cdot \nabla _k f=\frac{f_0-f}{\tau}$$

