# Unified Geometric Algebra

The unified geometric algebra is the algebraic closure of the complex geometric algebra.  By adding algebraic closure, we sacrifice a few properties. 

# Guide for making the Geometric Algebra algebraically closed

Assume that we have a smooth function f such that we can define differentials dx that satisfy for all x

<img src="https://latex.codecogs.com/svg.latex?f(x&plus;dx)&space;=&space;\sum_i&space;\frac{d^i&space;f}{i!}&space;(x)" title="f(x+dx) = \sum_i \frac{d^i f}{i!} (x)" />

where <img src="https://latex.codecogs.com/svg.latex?d^n&space;f" title="d^n f" /> is strictly an nth order polynomial in dx.  The above then simplifies to (for some n)

<img src="https://latex.codecogs.com/svg.latex?f(x&plus;dx)&space;=&space;f(x)&space;&plus;&space;\frac{d^n&space;f}{n!}(x)" title="f(x+dx) = f(x) + \frac{d^n f}{n!}(x)" />

Note, f is polynomial if and only if n has a maximum, which is the order of the polynomial.

As long as we can always choose dx such that <img src="https://latex.codecogs.com/svg.latex?\widehat{d^n&space;f}&space;=&space;-&space;\widehat{f}" title="\widehat{d^n f} = - \widehat{f}" />, then f has a root if it is polynomial.

Therefore, our task is to construct the algebra so that such a dx always exists.

# Claim

If we add inverses and roots to the complex geometric algebra, all dx in the form of the above exists.

Assume that dx commutes with all elements (that is, there are infinitesimals so small that they're parallel to all elements).  Then

<img src="https://latex.codecogs.com/svg.latex?d^n&space;f&space;=&space;dx^n&space;f^{(n)}&space;=&space;f^{(n)}&space;dx^n" title="d^n f = dx^n f^{(n)} = f^{(n)} dx^n" />

and so picking dx such that <img src="https://latex.codecogs.com/svg.latex?f^{(n)}&space;dx^n&space;=&space;dx^n&space;f^{(n)}&space;\propto&space;-f" title="f^{(n)} dx^n = dx^n f^{(n)} \propto -f" /> sends Newton's Method in the correct direction

So we have at least two options for the direction of dx

<img src="https://latex.codecogs.com/svg.latex?dx&space;\propto&space;[-f&space;f^{-(n)}]^{\frac{1}{n}}" title="dx \propto [-f f^{-(n)}]^{\frac{1}{n}}" /> or <img src="https://latex.codecogs.com/svg.latex?dx&space;\propto&space;[-&space;f^{-(n)}&space;f]^{\frac{1}{n}}" title="dx \propto [- f^{-(n)} f]^{\frac{1}{n}}" />

---

# Non-Distributivity of Inverse

If the inverse distributed, then due to the existence of 0-divisors in the geometric algebra, we would have elements that would multiply together to get 0^{-1}.  Therefore, the inverse cannot distribute, and in general, sums and products of inverse elements cannot be simplified.

---

# Inverses and exponents of null elements can be defined formally

For a finite number of dimension, there are only a finite number of unit null vectors in the geometric algebra.  Therefore, we can formally add inverses without it leading to a general unsolvability of the theory.

---

# Blade-Vectors and Extended Blades

For every basis blade of the complex geometric algebra, we add a new vector element called a blade-vector.

Some examples:

1: <img src="https://latex.codecogs.com/svg.latex?\inline&space;\hat{1}" title="\hat{1}" />

<img src="https://latex.codecogs.com/svg.latex?\inline&space;\hat{x}\hat{y}" title="\hat{x}\hat{y}" />: <img src="https://latex.codecogs.com/svg.latex?\inline&space;\widehat{xy}" title="\widehat{xy}" />

We can then form extended blades from these blade-vectors: <img src="https://latex.codecogs.com/svg.latex?\inline&space;\hat{1}\widehat{xy}\hat{x}\hat{y}" title="\hat{1}\widehat{xy}\hat{x}\hat{y}" />

# Down Projection

Every extended blade can be down projected onto the complex geometric algebra.  Down projection forms an equivalency relation

<img src="https://latex.codecogs.com/svg.latex?\inline&space;\hat{1}\widehat{xy}\hat{x}\hat{y}&space;\equiv&space;\hat{x}\hat{y}\hat{x}\hat{y}&space;=&space;-1" title="\hat{1}\widehat{xy}\hat{x}\hat{y} \equiv \hat{x}\hat{y}\hat{x}\hat{y} = -1" />

# The Unified Geometric Algebra as a Modular Algebra

Modulo the down projection, all extended multivectors are equivalent to complex vectors, which have both inverses and arbitrary exponents as long as they are not null vectors.

Hypothesis: <img src="https://latex.codecogs.com/svg.latex?\inline&space;a&space;\equiv&space;b&space;\implies&space;a^{n&plus;1}&space;\equiv&space;a^n&space;b&space;\equiv&space;b&space;a^n" title="a \equiv b \implies a^{n+1} \equiv a^n b \equiv b a^n" />

This in particular would imply <img src="https://latex.codecogs.com/svg.latex?\inline&space;a&space;\equiv&space;b&space;\implies&space;1&space;\equiv&space;a^{-1}&space;b&space;\equiv&space;b&space;a^{-1}" title="a \equiv b \implies 1 \equiv a^{-1} b \equiv b a^{-1}" />, which is to say that if a and b are equivalent, then they share an inverse.


---

# Coding

Given the general form of a polynomial, I should be able to code up Newton's Method and prove that this all works.  Use general expression trees or an interative approach (with autodifferentiation) to building functions.  In the interative approach, polynomials are any functions that do not involve division of x or loops that depend on the value of x
