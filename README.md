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
