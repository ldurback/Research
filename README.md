# Geometric Algebra of Directions

While the geometric algebra begins with a basis of axes (t, x, y, z, etc.), the geometric algebra of directions begins with a basis of directions (past, future, up, down, left, right, forward, backward).

First, introduce 2 unit vectors for each axis: <img src="https://latex.codecogs.com/png.latex?\inline&space;\widehat{&plus;x_i}" title="\widehat{+x_i}" />, <img src="https://latex.codecogs.com/png.latex?\inline&space;\widehat{-x_i}" title="\widehat{-x_i}" />.

Both of these unit vectors have the same squared norm.  <img src="https://latex.codecogs.com/png.latex?\inline&space;\widehat{&plus;&space;x_i}^2&space;=&space;\widehat{-&space;x_i}^2&space;=&space;\widehat{x_i}^2&space;=&space;\pm&space;1" title="\widehat{+ x_i}^2 = \widehat{- x_i}^2 = \widehat{x_i}^2 = \pm 1" />

We will later define <img src="https://latex.codecogs.com/png.latex?\inline&space;\widehat{x_i}" title="\widehat{x_i}" /> so that this is true.

While <img src="https://latex.codecogs.com/png.latex?\inline&space;\widehat{&plus;x_i}" title="\widehat{+x_i}" /> and <img src="https://latex.codecogs.com/png.latex?\inline&space;\widehat{-x_i}" title="\widehat{-x_i}" /> do not commute or anti-communte, we can define the symmetric and anti-symmetric parts of their product.

<img src="https://latex.codecogs.com/png.latex?\inline&space;\widehat{&plus;x_i}&space;\cdot&space;\widehat{-x_i}&space;=&space;-\widehat{&plus;x_i}^2&space;=&space;-\widehat{-x_i}^2&space;=&space;-\widehat{x_i}^2" title="\widehat{+x_i} \cdot \widehat{-x_i} = -\widehat{+x_i}^2 = -\widehat{-x_i}^2 = -\widehat{x_i}^2" />

<img src="https://latex.codecogs.com/png.latex?\inline&space;(\widehat{&plus;x_i}&space;\wedge&space;\widehat{-x_i})^2&space;=&space;\pm&space;1" title="(\widehat{+x_i} \wedge \widehat{-x_i})^2 = \pm 1" />

The anti-symmetric product of <img src="https://latex.codecogs.com/png.latex?\inline&space;\widehat{&plus;x_i}" title="\widehat{+x_i}" /> and <img src="https://latex.codecogs.com/png.latex?\inline&space;\widehat{-x_i}" title="\widehat{-x_i}" /> is a unit bivector.

Then, for orthogonal axes, we have (<img src="https://latex.codecogs.com/png.latex?\inline&space;i&space;\neq&space;j" title="i \neq j" />) <img src="https://latex.codecogs.com/png.latex?\inline&space;\widehat{&plus;x_i}&space;\widehat{&plus;x_j}&space;=&space;\widehat{-x_j}&space;\widehat{&plus;x_i}&space;=&space;\widehat{-x_i}&space;\widehat{-x_j}&space;=&space;\widehat{&plus;x_j}&space;\widehat{-x_i}" title="\widehat{+x_i} \widehat{+x_j} = \widehat{-x_j} \widehat{+x_i} = \widehat{-x_i} \widehat{-x_j} = \widehat{+x_j} \widehat{-x_i}" />

# Geometric Algebra as a subset of the Geometric Algebra of Directions

Define <img src="https://latex.codecogs.com/png.latex?\inline&space;\widehat{x_i}&space;=&space;\frac{1}{2}&space;(\widehat{&plus;x_i}&space;-&space;\widehat{-x_i})" title="\widehat{x_i} = \frac{1}{2} (\widehat{+x_i} - \widehat{-x_i})" />

Then we have <img src="https://latex.codecogs.com/png.latex?\inline&space;\widehat{&plus;x_i}&space;\cdot&space;\widehat{x_i}&space;=&space;\widehat{&plus;x_i}&space;\cdot&space;\frac{1}{2}&space;(\widehat{&plus;x_i}&space;-&space;\widehat{-x_i})&space;=&space;\widehat{&plus;x_i}^2&space;=&space;\widehat{-x_i}^2" title="\widehat{+x_i} \cdot \widehat{x_i} = \widehat{+x_i} \cdot \frac{1}{2} (\widehat{+x_i} - \widehat{-x_i}) = \widehat{+x_i}^2 = \widehat{-x_i}^2" />

and <img src="https://latex.codecogs.com/png.latex?\inline&space;\widehat{-x_i}&space;\cdot&space;\widehat{x_i}&space;=&space;\widehat{-x_i}&space;\cdot&space;\frac{1}{2}&space;(\widehat{&plus;x_i}&space;-&space;\widehat{-x_i})&space;=&space;-\widehat{&plus;x_i}^2&space;=&space;-\widehat{-x_i}^2" title="\widehat{-x_i} \cdot \widehat{x_i} = \widehat{-x_i} \cdot \frac{1}{2} (\widehat{+x_i} - \widehat{-x_i}) = -\widehat{+x_i}^2 = -\widehat{-x_i}^2" />

so by this definition, <img src="https://latex.codecogs.com/png.latex?\inline&space;\widehat{x_i}^2&space;=&space;\widehat{&plus;x_i}^2&space;=&space;\widehat{-x_i}^2" title="\widehat{x_i}^2 = \widehat{+x_i}^2 = \widehat{-x_i}^2" />

For i != j, we have <img src="https://latex.codecogs.com/png.latex?\inline&space;\widehat{x_i}&space;\cdot&space;\widehat{x_j}&space;=&space;\frac{1}{4}&space;(\widehat{&plus;x_i}&space;-&space;\widehat{-x_i})&space;(\widehat{&plus;x_j}&space;-&space;\widehat{-x_j})&space;&plus;&space;\frac{1}{4}&space;(\widehat{&plus;x_j}&space;-&space;\widehat{-x_j})&space;(\widehat{&plus;x_i}&space;-&space;\widehat{-x_i})&space;=&space;0" title="\widehat{x_i} \cdot \widehat{x_j} = \frac{1}{4} (\widehat{+x_i} - \widehat{-x_i}) (\widehat{+x_j} - \widehat{-x_j}) + \frac{1}{4} (\widehat{+x_j} - \widehat{-x_j}) (\widehat{+x_i} - \widehat{-x_i}) = 0" />

