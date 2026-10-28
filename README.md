
# — Angular Momentum Coupling

**Study notes and companion program:** `angular_momentum.py`

## 1\. Why Couple Angular Momenta?

Nuclei, like atoms and molecules, are built from constituents that each carry orbital angular momentum and spin. The total angular momentum of the system is assembled from these contributions.

The mathematical framework for combining angular momenta is the subject of this chapter:

- **Clebsch–Gordan (CG) coefficients** and **3j symbols** for coupling two angular momenta.
- **6j symbols** for recoupling three angular momenta.
- **9j symbols** for recoupling four angular momenta.

These tools are essential for describing angular momentum in quantum mechanics and nuclear physics.

## 2\. Definition of an Angular Momentum Operator

A vector operator

$$
\mathbf{J}=(J_x,J_y,J_z)
$$

is an angular momentum operator if its components are Hermitian and satisfy the angular momentum commutation relations:

$$
J_k^\dagger=J_k,
\qquad
[J_i,J_j]=i\hbar\,\epsilon_{ijk}J_k.
$$

### 2.1 Eigenstates and Eigenvalues

The simultaneous eigenstates of $\mathbf{J}^2$ and $J_z$, denoted by $\lvert jm\rangle$, satisfy

$$
\mathbf{J}^2\lvert jm\rangle
=j(j+1)\hbar^2\lvert jm\rangle,
$$

$$
J_z\lvert jm\rangle
=m\hbar\lvert jm\rangle,
$$

where

$$
m=-j,-j+1,\ldots,j-1,j.
$$

### 2.2 Ladder Operators

The ladder operators are defined as

$$
J_\pm=J_x\pm iJ_y.
$$

They obey the commutation relations

$$
[J_+,J_-]=2\hbar J_z,
$$

$$
[J_\pm,J_z]=\mp\hbar J_\pm.
$$

Their action on angular momentum eigenstates is

$$
J_\pm\lvert jm\rangle
=
\hbar\sqrt{(j\mp m)(j\pm m+1)}
\lvert j,m\pm1\rangle.
$$

Starting from the stretched state $\lvert j,j\rangle$, repeated application of $J_-$ generates the entire angular momentum multiplet.

## 3\. Coupling Two Angular Momenta

Let $\mathbf{J}_1$ and $\mathbf{J}_2$ be two independent angular momentum operators whose components commute with one another. Define the total angular momentum as

$$
\mathbf{J}=\mathbf{J}_1+\mathbf{J}_2.
$$

Two complete bases can be used to describe the system.

| Basis | Commuting observables | Basis states |
| --- | --- | --- |
| Uncoupled | $J_1^2,J_{1z},J_2^2,J_{2z}$ | $\lvert j_1m_1j_2m_2\rangle=\lvert j_1m_1\rangle\lvert j_2m_2\rangle$ |
| Coupled | $J_1^2,J_2^2,J^2,J_z$ | $\lvert j_1j_2;jm\rangle$ |

In the coupled basis, the individual angular momentum magnitudes $j_1$ and $j_2$ remain well-defined, while the total angular momentum $j$ and its projection $m$ are specified. The individual projections $m_1$ and $m_2$ are generally not definite.

### 3.1 Clebsch–Gordan Coefficients

The two bases are related by a unitary transformation whose matrix elements are the **Clebsch–Gordan coefficients**:

$$
\boxed{
\begin{aligned}
\lvert j_1j_2;jm\rangle
={}&\sum_{m_1,m_2}
\langle j_1m_1,j_2m_2\mid jm\rangle\\
&\qquad\times
\lvert j_1m_1j_2m_2\rangle.
\end{aligned}
}
$$

Here, $\langle j_1m_1,j_2m_2\mid jm\rangle$ denotes a Clebsch–Gordan coefficient.

### 3.2 Selection Rules

A Clebsch–Gordan coefficient can be nonzero only when the following conditions are satisfied.

1. **Projection conservation:**
   $$
   m_1+m_2=m.
   $$
2. **Triangle condition:**
   $$
   |j_1-j_2|\leq j\leq j_1+j_2.
   $$
3. **Allowed total angular momenta:**
   $$
   j=|j_1-j_2|,\ |j_1-j_2|+1,\ldots,j_1+j_2.
   $$
   The values of $j_1+j_2+j$ must be integers.

### 3.3 Phase Convention: Condon–Shortley

We use the Condon–Shortley phase convention. In particular,

$$
\langle j_1j_1,j_2j_2\mid j_1+j_2,j_1+j_2\rangle=+1.
$$

The convention also fixes the signs of the remaining coefficients, including the standard nonnegative convention for the coefficients

$$
\langle j_1m_1,j_2,-j_2\mid jm\rangle
$$

when the corresponding coefficient is nonzero and the stated convention applies.

### 3.4 Key Properties of Clebsch–Gordan Coefficients

**Orthogonality**

$$
\begin{aligned}
&\sum_{m_1,m_2}
\langle j_1m_1,j_2m_2\mid jm\rangle\\
&\quad\times
\langle j_1m_1,j_2m_2\mid j'm'\rangle
=\delta_{jj'}\delta_{mm'}.
\end{aligned}
$$

**Completeness**

$$
\begin{aligned}
&\sum_{j,m}
\langle j_1m_1,j_2m_2\mid jm\rangle\\
&\quad\times
\langle j_1m_1',j_2m_2'\mid jm\rangle
=\delta_{m_1m_1'}\delta_{m_2m_2'}.
\end{aligned}
$$

**Exchange of angular momenta**

$$
\begin{aligned}
&\langle j_2m_2,j_1m_1\mid jm\rangle\\
&\qquad=(-1)^{j_1+j_2-j}
\langle j_1m_1,j_2m_2\mid jm\rangle.
\end{aligned}
$$

**Reversal of projections**

$$
\begin{aligned}
&\langle j_1,-m_1,j_2,-m_2\mid j,-m\rangle\\
&\qquad=(-1)^{j_1+j_2-j}
\langle j_1m_1,j_2m_2\mid jm\rangle.
\end{aligned}
$$

**Zero-projection condition**

$$
\langle j_1\,0,j_2\,0\mid j\,0\rangle=0
$$

unless $j_1+j_2+j$ is even.

**Coupling to angular momentum zero**

$$
\langle jm,00\mid jm\rangle=1.
$$

For two identical angular momentum magnitudes coupled to zero,

$$
\boxed{
\langle jm,jm'\mid 00\rangle
=
\frac{(-1)^{j-m}}{\hat j}\delta_{m,-m'},
}
$$

where

$$
\hat j\equiv\sqrt{2j+1}.
$$

**Recoupling identities**

$$
\begin{aligned}
\langle j_1m_1,j_2m_2\mid jm\rangle
={}&(-1)^{j_2+m_2}\frac{\hat j}{\hat j_1}\\
&\times\langle j_2,-m_2,jm\mid j_1m_1\rangle,
\end{aligned}
$$

and

$$
\begin{aligned}
\langle j_1m_1,j_2m_2\mid jm\rangle
={}&(-1)^{j_1-m_1}\frac{\hat j}{\hat j_2}\\
&\times\langle jm,j_1,-m_1\mid j_2m_2\rangle.
\end{aligned}
$$

## 4\. Wigner 3j Symbols

The Wigner 3j symbol is a symmetric reformulation of a Clebsch–Gordan coefficient:

$$
\boxed{
\begin{pmatrix}
j_1&j_2&j_3\\
m_1&m_2&m_3
\end{pmatrix}
=
\frac{(-1)^{j_1-j_2-m_3}}{\hat j_3}
\langle j_1m_1,j_2m_2\mid j_3,-m_3\rangle.
}
$$

The inverse relation is

$$
\begin{aligned}
\langle j_1m_1,j_2m_2\mid j_3m_3\rangle
={}&(-1)^{j_1-j_2+m_3}\hat j_3\\
&\times
\begin{pmatrix}
j_1&j_2&j_3\\
m_1&m_2&-m_3
\end{pmatrix}.
\end{aligned}
$$

### 4.1 Properties of 3j Symbols

A 3j symbol vanishes unless both the triangle condition

$$
\Delta(j_1j_2j_3)
$$

and the projection condition

$$
m_1+m_2+m_3=0
$$

are satisfied.

Here, $\Delta(j_1j_2j_3)$ denotes the triangle condition: the three angular momenta must be able to couple to form a valid angular momentum.

**Permutation and sign symmetries**

- Even permutations of the columns leave the symbol unchanged.
- Odd permutations of the columns multiply it by $(-1)^{j_1+j_2+j_3}$.
- Reversing all magnetic quantum numbers also multiplies it by $(-1)^{j_1+j_2+j_3}$.

**Special case with****$j_3=0$**

$$
\begin{pmatrix}
j_1&j_2&0\\
m_1&m_2&0
\end{pmatrix}
=
\frac{(-1)^{j_1-m_1}}{\hat j_1}
\delta_{j_1j_2}\delta_{m_1,-m_2}.
$$

**All-zero projections**

$$
\begin{pmatrix}
j_1&j_2&j_3\\
0&0&0
\end{pmatrix}=0
$$

unless $j_1+j_2+j_3$ is even.

**Sum rule**

$$
\sum_{m_1,m_2,m_3}
\begin{pmatrix}
j_1&j_2&j_3\\
m_1&m_2&m_3
\end{pmatrix}^{\!2}
=
\Delta(j_1j_2j_3).
$$

### 4.2 Useful Closed-Form Expressions

Closed-form expressions exist for several frequently occurring combinations, including

$$
\left(j+\frac12,\ j,\ \frac12\right),
\qquad
(j+1,\ j,\ 1),
\qquad
(j,\ j,\ 1),
\qquad
(j,\ j,\ 2).
$$

For example,

$$
\boxed{
\begin{pmatrix}
j&j&1\\
m&-m&0
\end{pmatrix}
=
(-1)^{j-m}
\frac{m}{\sqrt{j(j+1)(2j+1)}}.
}
$$

These expressions are reproduced numerically in the program's test suite.

## 5\. Three Angular Momenta: The Wigner 6j Symbol

Consider three angular momenta,

$$
\mathbf J=\mathbf J_1+\mathbf J_2+\mathbf J_3.
$$

There are three possible pairwise coupling orders:

- Couple $\mathbf J_1$ and $\mathbf J_2$ first, defining $\mathbf J_{12}$.
- Couple $\mathbf J_2$ and $\mathbf J_3$ first, defining $\mathbf J_{23}$.
- Couple $\mathbf J_1$ and $\mathbf J_3$ first, defining $\mathbf J_{13}$.

Although these coupling schemes describe the same total angular momentum, their intermediate-coupling states differ.

The overlap between two coupling schemes defines the Wigner 6j symbol. For example,

$$
\begin{aligned}
&\lvert j_1,j_2j_3(j_{23});jm\rangle\\
&=\sum_{j_{12}}
(-1)^{j_1+j_2+j_3+j}
\hat j_{12}\hat j_{23}
\begin{Bmatrix}
j_1&j_2&j_{12}\\
j_3&j&j_{23}
\end{Bmatrix}\\
&\qquad\times
\lvert j_1j_2(j_{12})j_3;jm\rangle.
\end{aligned}
$$

The 6j symbol contains no magnetic quantum numbers because the two bases already have the same total angular momentum $j$ and projection $m$.

A 6j symbol can also be expressed as a sum over products of four 3j symbols.

### 5.1 Properties of 6j Symbols

**Triangle conditions**

A 6j symbol vanishes unless all four required triangle conditions are satisfied:

$$
\Delta(j_1j_2j_3),\quad
\Delta(l_1l_2j_3),\quad
\Delta(l_1j_2l_3),\quad
\Delta(j_1l_2l_3).
$$

**Tetrahedral symmetries**

The 6j symbol is invariant under column permutations and under interchanging the upper and lower entries in any two columns. These transformations generate 24 tetrahedral symmetries.

**Relation to the Racah****$W$****coefficient**

$$
\begin{aligned}
&W(j_1j_2l_2l_1;j_3l_3)\\
&\quad=(-1)^{j_1+j_2+l_1+l_2}
\begin{Bmatrix}
j_1&j_2&j_3\\
l_1&l_2&l_3
\end{Bmatrix}.
\end{aligned}
$$

**Special case with one zero entry**

$$
\boxed{
\begin{Bmatrix}
j_1&j_2&j_3\\
0&j_3&j_2
\end{Bmatrix}
=
\frac{(-1)^{j_1+j_2+j_3}}{\hat j_2\hat j_3}.
}
$$

**Unitarity relation**

$$
\begin{aligned}
&\sum_j\hat j^2
\begin{Bmatrix}
j_1&j_2&j\\
j_3&j_4&j'
\end{Bmatrix}
\begin{Bmatrix}
j_1&j_2&j\\
j_3&j_4&j''
\end{Bmatrix}\\
&\qquad=\frac{\delta_{j'j''}}{\hat j'^2}.
\end{aligned}
$$

**Additional sum rule**

$$
\begin{aligned}
&\sum_j(-1)^{j_1+j_2+j}\hat j^2
\begin{Bmatrix}
j_1&j_1&j\\
j_2&j_2&j'
\end{Bmatrix}\\
&\qquad=\hat j_1\hat j_2\delta_{j'0}.
\end{aligned}
$$

**Closed form with a 1 in the lower row**

$$
\begin{aligned}
\begin{Bmatrix}
j_1&j_2&j_3\\
1&j_3&j_2
\end{Bmatrix}
={}&(-1)^s\\
&\times
\frac{j_1(j_1+1)-j_2(j_2+1)-j_3(j_3+1)}
{\sqrt{
4j_2(j_2+1)(2j_2+1)
j_3(j_3+1)(2j_3+1)
}},
\end{aligned}
$$

where

$$
s=j_1+j_2+j_3.
$$

Additional closed-form expressions involving $\tfrac12$ or $1$ in the lower row are included in the chapter's reference material and program tests.

## 6\. Four Angular Momenta: The Wigner 9j Symbol

For four angular momenta, two natural coupling schemes are

$$
(12)(34)
\qquad\text{and}\qquad
(13)(24).
$$

The overlap between these schemes is expressed using the Wigner 9j symbol:

$$
\begin{aligned}
&\lvert j_1j_3(j_{13})j_2j_4(j_{24});jm\rangle\\
&=\sum_{j_{12},j_{34}}
\hat j_{12}\hat j_{34}\hat j_{13}\hat j_{24}\\
&\quad\times
\begin{Bmatrix}
j_1&j_2&j_{12}\\
j_3&j_4&j_{34}\\
j_{13}&j_{24}&j
\end{Bmatrix}\\
&\quad\times
\lvert j_1j_2(j_{12})j_3j_4(j_{34});jm\rangle.
\end{aligned}
$$

The rows and columns encode the angular momentum couplings. The final row and column specify how the intermediate angular momenta combine to produce the total angular momentum $j$.

### 6.1 Properties of 9j Symbols

**Triangle conditions**

A 9j symbol vanishes unless every row and every column satisfies the triangle condition. There are six such conditions.

**Permutation symmetries**

- Transposing the 9j array leaves the symbol unchanged.
- An odd permutation of rows or columns multiplies it by $(-1)^\Sigma$, where $\Sigma$ is the sum of all nine angular momentum entries.

**Reduction to a 6j symbol**

When the bottom-right entry is zero,

$$
\begin{aligned}
&\begin{Bmatrix}
j_1&j_2&j_{12}\\
j_3&j_4&j_{34}\\
j_{13}&j_{24}&0
\end{Bmatrix}\\
&=\delta_{j_{12}j_{34}}\delta_{j_{13}j_{24}}
\frac{(-1)^{j_{12}+j_{13}+j_2+j_3}}
{\hat j_{12}\hat j_{13}}\\
&\quad\times
\begin{Bmatrix}
j_1&j_2&j_{12}\\
j_4&j_3&j_{13}
\end{Bmatrix}.
\end{aligned}
$$

**General evaluation**

A 9j symbol can be evaluated as a sum involving a product of three 6j symbols. This is the method used by the companion program.

**Orthogonality**

$$
\begin{aligned}
&\sum_{j_{13},j_{24}}
\hat j_{13}^{\,2}\hat j_{24}^{\,2}
\begin{Bmatrix}
j_1&j_2&j_{12}\\
j_3&j_4&j_{34}\\
j_{13}&j_{24}&j
\end{Bmatrix}\\
&\quad\times
\begin{Bmatrix}
j_1&j_2&j_{12}'\\
j_3&j_4&j_{34}'\\
j_{13}&j_{24}&j
\end{Bmatrix}\\
&=\delta_{j_{12}j_{12}'}
\delta_{j_{34}j_{34}'}
\hat j_{12}^{-2}\hat j_{34}^{-2}.
\end{aligned}
$$

### 6.2 Physical Application: The $LS\leftrightarrow jj$ Transformation

The transformation between the $LS$-coupling and $jj$-coupling schemes for two nucleons is expressed using a 9j symbol with the array

$$
\boxed{
\begin{Bmatrix}
l_1&s_1&j_1\\
l_2&s_2&j_2\\
L&S&J
\end{Bmatrix}.
}
$$

Here:

- $l_1,l_2$ are the individual orbital angular momenta.
- $s_1,s_2$ are the individual spins.
- $j_1,j_2$ are the individual total angular momenta in the $jj$-coupling scheme.
- $L$ is the total orbital angular momentum.
- $S$ is the total spin.
- $J$ is the total angular momentum of the two-nucleon system.

The 9j symbol provides the recoupling coefficient connecting these two descriptions.

## 7\. Exercises Covered by the Program

The companion program, `angular_momentum.py`, implements calculations and tests related to the exercises listed below.

| Exercise | Program functionality |
| --- | --- |
| 1.2 / 1.21 | `allowed_couplings()` lists the allowed $J^\pi$ values for two-particle configurations. |
| 1.3, 1.4 | `j_matrices(1)` constructs $J^2,J_\pm,J_z,J_x,J_y$; `rigid_rotor()` diagonalizes $H=\sum_k J_k^2/(2I_k)$. |
| 1.7 | `cg()` reproduces the Clebsch–Gordan table for $j_1=1$ and $j_2=\tfrac12$. |
| 1.8, 1.9, 1.14 | `run_tests()` checks orthogonality and completeness relations. |
| 1.16 | `six_j()` evaluates the two requested 6j symbols. |
| 1.22 | `nine_j()` evaluates the 9j symbol used in the $LS$-to-$jj$ transformation. |

## 8\. Summary

Angular momentum coupling provides a systematic way to combine individual angular momenta into a total angular momentum.

The central tools are:

- **Clebsch–Gordan coefficients:** transform between uncoupled and coupled bases for two angular momenta.
- **3j symbols:** express the same coupling information in a more symmetric form.
- **6j symbols:** transform between different coupling orders for three angular momenta.
- **9j symbols:** transform between different coupling schemes for four angular momenta.

