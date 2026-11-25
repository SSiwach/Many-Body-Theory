
#  Angular Momentum Coupling

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
J_\pm\lvert jm\rangle =
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

   $$ m_1+m_2=m. $$
3. **Triangle condition:**
   $$
   |j_1-j_2|\leq j\leq j_1+j_2.
   $$
4. **Allowed total angular momenta:**
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
\boxed{\langle jm,jm'\mid 00\rangle
=\frac{(-1)^{j-m}}{\hat j}\delta_{m,-m'},}
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

$$ \boxed{
\begin{pmatrix}
j_1&j_2&j_3\\
m_1&m_2&m_3
\end{pmatrix}
= \frac{(-1)^{j_1-j_2-m_3}}{\hat j_3}
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

## 2. Rotations and Wigner D functions
A rotation of the coordinate axes (Euler angles $\alpha,\beta,\gamma$) acts on
vector components through an orthogonal matrix, $V'=RV$, and on second-rank
Cartesian tensors by a similarity transformation $T'=RTR^{-1}$.

The same rotation induces a unitary operator $U(R)$ on the $(2j+1)$-dimensional
space of states $|jm\rangle$. Its matrix elements are the Wigner D functions,

$$D^{j}_{m'm}(\alpha,\beta,\gamma)=\langle jm'|U(R)|jm\rangle,\qquad
U(R)|jm\rangle=\sum_{m'}D^{j}_{m'm}(R)|jm'\rangle .$$

Special cases: $D^{l}_{m0}\propto Y^*_{lm}$ and $D^{l}_{00}=P_l(\cos\beta)$.

## 3. Spherical tensor operators
A set of $2L+1$ operators $T_{LM}$, $M=-L,\dots,L$, is a **spherical tensor of
rank $L$** if it rotates like the states $|LM\rangle$:

$$U(R)\,T_{LM}\,U^\dagger(R)=\sum_{M'}T_{LM'}D^{L}_{M'M}(R).$$

Equivalently (and much more practical for checking):

$$[J_z,T_{LM}]=M\,T_{LM},\qquad
[J_\pm,T_{LM}]=\sqrt{(L\pm M+1)(L\mp M)}\;T_{L,M\pm1}.$$

Names: $L=0$ scalar/monopole, $L=1$ vector/dipole, $L=2$ quadrupole,
$L=3$ octupole.

### Spherical components of a vector
The (covariant) components used throughout the book are

$$V_{\pm1}=\mp\tfrac{1}{\sqrt2}(V_x\pm iV_y),\qquad V_0=V_z ,$$

with contravariant partners $V^{\mu}=(-1)^{\mu}V_{-\mu}$. For the position
vector, $r_\mu=\sqrt{4\pi/3}\,r\,Y_{1\mu}(\theta,\varphi)$ — so $Y_1$ behaves as a
vector, and in general $Y_\lambda$ is a spherical tensor of rank $\lambda$.

Rank-1 spherical tensors you meet constantly: $J_\mu$, $r_\mu$, $\sigma_\mu$, $Y_{1\mu}$.

Dot and cross products in spherical form:

$$\mathbf A\cdot\mathbf B=\sum_\mu(-1)^\mu A_\mu B_{-\mu},\qquad
[\mathbf A\times\mathbf B]_\mu=-i\sqrt2\sum_{\nu\nu'}(1\nu1\nu'|1\mu)A_\nu B_{\nu'} .$$

A Cartesian rank-2 tensor is *reducible*: trace → scalar, antisymmetric part →
vector, symmetric traceless part → quadrupole. Spherical tensors are irreducible.

## 4. The Wigner–Eckart theorem
For a rank-$L$ tensor between states of good angular momentum,

$$\langle\xi'j'm'|T_{LM}|\xi jm\rangle
=\hat j'^{\,-1}(jmLM|j'm')\,(\xi'j'\|T_L\|\xi j)
=(-1)^{j'-m'}\begin{pmatrix}j'&L&j\\-m'&M&m\end{pmatrix}(\xi'j'\|T_L\|\xi j).$$

(Racah / Edmonds convention for the reduced matrix element $(\;\|\;\|\;)$.)

Consequences:
* **Selection rules**: non-zero only if $\Delta(jLj')$ and $m+M=m'$ —
  angular momentum conservation built in.
* **One matrix element fixes all**: knowing it for one $(m_0,M_0,m_0')$ gives
  every other by a ratio of CG coefficients.
* **Hermitian tensors** $(T_{LM})^\dagger=(-1)^M T_{L,-M}$ satisfy
  $(\xi j\|T_L\|\xi'j')=(-1)^{j-j'}(\xi'j'\|T_L\|\xi j)^*$.

### Basic reduced matrix elements ($\hbar=1$)
| operator | reduced matrix element |
|---|---|
| identity | $(j'\|1\|j)=\delta_{jj'}\hat j$ |
| $\mathbf J$ | $(j'\|J\|j)=\delta_{jj'}\sqrt{j(j+1)(2j+1)}$ |
| $Y_L$ | $(l'\|Y_L\|l)=(-1)^{l'}\dfrac{\hat l'\hat L\hat l}{\sqrt{4\pi}}\begin{pmatrix}l'&L&l\\0&0&0\end{pmatrix}$ |
| spin $\tfrac12$ | $(\tfrac12\|S\|\tfrac12)=\sqrt{3/2}$, $(\tfrac12\|\sigma\|\tfrac12)=\sqrt6$ |

## 5. Pauli matrices
$\mathbf S=\tfrac12\boldsymbol\sigma$ with

$$\sigma_x=\begin{pmatrix}0&1\\1&0\end{pmatrix},\;
\sigma_y=\begin{pmatrix}0&-i\\i&0\end{pmatrix},\;
\sigma_z=\begin{pmatrix}1&0\\0&-1\end{pmatrix}.$$

$[\sigma_i,\sigma_j]=2i\epsilon_{ijk}\sigma_k$, $\{\sigma_i,\sigma_j\}=2\delta_{ij}$,
$(\boldsymbol\sigma\cdot\mathbf A)(\boldsymbol\sigma\cdot\mathbf B)=\mathbf A\cdot\mathbf B+i\boldsymbol\sigma\cdot(\mathbf A\times\mathbf B)$, etc.

In spherical components:

$$[\sigma_\mu,\sigma_\nu]=-2\sqrt2\,(1\mu1\nu|1M)\sigma_M,\qquad
\{\sigma_\mu,\sigma_\nu\}=2(-1)^\mu\delta_{\mu,-\nu},\qquad
\sigma_\mu\sigma_\nu=(-1)^\mu\delta_{\mu,-\nu}-2\sqrt2(1\mu1\nu|1M)\sigma_M .$$

## 6. Coupled tensor operators
Tensor product: $[T_{L_1}S_{L_2}]_{LM}=\sum(L_1M_1L_2M_2|LM)T_{L_1M_1}S_{L_2M_2}$.
Scalar product: $T_L\cdot S_L=(-1)^L\hat L[T_LS_L]_{00}=\sum_M(-1)^MT_{LM}S_{L,-M}$.
Cross product: $(\mathbf T\times\mathbf S)_M=-i\sqrt2[T_1S_1]_{1M}$.

### Theorem I — operators in different spaces (9j)
If $T_{L_1}$ acts on space 1 and $S_{L_2}$ on space 2,

$$(j_1j_2j\|[T_{L_1}S_{L_2}]_L\|j_1'j_2'j')=\hat j\hat L\hat j'
\begin{Bmatrix}j_1&j_2&j\\j_1'&j_2'&j'\\L_1&L_2&L\end{Bmatrix}
(j_1\|T_{L_1}\|j_1')(j_2\|S_{L_2}\|j_2').$$

Scalar-product special case:

$$(j_1j_2j\|T_L\cdot S_L\|j_1'j_2'j')=\delta_{jj'}(-1)^{j_2+j+j_1'}\hat j
\begin{Bmatrix}j_1&j_2&j\\j_2'&j_1'&L\end{Bmatrix}(j_1\|T_L\|j_1')(j_2\|S_L\|j_2').$$

Applied to one nucleon in $|l\tfrac12 j\rangle$ (radial part factored out):

$$(l\tfrac12j\|\sigma\|l'\tfrac12j')=\sqrt6\,\delta_{ll'}\hat j\hat j'(-1)^{l+j+3/2}
\begin{Bmatrix}\tfrac12&\tfrac12&1\\j&j'&l\end{Bmatrix}$$

$$(l\tfrac12j\|Y_\lambda\|l'\tfrac12j')=\frac{1}{\sqrt{4\pi}}(-1)^{j'-\frac12+\lambda}
\frac{1+(-1)^{l+l'+\lambda}}{2}\hat j\hat j'\hat\lambda
\begin{pmatrix}j&j'&\lambda\\\tfrac12&-\tfrac12&0\end{pmatrix}$$

$$(l\tfrac12j\|L\|l'\tfrac12j')=\delta_{ll'}\hat j\hat j'\sqrt{l(l+1)(2l+1)}(-1)^{l+j'+3/2}
\begin{Bmatrix}l&l&1\\j'&j&\tfrac12\end{Bmatrix}$$

Diagonal closed forms:

$$(l\tfrac12j\|\sigma\|l\tfrac12j)=\sqrt{\tfrac{2j+1}{j(j+1)}}\big[j(j+1)-l(l+1)+\tfrac34\big],\qquad
(l\tfrac12j\|L\|l\tfrac12j)=\sqrt{\tfrac{2j+1}{4j(j+1)}}\big[j(j+1)+l(l+1)-\tfrac34\big].$$

### Theorem II — operators in the same space (6j + completeness)

$$(\alpha'j'\|[T_{L_1}S_{L_2}]_L\|\alpha j)=(-1)^{j+L+j'}\hat L\sum_{\alpha''j''}
\begin{Bmatrix}L_1&L_2&L\\j&j'&j''\end{Bmatrix}
(\alpha'j'\|T_{L_1}\|\alpha''j'')(\alpha''j''\|S_{L_2}\|\alpha j),$$

with scalar-product case
$(\alpha'j'\|T_L\cdot S_L\|\alpha j)=\delta_{jj'}\hat j^{-1}\sum_{\alpha''j''}(-1)^{j-j''}
(\alpha'j\|T_L\|\alpha''j'')(\alpha''j''\|S_L\|\alpha j)$ and e.g.
$(l'\|L^2\|l)=\delta_{ll'}\,l(l+1)\hat l$.


## 1. From A interacting nucleons to A quasiparticles
The A-body Schrödinger equation for strongly interacting point nucleons
cannot be solved exactly (A ≳ 10). The strategy is to trade strongly
interacting *particles* for weakly interacting *quasiparticles*. The simplest
version is the mean field: add and subtract a one-body potential,

$$H=T+V=\underbrace{\sum_i\big[t(\mathbf r_i)+v(\mathbf r_i)\big]}_{H_{MF}=\sum_i h(\mathbf r_i)}
+\underbrace{\Big[\sum_{i<j}v(\mathbf r_i,\mathbf r_j)-\sum_iv(\mathbf r_i)\Big]}_{V_{RES}} .$$

$H_{MF}$ separates: the A-body problem becomes one one-body problem
$h\phi_\alpha=\varepsilon_\alpha\phi_\alpha$, with product (Hartree) or
antisymmetrised product (Hartree–Fock, **Slater determinant**) wave functions
and $E=\sum_i\varepsilon_{\alpha_i}$. The residual interaction $V_{RES}$ is
left for perturbation theory or the methods of later chapters.

Picture: each nucleon feels the time-averaged field of the other $A-1$ — a
useful intuition, not a computable recipe.

## 2. Self-consistent vs phenomenological mean field
*Hartree–Fock*: minimise $\langle\Psi_0|H|\Psi_0\rangle$ over the orbitals with
normalisation as a constraint. The Lagrange multipliers turn out to be the
single-particle energies, and one gets a Schrödinger-like equation whose
potential is a functional of the unknown orbitals. It is nonlinear and solved
by iteration until self-consistency: $\phi^{(0)}\to V^{(0)}\to\phi^{(1)}\to V^{(1)}\to\cdots$
(derived properly in Sect. 4.5).

*Phenomenological shortcut*: just choose the well.

| potential | form | parameters |
|---|---|---|
| harmonic oscillator | $v_{HO}=-V_1+\tfrac12 m_N\omega^2r^2$ | $\hbar\omega$, $V_1$ |
| Woods–Saxon | $v_{WS}=-\dfrac{V_0}{1+e^{(r-R)/a}}$ | $R=1.27A^{1/3}$ fm, $a=0.67$ fm, $V_0=\big(51\pm33\tfrac{N-Z}{A}\big)$ MeV (+ protons, − neutrons) |

An HO can be made "equivalent" to a WS well by matching the major-shell
spacing ($\hbar\omega$) and the $0s$ energy ($V_1$). Near the bottom the wave
functions agree well; near zero energy WS functions have long tails that HO
functions lack.

## 3. Spin–orbit interaction and magic numbers
A central well alone gives shell gaps at 2, 8, 20, **40, 70, 112** — wrong
beyond 20. Adding $v_{LS}(r)\,\mathbf L\cdot\mathbf S$ splits each $l$ into
$j=l\pm\tfrac12$ and produces the observed **2, 8, 20, 28, 50, 82, 126**.

Nuclear spin–orbit is *not* the atomic (electromagnetic, meV) effect: it is of
MeV size, comparable to level spacings, and has the opposite ordering
($j=l+\tfrac12$ lower). Its origin is treated phenomenologically:

$$v_{LS}(r)=v^{(0)}_{LS}\Big(\frac{r_0}{\hbar}\Big)^2\frac1r\frac{d}{dr}\frac{1}{1+e^{(r-R)/a}},\qquad v^{(0)}_{LS}=0.44\,V_0 ,$$

peaked at the surface because of the derivative.

Since $J^2=L^2+2\mathbf L\cdot\mathbf S+S^2$, in the coupled basis $|l\tfrac12jm\rangle$

$$\mathbf L\cdot\mathbf S=\tfrac12\big[j(j+1)-l(l+1)-\tfrac34\big]\hbar^2,$$

so the spin–orbit term is diagonal and the single-particle states are the
coupled states $|nl\tfrac12jm\rangle$. Splitting of the partners:

$$\Delta^{LS}_{nl}=\varepsilon_{nlj_-}-\varepsilon_{nlj_+}\approx-(l+\tfrac12)\hbar^2C_{nl},\qquad
C_{nl}=\int_0^\infty r^2dr\,f^2_{nl}(r)v_{LS}(r)<0 ,$$

i.e. roughly linear in $l$ (exactly linear if $v_{LS}$ is a constant).

## 4. Solving the Woods–Saxon problem
Full single-particle Hamiltonian (protons also feel the uniformly charged
sphere Coulomb potential $v_C$):

$$h=-\frac{\hbar^2}{2m_N}\Big[\nabla_r^2-\frac{L^2/\hbar^2}{r^2}\Big]+v_{WS}+v_C+v_{LS}\,\mathbf L\cdot\mathbf S,\qquad
v_C(r)=\frac{Ze^2}{4\pi\epsilon_0}\begin{cases}\dfrac{3-(r/R)^2}{2R}&r\le R\\[4pt]\dfrac1r&r>R\end{cases}$$

The radial equation $h_{lj}(r)f_{nlj}(r)=\varepsilon_{nlj}f_{nlj}(r)$ is solved
by expanding in **harmonic oscillator radial functions**,

$$f_{nlj}(r)=\sum_\nu A^{(nlj)}_\nu g_{\nu l}(r),\qquad
g_{nl}(r)=\sqrt{\frac{2\,n!}{b^3\Gamma(n+l+\frac32)}}\Big(\frac rb\Big)^l e^{-r^2/2b^2}L^{(l+1/2)}_n(r^2/b^2),$$

with $N=2n+l$, $\varepsilon_{nl}=-V_1+(N+\tfrac32)\hbar\omega$, $n$ = number of
nodes (0,1,2,…), phase $g_{nl}\to r^l>0$ at the origin, and oscillator length

$$b=\frac{\hbar c}{\sqrt{(m_Nc^2)(\hbar\omega)}}\approx\frac{197.33}{\sqrt{940\,\hbar\omega[\mathrm{MeV}]}}\ \mathrm{fm},\qquad
\hbar\omega=45A^{-1/3}-25A^{-2/3}\ \mathrm{MeV}\ \text{(Blomqvist–Molinari)}.$$

(The cruder $\hbar\omega=41A^{-1/3}$, $b=1.005A^{1/6}$ fm is also common.)

Using the oscillator equation to eliminate $\nabla_r^2$, the matrix to
diagonalise is

$$\langle\nu'|h_{lj}|\nu\rangle=\int_0^\infty r^2dr\,g_{\nu'l}g_{\nu l}\Big[\frac{\hbar^2}{2m_N}\Big(\frac{4\nu+2l+3}{b^2}-\frac{r^2}{b^4}\Big)
+v_{WS}+v_C+\tfrac12\big(j(j+1)-l(l+1)-\tfrac34\big)\hbar^2v_{LS}\Big].$$

Findings (Tables 3.1–3.4 for $^{16}$O, $^{40}$Ca): the dominant component is
$\nu=n$; deep states are almost pure oscillator states; $\nu\le8$ converges.
Some high $l>0$ states sit at *positive* energy but are quasi-bound behind the
centrifugal barrier $v_{cf}(R)\approx13.2A^{-2/3}l(l+1)$ MeV (plus, for
protons, the Coulomb barrier $v_C(R)\approx1.15ZA^{-1/3}$ MeV).

## 5. Many-nucleon configurations
Baranger notation: $|\alpha\rangle=|a\,m_\alpha\rangle$, $a=n_al_aj_a$, with

$$\phi_\alpha(\mathbf x)=\eta_a\,g_{n_al_a}(r)\,[Y_{l_a}(\Omega)\chi_{1/2}]_{j_am_\alpha},\qquad
\eta_a=\begin{cases}1&\text{Condon–Shortley}\\ i^{l_a}&\text{Biedenharn–Rose}\end{cases}$$

(CS is used in the book; BR makes BCS amplitudes positive, $u^{(CS)}_a=(-1)^{l_a}u^{(BR)}_a$.)

Orbitals are orthonormal and complete. The A-nucleon wave function is a
product of a proton and a neutron Slater determinant,

$$\Psi_{\pi_1\cdots\pi_Z}=\frac{1}{\sqrt{Z!}}\det\big[\phi_{\pi_i}(\mathbf x_k)\big],$$

which is antisymmetric under any exchange and vanishes if two labels coincide
— the Pauli principle. Each determinant = one configuration; its mean-field
energy is the sum of occupied single-particle energies, e.g. for the 10
protons of Ne: $E_0=2\varepsilon_{0s_{1/2}}+4\varepsilon_{0p_{3/2}}+2\varepsilon_{0p_{1/2}}+2\varepsilon_{0d_{5/2}}$,
and the first excited configuration lifts one proton $0d_{5/2}\to1s_{1/2}$.
The highest occupied level defines the **Fermi energy** (one for protons, one
for neutrons). Slater determinants are orthonormal and complete in the
Z-particle space.

