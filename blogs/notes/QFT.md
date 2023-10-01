---
layout: page
permalink: /blogs/notes/QFT/index.html
title: QFT
<head>
<script type="text/x-mathjax-config">
    MathJax.Hub.Config({
      extensions: ["tex2jax.js"],
      jax: ["input/TeX", "output/HTML-CSS"],
      tex2jax: {
        <!--$表示行内元素，$$表示块状元素 -->
        inlineMath: [ ['$','$'], ["\\(","\\)"] ],
        displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
        processEscapes: true
      },
      "HTML-CSS": { availableFonts: ["TeX"] }
    });
</script>
<script type="text/javascript" async src="https://cdn.mathjax.org/mathjax/latest/MathJax.js">
</script>
<head>
---

## QFT


### Introduction

#### Why QFT?

field is used to construct laws of Nature that are local.

- [ans1]QM and SR inmplies that particle number is not conserved.
    
    $\Delta E>2m c^2$ means we can pop out particle anti-particle pairs.
    compton wavelength always smaller than de Broglie wavelength.
    
    the de Broglie wavelength is the distance at which the wavelike nature of particles becomes apparent; the Compton wavelength is the distance at which the concept of a single pointlike particle breaks down completely.
    
    Negative probabilities, infinite towers of negative energy states, or a breakdown in causality are problems when we construct a relativitic version of the one-particle Schrodinger equation.
    
    
- [ans2]All particles of the same type are indistinguishable.
    
    the particle field means the stuff of one type particle and we take one from the stuff to create the particle, so that the same type particles are indistinguishable.
    
    "same" in the quantum world means swapping two particles will not change the state --apart from a possible minus sign. The minus sign determines the statistics of the particle.
    
    




#### What is QFT?
QFT is the quantization of a classical field.

freedom are operator valued functions of space and time which means infinite degrees.

principle: locality, symmetry and renormalization group flow(the
decoupling of short distance phenomena from physics at larger scales)






### Classical Field Theory

#### The Dynamics of Fields


- A field is a quantity defined at every point of space and time.


$$
\phi_{a}(\vec{x}, t)
$$

a and x are considered as labels.



- Example : Electromagnetic field

we can derive E and B from a 4 component field$A^{\mu}(\vec{x},t)=(\phi,\vec{A})$ 

$$
\vec{E}=-\nabla \phi-\frac{\partial \vec{A}}{\partial t} \quad \text { and } \quad \vec{B}=\nabla \times \vec{A}
$$

- the Lagrangian

$$
L(t)=\int d^{3} x \mathcal{L}\left(\phi_{a}, \partial_{\mu} \phi_{a}\right)
$$

$$
S=\int_{t_{1}}^{t_{2}} d t \int d^{3} x \mathcal{L}=\int d^{4} x \mathcal{L}
$$

$$
\begin{aligned}
\delta S &=\int d^{4} x\left[\frac{\partial \mathcal{L}}{\partial \phi_{a}} \delta \phi_{a}+\frac{\partial \mathcal{L}}{\partial\left(\partial_{\mu} \phi_{a}\right)} \delta\left(\partial_{\mu} \phi_{a}\right)\right] \\
&=\int d^{4} x\left[\frac{\partial \mathcal{L}}{\partial \phi_{a}}-\partial_{\mu}\left(\frac{\partial \mathcal{L}}{\partial\left(\partial_{\mu} \phi_{a}\right)}\right)\right] \delta \phi_{a}+\partial_{\mu}\left(\frac{\partial \mathcal{L}}{\partial\left(\partial_{\mu} \phi_{a}\right)} \delta \phi_{a}\right)
\end{aligned}
$$

$$
\partial_{\mu}\left(\frac{\partial \mathcal{L}}{\partial\left(\partial_{\mu} \phi_{a}\right)}\right)-\frac{\partial \mathcal{L}}{\partial \phi_{a}}=0
$$

- Example: The Klein-Gorgon Equation

$$
\begin{aligned}
\mathcal{L} &=\frac{1}{2} \eta^{\mu \nu} \partial_{\mu} \phi \partial_{\nu} \phi-\frac{1}{2} m^{2} \phi^{2} \\
&=\frac{1}{2} \dot{\phi}^{2}-\frac{1}{2}(\nabla \phi)^{2}-\frac{1}{2} m^{2} \phi^{2}
\end{aligned}
$$

$$
T=\int d^{3} x \frac{1}{2} \dot{\phi}^{2}
$$

$$
V=\int d^{3} x \frac{1}{2}(\nabla \phi)^{2}+\frac{1}{2} m^{2} \phi^{2}
$$

the first term is called the gradient energy, the last term is called the potential energy.

So the Euler-Lagrange equation is then

$$
\ddot{\phi}-\nabla^{2} \phi+m^{2} \phi=0
$$

or 

$$
\partial_{\mu} \partial^{\mu} \phi+m^{2} \phi=0
$$

which is the Klein-Gordon Equantion. 

- Example: First order Lagrangians

$$
\mathcal{L}=\frac{i}{2}\left(\psi^{\star} \dot{\psi}-\dot{\psi}^{\star} \psi\right)-\nabla \psi^{\star} \cdot \nabla \psi-m \psi^{\star} \psi
$$

$$
\frac{\partial \mathcal{L}}{\partial \psi^{\star}}=\frac{i}{2} \dot{\psi}-m \psi \quad \text { and } \quad \frac{\partial \mathcal{L}}{\partial \dot{\psi}^{\star}}=-\frac{i}{2} \psi \quad \text { and } \quad \frac{\partial \mathcal{L}}{\partial \nabla \psi^{\star}}=-\nabla \psi
$$

$$
i \frac{\partial \psi}{\partial t}=-\nabla^{2} \psi+m \psi
$$

it looks like the Schrödinger equation.

The initial data required on a Cauchy surface differs for the two examples above.When L $ \sim  \dot{\phi}^2$,$\phi$  and $ \dot{\phi}$ must be specified to determine the future evolution.When L $\sim   \psi^* \psi $ ,only $\psi$ and $\psi^*$ are needed.

\item Example:Maxwell's Equations

we can derive Maxwell's equations in the vacuum from the Lagrangian.

$$
\mathcal{L}=-\frac{1}{2}\left(\partial_{\mu} A_{\nu}\right)\left(\partial^{\mu} A^{\nu}\right)+\frac{1}{2}\left(\partial_{\mu} A^{\mu}\right)^{2}
$$

$$
\frac{\partial \mathcal{L}}{\partial\left(\partial_{\mu} A_{\nu}\right)}=-\partial^{\mu} A^{\nu}+\left(\partial_{\rho} A^{\rho}\right) \eta^{\mu \nu}
$$

$$
\partial_{\mu}\left(\frac{\partial \mathcal{L}}{\partial\left(\partial_{\mu} A_{\nu}\right)}\right)=-\partial^{2} A^{\nu}+\partial^{\nu}\left(\partial_{\rho} A^{\rho}\right)=-\partial_{\mu}\left(\partial^{\mu} A^{\nu}-\partial^{\nu} A^{\mu}\right) \equiv-\partial_{\mu} F^{\mu \nu}=0
$$

we can obtain the rest Maxwell's equation($\nabla \cdot \vec{E}=0$ and $\partial \vec{E} / \partial t=\nabla \times \vec{B}$) from $\vec{E}=-\nabla \phi-\frac{\partial \vec{A}}{\partial t} \quad$ and $\quad \vec{B}=\nabla \times \vec{A}$. 

we can also rewrite the Lagrangian as follow

$$
\mathcal{L}=-\frac{1}{4} F_{\mu \nu} F^{\mu \nu}
$$


- Locality

The examples above are local which means there are no terms couping $\phi (\vec{x},t)$ directly to $\phi (\vec{y},t)$ such as $L=\int d^{3} x d^{3} y \phi(\vec{x}) \phi(\vec{y})$.

A priori, there is no reason for this. $\vec{x}$ is merely a label, and we always couple labels together such as $\partial_{3} A_{0} \partial_{0} A_{3}$.  

But the closest we get for the
$\vec{x}$ label is a coupling between $\phi (\vec{x})$ and $\phi(\vec{c}+\delta \vec{x})$ through the gradient term ($\nabla \phi$)$^2$

This property of locality is, as far as we know, a key feature of all theories of Nature.
Indeed, one of the main reasons for introducing field theories in classical physics is to
implement locality. In this course, we will only consider local Lagrangians.



#### Lorentz Invariance

One of the main motivation to develop QFT is to reconcile QM and SR. So we want to construct field theory in which space and time are equal and the theory is Lorentz covariant.

$$
x^{\mu} \longrightarrow\left(x^{\prime}\right)^{\mu}=\Lambda_{~~ \nu}^{\mu} x^{\nu}
$$

where $\Lambda^{\mu}_{~~\nu}$ satisfies

$$
\Lambda_{~~ \sigma}^{\mu} \eta^{\sigma \tau} \Lambda_{~~ \tau}^{\nu}=\eta^{\mu \nu}
$$

The Lorentz transformations form a Lie group under matrix
multiplication.

the scalar field under the Lorentz transformation $x \rightarrow \Lambda x$ ,transform as $\phi(x) \rightarrow \phi^{\prime}(x)=\phi\left(\Lambda^{-1} x\right)$




- Example:The Klein-Gordon Equation
    
    transform the derivative as a vector meaning
    
    $$\left(\partial_{\mu} \phi\right)(x) \rightarrow\left(\Lambda^{-1}\right)_{\mu}^{\nu}\left(\partial_{\nu} \phi\right)(y)$$
    
    $y=\Lambda ^{-1}x$.So the Lagrangian density transform as 

$$
\begin{aligned}
\mathcal{L}_{\text {deriv }}(x)=\partial_{\mu} \phi(x) \partial_{\nu} \phi(x) \eta^{\mu \nu} & \longrightarrow\left(\Lambda^{-1}\right)_{\mu}^{\rho}\left(\partial_{\rho} \phi\right)(y)\left(\Lambda^{-1}\right)^{\sigma}{ }_{\nu}\left(\partial_{\sigma} \phi\right)(y) \eta^{\mu \nu} \\
&=\left(\partial_{\rho} \phi\right)(y)\left(\partial_{\sigma} \phi\right)(y) \eta^{\rho \sigma} \\
&=\mathcal{L}_{\text {deriv }}(y)
\end{aligned}
$$
    
    we find that the action is indeed invariant under Lorentz transformations.
    
$$
S=\int d^{4} x \mathcal{L}(x) \longrightarrow \int d^{4} x \mathcal{L}(y)=\int d^{4} y \mathcal{L}(y)=S
$$

(det $\lambda=1$ )

- Example:First Order Dynamics
    
    first-order Lagrangian is not Lorentz invariant.
    
    To see if the action is Lorentz invariant: the Lorentz indices are contracted with Lorentz invariant objects. Such as 
    $\eta_{\mu \nu}  \epsilon_{\mu \nu \rho \sigma} \gamma_{\mu}$    
    
- Example:Maxwell's Equations
    
    $$ A^{\mu}(x) \rightarrow \Lambda_{\nu}^{\mu} A^{\nu}\left(\Lambda^{-1} x\right)$$ 
    it is invariant. 
    
    

#### Symmetries

There are Lorentz symmetries, internal symmetries, gauge symmetries,
supersymmetries $\cdots$

we start by recasting Noether's theorem.



- Noether's Theorem
    
    every continuous symmetry of the Lagrangian gives rise to a conserved current $j^{\mu}(x)$ such that the equation of motion imply 
    
    $$\partial_{\mu}j^{\mu}=0$$
    
    Comment: A conserved current implies a conserved charge Q,defined as $Q=\int_{\mathbf{R}^{3}}d^3x j^0$
    
    obviously, we have $$\frac{d Q}{d t}=\int_{\mathbf{R}^{3}} d^{3} x \frac{\partial j^{0}}{\partial t}=-\int_{\mathbf{R}^{3}} d^{3} x \nabla \cdot \vec{j}=0$$

    assuming $\vec{j}\rightarrow0 $ as $|\vec{x}|\rightarrow\infty$
    
    
- Proof NT
    
    a transformation is a symmetry if the Lagrangian changes by a total derivative,
    
    $$
    \delta \phi_{a}(x)=X_{a}(\phi)$$
    
    $$
    \delta \mathcal{L}=\partial_{\mu} F^{\mu}
    $$
    $$
    \begin{aligned}
    \delta \mathcal{L} &=\frac{\partial \mathcal{L}}{\partial \phi_{a}} \delta \phi_{a}+\frac{\partial \mathcal{L}}{\partial\left(\partial_{\mu} \phi_{a}\right)} \partial_{\mu}\left(\delta \phi_{a}\right) \\
    &=\left[\frac{\partial \mathcal{L}}{\partial \phi_{a}}-\partial_{\mu} \frac{\partial \mathcal{L}}{\partial\left(\partial_{\mu} \phi_{a}\right)}\right] \delta \phi_{a}+\partial_{\mu}\left(\frac{\partial \mathcal{L}}{\partial\left(\partial_{\mu} \phi_{a}\right)} \delta \phi_{a}\right)
    \end{aligned}
    $$

    and the equations of motion are satisfied , so
    
    $$
    \delta \mathcal{L}=\partial_{\mu}\left(\frac{\partial \mathcal{L}}{\partial\left(\partial_{\mu} \phi_{a}\right)} \delta \phi_{a}\right)
    $$
    
    therefore we can define current
    
    $$
    j^{\mu}=\frac{\partial \mathcal{L}}{\partial\left(\partial_{\mu} \phi_{a}\right)} X_{a}(\phi)-F^{\mu}(\phi)
    $$

- Example: Translations and the Energy-Momentum Tensor
    
    $$
    x^{\nu} \rightarrow x^{\nu}-\epsilon^{\nu} \quad \Rightarrow \quad \phi_{a}(x) \rightarrow \phi_{a}(x)+\epsilon^{\nu} \partial_{\nu} \phi_{a}(x)
    $$
    
    $$
    \left(j^{\mu}\right)_{\nu}=\frac{\partial \mathcal{L}}{\partial\left(\partial_{\mu} \phi_{a}\right)} \partial_{\nu} \phi_{a}-\delta_{\nu}^{\mu} \mathcal{L} \equiv T_{\nu}^{\mu}
    $$

    so we get the energy-momentum tensor.
    
    $$
    E=\int d^{3} x T^{00} \quad \text { and } \quad P^{i}=\int d^{3} x T^{0 i}
    $$

    for Lagrangian
    
    $$
    \begin{aligned}
    \mathcal{L} &=\frac{1}{2} \eta^{\mu \nu} \partial_{\mu} \phi \partial_{\nu} \phi-\frac{1}{2} m^{2} \phi^{2} \\
    &=\frac{1}{2} \dot{\phi}^{2}-\frac{1}{2}(\nabla \phi)^{2}-\frac{1}{2} m^{2} \phi^{2}
    \end{aligned}
    $$
    
    we can get
    
    $$
    T^{\mu \nu}=\partial^{\mu} \phi \partial^{\nu} \phi-\eta^{\mu \nu} \mathcal{L}
    $$
    
    $$
    \begin{aligned}
    E &=\int d^{3} x \frac{1}{2} \dot{\phi}^{2}+\frac{1}{2}(\nabla \phi)^{2}+\frac{1}{2} m^{2} \phi^{2} \\
    P^{i} &=\int d^{3} x \dot{\phi} \partial^{i} \phi
    \end{aligned}
    $$
    
    we can always massage the energy-momentum tensor into symmetric form by adding
    
    $$
    \Theta^{\mu \nu}=T^{\mu \nu}+\partial_{\rho} \Gamma^{\rho \mu \nu}
    $$
    
    and $\Gamma^{\rho \mu \nu}=-\Gamma^{\mu \rho \nu}$.so that $\partial_{\mu} \partial_{\rho} \Gamma^{\rho \mu \nu}=0$.
    
- Example: Lorentz Transformations and Angular Momentum
    
    Lorentz transformation
    
    $$
    \Lambda_{\nu}^{\mu}=\delta_{\nu}^{\mu}+\omega_{\nu}^{\mu}
    $$
    
    $$
    \begin{aligned}
    &\left(\delta_{\sigma}^{\mu}+\omega_{\sigma}^{\mu}\right)\left(\delta_{\tau}^{\nu}+\omega_{\tau}^{\nu}\right) \eta^{\sigma \tau}=\eta^{\mu \nu} \\
    \Rightarrow \quad & \omega^{\mu \nu}+\omega^{\nu \mu}=0
    \end{aligned}
    $$

    $$
    \begin{aligned}
    \phi(x) \rightarrow \phi^{\prime}(x) &=\phi\left(\Lambda^{-1} x\right) \\
    &=\phi\left(x^{\mu}-\omega_{\nu}^{\mu} x^{\nu}\right) \\
    &=\phi\left(x^{\mu}\right)-\omega_{\nu}^{\mu} x^{\nu} \partial_{\mu} \phi(x)
    \end{aligned}
    $$

    $$
    \delta \mathcal{L}=-\omega^{\mu}{ }_{\nu} x^{\nu} \partial_{\mu} \mathcal{L}=-\partial_{\mu}\left(\omega^{\mu}{ }_{\nu} x^{\nu} \mathcal{L}\right)
    $$

    notes that $\mu \neq \nu$
    
    $$
    \begin{aligned}
    j^{\mu} &=-\frac{\partial \mathcal{L}}{\partial\left(\partial_{\mu} \phi\right)} \omega^{\rho}{ }_{\nu} x^{\nu} \partial_{\rho} \phi+\omega_{\nu}^{\mu} x^{\nu} \mathcal{L} \\
    &=-\omega_{\nu}^{\rho}\left[\frac{\partial \mathcal{L}}{\partial\left(\partial_{\mu} \phi\right)} x^{\nu} \partial_{\rho} \phi-\delta_{\rho}^{\mu} x^{\nu} \mathcal{L}\right]=-\omega_{\nu}^{\rho} T_{\rho}^{\mu} x^{\nu}
    \end{aligned}
    $$

    we can have 6 currents determinded by $\omega^{\mu}_{}_{\nu}$. 
    
    $$
    \left(\mathcal{J}^{\mu}\right)^{\rho \sigma}=x^{\rho} T^{\mu \sigma}-x^{\sigma} T^{\mu \rho}
    $$

    $\rho \sigma = 1,2,3$ means rotation and reflect 3 conserved charge which is the angular momentum.
    
    but to boost,
    
    $$
    Q^{0 i}=\int d^{3} x\left(x^{0} T^{0 i}-x^{i} T^{00}\right)
    $$

    $$
    \begin{aligned}
    0=\frac{d Q^{0 i}}{d t} &=\int d^{3} x T^{0 i}+t \int d^{3} x \frac{\partial T^{0 i}}{\partial t}-\frac{d}{d t} \int d^{3} x x^{i} T^{00} \\
    &=P^{i}+t \frac{d P^{i}}{d t}-\frac{d}{d t} \int d^{3} x x^{i} T^{00}
    \end{aligned}
    $$

    $$
    \frac{d}{d t} \int d^{3} x x^{i} T^{00}=\mathrm{constant}
    $$

    this means the center of energy of the field travels with a constant
velocity.
    

- Internal Symmetries
    
    The above two examples involved transformations of spacetime, as well as transformations
of the field.An internal symmetry is one that only involves a transformation of
the fields and acts the same at every point in spacetime.
    
    <!-- 前面记录太详细了，后面改变风格 -->
    
    $$
    \mathcal{L}=\partial_{\mu} \psi^{\star} \partial^{\mu} \psi-V\left(|\psi|^{2}\right)
    $$
    
    $$
    \psi(x)=\left(\phi_{1}(x)+i \phi_{2}(x)\right) / \sqrt{2}
    $$

    the equation of motion
    
    $$
    \partial_{\mu} \partial^{\mu} \psi+\frac{\partial V\left(\psi^{\star} \psi\right)}{\partial \psi^{\star}}=0
    $$
    
    symmetry is rotating $\phi_{1}$ and $\phi_{2}$,it is equal to retate the phase of $\psi$:
    
    $$
    \psi \rightarrow e^{i \alpha} \psi \quad \text { or } \quad \delta \psi=i \alpha \psi
    $$
    because of $\delta \mathcal{L}=0 $
    the current is 
    $$
    j^{\mu}=i\left(\partial^{\mu} \psi^{\star}\right) \psi-i \psi^{\star}\left(\partial^{\mu} \psi\right)
    $$

    the conserved charges have the interpretation of electric charge or particle number.
    
- Non-Abelian Internal Symmetries
    
     invariant under the non-Abelian symmetry group:SO(N),O(N),SU(N). Global symmetry which is different from  “local gauge” symmetries.
     
-
    
     a quick method to determine the conserved current associated to an internal symmetry $\delta \phi = \alpha \phi$

#### Free Fields

---

### Interacting Fields

---

### The Dirac Equation

---

### Quantizing the Dirac Field

---

### Quantum Electrodynamics



