# Unified Geometric Algebra

The unified geometric algebra is the algebraic closure of the complex geometric algebra.  By adding algebraic closure, we sacrifice the associativity of the algebra.

# Guide for making the Unified Geometric Algebra algebraically closed

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

# Magnitude of Inverse

<img src="https://latex.codecogs.com/svg.latex?|a^{-1}|&space;=&space;|a|^{-1}" title="|a^{-1}| = |a|^{-1}" />

---

# Interpretation

Find interpretation of <img src="https://latex.codecogs.com/svg.latex?x&space;x^{-1}&space;=&space;1" title="x x^{-1} = 1" />

Create new vectors <img src="https://latex.codecogs.com/svg.latex?\inline&space;\widehat{1}" title="\widehat{1}" /> and <img src="https://latex.codecogs.com/svg.latex?\inline&space;\widehat{i}" title="\widehat{i}" /> that correspond to 1 and i as vectors.

Given the number 1 is a special direction that commutes with everything and i is a hidden dimension that commutes with everything, all elements of the unified geometric algebra correspond to vectors.

---

# 1-hat, i-hat, and xy-hat

1-hat and i-hat are special vectors that can be converted to scalars whenever they are on the very left side of a multiplication and no further calculations will be done with them.

<img src="https://latex.codecogs.com/svg.latex?\inline&space;\widehat{1}a&space;=&space;a,&space;\:&space;a\widehat{1}&space;\neq&space;a" title="\widehat{1}a = a, \: a\widehat{1} \neq a" />

<img src="https://latex.codecogs.com/svg.latex?\inline&space;\widehat{i}a&space;=&space;ia,&space;\:&space;a\widehat{i}&space;\neq&space;ai" title="\widehat{i}a = ia, \: a\widehat{i} \neq ai" />

With the addition of these elements, <img src="https://latex.codecogs.com/svg.latex?\inline&space;(a&plus;b\hat{x})^{-1}&space;=&space;(a\hat{1}&plus;b\hat{x})^{-1}=\frac{(a\hat{1}&plus;b\hat{x})}{|a\hat{1}&plus;b\hat{x}|}=\frac{a\hat{1}&plus;b\hat{x}}{\sqrt{a^2&plus;b^2}}" title="(a+b\hat{x})^{-1} = (a\hat{1}+b\hat{x})^{-1}=\frac{(a\hat{1}+b\hat{x})}{|a\hat{1}+b\hat{x}|}=\frac{a\hat{1}+b\hat{x}}{\sqrt{a^2+b^2}}" />

So now scalars + vectors have inverses.

What if we assign a vector to each blade and make every geometric element equivalent to a vector?

<img src="https://latex.codecogs.com/svg.latex?\inline&space;\widehat&space;{\hat{x}\hat{y}}a&space;\to&space;\hat{x}\hat{y}a" title="\widehat {\hat{x}\hat{y}}a \to \hat{x}\hat{y}a" />

Now every element has inverses.

# Real Exponents

If x = e^y for some y (if x has a logarithm), then x^r = e^ry.  e^x does exist for all x, so we just need logarithms to exist for all elements.

For bivectors, <img src="https://latex.codecogs.com/svg.latex?\inline&space;\hat{x}\hat{y}&space;=&space;e^{\frac{\pi}{2}\hat{x}\hat{y}}" title="\hat{x}\hat{y} = e^{\frac{\pi}{2}\hat{x}\hat{y}}" />

In general, we can take the logarithm of any real scalar + bivector.  Therefore, if we use our new unit vectors to convert x to a sum of a real scalar + a bivector, we can take its logarithm and therefore, we can exponentiate it to arbitrary real values.

---

# Coding

Given the general form of a polynomial, I should be able to code up Newton's Method and prove that this all works.  Use general expression trees or an interative approach (with autodifferentiation) to building functions.  In the interative approach, polynomials are any functions that do not involve division of x or loops that depend on the value of x
