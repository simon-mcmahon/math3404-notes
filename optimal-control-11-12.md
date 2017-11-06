# Module 11

PMP for control to a target curve
same as the original PMP theorem (H = linear combination of phi and f_i)  
(phi dot is negative derivative of H wrt x_i)   
(H(phi*, x*, u*) = 0 and for all time if the final time unspecified).

The curve C which is being navigated to is C: G(x1,x2) = 0 at t = t1.

**Modification:**

The phi_i varioables are perpendicular to tangent at C at x*(t1). (Transversality condition).

**Corrollary:**

If the state at t1 for the x variables is completely unspecified. The modification becomes:
phi_i(t1) = 0

Transversality condition at Q (the equilibrium point when u* = -1) is:
a*phi1(t1) + b*phi2(t1) = 0 where (a,b) is tangent to G(x1,x2) = 0 at x = x*(t1).

**Also:**

If the problem is a single DE (only x1 dependent, with free endpoint x(t1) ), the condition is simply phi1(t1) = 0.

## Problems where cost dependent on x(t1):

In general, we redefine the cost function J = g(x^1) + integral of f0 from t0 to t1.
Note here that x^0 is the initial and x^1 is the final state function.

The general state equations are xdot = f(x,u) = ( f_1, f_2 , ... , f_m). This is a vector set of equations.

We then define the cost variable X_0 such that:

X_0(t0) = 0

and the sum of the linear combinations of the derivative of the arrival cost function (g) with xi and f_i from i=1 to m and add f_0.

The definition, with some work becomes that.
X_0(t1) = J - g(x(t0)). 

But we already know the value of x(t0) = x^0 as this is constant and so g(x(t0)) so minimizing J is an identical problem to minimizing X_0.

With that in mind we redefine the hamiltonian as the linear combination of phi and f_i equations but instead of f0, we replace it with X_0(dot).

MATH MATH MATH

In the end we write H' (not derivative, just a modified hamiltonian in terms of the pseudo-costate variables).
H' = -f0 + sum(lambda_j * f_j)
We then maximize H' as a function of u as before.

The definition of these pseudo costate variables (lambda_i) is :
lambda_i = phi_i - partial derivative of g wrt x_i.

**Transversality Condition:**
In this problem, if we still assume that the end is free x(t1) = x^1 independent

phi_i(t1) = 0  for i = 1, 2, ..., n
lambda_i (t1) = -1 * partial derivative of g wrt to x_i evaluated at t1 (for i = 1,2,...,n)

### Example 1:
#### Strategy:
write out H' from the state equations. derive H' wrt u. write out the pseudo costate equations 
solve d H'/du = 0 to find u* in terms of lambda. Integrate the pseudo costate equations to find lambda and sub into u* to find u* as a function of time.

Substitute back into state equation and integrate. Apply the x(t0) end point condition.
Apply the end point condition for t1 to solve for constants A and B (found in integrate of pseudo costate and state equations respectively).
(t1 value is also solveable but we do not need to find it).
Find the optimal values of u* and x. Finish.


# Module 12 (Quadratic Cost)

## Sumamry:

Goes through the formulation of a quadratic cost function optimal control function (linear state equtaion) problem formulation.
derives the PMP from the calculus of variations when u unconstrained.

Does optimal control through the lens of calculus of variations.

The tutorial sheet 10 has precisely 2 quadratic optimal control problems of similiar difficulty to the example given in module 11 and the two previous years practise exams do not feature them. It is unlikely this will be on the final in a large part.

