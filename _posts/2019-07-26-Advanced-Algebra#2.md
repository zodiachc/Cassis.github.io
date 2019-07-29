Notes on LINEAR ALGEBRA Jim Hefferon

# Linear equations and matrices

### Solving systems of linear equations

#### Gauss’s Method

$$
\begin{aligned} a_{1,1} x_{1}+a_{1,2} x_{2}+\cdots+a_{1, n} x_{n} &=d_{1} \\ a_{2,1} x_{1}+a_{2,2} x_{2}+\cdots+a_{2, n} x_{n} &=d_{2} \\ & \vdots \\ a_{m, 1} x_{1}+a_{m, 2} x_{2}+\cdots+a_{m, n} x_{n} &=d_{m} \end{aligned}
$$

In the system, the equations involve only the first power of each variable. This chapter shows how to solve any such system of equations.

> **Theorem** (Gauss’s Method): If a linear system is changed to another by one of these operations
>
> (1) an equation is <u>swapped</u> with another
>
> (2) an equation has both sides <u>multiplied</u> by a nonzero constant
>
> (3) an equation is replaced by the <u>sum</u> of itself and a multiple of another
>
> then the two systems have <u>the same set of solutions</u>.(同解)

The three operations from Theorem are the elementary reduction operations. They are swapping, multiplying by a scalar (or rescaling), and row combination.（初等行变换）

> **Definition** In each row of a system,the first variable with a nonzero coefficient is the row’s **leading variable**. A system is in **echelon form**（阶梯形） if each leading variable is to the right of the leading variable in the row above it, except for the leading variable in the first row, and any all-zero rows are at the bottom.

Gauss’s Method uses the row operations to set a system up for back substitution. If any step shows a contradictory equation then we can stop with the conclusion that the system <u>has no solutions</u>. If we reach echelon form without a contradictory equation, and each variable is a leading variable in its row, then the system has <u>a unique solution</u> and we find it by back substitution. Finally, if we reach echelon form without a contradictory equation, and at least one variable is not a leading variable, then the system has <u>many solutions</u>.

#### Describing the Solution Set

A linear system with a unique solution and with no solution  is easy to describe the solution set. Solution sets are a challenge to describe only when they contain many elements.

> **Definition**: In an echelon form linear system the variables that are not leading are **free**.

 we will solve linear systems by bringing them to echelon form and then parametrizing with the free variables.

> **Example**：
> $$
> \begin{aligned}x+y+z-w&=1 \\ y-z+w&=-1 \\ 3x+6 z-6 w&=6 \\ -y+z-w&=1\end{aligned}
> $$
> we can get 
> $$
> \begin{aligned} x+y+z-w &=1 \\ y-z+w &=-1 \\ 0 &=0 \\ 0 &=0 \end{aligned}
> $$
> $z, w$ free.
>
> The solution set
> $$
> \begin{equation*}
> \{(2-2 z+2 w,-1+z-w, z, w) \vert z, w \in \mathbb{R}\}
> \end{equation*}
> $$
>

We develope a streamlined notation for linear systems and their solution sets.

> **Definition**: An $m \times n$ **matrix** is a rectangular array of numbers with m rows and $n$ columns. Each number in the matrix is an **entry**. We denote the set of all $n \times m$ matrices by $\mathcal{M}_{n \times m}$ . 

We do Gauss’s Method using matrices in essentially the same way that we did it for systems of equations: a matrix row’s leading entry is its first nonzero entry (if it has one) and we perform row operations to arrive at matrix **echelon form**, where the leading entry in lower rows are to the right of those in the rows above. 

Matrix notation also clarifies the descriptions of solution sets.

> **Definition** A column vector, often just called a vector, is a matrix with a single column. A matrix with a single row is a row vector. The entries of a vector are sometimes called components. A column or row vector whose components are all zeros is a zero vector.

The style of description of solution sets that we use involves adding the vectors, and also multiplying them by real numbers. we can understand those operations geometrically.
>$$
>\begin{equation*}
>\{\left(\begin{array}{c}{2} \\ {-1} \\ {0} \\ {0}\end{array}\right)+\left(\begin{array}{c}{-2} \\ {1} \\ {1} \\ {0}\end{array}\right) \cdot z+\left(\begin{array}{c}{2} \\ {-1} \\ {0} \\ {1}\end{array}\right) \cdot w \left\vert z, w \in \mathbb{R}\right.\}
>\end{equation*}
>$$
>

So, here come two questions: 

+ can we always describe solution sets as above, with a particular solution vector added to an unrestricted linear combination of some other vectors? (see 1.1.4)
+ is it impossible to solve a problem one way to get y and w free and solve it another way to get y and z free?(see 1.1.3)

#### Reduced Echelon Form

> **Definition** A matrix or linear system is in **reduced echelon form** if, in addition to beint in echelon form, each leading entry is a 1 and is the only nonzero entry in its colum.

For different echelon forms, we can think of them as interrelated, where we can get from one to another by row operations. 

> **Lemma** Elementary row operations are reversible.

Again, the point of view that we are developing, supported now by the lemma, is that the term ‘reduces to’ is misleading: where A −→ B, we shouldn’t think of B as after A or simpler than A. Instead we should think of the two matrices as interrelated.

> **Lemma** Between matrices, ‘reduces to’ is an equivalence relation.(行相抵/等价)

> **Definition** Two matrices that are interreducible by elementary row operations are **row equivalent**.

Where one matrix reduces to another, each row of the second is a <u>linear combination of the rows</u> of the first.

We now have the insight that Gauss’s Method builds linear combinations of the rows. But of course its goal is to end in echelon form, since that is a particularly basic version of a linear system, as it has isolated the variables.

> **Lemma**: In an echelon form matrix, no nonzero row is a linear combination of the other nonzero rows.(各行向量线性无关)

> **Theorem** Each matrix is row equivalent to a unique reduced echelon form matrix.

> **Corollary** If from a starting linear systems we derive by Gauss’s Method two different echelon form systems, then the two have the same free variables.

In Gauss’s Method we start with a matrix and then derive a sequence of other matrices. We defined two matrices to be related if we can derive one from the other. That relation is an equivalence relation, called row equivalence, and so partitions the set of all matrices into row equivalence classes.

We have proved there is one and only one reduced echelon form matrix in each row equivalence class. So the reduced echelon form is a canonical form∗ for row equivalence: the reduced echelon form matrices are representatives of the classes.


#### General = Particular + Homogeneous

> **Theorem**: Any linear system's solution set has the form
> $$
> \begin{equation*}
> \left\{\vec{p}+c_{1} \vec{\beta}_{1}+\cdots+c_{k} \vec{\beta}_{k} \vert c_{1}, \ldots, c_{k} \in \mathbb{R}\right\}
> \end{equation*}
> $$
> where $\vec{p}$ is any particular solution and where the number of vectors $\vec{\beta}_{1}, \ldots,\vec{\beta}_{k}$ equals the number of free variables that the system has after a Gaussian reduction.

> **Definition** A linear equation is **homogeneous** if it has a constant of zero, so that it can be written as $a_{1} x_{1}+a_{2} x_{2}+\cdots+a_{n} x_{n}=0$ .

> **Lemma 1** For any homogeneous linear system there exist vectors $\vec{\beta}_{1}, \ldots, \vec{\beta}_{k}$ such that the solution set of the system is
> $$
> \left\{c_{1} \vec{\beta}_{1}+\cdots+c_{k} \vec{\beta}_{k} \vert c_{1}, \ldots, c_{k} \in \mathbb{R}\right\}
> $$
> where $k$ is the number of free variables in an echelon form version of the system.

This shows, as discussed between the lemma and its proof, that we can parametrize solution sets using the free variables. We say that the set of vectors $\left\{\mathrm{c}_{1} \vec{\beta}_{1}+\cdots+\mathrm{c}_{\mathrm{k}} \vec{\beta}_{\mathrm{k}} \vert \mathrm{c}_{1}, \ldots, \mathrm{c}_{\mathrm{k}} \in \mathbb{R}\right\}$ is **generated by or spanned by** the set $\left\{\vec{\beta}_{1}, \ldots, \vec{\beta}_{\mathrm{k}}\right\}$  

> **Lemma 2** For a linear system and for any particular solution $\vec{p},$ the solution set equals $\{\vec{p}+\overrightarrow{\mathrm{h}} \vert \overrightarrow{\mathrm{h}} \text { satisfies the associated homogeneous system }\} .$

> **Corollary** Solution sets of linear systems are either empty, have one element, or have infinitely many elements.

First observe a homogeneous system with at least one non- $\overrightarrow{0}$ solution $\vec{v}$ has infinitely many solutions. 

Now apply Lemma 2 to conclude that a solution set $\{\vec{p}+\overrightarrow{\mathrm{h}} \vert \overrightarrow{\mathrm{h}} \text { solves the associated homogeneous system }\}$  is either empty (if there is no particular solution $\vec{p} )$ , or has one element (if there is a $\vec{p}$ and the homogeneous system has the unique solution $\overrightarrow{0} ),$ or is infinite (if there is a $\vec{p}$ and the homogeneous system has a non- $\overrightarrow{0}$ solution, and thus by the prior paragraph has infinitely many solutions).

### Linear Geometry

#### Vectors in Space

An object in $\mathbb{R},$ or in any $\mathbb{R}^{n}$ , comprised of a magnitude and a direction is a **vector** (we use the same word as in the prior section because we shall show below how to describe such an object with a column vector).

A point can be describe by the vector. In $\mathbb{R}^2$, $\left\{\left(\begin{array}{l}{x_{1}} \\ {x_{2}}\end{array}\right) | x_{1}, x_{2} \in \mathbb{R}\right\}$ 

$r \cdot\left(\begin{array}{c}{v_{1}} \\ {v_{2}}\end{array}\right)=\left(\begin{array}{c}{r v_{1}} \\ {r v_{2}}\end{array}\right) \quad\left(\begin{array}{c}{v_{1}} \\ {v_{2}}\end{array}\right)+\left(\begin{array}{c}{w_{1}} \\ {w_{2}}\end{array}\right)=\left(\begin{array}{c}{v_{1}+w_{1}} \\ {v_{2}+w_{2}}\end{array}\right)$ we can now understand those operations geometrically.

> **Definition**: a set of the form $\left\{\vec{p}+t_{1} \vec{v}_{1}+t_{2} \vec{v}_{2}+\cdots+t_{k} \vec{v}_{k} | t_{1}, \ldots, t_{k} \in \mathbb{R}\right\}$
> where $\vec{v}_{1}, \ldots, \vec{v}_{k} \in \mathbb{R}^{n}$ and $k \leqslant n$ is a **$k$ -dimensional linear surface** (or *k-flat*).

When the dimension of the linear surface is one less than the dimension of the space, the surface is called a hyperplane.

We now can restate in geometric terms our conclusions from earlier. First, the solution set of a linear system with $n$ unknowns is a linear surface in $R^n$. Specifically, it is a $k$-dimensional <u>linear surface</u>, where k is the number of free variables in an echelon form version of the system. For instance, in the single equation case the solution set is an $n − 1$ -dimensional <u>hyperplane</u> in $R^n$, where $n \geqslant􏰸 1$. Second, the solution set of a homogeneous linear system is a linear surface passing through the origin. Finally, we can view the general solution set of any linear system as being the solution set of its associated homogeneous system offset from the origin by a vector, namely by any particular solution.

#### Length and Angle Measures

> **Definition**: The length of a vector $\vec{v} \in \mathbb{R}^{n}$ is the square root of the sum of the squares of its components.
> $$
> |\vec{v}|=\sqrt{v_{1}^{2}+\cdots+v_{n}^{2}}
> $$
>

Use Law of Cosin, we can get:

> **Definition**: The **dot product** (or inner product or scalar product) of two $n$-component real vectors is the linear combination of their components.
> $$
> \vec{u} \cdot \vec{v}=u_{1} v_{1}+u_{2} v_{2}+\cdots+u_{n} v_{n}
> $$
>

> **Theorem** (Cauchy-Schwarz Inequality) For any $\vec{u}, \vec{v} \in \mathbb{R}^{n}$
> $$
> |\overrightarrow{u} \cdot \vec{v}| \leqslant|\vec{u}||\vec{v}|
> $$
> with equality if and only if one vector is a scalar multiple of the other.

> **Theorem** (Triangle Inequality) For any $\vec{u}, \vec{v} \in \mathbb{R}^{n}$
> $$
> |\vec{u}+\vec{v}| \leqslant|\vec{u}|+|\vec{v}|
> $$
> with equality if and only if one of the vectors is a nonnegative scalar multiple of
> the other one.

> **Definition** The angle between two nonzero vectors $\vec{u}, \vec{v} \in \mathbb{R}^{n}$ is
> $$
> \theta=\arccos \left(\frac{\vec{u} \cdot \vec{v}}{|\vec{u}||\vec{v}|}\right)
> $$
>

> **Corollary** Vectors from $\mathbb{R}^{n}$ are orthogonal, that is, perpendicular, if and only if their dot product is zero. They are parallel if and only if their dot product equals the product of their lengths.



**总结：第一章学习线性系统，第一节提出用Gauss消元法化简方程到echelon form来判断有没有解，并用back substitution来求解。对于唯一解与无解时，比较容易处理。对多解时，对自由变量参数化来描述解集。之后我们引入了矩阵来化简过程，并用向量来表示解集(这是有几何意义在里面的，第二节)。接着我们证明了同一个线性方程组的每种阶梯形都有相同的自由向量；通解可以用特解加齐次解表示。1.1.3表示了矩阵的行等价类的代表元为Reduced echelon form，可以用Gauss-Jordan法来求 **。

# Vector spaces

The first chapter finished with a fair understanding of how Gauss’s Method solves a linear system. It systematically takes linear combinations of the rows. Here we move to a general study of linear combinations.

We want the results about linear combinations to apply anywhere that linear combinations make sense. We shall call any such set a vector space. Our results, instead of being phrased as “Whenever we have a collection in which we can sensibly take linear combinations . . . ”, will be stated “In any vector space . . . ”

### Definitions

> **Definition**  A set $\mathbb{F}$ with two binary operations $+$ and $\times$ is a **field** if both $(\mathbb{F},+, 0)$ and $(\mathbb{F} \backslash\{0\}, \times, 1)$ are abelian groups and the distribution law holds:
> $$
> \begin{equation*}
> (a+b) c=a c+b c, \text { for all } a, b, c \in \mathbb{F}
> \end{equation*}
> $$
>

> **Definition** A **vector space $V$** (over $\mathbb{F}$) is an *abelian group* $(V,+,0)$ together with a scalar multiplication F×V →V such that for all $a,b∈F,v,w∈V$ :
> $$
> \begin{equation*}
> \begin{array}{l}{\text { (1) } a(v+w)=a v+a w} \\ {\text { (2) }(a+b) v=a v+b v} \\ {\text { (3) }(a b) v=a(b v)} \\ {\text { (4) } 1 . v=v}\end{array}
> \end{equation*}
> $$
>

> **Definition** For any vector space, a subspace is a subset that is itself a vector space, under the inherited operations.

> **Lemma** For a nonempty subset S of a vector space, under the inherited operations the following are equivalent statements.
>
> (1) S is a subspace of that vector space
>
> (2) S is closed under linear combinations of pairs of vectors: for any vectors $\vec{s}_{1}, \vec{s}_{2} \in S$ and scalars $r_{1}, r_{2}$ the vector $r_{1} \vec{s}_{1}+r_{2} \vec{s}_{2}$ is in $S$
>
> (3) S is closed under linear combinations of any number of vectors: for any vectors $\vec{s}_{1}, \ldots, \vec{s}_{n} \in S$ and scalars $r_{1}, \ldots, r_{n}$ the vector $r_{1} \vec{s}_{1}+\cdots+r_{n} \vec{s}_{n}$ is an element of $S .$

Lemma suggests that a good way to think of a vector space is as a collection of unrestricted linear combinations.

> **Definition** The **span** (or linear closure) of a nonempty subset $S$ of a vector space is the set of all linear combinations of vectors from $S$.
>
> $[\mathrm{S}]=\left\{c_{1} \overrightarrow{\mathrm{s}}_{1}+\cdots+\mathrm{c}_{\mathrm{n}} \overrightarrow{\mathrm{s}}_{\mathrm{n}} \vert \mathrm{c}_{1}, \ldots, \mathrm{c}_{\mathrm{n}} \in \mathbb{R} \text { and } \vec{s}_{1}, \ldots, \overrightarrow{\mathrm{s}}_{\mathrm{n}} \in \mathrm{S}\right\}$
>
> The span of the empty subset of a vector space is its trivial subspace.

> **Lemma** In a vector space, the span of any subset is a subspace.

The converse of the lemma holds: any subspace is the span of some set, because a subspace is obviously the span of itself, the set of all of its members. Thus a subset of a vector space is a subspace if and only if it is a span. This fits the intuition that a good way to think of a vector space is as a collection in which linear combinations are sensible. (the span of a subset S of a vector space is the smallest subspace containing all of the members of S.)

### Linear Independence

The prior section shows how to understand a vector space as a span, as an unrestricted linear combination of some of its elements. In this section we will use the second sense of ‘minimal spanning set’.

> **Definition** In any vector space, a set of vectors is linearly independent if none of its elements is a linear combination of the others from the set. Otherwise the set is linearly dependent.

> **Lemma** A subset $S$ of a vector space is linearly independent if and only if among its elements the only linear relationship $c_{1} \vec{s}_{1}+\cdots+c_{n} \vec{s}_{n}=\overrightarrow{0}$ (with $\vec{s}_{i} \neq \vec{s}_{j}$ for all $i \neq j$ is the trivial one $c_{1}=0, \ldots, c_{n}=0$ .

### Basis and Dimension

>  **Definition** A basis for a vector space is a sequence of vectors that is linearly independent and that spans the space.

> **Definition** For any $\mathbb{R}^{n}$
> $$
> \varepsilon_{n}=\left\langle\left(\begin{array}{l}{1} \\ {0} \\ {\vdots} \\ {0}\end{array}\right),\left(\begin{array}{c}{0} \\ {1} \\ {\vdots} \\ {0}\end{array}\right), \ldots,\left(\begin{array}{c}{0} \\ {0} \\ {\vdots} \\ {1}\end{array}\right)\right\rangle
> $$
> is the standard (or natural) basis. 

> **Theorem** In any vector space, a subset is a basis if and only if each vector in the space can be expressed as a linear combination of elements of the subset in one and only one way. （唯一表示定理）

> **Definition** In a vector space with basis $\mathrm{B}$ the representation of $\vec{v}$ with respect to $\mathrm{B}$ is the column vector of the coefficients used to express $\vec{v}$ as a linear combination of the basis vectors:
> $$
> \operatorname{Rep}_{\mathrm{B}}(\vec{v})=\left(\begin{array}{c}{\mathrm{c}_{1}} \\ {\mathrm{c}_{2}} \\ {\vdots} \\ {c_{\mathrm{n}}}\end{array}\right)
> $$
> where $\mathrm{B}=\left\langle\vec{\beta}_{1}, \ldots, \vec{\beta}_{n}\right\rangle$ and $\vec{v}=c_{1} \vec{\beta}_{1}+c_{2} \vec{\beta}_{2}+\cdots+c_{n} \vec{\beta}_{n} .$ The $c^{\prime}$ 's are the coordinates of $\vec{v}$ with respect to B.

Remark Definition  requires that a basis be a sequence because without that we couldn’t write these coordinates in a fixed order.

The previous subsection defines a basis of a vector space and shows that a space can have many different bases. So we cannot talk about “the” basis for a vector space. 

We can however find something about the bases that is uniquely associated with the space. This subsection shows that any two bases for a space have the same number of elements. So with each space we can associate a number, the number of vectors in any of its bases.

>  **Definition** A vector space is finite-dimensional if it has a basis with only finitely many vectors.

> **Lemma** (Exchange Lemma) Assume that $B=\left\langle\vec{\beta}_{1}, \ldots, \vec{\beta}_{n}\right\rangle$ is a basis for a vector space, and that for the vector $\vec{v}$ the relationship $\vec{v}=c_{1} \vec{\beta}_{1}+c_{2} \vec{\beta}_{2}+\cdots+c_{n} \vec{\beta}_{n}$ has $c_{i} \neq 0 .$ Then exchanging $\vec{\beta}_{i}$ for $\vec{v}$ yields another basis for the space.

> **Theorem** In any finite-dimensional vector space, all bases have the same number of elements.

> **Definition** The dimension of a vector space is the number of vectors in any of its bases.



### Vector Spaces and Linear Systems

We will now reconsider linear systems and Gauss’s Method, aided by the tools and terms of this chapter (rank, linear independence, basis) . We will make three points.

+ For the first, recall the insight from the Chapter One that Gauss’s Method works by taking <u>linear combinations of rows</u> — if two matrices are related by row operations A −→ · · · −→ B then each row of B is a linear combination of the rows of A. Therefore, the right setting in which to study row operations in general, and Gauss’s Method in particular, is the following vector space.

> **Definition** The **row space** of a matrix is the span of the set of its rows. The **row rank** is the dimension of this space, the number of linearly independent rows.

> **Lemma 1**  If two matrices A and B are related by a row operation then their row spaces are equal. Hence, row-equivalent matrices have the same row space and therefore the same row rank.

Gauss’s Method performs the row operations systematically, with the goal of echelon form. so

> **Lemma 2** The nonzero rows of an echelon form matrix make up a linearly independent set.

Thus, in the language of this chapter, Gaussian reduction works by eliminating linear dependences among rows, leaving the span unchanged, until no nontrivial linear relationships remain among the nonzero rows. In short, **Gauss’s Method produces a basis for the row space**. (Thus, the first point for this subsection is that the tools of this chapter give us a more conceptual understanding of Gaussian reduction.)

+ For the second point observe that row operations on a matrix can change its column space. This observation makes next result surprising.

> **Lemma 3** Row operations do not change the column rank.

(row operations do not affect linear relationships among columns,)

By Lemma 1&3，we can have

> **Theorem** For any matrix, the row rank and column rank are equal.

So the second point that we have made in this subsection is that the column space and row space of a matrix have the same dimension.

+ Our final point is that the concepts that we’ve seen arising naturally in the study of vector spaces are exactly the ones that we have studied with linear systems.

> **Theorem** For linear systems with $n$ unknowns and with matrix of coefficients $A$, the statements
>
> (1) the rank of $A$ is $r$
>
> (2) the vector space of solutions of the associated homogeneous system has dimension $n − r$ are equivalent.

So if the system has at least one particular solution then for the set of solutions, the number of parameters equals n − r, the number of variables minus the rank of the matrix of coefficients.

# Linear transformations

### Isomorphisms

> **Definition** An isomorphism between two vector spaces $V$ and $W$ is a map $f: V \to W$ that
>
> (1) is a correspondence: $f$ is one-to-one and onto;
>
> (2) preserves structure:if $\vec{v}_{1}, \vec{v}_{2} \in \mathrm{V}$ then
> $$
> \quad f\left(\vec{v}_{1}+\vec{v}_{2}\right)=f\left(\vec{v}_{1}\right)+f\left(\vec{v}_{2}\right)
> $$
> and if $\vec{v} \in \mathrm{V}$ and $\mathrm{r} \in \mathbb{R}$ then
>
> $$
> f(r \vec{v})=rf(\vec{v})
> $$
> (we write $V \cong W,$ read "V is isomorphic to $W^{\prime \prime},$ when such a map exists).

> **Definition** An automorphism is an isomorphism of a space with itself.

When two (unequal) spaces are isomorphic we think of them as almost equal, as equivalent. We shall make that precise by proving that the relationship ‘is isomorphic to’ is an equivalence relation.

> **Theorem** Isomorphism is an equivalence relation between vector spaces.

The next result characterizes these classes by dimension. That is, we can describe each class simply by giving the number that is the dimension of all of the spaces in that class.

> **Lemma** If spaces are isomorphic then they have the same dimension.
>
> **Lemma** If spaces have the same dimension then they are isomorphic.

> **Theorem** Vector spaces are isomorphic if and only if they have the same dimension.

### Homomorphisms

> **Definition** A function between vector spaces h : $V → W$ that <u>preserves addition and scalar multiplication</u> is a **homomorphism** or **linear map**.

> **Lemma** The following are equivalent for any map $f: V → W$ between vector spaces.
>
> (1) $f$ is a homomorphism
>
> (2) $f\left(c_{1} \cdot \vec{v}_{1}+c_{2} \cdot \vec{v}_{2}\right)=c_{1} \cdot f\left(\vec{v}_{1}\right)+c_{2} \cdot f\left(\vec{v}_{2}\right)$ for any $c_{1}, c_{2} \in \mathbb{R}$ and $\vec{v}_{1}, \vec{v}_{2} \in V$ 
>
> (3) $f\left(c_{1} \cdot \vec{v}_{1}+\cdots+c_{n} \cdot \vec{v}_{n}\right)=c_{1} \cdot f\left(\vec{v}_{1}\right)+\cdots+c_{n} \cdot f\left(\vec{v}_{n}\right)$ for any $c_{1}, \ldots, c_{n} \in \mathbb{R}$ and $\vec{v}_{1}, \ldots, \vec{v}_{n} \in V$

For homomorphisms we have a weaker but still very useful result.(比起同构的维数相等)

> **Theorem** A homomorphism is determined by its action on a basis: if $V$ is a vector space with basis $\left\langle\vec{\beta}_{1}, \ldots, \vec{\beta}_{n}\right\rangle$,  $W$ is a vector space, and if $\vec{w}_{1}, \ldots, \vec{w}_{n} \in W$ (these codomain elements need not be distinct), then there exists a homomorphism from $\mathrm{V}$ to $W$ sending each $\vec{\beta}_{i}$ to $\vec{w}_{i},$ and that homomorphism is unique.(同态由一组基及其象决定)

> **Definition** Let $\text{Hom}(V,W)$ be the set of linear maps from $V$ to $W$. It’s a vector space over $\mathbb{F}$.

---

>  **Lemma** Under a homomorphism, the image of any subspace of the domain is a subspace of the codomain. In particular, the image of the entire space, the range of the homomorphism, is a subspace of the codomain.

> **Definition** The range space of a homomorphism $\mathcal{A}$: V → W is  $\mathcal{R}( \mathcal{A} ) = \{ \mathcal{A} ( \vec{v} ) | \vec{v} \in V \}$  
>
> sometimes denoted $\mathcal{A}(V)$. The dimension of the range space is **the map’s rank**.

The prior result shows that, in passing from the definition of isomorphism to the more general definition of homomorphism, omitting the onto requirement doesn’t make an essential difference. Any homomorphism is onto some space, namely its range.

However, omitting the one-to-one condition does make a difference. A homomorphism may have many elements of the domain that map to one element of the codomain.

> **Lemma** For any homomorphism the inverse image of a subspace of the range is a subspace of the domain. In particular, the inverse image of the trivial subspace of the range is a subspace of the domain.

> **Theorem** A linear map’s rank plus its nullity equals the dimension of its domain.

> **Corollary** The rank of a linear map is less than or equal to the dimension of the domain. Equality holds if and only if the nullity of the map is 0.

> **Lemma** Under a linear map, the image of a linearly dependent set is linearly dependent.

> **Theorem** Where $V$ is an n-dimensional vector space, these are equivalent statements about a linear map $\mathcal{A} : V \rightarrow W$ .
>
> (1) $\mathcal{A}$ is one-to-one
>
> (2) $\mathcal{A}$ has an inverse from its range to its domain that is a linear map
>
> (3) $N (\mathcal{A}) = \{0 \}$, that is, nullity($\mathcal{A}$) = 0
>
> (4) rank($\mathcal{A}$) = n
>
> (5) if $⟨\vec{\beta}_1,...,\vec{\beta}_n⟩$  is a basis for V then $⟨\mathcal{A}(\vec{\beta}_1),…,\mathcal{A}(\vec{\beta}_n)⟩$ is a basis for $\mathcal{A}(V)$  

### Computing Linear Maps

**The prior section shows that a linear map is determined by its action on a basis.** 

The equation
$$
\begin{equation*}
h(\vec{v})=h\left(c_{1} \cdot \vec{\beta}_{1}+\cdots+c_{n} \cdot \vec{\beta}_{n}\right)=c_{1} \cdot h\left(\vec{\beta}_{1}\right)+\cdots+c_{n} \cdot h\left(\vec{\beta}_{n}\right)
\end{equation*}
$$
describes how we get the value of the map on any vector $\vec{v}$ by starting from the value of the map on the vectors $\vec{\beta}_i$ in a basis and extending linearly.

#### Representing Linear Maps with Matrices

> **Definition** Suppose that $V$ and $W$ are vector spaces of dimensions $n$ and $m$ with bases $B=\left\langle\vec{\beta}_{1}, \ldots, \vec{\beta}_{n}\right\rangle$ and $B'=\left\langle\vec{\beta}_{1}', \ldots, \vec{\beta}_{m}'\right\rangle$ and that $\mathcal{A} : V \rightarrow W$ is a linear map. If 
> $$
> \begin{equation*}
> \operatorname{Rep}_{B'}\left(\mathcal{A}\left(\vec{\beta}_{1}\right)\right)=\left(\begin{array}{c}{a_{1,1}} \\ {a_{2,1}} \\ {\vdots} \\ {a_{m, 1}}\end{array}\right)_{D} \quad \ldots \quad \operatorname{Rep}_{B'}\left(\mathcal{A}\left(\vec{\beta}_{n}\right)\right)=\left(\begin{array}{c}{a_{1, n}} \\ {a_{2, n}} \\ {\vdots} \\ {a_{m, n}}\end{array}\right)_{D}
> \end{equation*}
> $$
> then 
> $$
> \begin{equation*}
> _{B'}[\mathcal{A}]_B=\left(\begin{array}{cccc}{a_{1,1}} & {a_{1,2}} & {\ldots} & {a_{1, n}} \\ {a_{2,1}} & {a_{2,2}} & {\ldots} & {a_{2, n}} \\ {} & {\vdots} & {} \\ {a_{m, 1}} & {a_{m, 2}} & {\ldots} & {a_{m, n}}\end{array}\right)_{B, \mathrm{D}}
> \end{equation*}
> $$
> is the matrix representation of $h$ with respect to $B, B'$.



> **Thoerem** Assume that $V$ and $W$ are vector spaces of dimensions $n$ and $m$ with bases $B$ and $D$, and that $\mathcal{A}: V → W$ is a linear map, and $\vec{v} \in V$ is represented by 
> $$
> \begin{equation*}
> \operatorname{Rep}_{B}(\vec{v})=\left(\begin{array}{c}{x_{1}} \\ {x_{2}} \\ {\vdots} \\ {x_{n}}\end{array}\right)_{B}
> \end{equation*}
> $$
> then the representation of the image of $\vec{v}$ is this.
> $$
> \begin{equation}
> \operatorname{Rep}_{B'}(\mathcal{A}(\vec{v}))=A \cdot \operatorname{Rep}_{\mathrm{B}}(\vec{v})
> \end{equation}
> $$
>

we can interpret $\mathcal{A}$ as left multiplication by A.

#### Any Matrix Represents a Linear Map

The prior subsection shows that the action of a linear map $\mathcal{A}$ is described by a matrix $A$, with respect to appropriate bases, in this way.
$$
\begin{equation*}
\vec{v}=\left(\begin{array}{c}{x_{1}} \\ {\vdots} \\ {x_{n}}\end{array}\right)_{\mathrm{B}} \quad \xrightarrow{\mathcal{A}}\quad \mathrm{h}(\vec{v})=\left(A\cdot\left(\begin{array}{c}{x_1} \\ {\vdots} \\ {x_n}\end{array}\right)\right)_{\mathrm{B'}}
\end{equation*}
$$
Here we will show the converse, that each matrix represents a linear map.

> **Theorem** Any matrix represents a homomorphism between vector spaces of appropriate dimensions, with respect to any pair of bases. （$A_{m\times n} $  则n维映到m维） 

Given a matrix, to come up with an associated map we can choose among many domain and codomain spaces, and many bases for those. So a matrix can represent many maps. We finish this section by illustrating how the matrix can give us information about the associated maps.

> **Theorem** The rank of a matrix equals the rank of any map that it represents.

> **Corollary** Let $\mathcal{A}$ be a linear map represented by a matrix $A$. Then $\mathcal{A}$ is onto if and only if the rank of $A$ equals the number of its rows, and h is one-to-one if and only if the rank of $A$ equals the number of its columns.

> **Definition** A linear map that is one-to-one and onto is nonsingular , otherwise it is singular. That is, a linear map is nonsingular if and only if it is an isomorphism.

> **Lemma** A nonsingular linear map is represented by a square matrix. A square matrix represents nonsingular maps if and only if it is a nonsingular matrix. Thus, a matrix represents isomorphisms if and only if it is square and nonsingular.

We’ve now seen that the relationship between maps and matrices goes both ways: <u>for a particular pair of bases, any linear map is represented by a matrix and any matrix describes a linear map</u>. That is, by fixing spaces and bases we get a correspondence between maps and matrices. In the rest of this chapter we will explore this correspondence. For instance, we’ve defined for linear maps the operations of addition and scalar multiplication and we shall see what the corresponding matrix operations are. We shall also see the matrix operation that represent the map operation of composition. And, we shall see how to find the matrix that represents a map’s inverse.

### Matrix  Operations

The prior section shows how matrices represent linear maps. We now explore how this representation interacts with things that we already know.

Set $_{B'}[\mathcal{A}]_B=A$ , we have:
$$
\mathcal{A}(\beta_1, \ldots, \beta_n)=(\beta_1', \ldots, \beta_n')A
$$
Note that $_{B'}[a \mathcal{A}]_{B}=a\left(_{B'}[\mathcal{A}]_{B}\right)$ and $_{B^{\prime}}[\mathcal{A}+\mathcal{B}]_B=_{B^{\prime}}[\mathcal{A}]_B+_{B'}[\mathcal{B}]_B$ 

Furthermore, if $\mathcal{C} \in \operatorname{Hom}(W, U)$ for some finite dimensional vector space $U$ with basis $B^{\prime \prime},$ then:
$$
_{B^{\prime \prime}}[\mathcal{C} \circ \mathcal{A}]_{B}=_{B^{\prime \prime}}[\mathcal{C}]_{B^{\prime} B^{\prime}}[\mathcal{A}]_{B}
$$

>  **Lemma** The composition of linear maps is linear.
>
> **Theorem**  The assignment $\mathcal{A} \mapsto_{B'}[\mathcal{A}]_{B}$ is an **isomorphism** of vector spaces from $\text{Hom}(V,W)$
> to the space of $(m \times n)$ -matrices over $\mathbb{F}$ . It takes composition of maps to multiplication of matrices.

（Hom $(V, W)$ 与矩阵环同构） 

> **Theorem** If F, G, and H are matrices, and the matrix products are defined, then the product is associative (FG)H = F(GH) and distributes over matrix addition F(G + H) = FG + FH and (G + H)F = GF + HF.

We finish this subsection by applying these observations to get matrices that perform Gauss’s Method and Gauss-Jordan reduction. We have already seen how to produce a matrix that rescales rows, and a row swapper.

>  **Definition** The elementary reduction matrices (or just elementary matri- ces) result from applying a single Gaussian operation to an identity matrix.
>
> $(1) I \stackrel{\mathrm{k} \rho_{\mathfrak{j}}}{\longrightarrow} \mathrm{M}_{\mathfrak{i}}(\mathrm{k})$ for $\mathrm{k} \neq 0$ 
>
>  $ (2) I \stackrel{\rho_{\mathfrak{i}} \leftrightarrow \rho_{\mathfrak{j}}}{\longrightarrow} \quad \mathrm{P}_{\mathfrak{i}, \mathfrak{j}}$ for $\mathfrak{i} \neq \mathfrak{j}$  
>
> $(3) I \stackrel{k \rho_{i}+\rho_{j}}{\longrightarrow} \quad C_{i, j}(k)$ for $i \neq j$

> **Lemma** Matrix multiplication can do Gaussian reduction. 

> **Corollary** For any matrix $H$ there are elementary reduction matrices $R_1,..., R_r$ such that $R_r ·R_{r−1} ···R_1 ·H$ is in reduced echelon form.

Until now we have taken the point of view that our primary objects of study are v<u>ector spaces and the maps between them</u>, and we seemed to have adopted matrices only for computational convenience. This subsection show that this isn’t the entire story.

Understanding matrix operations by understanding the mechanics of how the entries combine is also useful. In the rest of this book we shall continue to focus on maps as the primary objects but we will be pragmatic—if the matrix point of view gives some clearer idea then we will go with it.

---

We finish this section by considering how to represent the inverse of a linear map.

# Inner product spaces

# 