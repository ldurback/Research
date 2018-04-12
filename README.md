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

# Inverses and exponents of null elements are defined formally

For a finite number of dimension, there are only a finite number of unit null vectors in the geometric algebra.  Therefore, we can formally add inverses without it leading to a general unsolvability of the theory.

# Casting elements as real vectors and back

By adding new basis elements, we can cast every element as a complex vector.

Example: The element <img src="https://latex.codecogs.com/svg.latex?\inline&space;1&plus;2\hat{x}&plus;2i\hat{x}\hat{y}" title="1+2\hat{x}+2i\hat{x}\hat{y}" /> can be cast to a vector as <img src="https://latex.codecogs.com/svg.latex?\inline&space;\hat{1}&plus;2\hat{x}&plus;2i\widehat{xy}" title="\hat{1}+2\hat{x}+2i\widehat{xy}" />

Except for null vectors, all vectors have inverses and exponents in the complex geometric algebra.

At the end of all calculations, we want to cast everything to the complex geometric algebra without these new basis elements.  This lets us talk about elements as if they had inverses and exponents.



---

# Putting it together

Choose <img src="https://latex.codecogs.com/svg.latex?\inline&space;dx&space;\propto&space;[-\vec{f}&space;\vec{f}^{-(n)}]^{\frac{1}{n}}" title="dx \propto [-\vec{f} \vec{f}^{-(n)}]^{\frac{1}{n}}" />

Then <img src="https://latex.codecogs.com/svg.latex?\inline&space;d^n&space;f&space;=&space;dx^n&space;f^{(n)}&space;\propto&space;-\vec{f}&space;\vec{f}^{-(n)}f^{(n)}" title="d^n f = dx^n f^{(n)} \propto -\vec{f} \vec{f}^{-(n)}f^{(n)}" />

---

# Coding

Given the general form of a polynomial, I should be able to code up Newton's Method and prove that this all works.  Use general expression trees or an interative approach (with autodifferentiation) to building functions.  In the interative approach, polynomials are any functions that do not involve division of x or loops that depend on the value of x
