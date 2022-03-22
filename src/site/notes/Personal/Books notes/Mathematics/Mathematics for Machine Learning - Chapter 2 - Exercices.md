---
{"dg-publish":true,"dg-permalink":"Chapter 2 - Linear Algebra - Exercices","permalink":"/Chapter 2 - Linear Algebra - Exercices/"}
---

<-- [[Personal/Books notes/Mathematics/Mathematics for Machine Learning - Chapter 2 - Linear Algebra|Mathematics for Machine Learning - Chapter 2 - Linear Algebra]]

#### Exercice 2.1
> We consider $(\mathbb{R} \setminus \{-1\},\star)$, where
> $$a\star b:=ab+a+b, \quad\quad a, b \in \mathbb{R}\setminus\{-1\} \quad (2.134)$$
> **a)** Show that $(\mathbb{R} \setminus \{-1\},\star)$ is an Abelian group
> **b)** Solve
> $$3\star x\star x=15$$
> in the Abelian group $(\mathbb{R}\setminus\{-1\},\star)$, where $\star$ is defined in (2.134)

-> [[Topics/Mathematics/Group theory|Group theory]], [[___INBOX___/__à trier/Vector spaces|Vector spaces]], ...

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
> Let $n$ be in $\mathbb{N}\setminus\{0\}$. Let $k, x$ be in $\mathbb{Z}$. We define the congruence class $\overline{k}$ of the integer $k$ as the set
> $$\overline{k}=\{x \in \mathbb{Z}|x-k=0(\mod n)=\{x\in\mathbb{Z}|\exists a\in \mathbb{Z}: (x-k=n\cdot a)\}$$
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
#### Exercice 2.3
> Consider the set $\mathcal{G}$ of 3x3 matrices defined as follows:
> $\mathcal{G}=\{\begin{bmatrix} 1 & x & 2 \\\\ 0 & 1 & y \\\\ 0 & 0 & 1 \end{bmatrix} \in \mathbb{R}^{3\times 3} | x,y,z \in \mathbb{R}\}$
> We define $\cdot$ as the standard matrix multiplication.
> Is ($\mathcal{G},\cdot$) a group ? If yes, is it Abelian ? Justify your answer.

==TODO==

---
#### 2.4
> Compute the following matrix products, if possible :
> **a)** $\begin{bmatrix}1&2\\4&5\\7&8\end{bmatrix} \begin{bmatrix}1&1&0\\0&1&1\\1&0&1\end{bmatrix}$
> **b)** $\begin{bmatrix}1&2&3\\4&5&6\\7&8&9\end{bmatrix} \begin{bmatrix}1&1&0\\0&1&1\\1&0&1\end{bmatrix}$
> **c)** $\begin{bmatrix}1&1&0\\0&1&1\\1&0&1\end{bmatrix} \begin{bmatrix}1&2&3\\4&5&6\\7&8&9\end{bmatrix}$
> **d)** $\begin{bmatrix}1&2&1&2\\4&1&-1&-4\end{bmatrix} \begin{bmatrix}0&3\\1&-1\\2&1\\5&2\end{bmatrix}$
> **e)** $\begin{bmatrix}0&3\\1&-1\\2&1\\5&2\end{bmatrix} \begin{bmatrix}1&2&1&2\\4&1&-1&-4\end{bmatrix}$

**a)** impossible
**b)** $\begin{bmatrix}4&3&5\\10&9&11\\16&15&17\end{bmatrix}$
**c)** $\begin{bmatrix}5&7&9\\11&13&15\\8&10&12\end{bmatrix}$
**d)** $\begin{bmatrix}14&6\\-21&2\end{bmatrix}$
**e)** $\begin{bmatrix}12&3&-3&-12\\-3&1&2&6\\6&5&1&0\\13&12&3&2\end{bmatrix}$

---
#### Exercice 2.5
> Find the set $\mathcal{S}$ of all solutions in $x$ of the following inhomogeneous linear systems $Ax=b$, where $A$ and $b$ are defined as follows:
> **a)** 
> $$A=\begin{bmatrix}1&1&-1&-1\\2&5&-7&-5\\2&-1&1&3\\5&2&-4&2\end{bmatrix}, b=\begin{bmatrix}1\\-2\\4\\6\end{bmatrix}$$
> **b)** 
> $$A=\begin{bmatrix}1&-1&0&0&1\\1&1&0&-3&0\\2&-1&0&1&-1\\-1&2&0&-2&-1\end{bmatrix}, b=\begin{bmatrix}3\\6\\5\\-1\end{bmatrix}$$

**a)** ==TODO== (recopy)

**b)** $X=X_p+X_N=\begin{bmatrix}3\\0\\0\\-1\\0\end{bmatrix}+\begin{bmatrix}\beta\\2\beta\\\alpha\\\beta\\\beta\end{bmatrix}$

---
#### 2.6
> Using Gaussian elimination, find all solutions of the inhomogeneous equation system $Ax=b$ with
> $$A=\begin{bmatrix}0&1&0&0&1&0\\0&0&0&1&1&0\\0&1&0&0&0&1\end{bmatrix}, b=\begin{bmatrix}2\\-1\\1\end{bmatrix}$$

$X=\begin{bmatrix}0\\1\\0\\-2\\1\\0\end{bmatrix}+\begin{bmatrix}\alpha\\-\beta\\\gamma\\-\beta\\\beta\\\beta\end{bmatrix}$

---
#### Exercice 2.7
> Find all solutions in $x=\begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix} \in \mathbb{R}^3$ of the equation system $Ax=12x$,
> where
> $$A=\begin{bmatrix}6&4&3\\6&0&9\\0&8&0\end{bmatrix}$$
> and $\sum_{i=1}^3x_i=1$

We can rewrite it as an homogeneous system :
$(A-12I)x = 0$

Then put it in augmented form (with last line corresponding to the constraint on $x_i$ :
=> $\begin{bmatrix}-6&4&3&0\\6&-12&9&0\\0&8&-12&0\\1&1&1&1\end{bmatrix}$
We can put it in reduced row-echelon form, to obtain the identity matrix on the left, then :
we get $x=\begin{bmatrix}\frac{3}{8}\\\frac{3}{8}\\\frac{1}{4}\end{bmatrix}$

---
#### Exercice 2.8
> Determine the **inverses** of the following matrices if possible:
> **a)**
> $$A=\begin{bmatrix}2&3&4\\3&4&5\\4&5&6\end{bmatrix}$$
> **b)**
> $$A=\begin{bmatrix}1&0&1&0\\0&1&1&0\\1&1&0&1\\1&1&1&0\end{bmatrix}$$

**a)** impossible : no inverse (=singular matrix), because of linear dependence (see Chapter 2.5) it can be reduced and have some free variables : **invertible square matrix has no free variables**

**b)** Done by Gaussian elimination on an augmented matrix (with identity matrix on the right) until we get the identity matrix on the left. Solution :

$\begin{bmatrix} 1&0&0&0&0&-1&0&-1 \\ 0&1&0&0&-1&0&0&1 \\ 0&0&1&0&1&1&0&-1 \\ 0&0&0&1&1&1&1&-2 \end{bmatrix}$

---
> **Subspaces** -> https://www.quora.com/W-x_1-x_2-x_3-T-3x_1+-frac-1-4-x_2-0-Is-W-a-subspace-of-mathbb-R-3

#### Exercice 2.9
> Which of the following sets are **subspaces** of $\mathbb{R}^3$ ?
	- $A=\{(\lambda, \lambda+\mu^3, \lambda-\mu^3)|\lambda,\mu\in \mathbb{R}\}$
	- $B=\{(\lambda^2, -\lambda^2, 0)|\lambda \in \mathbb{R}\}$
	- **c)** Let $\gamma$ be in $\mathbb{R}$
		$C=\{(\xi_1, \xi_2, \xi_3)\in\mathbb{R}^3|\xi_1-2\xi_2+3\xi_3=\gamma\}$
	- $D=\{(\xi_1, \xi_2, \xi_3)\in\mathbb{R}^3|\xi_2\in\mathbb{Z}\}$

-> find if closure property (under vector addition, and scalar multiplication?), associativity null element (0,0,0), "inverse" element ?

==TODO==

---
#### 2.10
> Are the following sets of vectors **linearly independent** ?
> **a)**
> $$x_1=\begin{bmatrix}2\\-1\\3\end{bmatrix}, x_2=\begin{bmatrix}1\\1\\-2\end{bmatrix}, x_3=\begin{bmatrix}3\\-3\\8\end{bmatrix}$$
> **b)**
> $$x_1=\begin{bmatrix}1\\2\\1\\0\\0\end{bmatrix}, x_2=\begin{bmatrix}1\\1\\0\\1\\1\end{bmatrix}, x_3=\begin{bmatrix}1\\0\\0\\1\\1\end{bmatrix}$$

-> find if all pivot colums => independent

**a)** -> **Yes**, no free column
**b)** -> **Yes**, no free column

---
#### 2.11
> Write
> $$y=\begin{bmatrix}-1\\-2\\5\end{bmatrix}$$
> as linear combinaison of
> $$x_1=\begin{bmatrix}1\\1\\1\end{bmatrix}, x_2=\begin{bmatrix}1\\2\\3\end{bmatrix}, x_3=\begin{bmatrix}2\\-1\\1\end{bmatrix}$$

Put in augmented form : $[x_1 x_2 x_3|y]$, do Gaussian elimination until I get identity matrix...
=> $y=-6x_1+3x_2+2x_3$

---
#### Exercice 2.12
> Consider two subspaces of $\mathbb{R}^4$:
> $$U_1=span[\begin{bmatrix}1\\1\\-3\\1\end{bmatrix}, \begin{bmatrix}2\\-1\\0\\-1\end{bmatrix}, \begin{bmatrix}-1\\1\\-1\\1\end{bmatrix}], U_2=span[\begin{bmatrix}-1\\-2\\2\\1\end{bmatrix}, \begin{bmatrix}2\\-2\\0\\0\end{bmatrix}, \begin{bmatrix}-3\\6\\-2\\-1\end{bmatrix}]$$
> Determine the **basis** of $U_1\cap U_2$.

=> ==DONE==

---
#### Exercice 2.13
- find dimension of a (sub)space
- intersection of basis

==TODO==

---
#### Exercice 2.14
> Consider two subspaces $U_1$ and $U_2$, where $U_1$ is spanned by the columns of $A_1$ and $U_2$ is spanned by the columns of $A_2$ with
> $$A_1=\begin{bmatrix}1&0&1\\1&-2&-1\\2&1&3\\1&0&1\end{bmatrix}, A_2=\begin{bmatrix}3&-3&0\\1&2&3\\7&-5&2\\3&-1&2\end{bmatrix}$$
> **a)** Determine the dimension of $U_1, U_2$
> **b)** Determine bases of $U_1$ and $U_2$
> **c)** Determine a basis of $U_1\cap U_2$

==TODO==

**a)** The dimension of a subspace is the number of his basis vectors. To find the basis we must execute 3 steps
- Write the spanning vectors as columns of a matrix $A$ (already done for us)
- Determine the row-echelon form of $A$
- The spanning vectors associated with the pivot columns are a basis of $U$

$A_1=\begin{bmatrix}\cellcolor{lightgray} 1 & 0 & 1\\0 & \cellcolor{lightgray} 1 & 0\\ 0 & 0 & \cellcolor{lightgray} 1\\ 0 & 0 & 0 \end{bmatrix}$ => dimension : 3
$A_2=\begin{bmatrix}\cellcolor{lightgray} 1 & 2 & 3\\0 & \cellcolor{lightgray} 1 & 1\\0&0&0\\0&0&0\end{bmatrix}$ => dimension : 2

**c)** a basis of $U_1\cap U_2$ : $\begin{bmatrix}1&0\\0&1\\0&0\\0&0\end{bmatrix}$

---
#### Exercice 2.15
> Let $F=\{(x,y,z)\in \mathbb{R}^3|x+y-z=0\}$ and $G=\{(a-b, a+b, a-3b)|a,b\in\mathbb{R}\}$
> **a)** Show that $F$ and $G$ are subspaces of $\mathbb{R}^3$
> **b)** Calculate $F\cap G$ without resorting to any basis vector.
> **c)** Find one basis for $F$ and one for $G$, calculate $F\cap G$ using the basis vectors previously found and check your result with the previous question.

==TODO==

**a)** To be a subspace (of $\mathbb{R}^3$), it must : (-> see *Example 2.12*, page **39**)
- not be the empty set $\emptyset$, but it must contain $0$
- closure with respect to the **outer** and **inner** operation
	- $\forall \lambda \in \mathbb{R}, \exists x \in \mathcal{U} : \lambda x \in \mathcal{U}$
	- $\forall x,y \in \mathcal{U} : x + y \in \mathcal{U}$

==For $F$==, the subspace is not empty and contains $0$.
If we multiply an element by $\lambda$ we stay in the subspace because we get $\lambda x+\lambda y-\lambda z=0$ and the sum is also equals to $0$ (-> outer operation : ==OK==)
If we add $(x_1+x_2)+(y_1+y_2)-(z_1+z_2)=0$, we see that each 3 sums (in parenthesis) are still in $\mathbb{R}$ so -> inner operation : ==OK==
==> `F is a subspace`

==For $G$==, 



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
> $$\Phi:\mathbb{R}^3\rightarrow\mathbb{R}^2, \quad x\rightarrow\begin{bmatrix}1&2&3\\1&4&3\end{bmatrix}x$$
> **e)** Let $\theta$ be in $[0,2\pi]$ and
> $$\Phi:\mathbb{R}^2\rightarrow\mathbb{R}^2, \quad x\rightarrow\begin{bmatrix}\cos(\theta)&\sin(\theta)\\-\sin(\theta)&\cos(\theta)\end{bmatrix}x$$

==TODO==

---
#### Exercice 2.17
> Consider the linear mapping
> $$\Phi:\mathbb{R}^3\rightarrow\mathbb{R}^4, \Phi(\begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix})=\begin{bmatrix}3x_1+2x_2+x_3\\x_1+x_2+x_3\\x_1-3x_2\\2x_1+3x_2+x_3\end{bmatrix}$$
**a)** Find the transformation matrix $A_\Phi$
**b)** Determine $rk(A_\phi)$
**c)** Compute the kernel and image of $\Phi$. What are $dim(ker(\Phi))$ and $dim(Im(\Phi))$ ?

==TODO==

**a)** -> see ***definition 2.19 (Transformation matrix)***
$A_\Phi=\begin{bmatrix}3&1&1&2\\2&1&-3&3\\1&1&0&1\end{bmatrix}$

**b)** -> row reduced form -> count number of pivot columns
$rk(A_\Phi)=3$

$=dim(Im(A))$ ?

**c)** kernel = null space
(-> see ***Chap 2.7.3***)



---
#### Exercice 2.18
> Let $E$ be a vector space. Let $f$ and $g$ be two **automorphisms** on $E$ such that $f\circ g=id_E$ (i.e., $f\circ g$ is the identity matrix $id_E$). Show that $ker(f)=ker(g\circ f)$, $Im(g)=Im(g\circ f)$ and that $ker(f)\cap Im(g)=\{0_E\}$

==TODO==

---
#### Exercice 2.19
> Consider an endomorphism $\Phi : \mathbb{R}^3 \rightarrow \mathbb{R}^3$ whose transformation matrix (with respect to the standard basis in $\mathbb{R}^3$) is
> $$A_\Phi=\begin{bmatrix}1&1&0\\1&-1&0\\1&1&1\end{bmatrix}$$
> **a)** Determine $ker(\Phi)$ and $Im(\Phi)$
> **b)** Determine the transformation matrix $A_\Phi$ with respect to the basis
> $$B=$$
> i.e., perform a **basis change** toward the new basis $B$.

==TODO==

---
#### Exercice 2.20
- a. 
- b. 
- c. 
- d. 
- e. 
- f. 

==TODO==
