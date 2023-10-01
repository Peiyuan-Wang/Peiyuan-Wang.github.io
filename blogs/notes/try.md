---
layout: page
permalink: /blogs/notes/Lecture Note-Mean Field/index.html
title: Lecture Note-Mean Field
---

## Lecture Note-Mean Field



### Partons


We can decompose physical fermion into bosonic parton and fermionic parton.

$$
c_{i  l \sigma}= b_{i l }  f_{i l  \sigma}
$$

Bosonic parton carries the total charge symmetry and the inter-layer symmetry, fermionic parton carries the spin SU(2) symmetry.

### Bosonic parton mean field

By using mean field theory , we can get the Hamiltonian of bosonic parton witch resemble the bose hubbard model.

$$
H=-t_{b}\sum_{l=1}^{2} \sum_{\langle i, j\rangle}\left(b_{il}^{\dagger} b_{jl}+\text { h.c. }\right)-\sum_{l=1}^{2}\sum_{i} \mu_{i} n_{il}+J_{b} \sum_{i} n_{i1}n_{i2}
$$

Parameter l means different layers . $J_{b}=J\langle f_{1}^{\dagger}f_{2}f_{3}^{\dagger}f_{4} \rangle$ means the inter layer interaction parameter. $t_{b}=t\langle f_{i}f_{j} \rangle$ means the hopping parameter.


$$ 
H_{i}=\sum_{l=1}^{2} -2 z t_{b}\left(\psi\left(b_{il}^{\dagger}+b_{il}\right)-\psi^{2}\right)-\mu_{i} n_{il}+J_{b} n_{i1}n_{i2}
$$

So the Hamiltonian on each site can be written as follow

$$
H=J_{b} n_{1}n_{2} -\mu n_{1}-\mu n_{2}-t_{b} \psi\left(b_{1}^{\dagger}+b_{1}+b_{2}^{\dagger}+b_{2}\right)+2t_{b} \psi^{2}
$$

The expectation value of energy is

$$
E_{0}=\langle n_{1}n_{2}|H| n_{1}n_{2}\rangle=J_{b} n_{1}n_{2} -\mu n_{1}-\mu n_{2}
$$

We can find the ground state by minimizing the free energy

$$
\partial_{n_{1}} E_{0}=\partial_{n_{1}}\left(J_{b} n_{1}n_{2} -\mu n_{1}-\mu n_{2}\right)=0
$$
$$
\partial_{n_{2}} E_{0}=\partial_{n_{2}}\left(J_{b} n_{1}n_{2} -\mu n_{1}-\mu n_{2}\right)=0
$$

$$
n_{1}=n_{2}=[\frac{\mu}{J_{b}}]
$$

And $| n_{1}n_{2}\rangle$ is the ground state.



The free energy can be expanded in power series of $\psi$

$$
E(\psi) \equiv\langle\Psi|H| \Psi\rangle=E_{0}+E_{1} \psi+\frac{1}{2} E_{2} \psi^{2}+\frac{1}{6} E_{3} \psi^{3}+\frac{1}{24} E_{4} \psi^{4}+\ldots
$$

Because of the projective $\mathbb{Z}_{2}^{\mathcal{S}}$ action, we shuold have:

$$
E_{1}=E_{3}=\ldots=0
$$

So the second order coefficient can be calculated from

$$
E_{2}=\partial_{\psi}^{2} E=\sum_{m \neq n} \frac{\langle n|\partial H| m\rangle\langle m|\partial H| n\rangle+\langle n|\partial H| m\rangle\langle m|\partial H| n\rangle}{E_{n}-E_{m}}
$$

$$
E_{2}=-2t_{b}^2 \sum_{(m_{1},m_{2}) \neq (n_{1},n_{2})} \frac{\langle n_{1},n_{2}|\partial H| m_{1},m_{2}\rangle\langle m_{1},m_{2}|\partial H| n_{1},n_{2}\rangle}{E_{n_{1},n_{2}}-E_{m_{1},m_{2}}}
$$


where $\partial H=-t_{b}\left(b_{1}^{\dagger}+b_{1}+b_{2}^{\dagger}+b_{2}\right)
$. So, the result is:

$$
E_{2}=\frac{2\mu-J_{b}(n_{1}n_{2})}{(\mu - J_{b}n_{1})(\mu - J_{b}n_{2}) }
$$

$$
E=E_{0}+\frac{1}{2}\left(E_{2}+4 t_{b}\right) \psi^{2}
$$

so that we can obtain the energy as a faction of $\psi$ , $\mu$ , $J_{b}$ and $t_{b}$ (n should be replaced by the function of the ground state)


$$
E_{b}\left(t_{b}, \psi, J_{b}\right)
$$

$$
t_{b}=t\left\langle f_{i}^{\dagger} f_{j}\right\rangle, \quad J_{b}=J\langle\text { ffff }\rangle $$

Where $\langle\text { ffff }\rangle $ can be calculate by using Wick Theory
$$\langle f_{1}f_{2}f_{3}f_{4} \rangle = \langle f_{1}f_{2} \rangle \langle f_{3}f_{4} \rangle+\langle f_{1}f_{3} \rangle \langle f_{2}f_{4} \rangle+ \langle f_{1}f_{4} \rangle\langle f_{2}f_{3} \rangle$$






### Fermionic parton mean field

By using mean field theory , we can get the Hamiltonian of fermionic parton.

$$
H=-t_{f}\left(f_{i}^{\dagger} f_{j}+\text { h.c. }\right)+J\left(f_{i, 1 \downarrow}^{\dagger} f_{i, 2 \downarrow} f_{i, 2 \uparrow}^{\dagger} f_{i, 1 \uparrow}+h.c.\right)
$$

where $
t_{f}=t \psi^{2}
$,according to the mean field result of bosonic parton. 

We can use mean field again to the Hamiltonian of fermionic parton and obtain:

$$
H=-t \psi^{2}\sum_{l}^{4}\left(f_{li}^{\dagger} f_{lj}+h . c .\right)+\lambda(-)^{i}\left(f_{i, 2 \uparrow}^{\dagger} f_{i, 1 \uparrow}+f_{i, 1 \downarrow}^{\dagger} f_{i, 2 \downarrow} -f_{i, 1 \downarrow}^{\dagger}  f_{i, 1 \uparrow}- f_{i, 2 \uparrow}^{\dagger}f_{i, 2 \downarrow} +h.c.\right)
$$

where $\lambda$ is the mean field term

For the honeycomb lattice, we can write the Hamiltonian as follow


$$
H_{r}=-t \psi^{2}\sum_{l}^{4}\left(f_{l(r+\delta_{1})}^{\dagger} f_{lr}+f_{l(r+\delta_{2})}^{\dagger} f_{lr}+f_{l(r+\delta_{3})}^{\dagger} f_{lr}+f_{l(r-\delta_{1})}^{\dagger} f_{lr+\delta_{1}}+f_{l(r-\delta_{2})}^{\dagger} f_{lr+\delta_{1}}+f_{l(r-\delta_{3})}^{\dagger} f_{lr+\delta_{1}}\right)
$$
$$
+\lambda(
f_{r, 2 \uparrow}^{\dagger} f_{r, 1 \uparrow}+f_{r, 1 \downarrow}^{\dagger} f_{r, 2 \downarrow} -f_{r, 1 \downarrow}^{\dagger}  f_{r, 1 \uparrow}- f_{r, 2 \uparrow}^{\dagger}f_{r, 2 \downarrow} 
$$
$$
-f_{r+\delta_{1}, 2 \uparrow}^{\dagger} f_{r+\delta_{1}, 1 \uparrow}-f_{r+\delta_{1}, 1 \downarrow}^{\dagger} f_{r+\delta_{1}, 2 \downarrow} +f_{r+\delta_{1}, 1 \downarrow}^{\dagger}  f_{r+\delta_{1}, 1 \uparrow}+ f_{r+\delta_{1}, 2 \uparrow}^{\dagger}f_{r+\delta_{1}, 2 \downarrow}+h.c.)
$$


$$
\boldsymbol{\delta}_{1}=(0,-1) 
$$
$$
\boldsymbol{\delta}_{2}=\left(\frac{\sqrt{3}}{2}, \frac{1}{2}\right) $$
$$
\boldsymbol{\delta}_{3}=\left(-\frac{\sqrt{3}}{2}, \frac{1}{2}\right)
$$

r is the label of the unicellular which contain two atoms :A and B.

We can use fourier transformation and get the Hamiltonian in momentum space.

The creation and annihilation operator obey following equation

$$
c_{i} =\frac{1}{\sqrt{N}} \sum_{k} c_{k} e^{i k x}
$$
$$
c_{k} =\frac{1}{\sqrt{N}} \sum_{i} c_{i} e^{-i k x}
$$

$$
\frac{1}{N} \sum_{k} e^{i k j} e^{-i k j^{\prime}}=\delta_{j j^{\prime}} $$
$$
\frac{1}{N} \sum_{j} e^{i k j} e^{-i k^{\prime} j}=\delta_{k k^{\prime}}
$$

Then we can obtain the Hamiltonian as a 8 x 8 matrix and we can diagonalize it and calculate the ground state and the expectation value of energy.Energy is a function of $t_{f}$,$J$and$\lambda$ 

$$
E_{f}\left(t_{f}, J, \lambda\right)=E_{f}\left(t \psi^{2}, J, \lambda\right)
$$

### Conclusion

The total energy is equal to $E_{b}+E_{f}$, witch is a function of t,J, $\lambda$ and $\psi $ 

t and J are the parameter of the model. We can set them initially and find the value of  $\lambda$ and $\psi $ witch make the energy minimum. As we tuning the ratio of t and J,  $\lambda$ and $\psi $ will turn to be zero of not. There will be four situations and each one means a phenomenon.

$$
\begin{array}{cccccc}
\square & \psi=\langle b\rangle &\lambda & a & \left\langle c_{2}^{\dagger} c_{1}\right\rangle & U(1)_{\text {layer }} \\
t>>\mathrm{J} & O(1) & 0 & \text { Higgs } & 0 & \text { symm } \\
J>>\mathrm{t} & 0 & O(1) & \text { confine } & 0 & \text { symm } \\
? & 0 & 0 & \text { deconfine }(\mathrm{QED}) & 0 & \text { symm } \\
? & O(1) & O(1) & \text { Higgs } & O(1) & \text { broken }
\end{array}
$$

When the hopping term is dominant, we guess $\lambda$ will be zero and fermion will act like a free fermion. When the interaction term is dominant, we guess $\psi$  will be zero because the bosonic parton will condense on each site and transform into Mott state.

During the tuning, there must be two probably intermediate state.

If $\lambda$and $\psi $ are both zero, that means the gauge field is deconfined, this system emergent the QED.
If $\lambda$and $\psi $ are neither zero, that means the layer U(1) symmetry is broken.

### Questions

I find some questions and confusions when I was summing up the note.


- how can I transform the initial Hamiltonian into partons' Hamiltonian?

The Hamiltonian of SMG is 
$$
H=-t \sum_{\langle i j\rangle} \sum_{a=1}^{4}\left(c_{i a}^{\dagger} c_{j a}+\text { h.c. }\right)-V \sum_{i}\left(c_{i 1}^{\dagger} c_{i 2}^{\dagger} c_{i 3}^{\dagger} c_{i 4}^{\dagger}+\text { h.c. }\right)
$$

I find I still don't understand what do the four flavours(a) of fermion mean. How can I transform four annihilation operators   $c_{i 1}^{\dagger} c_{i 2}^{\dagger} c_{i 3}^{\dagger} c_{i 4}^{\dagger}$  into two annihilation operators and two creation operators  $c_{i 1}^{\dagger} c_{i 2} c_{i 3}^{\dagger} c_{i 4}$  , so that we can get the form of   $
J\left(f_{i, 1 \downarrow}^{\dagger} f_{i, 2 \downarrow} f_{i, 2 \uparrow}^{\dagger} f_{i, 1 \uparrow}+\ldots\right)
$ and $J_{b} \sum_{i} n_{1i}n_{2i}$ ?

- What does the flavour of parton mean?

I find how to transform c into partons in your paper
$$
c_{i a}=\sum_{b=1}^{4} B_{i a b} f_{i b}
$$

but I don't understand why bosonic parton has two kinds of flavours and fermionic parton has four different flavours with fermion.How can I correct the flavour form of the Hamiltonian I wrote?

- How can I prove what will happen in the intermediate state?

I can only retell the conclusion of the two different probably intermediate state. How can I explain it more rigorously? 
