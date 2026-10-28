# Chapter 1 — Angular Momentum Coupling

Study notes + companion program: [`angular_momentum.py`](./angular_momentum.py)

## 1. Why couple angular momenta?
Nuclei (like atoms and molecules) are built from constituents that each carry
orbital angular momentum and spin. The total angular momentum of the system is
assembled from these pieces. The machinery for doing this is the subject of
this chapter: Clebsch–Gordan (CG) coefficients and 3j symbols (two angular
momenta), 6j symbols (three) and 9j symbols (four).

## 2. Definition of an angular momentum operator
A vector operator $\mathbf J=(J_1,J_2,J_3)$ is an angular momentum if

$$J_k^\dagger = J_k,\qquad [J_i,J_j]=i\hbar\,\epsilon_{ijk}J_k .$$

Eigenstates $|j\,m\rangle$ satisfy

$$\mathbf J^2|j m\rangle=j(j+1)\hbar^2|j m\rangle,\qquad J_z|j m\rangle=m\hbar|j m\rangle,\qquad m=-j,\dots,j.$$

Ladder operators $J_\pm=J_x\pm iJ_y$ obey $[J_+,J_-]=2\hbar J_z$,
$[J_\pm,J_z]=\mp\hbar J_\pm$ and

$$J_\pm|j m\rangle=\hbar\sqrt{(j\mp m)(j\pm m+1)}\,|j\,m\pm1\rangle .$$

Starting from the "stretched" state $|j\,j\rangle$ and applying $J_-$
generates the whole multiplet.

## 3. Coupling two angular momenta
Let $\mathbf J_1,\mathbf J_2$ commute. Two complete bases exist:

| basis | commuting set | states |
|---|---|---|
| uncoupled | $\{J_1^2,J_{1z},J_2^2,J_{2z}\}$ | $\lvert j_1 m_1 j_2 m_2\rangle=\lvert j_1 m_1\rangle\lvert j_2 m_2\rangle$ |
| coupled | $\{J_1^2,J_2^2,J^2,J_z\}$ with $\mathbf J=\mathbf J_1+\mathbf J_2$ | $\lvert j_1 j_2 j m\rangle$ |

Coupling keeps the *lengths* $j_1,j_2$ sharp but only the *total* projection
$m$; the individual $m_1,m_2$ become indefinite.

The two bases are related by a real unitary transformation whose matrix
elements are the **Clebsch–Gordan coefficients**:

$$|j_1 j_2 j m\rangle=\sum_{m_1 m_2}(j_1 m_1 j_2 m_2|j m)\,|j_1 m_1 j_2 m_2\rangle .$$

### Selection rules
* $m_1+m_2=m$
* triangle condition $\Delta(j_1 j_2 j)$: $|j_1-j_2|\le j\le j_1+j_2$
* $j_1+j_2+j$ is an integer, so $j=|j_1-j_2|,\,|j_1-j_2|+1,\dots,j_1+j_2$

### Phase convention (Condon–Shortley)
$(j_1 j_1 j_2 j_2|j_1{+}j_2\; j_1{+}j_2)=+1$ and $(j_1 m_1 j_2\,{-}j_2|j m)\ge0$.

### Key properties
* Orthogonality: $\sum_{m_1m_2}(j_1m_1j_2m_2|jm)(j_1m_1j_2m_2|j'm')=\delta_{jj'}\delta_{mm'}$
* Completeness: $\sum_{jm}(j_1m_1j_2m_2|jm)(j_1m_1'j_2m_2'|jm)=\delta_{m_1m_1'}\delta_{m_2m_2'}$
* Swap order: $(j_2m_2j_1m_1|jm)=(-1)^{j_1+j_2-j}(j_1m_1j_2m_2|jm)$
* Flip projections: $(j_1\,{-}m_1\,j_2\,{-}m_2|j\,{-}m)=(-1)^{j_1+j_2-j}(j_1m_1j_2m_2|jm)$
* $(j_10j_20|j0)=0$ unless $j_1+j_2+j$ even
* $(jm\,00|jm)=1$
* Coupling to zero: $(jm\,j m'|00)=(-1)^{j-m}\hat j^{-1}\delta_{m,-m'}$ with the hat factor $\hat j\equiv\sqrt{2j+1}$
* Re-coupling (total with one constituent to give the other):
  $(j_1m_1j_2m_2|jm)=(-1)^{j_2+m_2}\dfrac{\hat j}{\hat j_1}(j_2\,{-}m_2\,jm|j_1m_1)
  =(-1)^{j_1-m_1}\dfrac{\hat j}{\hat j_2}(jm\,j_1\,{-}m_1|j_2m_2)$

## 4. 3j symbols
A more symmetric repackaging of the CG coefficient:

$$\begin{pmatrix}j_1&j_2&j_3\\m_1&m_2&m_3\end{pmatrix}
\equiv(-1)^{j_1-j_2-m_3}\,\hat j_3^{-1}\,(j_1m_1j_2m_2|j_3\,{-}m_3),$$

with inverse $(j_1m_1j_2m_2|j_3m_3)=(-1)^{j_2-j_1-m_3}\hat j_3\begin{pmatrix}j_1&j_2&j_3\\m_1&m_2&-m_3\end{pmatrix}$.

Properties:
* zero unless $\Delta(j_1j_2j_3)$ and $m_1+m_2+m_3=0$
* odd column permutation or flipping all $m$'s → factor $(-1)^{j_1+j_2+j_3}$; even permutations leave it unchanged
* $\begin{pmatrix}j_1&j_2&0\\m_1&m_2&0\end{pmatrix}=(-1)^{j_1-m_1}\hat j_1^{-1}\delta_{j_1j_2}\delta_{m_1,-m_2}$
* $\begin{pmatrix}j_1&j_2&j_3\\0&0&0\end{pmatrix}=0$ unless $j_1+j_2+j_3$ even
* $\sum_{m_1m_2m_3}\begin{pmatrix}j_1&j_2&j_3\\m_1&m_2&m_3\end{pmatrix}^2=\Delta(j_1j_2j_3)$

Closed forms exist for the small cases $(j{+}\tfrac12\;j\;\tfrac12)$,
$(j{+}1\;j\;1)$, $(j\;j\;1)$, $(j\;j\;2)$ — e.g.
$\begin{pmatrix}j&j&1\\m&-m&0\end{pmatrix}=(-1)^{j-m}\dfrac{m}{\sqrt{j(j+1)(2j+1)}}$.
All of them are reproduced numerically in the program's test suite.

## 5. Three angular momenta: the 6j symbol
With $\mathbf J=\mathbf J_1+\mathbf J_2+\mathbf J_3$ there are three coupling
orders ($\mathbf J_{12}$ first, $\mathbf J_{23}$ first, $\mathbf J_{13}$ first).
The allowed $j$ values are the same, the states are not. The overlap between
schemes defines the 6j symbol:

$$|j_1,j_2j_3(j_{23});jm\rangle=\sum_{j_{12}}(-1)^{j_1+j_2+j_3+j}\,\hat j_{12}\hat j_{23}
\begin{Bmatrix}j_1&j_2&j_{12}\\j_3&j&j_{23}\end{Bmatrix}|j_1j_2(j_{12})j_3;jm\rangle .$$

No projection quantum numbers appear: both bases already have good total $j$.
It can also be written as a sum over products of four 3j symbols.

Properties:
* zero unless the four triads $\Delta(j_1j_2j_3)$, $\Delta(l_1l_2j_3)$, $\Delta(l_1j_2l_3)$, $\Delta(j_1l_2l_3)$ hold
* invariant under any column permutation and under swapping upper/lower entries in any two columns (24 tetrahedral symmetries)
* Racah $W$: $W(j_1j_2l_2l_1;j_3l_3)=(-1)^{j_1+j_2+l_1+l_2}\begin{Bmatrix}j_1&j_2&j_3\\l_1&l_2&l_3\end{Bmatrix}$
* one zero entry: $\begin{Bmatrix}j_1&j_2&j_3\\0&j_3&j_2\end{Bmatrix}=\dfrac{(-1)^{j_1+j_2+j_3}}{\hat j_2\hat j_3}$
* unitarity: $\sum_j \hat j^2\begin{Bmatrix}j_1&j_2&j\\j_3&j_4&j'\end{Bmatrix}\begin{Bmatrix}j_1&j_2&j\\j_3&j_4&j''\end{Bmatrix}=\delta_{j'j''}\hat j'^{-2}$
* $\sum_j(-1)^{j_1+j_2+j}\hat j^2\begin{Bmatrix}j_1&j_1&j\\j_2&j_2&j'\end{Bmatrix}=\hat j_1\hat j_2\delta_{j'0}$
* closed form with a 1 in the lower row:
  $\begin{Bmatrix}j_1&j_2&j_3\\1&j_3&j_2\end{Bmatrix}=(-1)^{s}\dfrac{j_1(j_1+1)-j_2(j_2+1)-j_3(j_3+1)}{\sqrt{4j_2(j_2+1)(2j_2+1)j_3(j_3+1)(2j_3+1)}}$, $s=j_1+j_2+j_3$
  (several more with $\tfrac12$ or $1$ in the lower row are in the chapter and in the tests).

## 6. Four angular momenta: the 9j symbol
Two natural schemes: $(12)(34)$ and $(13)(24)$. Their overlap is the 9j symbol:

$$|j_1j_3(j_{13})j_2j_4(j_{24});jm\rangle=\sum_{j_{12}j_{34}}\hat j_{12}\hat j_{34}\hat j_{13}\hat j_{24}
\begin{Bmatrix}j_1&j_2&j_{12}\\j_3&j_4&j_{34}\\j_{13}&j_{24}&j\end{Bmatrix}|j_1j_2(j_{12})j_3j_4(j_{34});jm\rangle .$$

Rows encode the first scheme, columns the second, and the last row/column the
final coupling to $j$.

Properties:
* zero unless every row and every column satisfies the triangle rule (6 conditions)
* invariant under transposition; odd row/column permutation → $(-1)^{\Sigma}$, $\Sigma=$ sum of all nine entries
* reduction to a 6j symbol when the corner is zero:
  $\begin{Bmatrix}j_1&j_2&j_{12}\\j_3&j_4&j_{34}\\j_{13}&j_{24}&0\end{Bmatrix}=\delta_{j_{12}j_{34}}\delta_{j_{13}j_{24}}\dfrac{(-1)^{j_{12}+j_{13}+j_2+j_3}}{\hat j_{12}\hat j_{13}}\begin{Bmatrix}j_1&j_2&j_{12}\\j_4&j_3&j_{13}\end{Bmatrix}$
* general evaluation as a sum over a product of three 6j symbols (this is what the program uses)
* orthogonality: $\sum_{j_{13}j_{24}}\hat j_{13}^2\hat j_{24}^2\{9j\}\{9j'\}=\delta_{j_{12}j_{12}'}\delta_{j_{34}j_{34}'}\hat j_{12}^{-2}\hat j_{34}^{-2}$

Physical use: the $LS\leftrightarrow jj$ transformation for two nucleons is a
9j symbol with rows $(l_1\,s_1\,j_1),(l_2\,s_2\,j_2),(L\,S\,J)$.

## 7. Exercises covered by the program
| exercise | what the program does |
|---|---|
| 1.2 / 1.21 | `allowed_couplings()` lists $J^\pi$ of two-particle configurations |
| 1.3, 1.4 | `j_matrices(1)` builds $J^2,J_\pm,J_z,J_x,J_y$; `rigid_rotor()` diagonalises $H=\sum J_k^2/2I_k$ |
| 1.7 | `cg()` reproduces the $j_1=1,j_2=\tfrac12$ table |
| 1.8, 1.9, 1.14 | orthogonality / completeness checks in `run_tests()` |
| 1.16 | `six_j()` values of the two requested symbols |
| 1.22 | `nine_j()` value of the $LS$–$jj$ transformation symbol |
