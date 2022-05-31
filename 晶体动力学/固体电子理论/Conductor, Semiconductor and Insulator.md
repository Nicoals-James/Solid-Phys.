# Conductor and insulator
We just discuss **one-dimension** case
## No external field
$\varepsilon=0$  then then [[Nearly free electron model#conclusion|energy band]] $E(k)=E(-k)$, so there are the same number of electrons at state $k$ and $-k$, according to [[Fermi gas|Fermi distribution]]. 

Then [[Crystal dynamics#^b6e6dc|the velocity of each electron]] is 
$$v=\frac 1 \hbar \frac{\mathrm d E}{\mathrm d k}$$
Then $v(k)=-v(-k)$, so in the state $k$ and state $-k$ the movement of electrons is offset by each other. This explains why there is no current running in a crystal when there is no external field. By the way, the intensity of current is 
$$j=\sum_k-ev(k)=0$$

## In external field
### Empty
Clearly, if the energy band is empty, it is impossible to generate current. 

### Fully occupied (insulator)
![[Pasted image 20220515231128.png|300]] ![[Pasted image 20220515231215.png|300]] 

Full band means that every state $k$ is occupied by 2 **valence electron** (2 types of spin). 

By the [[Crystal dynamics#^733cfd|equation of motion]] we gain 
$$\frac{d p}{d t}=-e \varepsilon=\hbar \frac{\mathrm d k }{\mathrm  d t}$$
So $k$ is moving along the axis, of course it's periodic. Since all $k$ is occupied, number of electrons on $\pm k$ is always the same but their velocity goes opposite. So the intensity of current remains 0
$$j=\sum_k-ev(k)=0$$

![[Pasted image 20220515232736.png]]
(how the band flows)

### Partially occupied (conductor)
![[Pasted image 20220515232408.png|300]] ![[Pasted image 20220515232438.png|300]]
The energy band is not fully occupied, so when the external field starts to work, the symmetry of the distribution breaks.
$$j=\sum_k-ev(k)\neq 0$$
![[Pasted image 20220515232950.png]]
### Conclusion 
Generally, in one dimension case, there are $N$ $k$ s in the first BZ (ref: [[Free electron theory#State in vec k space|DOS]]) where $N$ is the number of primitive cells, so each energy band can hold $2N$ valence electrons.

![[Pasted image 20220516104950.png]]
- If band1 is full, band2 is empty then the crystal is **insulator**
- Only there is at least one band being not fully occupied then the crystal is **conductor**
- If a crystal is an insulator but it's energy gap of some band is small enough ($<2$ eV), then it's **semi-conductor** (it's can conduct via mixing other element).
# Examples
Mostly, the relation between the capacity of  electrons and energy bands is quite complicate. But in some case we can explain or do some supplement and explain. 

## Alkali metals
For _Li_ crystal:
- Structure: [[典型晶体结构#Body-Centered Cubic BCC|BCC]], there are 1 atoms in a primitive cell
- valence electron: $ns^1$

So if there $N$ primitive cells then $N$ _Li_ atoms then $N$ valence electrons.
- Capacity of electrons: $2N$

Capacity is larger then the number of valence electrons, so _Li_ is conductor.

## Alkaline earth metals (第二主族元素)
With the same analysis
- Structure: [[典型晶体结构#Hexagonal Close Cacking Ctructure 密堆积结构|hexagonal close-packed (hcp)]], there are 2 atoms in primitive cell 
- valence electron: $ns^2$ 

For $N$ primitive cells there are $4N$ valence electrons but $2N$ capacity of electron. **ERROR**

> **modification** the capacity of electrons
> Define capacity of electrons as the electrons number every energy band can hold.
> $$\text{capacity of electrons}=2N(2l+1)m$$
> Where $N$ is the number of primitive cells, $l$ is the azimuthal quantum number, $m$ is the **number of atoms** in a primitive cell

In new definition, capacity of electrons becomes $4N$ which equals the number of valence electrons. It's insulator? ERROR again. In fact crystal of Mg is 3-dimensional, so the energy band will be different at different direction.
![[Pasted image 20220516112135.png]]
According to the fig, Mg is conductor

## Elements in column IV
![[Pasted image 20220516112333.png]]
