---
title:  "Quantum Probability Current from Noether's Theorem"
mathjax: true
layout: post
excerpt_separator: <!--more-->
---

I recently saw part of a clever derivation of the probability continuity equation in non-relativistic quantum mechanics by simply appealing to Noether’s theorem. I have since completed the argument and wish to share it here.

<!--more-->

For this derivation, we make use of natural units. Further, this is by no means a first-principles derivation, but rather an interesting path one may take to find a fundamental physical result.

## The Lagrangian

To construct the Lagrangian, we first observe that we can think of the wavefunction as a complex scalar field that is a function of spacetime coordinates \\(x^mu\\). We then must demand that it reproduces the time-dependent Schrödinger equation and it’s Hermitian conjugate. These considerations lead us to

\begin{equation} \mathcal{L} = \frac{i}{2}(\dot{\psi}^\dagger\psi - \psi^\dagger\dot{\psi}) + \frac{1}{2m}\nabla\psi^\dagger\nabla\psi - \psi^\dagger\psi V(x^\mu), \end{equation}

where \\(V(x^\mu)\\) is a Hermitian function of the spacetime coordinates.

## Symmetry of the System

By staring at the Lagrangian we have written down, it is clear that it has a \(U(1)\) symmetry, that is to say

\begin{equation} \psi \to \psi^\prime = e^{i\alpha}\psi \text{ }(\psi^\dagger \to \psi^{\dagger\prime} = e^{-i\alpha}\psi^\dagger) \implies \mathcal{L} \to \mathcal{L}^\prime = \mathcal{L}, \end{equation}

Thus, we can vary the action by 
