# Factoring Polynomials with an Extended Complex Geometric Algebra

The geometric algebra can be extended so that it is algebraically closed (in the sense that every polynomial can be written in a form that makes the minima of the polynomial, and their locations, obvious).  By adding algebraic closure, we sacrifice a few properties. 

# Motivation

By having a higher dimensional algebra where every polynomial can be factored and we can solve any high dimensional linear pde.  Additionally, we can construct programming languages that have multi-variable auto-differentiation built in.

# Guide for making the Geometric Algebra algebraically closed

Assume that we have a smooth function f such that we can define differentials dx that satisfy for all x

<img src="https://latex.codecogs.com/svg.latex?f(x&plus;dx)&space;=&space;\sum_i&space;\frac{d^i&space;f}{i!}&space;(x)" title="f(x+dx) = \sum_i \frac{d^i f}{i!} (x)" />

where <img src="https://latex.codecogs.com/svg.latex?d^n&space;f" title="d^n f" /> is strictly an nth order polynomial in dx.  The above then simplifies to (for some n such that n is non-null)

<img src="https://latex.codecogs.com/svg.latex?f(x&plus;dx)&space;=&space;f(x)&space;&plus;&space;\frac{d^n&space;f}{n!}(x)" title="f(x+dx) = f(x) + \frac{d^n f}{n!}(x)" />

Note, f is polynomial if and only if n has a maximum, which is the order of the polynomial.

We will call any points x such that d^i f(x) is null for all i "null points" of f.  Note: For f polynomial, for any null points to exist, we need that <img src="https://latex.codecogs.com/svg.latex?\inline&space;f^{(m)}" title="f^{(m)}" /> is null (and constant) for m equal to the order of f.

As long as we can always choose dx such that <img src="https://latex.codecogs.com/svg.latex?\widehat{d^n&space;f}&space;=&space;-&space;\widehat{f}" title="\widehat{d^n f} = - \widehat{f}" />, then f has a root if it is polynomial.

If we assume that dx commutes with all elements (that is, there are infinitesimals so small that they're parallel to all elements).  Then

<img src="https://latex.codecogs.com/svg.latex?d^n&space;f&space;=&space;dx^n&space;f^{(n)}&space;=&space;f^{(n)}&space;dx^n" title="d^n f = dx^n f^{(n)} = f^{(n)} dx^n" />

Therefore, our task is to construct the algebra so that such a dx always exists.

---

# If we encounter a null point

We get null points iff <img src="https://latex.codecogs.com/svg.latex?\inline&space;p^{(m)}" title="p^{(m)}" /> is null.  Let <img src="https://latex.codecogs.com/svg.latex?\inline&space;n&space;:=&space;p^{(m)}" title="n := p^{(m)}" />

In that case, p(x) has no linear factorization.

---

# Blade-Vectors, Extended Blades, and the Extended Geometric Algebra

For every basis blade of the complex geometric algebra, we add a new vector element called a basic blade-vector.  We can then multiply the basic blade vectors together to create basic extended blades.  We can then repeat this process indefinitely to create the full set of blade-vectors and extended blades.  I will call the resulting geometric algebra the Extended Geometric Algebra.

Some examples of blade-vectors: <img src="https://latex.codecogs.com/svg.latex?\inline&space;\hat{1},&space;\:&space;\widehat{\hat{x}\hat{y}},&space;\:&space;\widehat{\hat{1}\widehat{\hat{x}\hat{y}}}" title="\hat{1}, \: \widehat{\hat{x}\hat{y}}, \: \widehat{\hat{1}\widehat{\hat{x}\hat{y}}}" />

An example of an extended blade: <img src="https://latex.codecogs.com/svg.latex?\inline&space;\hat{1}\widehat{(\hat{x}\hat{y})}\widehat{(\hat{1}\widehat{(\hat{x}\hat{y})})}" title="\hat{1}\widehat{(\hat{x}\hat{y})}\widehat{(\hat{1}\widehat{(\hat{x}\hat{y})})}" />

We will call the original blades of the geometric algebra the "simple blades".

# Vector Conversion

The vector conversion refers to the process of converting any element of the extended geometric algebra to a vector.

Simply convert every blade of the element to a blade-vector.

We will write the vector conversion of x as <img src="https://latex.codecogs.com/svg.latex?\inline&space;\vec{x}" title="\vec{x}" />

By definition of vector conversion, we have <img src="https://latex.codecogs.com/svg.latex?\overrightarrow{\vec{a}b}&space;=&space;\overrightarrow{ab}" title="\overrightarrow{\vec{a}b} = \overrightarrow{ab}" />

# Down Conversion

The down conversion refers to the process of converting any element of the extended geometric algebra to an element of the original geometric algebra.

Simply convert every extended blade of the element to a simple blade.

We will write the down converion of x as <img src="https://latex.codecogs.com/svg.latex?\inline&space;\underline{x}" title="\underline{x}" />

By definition of down conversion, we have <img src="https://latex.codecogs.com/svg.latex?\inline&space;\underline{\underline{a}b}&space;=&space;\underline{ab}" title="\underline{\underline{a}b} = \underline{ab}" />

# The Unified Geometric Algebra as the Extended Geometric Algebra Modulo the Down Conversion

Modulo the down conversion, all elements are equivalent to their vector conversion.  Every complex vector has arbitrary exponents (including an inverse) as do any products of 2 complex vectors.

By construction, we have <img src="https://latex.codecogs.com/svg.latex?\vec{a}b&space;\equiv&space;ab" title="\vec{a}b \equiv ab" />

and more generally <img src="https://latex.codecogs.com/svg.latex?a&space;\equiv&space;b&space;\implies&space;ac&space;\equiv&space;bc" title="a \equiv b \implies ac \equiv bc" />  I.e. we can substitute value on the left of a multiplication but not, in general, values on the right.

By the above statement, if we pick  <img src="https://latex.codecogs.com/svg.latex?dx&space;\propto&space;[-\vec{f}^{-(n)}&space;\vec{f}]^{\frac{1}{n}}" title="dx \propto [-\vec{f}^{-(n)} \vec{f}]^{\frac{1}{n}}" />, then Newton's Method on the Unified Geometric Algebra follows because:

<img src="https://latex.codecogs.com/svg.latex?d^n&space;f&space;=&space;f^{(n)}&space;dx^n&space;\propto&space;-f^{(n)}&space;\vec{f}^{-(n)}&space;\vec{f}&space;\equiv&space;-\vec{f}^{(n)}&space;\vec{f}^{-(n)}&space;\vec{f}&space;=&space;-\vec{f}&space;\equiv&space;-f" title="d^n f = f^{(n)} dx^n \propto -f^{(n)} \vec{f}^{-(n)} \vec{f} \equiv -\vec{f}^{(n)} \vec{f}^{-(n)} \vec{f} = -\vec{f} \equiv -f" />

For the special case where c is simple, we can substitute on the right: <img src="https://latex.codecogs.com/svg.latex?a&space;\equiv&space;b&space;\implies&space;\underline{c}a&space;\equiv&space;\underline{c}b" title="a \equiv b \implies \underline{c}a \equiv \underline{c}b" />

---

# Coding

Given the general form of a polynomial, I should be able to code up Newton's Method and prove that this all works.  Use general expression trees or an interative approach (with autodifferentiation) to building functions.  In the interative approach, polynomials are any functions that do not involve division of x or loops that depend on the value of x

---

# Background Material

# Factoring Complex Polynomials

A polynomial is factored when it is written as a product of linear terms.  Over the complex numbers, every polynomial can be shown to be factorable using an analytic method known as Newton's Method, which shows the existence of 0s of the polynomial.  If <img src="https://latex.codecogs.com/svg.latex?\inline&space;p(x_r)&space;=&space;0" title="p(x_r) = 0" />, then we can always find another polynomial q such that for all x, <img src="https://latex.codecogs.com/svg.latex?\inline&space;p(x)&space;=&space;(x-x_r)q(x)" title="p(x) = (x-x_r)q(x)" />.  Since q is of lower order than p by 1, Newton's Method shows the existence of m linear factors for any polynomial of order m.

Newton's method relies on the expansion <img src="https://latex.codecogs.com/svg.latex?\inline&space;f(x&plus;dx)&space;=&space;\sum&space;\frac{1}{i!}d^n&space;f&space;=&space;\sum&space;\frac{1}{i!}f^{(i)}(x)dx^i" title="f(x+dx) = \sum \frac{1}{i!}d^n f = \sum \frac{1}{i!}f^{(i)}(x)dx^i" /> where <img src="https://latex.codecogs.com/gif.latex?f^{(i)}" title="f^{(i)}" /> is the ith derivative of f, and <img src="https://latex.codecogs.com/gif.latex?f^{(0)}&space;=&space;f" title="f^{(0)} = f" />.  Since dx is an infinitesmimal, we can neglect all terms higher than the first one encountered and get

<img src="https://latex.codecogs.com/svg.latex?\inline&space;f(x&plus;dx)&space;=&space;f(x)&space;&plus;&space;\frac{1}{n!}d^n&space;f&space;=&space;f(x)&space;&plus;&space;\frac{1}{n!}f^{(n)}(x)dx^n" title="f(x+dx) = f(x) + \frac{1}{n!}d^n f = f(x) + \frac{1}{n!}f^{(n)}(x)dx^n" />

Note, as long as p is a polynomial (with order greater than 1), this expansion is never trivial since we always have some a non-zero f^{(i)}(x) (derivative or higher derivative of f).

If we take the magnitude of the result, we get <img src="https://latex.codecogs.com/svg.latex?\inline&space;|f(x&plus;dx)|&space;=&space;|f(x)&space;&plus;&space;\frac{1}{n!}d^n&space;f|&space;=&space;|f(x)&space;&plus;&space;\frac{1}{n!}f^{(n)}(x)dx^n|" title="|f(x+dx)| = |f(x) + \frac{1}{n!}d^n f| = |f(x) + \frac{1}{n!}f^{(n)}(x)dx^n|" />.  We can always make |f(x+dx)| smaller than |f(x)| by choosing <img src="https://latex.codecogs.com/svg.latex?\inline&space;dx&space;\propto&space;[-\frac{f}{f^{(n)}}]^{\frac{1}{n}}" title="dx \propto [-\frac{f}{f^{(n)}}]^{\frac{1}{n}}" />

Since such a dx always exists, this implies that, given a value of x, there is always a direction dx that we can move in to make |f(x)| smaller.

Why does this imply the existence of a zero if f is a polynomial?

Using the symbol <img src="https://latex.codecogs.com/svg.latex?\inline&space;Nx" title="Nx" /> to mean an infinite value of x (just as dx is an infinitesimal) and noting that the mth derivative of p is a constant where m is the order of p:

<img src="https://latex.codecogs.com/gif.latex?p(Nx)&space;=&space;\frac{p^{(m)}}{m!}&space;(Nx)^m" title="p(Nx) = \frac{p^{(m)}}{m!} (Nx)^m" />.  Since p(Nx) is, in general, infinite, the minima of p have to be attained when x is in the interior of the complex plane.  Therefore, as we follow the direction dx given above, we'll stay in a bounded region.

