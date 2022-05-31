- Importance of Fermi surface
The electronic transport and thermal properties of metal are closely related with the shape of Fermi surface, since these properties depend on the change in occupation of electron states near the Fermi surface.

# Construction of Fermi surface
## Free electron system 
Electrons are free then the energy of them should only content kinetic energy, so the fermi energy can be represented by fermi momentum
$$E_F=\frac{\hbar ^2\vec k_F^2}{2m}$$
Which is a sphere.

### Exp: square lattice
Calculate relation of $k_F$ and the number of primitive cells $N$. Then the relation of $N$ and $E_F$

Let the constant of lattice be $a$, then the side length of the reciprocal lattice is $\frac{2\pi}{a}$ (ref: [[倒易点阵（Reciprocal lattice）|reciprocal lattice]]) then the area of  [[Brillouin Zone|BZ]] is $\Omega^*=4\pi^2/a^2$. If there  are $N$ primitive cells in a BZ (there are $N$ $k$ values), and the number of occupied state is $2N$ (spin). (一个 $k$ 有占有 0，占有 1 两个态)
(ref: [[经典晶体振动#Density of q 波矢密度|dos]])

So the density of $k$
$$Z(\vec k)=2\frac N {\Omega^*}=\frac {Na^2}{2\pi^2}$$
If there are $\eta$ valence electrons, then 
$$\eta N=\int_0^{k_F}Z(\vec k)\mathrm d \vec k=\pi k_F^2\frac {2N}{\Omega^*}$$
So we obtain the relation 
$$k_F^2=\frac{2\pi\eta}{a^2}, \quad\quad k_F=\frac{\sqrt{2\pi\eta}}{a}$$
Then the fermi energy 
$$E_F=\frac{\hbar ^2 k_F^2}{2m}=\frac{\hbar^2 \pi \eta}{ma^2}$$

In the extended zone, draw the Fermi circle with radius of $k_F$, the states inside the circle are all occupied while the outside states are unoccupied.

If we represent $k_F$ in  the unit of $\frac \pi a$, then the half width of the reciprocal lattice is 1.
- when $\eta=1$, $k_F=0.798$
- when $\eta=2,3$, $k_F=1,128,1,273$
- when $\eta=4$, $k_F=1.596$

![[Pasted image 20220531101426.png|400]]

parallel translation to the 1st BZ($\eta=4$):
![[Pasted image 20220531101639.png]]


## Nearly free electron system
there are perturbation by weak periodic field 
(ref: [[Nearly free electron model]])
in this approximation, there are several properties(difference from free model):
- **Far from** the zone boundary, the constant energy surface is approximately spherical.
far from the boundary: ![[Nearly free electron model#^591150]]
since $|V_m|$ is small, $E$-surface is nearly a sphere. however near the boundary, $E$ depends on the deviation $\Delta$ (ellipsoid)![[Nearly free electron model#^d4fc28]]

- At the zone boundary, the constant energy surface is **perpendicular** to the boundary:
take one-dimensional lattice as an example: at the zone boundary, the energy is constant $E_+,E_-$ then $\partial E/\partial k=0$. then the surface will be protruded ("passivation")
![[Pasted image 20220531111132.png|400]]


# Experimental methods in Fermi surface studies
## De Hass-Van Alphen effect