# Distribution function 
According to the solution of [[Boltzmann transport equation#The relaxation time approximation 弛豫近似|relaxation approximation]], (detail form)
$$\frac 1 \hbar\left(\nabla_{k}E\cdot \nabla_rT\right)\frac{\partial f}{\partial T}-\frac e\hbar(\boldsymbol  \varepsilon +\boldsymbol  v \times \boldsymbol B)\cdot \nabla _k f=\frac{f_0-f}{\tau}$$
We can derivate the distribution function for **uniform temperature** under **external electric field**
- No temperature gradient 
- No magnet field

So the distribution function is represented by
$$f=f_{0}+\frac{e \tau}{\hbar} \boldsymbol{\varepsilon} \cdot \nabla_{k} f$$

Since we assume that the deviation is tiny, ensuring $f\sim f_0$, so we can write the equation in a explicit form:
$$f=f_{0}+\frac{e \tau}{\hbar} \boldsymbol{\varepsilon} \cdot \nabla_{k} f_0$$


# Derivation electric current density
By definition, the density of current:
$$\vec j=-e\int\vec v ~\mathrm d n$$
Where $\mathrm d n$ is the number of electrons, represented by
$$\mathrm d n=f \frac{2V}{(2\pi)^3}\mathrm d\vec k$$
(ref: [[Free electron theory#DOS|density of k of electrons]], coefficient $2$ comes from spin).

