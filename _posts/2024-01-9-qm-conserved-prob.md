---
title:  "Quantum Probability Current from Noether's Theorem"
mathjax: true
layout: post
excerpt_separator: <!--more-->
---

I recently saw part of a derivation of the probability continuity equation from
non-relativistic quantum mechanics by simply appealing to Noether's theorem with
a proper choice of Lagrangian. My curiosity was promptly piqued, and I present
below my work fleshing out this derivation.

<!--more-->

Before proceeding, I first note that I use natural units and the mostly minus
metric. Second, I caution that the following work does not serve as a
first-principles derivation and should not be thought of as such. Mainly, this 
work is mathematically interesting and not necessarily physically insightful.

## The Lagrangian

To construct the Lagrangian, we first observe that we can think of the
wavefunction as a complex scalar field that is a function of spacetime
coordinates \\(x^\mu\\). We then must demand that it reproduces the
time-dependent Schrödinger equation and it’s Hermitian conjugate. These
considerations lead us to write

\begin{align} 
    \mathcal{L} = \frac{i}{2}(\dot{\psi}^\dagger\psi - \psi^\dagger\dot{\psi}) + \frac{1}{2m}\nabla\psi^\dagger\nabla\psi - \psi^\dagger\psi V(x^\mu), 
\end{align}

where \\(V(x^\mu)\\) is a Hermitian function of the spacetime coordinates. By
staring at the Lagrangian we have written down, it is clear that it has a
\\(U(1)\\) symmetry. That is to say,
\\(\mathcal{L}\to\mathcal{L}^\prime=\mathcal{L}\\) for

<p>
\begin{align} 
    \psi &\to \psi^\prime = \psi e^{i\alpha}, \\
    \psi^\dagger &\to \psi^{\dagger\prime} = \psi^\dagger e^{-i\alpha},
\end{align}
</p>

where \\(e^{\pm i\alpha}\in U(1)\\). Given that this is a continuous symmetry, 
we can conclude from Noether's theorem that there exists an associated conserved 
current that can be derived from varying the action.

## Deriving the Conserved Current

We now want to consider a variation of the action by applying the symmetry
transformation both infinitesimally and as a function of the spacetime
coordinates. Let \\(e^{\pm i\varepsilon}\in U(1)\\) with
\\(\varepsilon=\varepsilon(x^\mu)\\) such that \\(\varepsilon \ll 1\\). We can
thus express the symmetry transformation as

\begin{align}
    \psi \to \psi^\prime = \psi e^{i\varepsilon} \approx \psi(1 + i\varepsilon),
\end{align}

where we have dropped terms of \\(\mathcal{O}(\varepsilon^2)\\) or higher, and
it is implied that we repeat the same procedure for \\(\psi^\dagger\\).
Computing \\(\delta S\\) up to leading order in the variation yields

\begin{align}
    \delta S = \int d^4x\, (-\dot\varepsilon\psi^\dagger\psi) + \frac{1}{2mi}(\nabla\varepsilon\cdot(\psi\nabla\psi^\dagger - \psi^\dagger\nabla\psi)).
\end{align}

Integrating by parts and demanding that \\(\varepsilon\\) vanishes at the
spacetime boundaries, we arrive at 

\begin{align}
    \delta S = \int d^4x\, \varepsilon\left(\frac{\partial}{\partial t}(\psi^\dagger\psi) - \frac{1}{2mi}\nabla\cdot(\psi\nabla\psi^\dagger - \psi^\dagger\nabla\psi)\right).
\end{align}

Requiring \\(\delta S = 0\\) as usual and noting that \\(\varepsilon\\) was an
arbitrary choice, we can pick off the expression 

\begin{align}
    \frac{\partial}{\partial t}(\psi^\dagger \psi) + \nabla\cdot\left[\frac{1}{2mi}(\psi^\dagger\nabla\psi - \psi\nabla\psi^\dagger)\right] = 0,
\end{align}

which is the recognizable probability conservation equation one finds in
non-relativistic quantum mechanics. 

## Final Comments

I must again emphasize that the above work is by no means a physically
meaningful derivation of the conserved probability current, but rather a
mathematically interesting one. Further, the achieved result is "quantum" only
by way of our Lagrangian being designed to reproduce the Schrödinger equation,
and thus having some relation to quantum mechanics.

It is in fact pertinent to mention that a more physically meaningful choice of
Lagrangian would be 

\begin{align}
    \mathcal{L} = i\psi^\dagger\dot{\psi} + \frac{1}{2m}\nabla\psi^\dagger\nabla\psi -\psi^\dagger\psi V(x^\mu).
\end{align}

By inspection, it is clear that this choice of Lagrangian both recovers the same
conserved current and reproduces both necessary Schrödinger equations for
\\(\psi\\) and \\(\psi^\dagger\\). However, it is also clear that simple demands
like the ones we made earlier to derive our original Lagrangian would not lead
us to the above expression. It turns out that the above Lagrangian can be
derived by taking the non-relativistic limit of a Klein-Gordon field[^1], which
is by itself far more physically motivating.

---

[^1]: In this case, the resulting field in the Lagrangian is known as a
    [Schrödinger field](https://en.wikipedia.org/wiki/Schr%C3%B6dinger_field){:target="_blank"}.
    To arrive at the result, one must assume that the fields are either
    classical or quantum. The former leads to a simpler derivation, while the
    latter is more complicated due to non-commutativity. More can be found
    [here](https://en.wikipedia.org/wiki/Klein%E2%80%93Gordon_equation#Non-relativistic_limit){:target="_blank"}.
