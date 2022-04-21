---
{"dg-publish":true,"dg-permalink":"mml/chap2/ex","permalink":"/mml/chap2/ex/","dgHomeLink":true,"dgPassFrontmatter":false}
---


↑ [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 2 - Linear Algebra|Chapter 2 - Linear Algebra]]
<-- **NONE** - [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 3 - Exercices|Chapter 3 - Exercices]] -->

---
#### Exercice 2.1 (Almost done)
> We consider $(\mathbb{R} \setminus \{-1\},\star)$, where
> $$a\star b:=ab+a+b, \quad\quad a, b \in \mathbb{R}\setminus\{-1\} \quad (2.134)$$
> **a)** Show that $(\mathbb{R} \setminus \{-1\},\star)$ is an Abelian group
> **b)** Solve
> $$3\star x\star x=15$$
> in the Abelian group $(\mathbb{R}\setminus\{-1\},\star)$, where $\star$ is defined in (2.134)

-> see : [[Topics/Mathematics/Group theory|Group theory]], [[___INBOX___/__à trier/Vector spaces|Vector spaces]], ...

**a)** We must show it is a group (closure, associativity, null element, inverse element) and commutative ?
- **Associativity** : $\forall a,b,c \in \mathcal{G}: (a\star b)\star c = a\star (b\star c)$
	- $(a\star b)\star c=(ab+a+b)\star c=(ab+a+b)c+(ab+a+b)+c=abc+ac+bc+ab+a+b+c$
	- $a\star (b\star c)=a\star (bc+b+c)=a(bc+b+c)+a+(bc+b+c)=abc+ab+ac+a+bc+b+c$
	- => both are equals -> ==$*$ operation is associative==
- **Neutral element** : $\exists e \in \mathcal{G}, \forall x \in \mathcal{G} : x\star e=x$ and $e\star x=x$
	- -> ==e = 0== => $a\star 0=0+a+0=a$ and $0\star b=0+0+b=b$
- **Inverse element** : $\forall x \in \mathcal{G}, \exists y \in \mathcal{G}:x\star y=e$ and $y\star x=e$ where $e$ is the neutral element
	- we have inverses of $a=-\frac{b}{b+1}$ and of $b=-\frac{a}{a+1}$ which belongs to $\mathcal{G}$
- **closure property** (-> $\forall a,b \in \mathcal{G} : a \star b \in \mathcal{G}$)
	-  $a*b$ must not equals to -1 => because the 
- **Abelian** :
	- we have $b\star a=ba+b+a$ which is the same as $ab+a+b=a\star b$
		- because multiplication is commutative, and addition associative

**b)** $3\star x\star x=...=(x+1)(x-3)$ ?

==TODO==

---
#### Exercice 2.2
> Let $n$ be in $\mathbb{N} \setminus \{0\}$. Let $k,x$ be in $\mathbb{Z}$. We define the congruence class $\overline{k}$ of the integer $k$ as the set :
> $$\overline{k}=\{x \in \mathbb{Z} | x-k = 0 \pmod n\}
=\{x\in\mathbb{Z}|\exists a\in \mathbb{Z}: (x-k=n\cdot a)\}$$
> We now define $\mathbb{Z} / n\mathbb{Z}$ (sometimes written $\mathbb{Z}_n$) as the set of all congruence classes modulo $n$. Euclidean division implies that this set is a finite set containing $n$ elements:
> $$\mathbb{Z}_n=\{\overline{0},\overline{1},...,\overline{n-1}\}$$
> For all $\overline{a}, \overline{b} \in \mathbb{Z}_n$, we define
> $$\overline{a} \oplus \overline{b} := \overline{a+b}$$
> **a)** Show that ($\mathbb{Z}_n, \oplus)$ is a group. Is it Abelian ?
> 
> **b)** We now define another operation $\otimes$ for all $\overline{a}$ and $\overline{b}$ in $\mathbb{Z}_n$ as
> 
> $$\overline{a} \otimes \overline{b} := \overline{a\times b}$$
> where $a\times b$ represents the usual multiplication in $\mathbb{Z}$.
> Let $n=5$. Draw the times table of the elements of $\mathbb{Z}_n\setminus\{\overline{0}\}$ under $\otimes$, i.e., calculate the products $\overline{a}\otimes\overline{b}$ for all $\overline{a}$ and $\overline{b}$ in $\mathbb{Z}_5\setminus\{\overline{0}\}$.
> Hence, show that $\otimes$ is closed under $\otimes$ and possess a neutral element for $\otimes$. Display the inverse of all elements in $\mathbb{Z}_5\setminus\{\overline{0}\}$ under $\otimes$. Conclude that $\mathbb{Z}_5\setminus\{\overline{0}\}$ is an Abelian group.
> 
> **c)** Show that $\mathbb{Z}_8\setminus\{\overline{0}\}$ is not a group.
> 
> **d)** We recall that the Bézout theorem states that two integers $a$ and $b$ are relatively prime (i.e., $gcd(a,b)=1$) if and only if there exists two integers $u$ and $v$ such that $au+bv=1$. Show that $(\mathbb{Z}_n\setminus\{\overline{0}\},\otimes)$ is a group if and only if $n\in\mathbb{N}\setminus\{0\}$ is prime.

**a)** We must
- show it is "closed"
	- by outer operation (multiplication by a scalar?) : 
	- by inner operation : ==no==, 
- Associativity ?
- Have a neutral element
- and an inverse
- To show a group is Abelian ? -> If we invert $a$ and $b$ we still get $\overline{a+b}$


**b)** 

**c)** 

**d)** `Bézout theorem / relatively prime` -> ?


==TODO==

---
#### Exercice 2.3 (Almost done)
> Consider the set $\mathcal{G}$ of 3x3 matrices defined as follows:
> $\mathcal{G}=\{\begin{bmatrix} 1 & x & 2 \newline 0 & 1 & y \newline 0 & 0 & 1 \end{bmatrix} \in \mathbb{R}^{3\times 3} | x,y,z \in \mathbb{R}\}$
> We define $\cdot$ as the standard matrix multiplication.
> Is ($\mathcal{G},\cdot$) a group ? If yes, is it Abelian ? Justify your answer.

-> It's a group if it is `closed` (closure property), has `associativity`, has a `neutral element` and has an `inverse`

**closure** : $\begin{bmatrix} 1 & x & z \newline 0 & 1 & y \newline 0 & 0 & 1 \end{bmatrix}\cdot \begin{bmatrix} 1 & x & z \newline 0 & 1 & y \newline 0 & 0 & 1 \end{bmatrix} = \begin{bmatrix} 1 & 2x & 2z+xy \newline 0 & 1 & 2y \newline 0 & 0 & 1 \end{bmatrix}$, which also belongs to $\mathcal{G}$.

**associativity** : ==TODO==

**neutral element** : ==TODO==

**inverse element** : ==TODO==

-> Generally, standard matrix multiplication is not Abelian (not commutative) but here it is ==Abelian== we get "twice" :
$$\begin{bmatrix} 1 & x_1+x_2 & z_1+z_2+x_1+y2 \newline 0 & 1 & y_1+y_2 \newline 0 & 0 & 1 \end{bmatrix}$$

---
#### 2.4
> Compute the following matrix products, if possible :
> **a)** $\begin{bmatrix}1&2 \newline 4&5 \newline 7&8\end{bmatrix} \begin{bmatrix}1&1&0 \newline 0&1&1 \newline 1&0&1\end{bmatrix}$
> **b)** $\begin{bmatrix}1&2&3 \newline 4&5&6 \newline 7&8&9\end{bmatrix} \begin{bmatrix}1&1&0 \newline 0&1&1 \newline 1&0&1\end{bmatrix}$
> **c)** $\begin{bmatrix}1&1&0 \newline 0&1&1 \newline 1&0&1\end{bmatrix} \begin{bmatrix}1&2&3 \newline 4&5&6 \newline 7&8&9\end{bmatrix}$
> **d)** $\begin{bmatrix}1&2&1&2 \newline 4&1&-1&-4\end{bmatrix} \begin{bmatrix}0&3 \newline 1&-1 \newline 2&1 \newline 5&2\end{bmatrix}$
> **e)** $\begin{bmatrix}0&3 \newline 1&-1 \newline 2&1 \newline 5&2\end{bmatrix} \begin{bmatrix}1&2&1&2 \newline 4&1&-1&-4\end{bmatrix}$

**a)** impossible
**b)** $\begin{bmatrix}4&3&5 \newline 10&9&11 \newline 16&15&17\end{bmatrix}$
**c)** $\begin{bmatrix}5&7&9 \newline 11&13&15 \newline 8&10&12\end{bmatrix}$
**d)** $\begin{bmatrix}14&6 \newline -21&2\end{bmatrix}$
**e)** $\begin{bmatrix}12&3&-3&-12 \newline -3&1&2&6 \newline 6&5&1&0 \newline 13&12&3&2\end{bmatrix}$

---
#### Exercice 2.5
> Find the set $\mathcal{S}$ of all solutions in $x$ of the following inhomogeneous linear systems $Ax=b$, where $A$ and $b$ are defined as follows:
> **a)** 
> $$A=\begin{bmatrix}1&1&-1&-1 \newline 2&5&-7&-5\newline 2&-1&1&3\newline 5&2&-4&2\end{bmatrix}, b=\begin{bmatrix}1\newline -2\newline 4\newline 6\end{bmatrix}$$
> **b)** 
> $$A=\begin{bmatrix}1&-1&0&0&1 \newline 1&1&0&-3&0 \newline 2&-1&0&1&-1 \newline -1&2&0&-2&-1\end{bmatrix}, b=\begin{bmatrix}3\newline 6\newline 5\newline -1\end{bmatrix}$$

**a)** ==TODO==
**b)** $X=X_p+X_N=\begin{bmatrix}3\newline 0\newline 0\newline -1\newline 0\end{bmatrix}+\begin{bmatrix}\beta\newline 2\beta\newline \alpha\newline \beta\newline \beta\end{bmatrix}$

---
#### 2.6
> Using Gaussian elimination, find all solutions of the inhomogeneous equation system $Ax=b$ with
> $$A=\begin{bmatrix}0&1&0&0&1&0\newline 0&0&0&1&1&0\newline 0&1&0&0&0&1\end{bmatrix}, b=\begin{bmatrix}2\newline -1\newline 1\end{bmatrix}$$

$X=X_p+X_N=\begin{bmatrix}0 \newline 1 \newline 0 \newline -2\newline 1\newline 0\end{bmatrix}+\begin{bmatrix} \alpha \newline -\beta \newline \gamma \newline -\beta \newline \beta \newline \beta \end{bmatrix}$

---
#### 2.7
> Find all solutions in $x=\begin{bmatrix}x_1 \newline x_2 \newline x_3\end{bmatrix} \in \mathbb{R}^3$ of the equation system $Ax=12x$,
> where
> $$A=\begin{bmatrix}6&4&3 \newline 6&0&9 \newline 0&8&0\end{bmatrix}$$
> and $\sum_{i=1}^3x_i=1$

We can rewrite it as an homogeneous system :
$(A-12I)x = 0$

Then put it in augmented form (with last line corresponding to the constraint on $x_i$ :
=> $\begin{bmatrix}-6&4&3&0 \newline 6&-12&9&0 \newline 0&8&-12&0 \newline 1&1&1&1\end{bmatrix}$
We can put it in reduced row-echelon form, to obtain the identity matrix on the left, then :
we get $x=\begin{bmatrix}\frac{3}{8} \newline \frac{3}{8} \newline \frac{1}{4}\end{bmatrix}$

---
#### 2.8
> Determine the **inverses** of the following matrices if possible:
> **a)**
> $$A=\begin{bmatrix}2&3&4 \newline 3&4&5 \newline 4&5&6\end{bmatrix}$$
> **b)**
> $$A=\begin{bmatrix}1&0&1&0 \newline 0&1&1&0 \newline 1&1&0&1 \newline 1&1&1&0\end{bmatrix}$$

**a)** impossible : no inverse (=singular matrix), because of linear dependence (see Chapter 2.5) it can be reduced and have some free variables : **invertible square matrix has no free variables**

**b)** Done by Gaussian elimination on an augmented matrix (with identity matrix on the right) until we get the identity matrix on the left. Solution :

$\begin{bmatrix} 1&0&0&0&0&-1&0&-1 \newline 0&1&0&0&-1&0&0&1 \newline 0&0&1&0&1&1&0&-1 \newline 0&0&0&1&1&1&1&-2 \end{bmatrix}$

---
> **Subspaces** -> https://www.quora.com/W-x_1-x_2-x_3-T-3x_1+-frac-1-4-x_2-0-Is-W-a-subspace-of-mathbb-R-3

#### Exercice 2.9
> Which of the following sets are **subspaces** of $\mathbb{R}^3$ ?
>	- $A=\{(\lambda, \lambda+\mu^3, \lambda-\mu^3)|\lambda,\mu\in \mathbb{R}\}$
>	- $B=\{(\lambda^2, -\lambda^2, 0)|\lambda \in \mathbb{R}\}$
>	- **c)** Let $\gamma$ be in $\mathbb{R}$
>		$C=\{(\xi_1, \xi_2, \xi_3)\in\mathbb{R}^3|\xi_1-2\xi_2+3\xi_3=\gamma\}$
>	- $D=\{(\xi_1, \xi_2, \xi_3)\in\mathbb{R}^3|\xi_2\in\mathbb{Z}\}$

-> find if closure property (under vector addition, and scalar multiplication?), associativity null element (0,0,0), "inverse" element ???

=> HOW ?
==TODO==

---
#### 2.10
> Are the following sets of vectors **linearly independent** ?
> **a)**
> $$x_1=\begin{bmatrix}2 \newline -1 \newline 3\end{bmatrix}, x_2=\begin{bmatrix}1 \newline 1 \newline -2\end{bmatrix}, x_3=\begin{bmatrix}3 \newline -3 \newline 8\end{bmatrix}$$
> **b)**
> $$x_1=\begin{bmatrix}1 \newline 2 \newline 1 \newline 0 \newline 0\end{bmatrix}, x_2=\begin{bmatrix}1 \newline 1 \newline 0 \newline 1 \newline 1\end{bmatrix}, x_3=\begin{bmatrix}1 \newline 0 \newline 0 \newline 1 \newline 1\end{bmatrix}$$

-> find if all pivot colums => independent

**a)** -> **Yes**, no free column
**b)** -> **Yes**, no free column

---
#### 2.11
> Write
> $$y=\begin{bmatrix}-1 \newline -2 \newline 5\end{bmatrix}$$
> as linear combinaison of
> $$x_1=\begin{bmatrix}1 \newline 1 \newline 1\end{bmatrix}, x_2=\begin{bmatrix}1 \newline 2 \newline 3\end{bmatrix}, x_3=\begin{bmatrix}2 \newline -1 \newline 1\end{bmatrix}$$

Put in augmented form : $[x_1 x_2 x_3|y]$, do Gaussian elimination until I get identity matrix...
=> $y=-6x_1+3x_2+2x_3$

---
#### Exercice 2.12
> Consider two subspaces of $\mathbb{R}^4$:
> $$U_1=span[\begin{bmatrix}1 \newline 1 \newline -3 \newline 1\end{bmatrix}, \begin{bmatrix}2 \newline -1 \newline 0 \newline -1\end{bmatrix}, \begin{bmatrix}-1 \newline 1 \newline -1 \newline 1\end{bmatrix}], U_2=span[\begin{bmatrix}-1 \newline -2 \newline 2 \newline 1\end{bmatrix}, \begin{bmatrix}2 \newline -2 \newline 0 \newline 0\end{bmatrix}, \begin{bmatrix}-3 \newline 6 \newline -2 \newline -1\end{bmatrix}]$$
> Determine the **basis** of $U_1\cap U_2$.

=> ==DONE ?== (recopy...)

---
#### Exercice 2.13
> Consider two subspaces $U_1$ and $U_2$, where $U_1$ is the solution space of the homogeneous equation system $A_1 x=0$ and $U_2$ is the solution space of the homogeneous equation system $A_2 x=0$ with
> $$A_1=\begin{bmatrix}1&0&1 \newline 1&-2&-1 \newline 2&1&3 \newline 1&0&1\end{bmatrix}, A_2=\begin{bmatrix}3&-3&0 \newline 1&2&3 \newline 7&-5&2 \newline 3&-1&2\end{bmatrix}$$
> **a)** Determine the dimension of $U_1, U_2$.
> **b)** Determine bases of $U_1$ and $U_2$.
> **c)** Determine a basis of $U_1\cap U_2$

==TODO==

---
#### Exercice 2.14
> Consider two subspaces $U_1$ and $U_2$, where $U_1$ is spanned by the columns of $A_1$ and $U_2$ is spanned by the columns of $A_2$ with
> $$A_1=\begin{bmatrix}1&0&1 \newline 1&-2&-1 \newline 2&1&3 \newline 1&0&1\end{bmatrix}, A_2=\begin{bmatrix}3&-3&0 \newline 1&2&3 \newline 7&-5&2 \newline 3&-1&2\end{bmatrix}$$
> **a)** Determine the dimension of $U_1, U_2$
> **b)** Determine bases of $U_1$ and $U_2$
> **c)** Determine a basis of $U_1\cap U_2$

==TODO==

**a)** The dimension of a subspace is the number of his basis vectors. To find the basis we must execute 3 steps
- Write the spanning vectors as columns of a matrix $A$ (already done for us)
- Determine the row-echelon form of $A$
- The spanning vectors associated with the pivot columns are a basis of $U$

$A_1=\begin{bmatrix}\cellcolor{lightgray} 1 & 0 & 1 \newline 0 & \cellcolor{lightgray} 1 & 0 \newline  0 & 0 & \cellcolor{lightgray} 1 \newline  0 & 0 & 0 \end{bmatrix}$ => dimension : 3
$A_2=\begin{bmatrix}\cellcolor{lightgray} 1 & 2 & 3 \newline 0 & \cellcolor{lightgray} 1 & 1 \newline 0&0&0 \newline 0&0&0\end{bmatrix}$ => dimension : 2

**c)** a basis of $U_1\cap U_2$ : $\begin{bmatrix}1&0 \newline 0&1 \newline 0&0 \newline 0&0\end{bmatrix}$

---
#### Exercice 2.15
> Let $F=\{(x,y,z)\in \mathbb{R}^3|x+y-z=0\}$ and $G=\{(a-b, a+b, a-3b)|a,b\in\mathbb{R}\}$
> **a)** Show that $F$ and $G$ are subspaces of $\mathbb{R}^3$
> **b)** Calculate $F\cap G$ without resorting to any basis vector.
> **c)** Find one basis for $F$ and one for $G$, calculate $F\cap G$ using the basis vectors previously found and check your result with the previous question.

**a)** To be a subspace (of $\mathbb{R}^3$), it must : (-> see *Example 2.12*, page **39**)
- not be the empty set $\emptyset$, but it must contain $0$
- closure with respect to the **outer** and **inner** operation
	- $\forall \lambda \in \mathbb{R}, \exists x \in \mathcal{U} : \lambda x \in \mathcal{U}$
	- $\forall x,y \in \mathcal{U} : x + y \in \mathcal{U}$

==For $F$==, the subspace is not empty and contains $0$.
If we multiply an element by $\lambda$ we stay in the subspace because we get $\lambda x+\lambda y-\lambda z=0$ and the sum is also equals to $0$ (-> outer operation : ==OK==)
If we add $(x_1+x_2)+(y_1+y_2)-(z_1+z_2)=0$, we see that each 3 sums (in parenthesis) are still in $\mathbb{R}$ so -> inner operation : ==OK==
==> `F is a subspace`

For $G$, 

==TODO==

---
#### Exercice 2.16
> Are the following mappings linear ?
> **a)** Let $a,b \in \mathbb{R}$.
> $$\Phi:L^1([a,b])\rightarrow\mathbb{R}, \quad f\rightarrow \Phi(f)=\int_a^bf(x)dx$$
> where $L^1([a,b])$ denotes the set of integrable functions on $[a,b]$.
> **b)**
> $$\Phi:C^1\rightarrow C^0, \quad f \rightarrow \Phi(f)=f^\prime$$
> where for $k\ge 1$, $C^k$ denotes the set of $k$ times continuously differentiable functions, and $C^0$ denotes the set of continuous functions.
> **c)**
> $$\Phi:\mathbb{R}\rightarrow\mathbb{R}, \quad x\rightarrow\Phi(x)=cos(x)$$
> **d)**
> $$\Phi:\mathbb{R}^3\rightarrow\mathbb{R}^2, \quad x\rightarrow\begin{bmatrix}1&2&3 \newline 1&4&3\end{bmatrix}x$$
> **e)** Let $\theta$ be in $[0,2\pi]$ and
> $$\Phi:\mathbb{R}^2\rightarrow\mathbb{R}^2, \quad x\rightarrow\begin{bmatrix}\cos(\theta)&\sin(\theta) \newline -\sin(\theta)&\cos(\theta)\end{bmatrix}x$$

**a)**
Is integration linear ? ...

**b)**
Is derivation linear ? ...

**c)**
is cos(x) linear ... ?

**d)**
matrix should be the representation of a linear mapping ... by definition ?

**e)**
Is rotation linear ?

==TODO==

---
#### Exercice 2.17
> Consider the linear mapping
> $$\Phi:\mathbb{R}^3\rightarrow\mathbb{R}^4, \Phi(\begin{bmatrix}x_1 \newline x_2 \newline x_3\end{bmatrix})=\begin{bmatrix}3x_1+2x_2+x_3 \newline x_1+x_2+x_3 \newline x_1-3x_2 \newline 2x_1+3x_2+x_3\end{bmatrix}$$
**a)** Find the transformation matrix $A_\Phi$
**b)** Determine $rk(A_\phi)$
**c)** Compute the kernel and image of $\Phi$. What are $dim(ker(\Phi))$ and $dim(Im(\Phi))$ ?

==TODO==

**a)** -> see ***definition 2.19 (Transformation matrix)***
$A_\Phi=\begin{bmatrix}3&1&1&2 \newline 2&1&-3&3 \newline 1&1&0&1\end{bmatrix}$

**b)** -> row reduced form -> count number of pivot columns
$rk(A_\Phi)=3$

$=dim(Im(A))$ ?

**c)** kernel = null space
(-> see ***Chap 2.7.3***)



---
#### Exercice 2.18
> Let $E$ be a vector space. Let $f$ and $g$ be two **automorphisms** on $E$ such that $f\circ g=id_E$ (i.e., $f\circ g$ is the identity matrix $id_E$). Show that $ker(f)=ker(g\circ f)$, $Im(g)=Im(g\circ f)$ and that $ker(f)\cap Im(g)=\{0_E\}$

==TODO==...

---
#### Exercice 2.19
> Consider an endomorphism $\Phi : \mathbb{R}^3 \rightarrow \mathbb{R}^3$ whose transformation matrix (with respect to the standard basis in $\mathbb{R}^3$) is
> $$A_\Phi=\begin{bmatrix}1&1&0 \newline 1&-1&0 \newline 1&1&1\end{bmatrix}$$
> **a)** Determine $ker(\Phi)$ and $Im(\Phi)$
> **b)** Determine the transformation matrix $A_\Phi$ with respect to the basis
> $$B=(\begin{bmatrix} 1 \newline 1 \newline 1 \end{bmatrix}, \begin{bmatrix} 1 \newline 2 \newline 1 \end{bmatrix}, \begin{bmatrix} 1 \newline 0 \newline 0 \end{bmatrix})$$
> i.e., perform a **basis change** toward the new basis $B$.

**a)**
- To determine $ker(\Phi)$ (the null space), we must solve x when $A_\Phi x=0$
If we row reduce we get : $\begin{bmatrix}1&1&0 \newline 0&-2&0 \newline 0&0&1\end{bmatrix}$ so the null space is a point $x=\begin{bmatrix}2 \newline -2 \newline 1 \end{bmatrix}$ ==FALSE: kernel should be empty has $A$ is full rank ...==
- $Im(\Phi)$ of the linear mapping $\Phi$ (or range) is the subspace spanned by the column vector : $span[\begin{bmatrix}1 \newline 0 \newline 0 \end{bmatrix}, \begin{bmatrix} 1 \newline -2 \newline 0 \end{bmatrix}, \begin{bmatrix}0 \newline 0 \newline 1 \end{bmatrix}]$ (rank 3 / full rank)

**b)** To perform a basis change (linear mapping $\Phi : V\rightarrow W$) from the original standard basis to $B$
- $\tilde{A_\Phi}=T^{-1}A_\Phi S$ (both T and S are regular)
- see also matrix equivalence ?

$\tilde{A_\Phi}=IA_\phi \begin{bmatrix} 1 & 1 & 1 \newline 1 & 2 & 0 \newline 1 & 1 & 0 \end{bmatrix}=\begin{bmatrix} 2 & 3 & 1 \newline 0 & -1 & 1 \newline 3 & 4 & 1 \end{bmatrix}$

==FALSE ?== It's not $I$ but $B^\intercal$ that we need ?

---
#### Exercice 2.20
> Let us consider $b_1, b_2, b_1^\prime, b_2^\prime$, 4 vectors of $\mathbb{R}^2$ expressed in the standard basis of $\mathbb{R}^2$ as
> $$b_1=\begin{bmatrix} 2 \newline 1 \end{bmatrix}, b_2=\begin{bmatrix} -1 \newline -1 \end{bmatrix}, b_1^\prime=\begin{bmatrix} 2 \newline -2 \end{bmatrix}, b_2^\prime=\begin{bmatrix} 1 \newline 1 \end{bmatrix}$$
> and let us define two ordered bases $B=(b_1, b_2)$ and $B^\prime=(b_1^\prime, b_2^\prime)$ of $\mathbb{R}^2$.
> **a)** Show that $B$ and $B^\prime$ are two bases of $\mathbb{R}^2$ and draw those basis vectors.
> **b)** Compute the matrix $P_1$ that performs a basis change from $B^\prime$ to $B$
> **c)** We consider $c_1, c_2, c_3$, there vectors of $\mathbb{R}^3$ defined in the standard basis of $\mathbb{R}^3$ as
> $$c_1=\begin{bmatrix} 1 \newline 2 \newline -1 \end{bmatrix}, c_2=\begin{bmatrix} 0 \newline -1 \newline 2 \end{bmatrix}, c_3=\begin{bmatrix} 1 \newline 0 \newline -1\end{bmatrix}$$
> and we define $C=(c_1, c_2, c_3)$.
> 	**(i)** Show that $C$ is a basis of $\mathbb{R}^3$, e.g., by using determinants (see Section 4.1).
> 	**(ii)** Let us call $C^\prime=(c_1^\prime, c_2^\prime, c_3^\prime)$ the standard basis of $\mathbb{R}^3$. Determine the matrix $P_2$ that performs the basis change from $C$ to $C^\prime$.
> **d)** We consider a homomorphism $\Phi : \mathbb{R}^2\rightarrow\mathbb{R}^3$, such that
> $$\Phi(b_1+b_2)=c_2+c_3$$
> $$\Phi(b_1-b_2)=2c_1-c_2+3c_3$$
> where $B=(b_1, b_2)$ and $C=(c_1, c_2, c_3)$ are ordered basis of $\mathbb{R}^2$ and $\mathbb{R}^3$, respectively.
> Determine the transformation matrix $A_\Phi$ of $\Phi$ with respect to the ordered bases $B$ and $C$.
> **e)** Determine $A^\prime$, the transformation matrix of $\Phi$ with respect to the ordered bases $B$ and $C^\prime$.
> **f)** Let us consider the vector $x\in\mathbb{R}^2$ whose coordinates in $B^\prime$ are $\begin{bmatrix}2 & 3\end{bmatrix}^\intercal$. In other words, $x=2b_1^\prime+3b_2^\prime$.
> 	**(i)** Calculate the coordinates of $x$ in $B$.
> 	**(ii)** Based on that, compute the coordinates of $\Phi(x)$ expressed in $C$.
> 	**(iii)** Then, write $\Phi(x)$ in terms of $c_1^\prime, c_2^\prime, c_3^\prime$.
> 	**(iv)** Use the representation of $x$ in $B^\prime$ and the matrix $A^\prime$ to find this result directly.

==TODO==
