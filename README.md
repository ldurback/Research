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

# The Unified Geometric Algebra as the Extended Geometric Algebra Modulo the Down Conversion

Modulo the down conversion, all elements are equivalent to their vector conversion.  Every non-null complex vector has arbitrary exponents (including an inverse) as do any products of 2 non-null complex vectors.

By construction, we have <img src="https://latex.codecogs.com/svg.latex?\vec{a}b&space;\equiv&space;ab" title="\vec{a}b \equiv ab" />

and more generally <img src="https://latex.codecogs.com/svg.latex?a&space;\equiv&space;b&space;\implies&space;ac&space;\equiv&space;bc" title="a \equiv b \implies ac \equiv bc" />  I.e. we can substitute value on the left of a multiplication but not, in general, values on the right.

By the above statement, if we pick  <img src="https://latex.codecogs.com/svg.latex?dx&space;\propto&space;[-\vec{f}^{-(n)}&space;\vec{f}]^{\frac{1}{n}}" title="dx \propto [-\vec{f}^{-(n)} \vec{f}]^{\frac{1}{n}}" />, then Newton's Method on the Unified Geometric Algebra follows because:

<img src="https://latex.codecogs.com/svg.latex?d^n&space;f&space;=&space;f^{(n)}&space;dx^n&space;\propto&space;-f^{(n)}&space;\vec{f}^{-(n)}&space;\vec{f}&space;\equiv&space;-\vec{f}^{(n)}&space;\vec{f}^{-(n)}&space;\vec{f}&space;=&space;-\vec{f}&space;\equiv&space;-f" title="d^n f = f^{(n)} dx^n \propto -f^{(n)} \vec{f}^{-(n)} \vec{f} \equiv -\vec{f}^{(n)} \vec{f}^{-(n)} \vec{f} = -\vec{f} \equiv -f" />

For the special case where c is simple, we can substitute on the right: <img src="https://latex.codecogs.com/svg.latex?a&space;\equiv&space;b&space;\implies&space;\underline{c}a&space;\equiv&space;\underline{c}b" title="a \equiv b \implies \underline{c}a \equiv \underline{c}b" />

---

# Coding

Given the general form of a polynomial, I should be able to code up Newton's Method and prove that this all works.  Use general expression trees or an interative approach (with autodifferentiation) to building functions.  In the interative approach, polynomials are any functions that do not involve division of x or loops that depend on the value of x
