# MATH3404 Revision 1 (2013 draft)

## Optimization in R^n

NB: Theorems are all based off the Taylor expansion and frequently require the existance of derivatives and bounded derivatives.

Remember that the hessian is the n x n matrix of the second derivatives of the original function of the x_i and x_j variables.

**If the interval is closed, also remember to check the end points of the interval before concluding a minimum or maximum on that interval.**

### Useful theorems summary

If f on OPEN interval in R^n and has cts 2nd order derivatives. Sufficient condition for local min at x=a is:
grad(f(a)) = 0 and h^T * H(a) * h > 0 FOR ALL h in the set of R^n.

h^T * H(a) * h > 0 IF AND ONLY IF det(H) and det( all principle minors (the square matrix along the main diagonal)) is positive.

Also:  

For a local maximum on an open interval grad(f(a)) = 0 and h^T * H(a) * h < 0 FOR ALL h in the set of R^n.

The h^T * H(a) * h < 0 is only true if the principal minor determinants alternate in sign -, +, -, +,... beginning with d^2f/dx_1^2 = -ve.

## Lagrange multipliers

Given f(x) and conditions gj(x) we can minimize f(x) by:

constructing L = f + linear combination of lambda_i * g_j 
solve grad(L) = 0 
Define B = grad g = grad (g1, g2, g3, ... , gm) = which is a m*m matrix where each column is the grad of one function gi.
construct borderd hessian H = (H_L, B; B, 0) at x = a (solution of grad(L) = 0)
The output should be an (m+n) square matrix.
Evaluate (or implicitly show that) det(H) != 0. This implies that the critical points are non-degenerate.

Necessary and sufficient conditions to minimize f.  

if the critical point is non-degenerate.

Local min if h^T H_L h >= 0  
Local max if h^T H_L h <= 0  
**Sign convention here is the same as for the 2nd derivative test**  

**The definition of the h (tangent space vectors are that h^T grad(g_i) = 0) for i = 1, 2, ..., m)**   
**h = column vector and so h^T is a row vector**  

The hessisan matrix H_L is an (n x n) matrix if n is the number of dimensions of the function composed of the 2nd partial derivative of the
ith and jth components.

## Optimization of functions (Calculus of variations begin)

### Fixed end point problems

E-L equation is a necessary condition.  
![EL](/EL.PNG)

If the functional is independent of time then:  
![EL-time-indep](/EL-t-indep.PNG)

### Variable end point

Transversality condition is added into the mix.

![transversality](/transversality.PNG)

When the solution curve is a constant value (cdot = 0), this simplifies to:

![tranversality-cdot](/transversality-cdot-zero.PNG)

When the endpoint is truly free and so the derivative of c can tend towards infinity.

![tranversality-cdot-inf](/transversality-cdot-inf.PNG)


### Isoperimetric Problems
Definition: Minimize a functional J but subject to the constraint that another functional I is equal to a constant c.

For fixed endpoints, for an optimal curve x = x*(t) to exist, it must be an extremal of:  
**J[x] + lambda * I[x] = integral of (f + lambda g) from t0 to t1 **
where f and g were the cost functions of the functionals J and I respectively.

#### Example:
##### Strategy:
Use E-L equation on the functional f + lambda*g to find a necessary equation in terms of variables lambda, k and l.
Use the 2 endpoint conditions AND then use the contraint itself (integral g from t0 to t1) = c.
This allows enough conditional equations to find the values of the 3 variables.

### Hilbert invariant integral and local minimizers

### Field of extremals
A field of extremals is a family of curves (usually dependent on variables k and l) which is a simple cover of the plane such that
one and only one curve passes through each point. We define in this family, a slope field

 xdot = p(t,x)

There is a unique value of slope for each point in the plane. The slope function satisfies an equation similiar to the E-L equation.  

 ![EL-slope-funct](/EL-slope-funct.PNG)

### Weierstrass Sufficient Conditions
In order for the extremal x = x*(t) give a strong locla minimum to J[x] it is SUFFICIENT that:
C* is a member of a field of extremals.
E(t,x,xdot,p) >= 0 for all (t and x) close to C* and arbitrary values of xdot.

E(t,x,xdot,p) is the Weierstrass Excess function.
This is the integrand of the Delta J.  

p is the slope of the field of extremals at (t,x).  
xdot is the slope of C at (t,x).  

![delta-J](/delta-j.PNG)
![excess-funct](/excess-funct.PNG)


#### Strategy for finding the field of extremals.
**TODO:**


# Note to self:
The phase portraits in the back of the book are the answer you are looking for to help you sketch the phase planes.
Find the meaning of the lines in the conbined phase portrait. (Looks to be the nullcline lines going through both P and Q (equilibrium points for the costate equations for both cases of u*)).

## Eigenvalue outputs and the relevant phase portrait general shape

### Real stable

### Real Unstable

### Real Saddle

### Pure imaginary

### Complex??? (possible differentiated based on the positive and negative value of the real component).
