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

# Note

In the complex geometric algebra, all elements have arbitrary exponents

# Claim

If we add formal inverses to the complex geometric algebra, all dx in the form of the above exists.

Assume that dx commutes with all elements (that is, there are infinitesimals so small that they're parallel to all elements).  Then

<img src="https://latex.codecogs.com/svg.latex?d^n&space;f&space;=&space;dx^n&space;f^{(n)}" title="d^n f = dx^n f^{(n)}" />

and so picking <img src="https://latex.codecogs.com/svg.latex?\widehat{dx}&space;\propto&space;(-f&space;f^{-(n)})^{\frac{1}{n}}" title="\widehat{dx} \propto (-f f^{-(n)})^{\frac{1}{n}}" /> sends Newton's Method in the correct direction

This exists because all elements have inverses and arbitrary exponents.

---

# Recursive Form

A geometric element is in recursive form when it is written <img src="https://latex.codecogs.com/svg.latex?x&space;=&space;R(x)" title="x = R(x)" />  We will call R(x) the recurse of x.

Note: A recurse does not uniquely specify an element.  However, if every polynomial recurse specifies at least one element, then R - x has a root at that value.

(What about the edge cases where R - x = a non-zero constant?  In that case, x is an infinite number.  Use non-standard analysis)

A recursive form is also a stable point of the mapping <img src="https://latex.codecogs.com/svg.latex?x&space;\to&space;R(x)" title="x \to R(x)" />

---

# Non-Distributivity of Inverse

If the inverse distributed, then due to the existence of 0-divisors in the geometric algebra, we would have elements that would multiply together to get 0^{-1}.  Therefore, the inverse cannot distribute, and in general, sums and products of inverse elements cannot be simplified.

---

# Interpretation

Find interpretation of <img src="https://latex.codecogs.com/svg.latex?x&space;x^{-1}&space;=&space;1" title="x x^{-1} = 1" />

Given the number 1 as being a special direction that commutes with everything and i is a hidden dimension that commutes with everything. 

---

# Coding

Given the general form of a polynomial, I should be able to code up Newton's Method and prove that this all works.  Use general expression trees or an interative approach (autodifferentiation) to building functions

```
f(x) {
  blah blah blah;
  
  return blah;
}
```
```
df/dx(x) {
  let d = new infinitesimal; // d^2 = 0
  return f(x + d).d_part;
}
```
```
d^2f/dx^2(x) {
  let e = new infinitesimal; // e^2 = 0
  return df/dx(x + e).e_part;
}
```

Example:
```
f(x, a, b, c) { // returns (ax+b)^2 + c
  x <- a*x;
  x <- x + b;
  x <- x*x;
  x <- x + c;
  
  return x;
}
```

Then stepping through f''(x, a, b, c), gives us
```
   x <- a*(x + d + e) = a*x + a*d + a*e
   x <- a*x + a*d + a*e + b = a*x + b + a*d + a*e
   x <- (a*x + b + a*d + a*e)*(a*x + b + a*d + a*e)
        = (a*x+b)*(a*x+b) + a*d*(a*x+b+a*e) + a*e*(a*x+b+a*d)
        = (a*x+b)*(a*x+b) + a*(a*x+b+2a*e)*d + a*(a*x+b)*e 
   x <- (a*x+b)*(a*x+b)+c + a*(a*x+b+2a*e)*d + a*(a*x+b)*e
   
   return a*(a*x+b+2a*e)
   return 2a*a
```
