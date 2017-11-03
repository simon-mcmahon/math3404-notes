TO DO:
Go through and sketch the curves in le



OPTIMAL control:
minimization or maximizatino of a functional subject to DE constraints

state space = space of the variables and solutions
control space = space of the "controls"

Control problem. Given a DE (*) control a system from an initial state to final state (using time free).
If possible system = controllable

Is possible we find the optimal control by minimizing the functional
J = integral of the cost function for x and u 

state qeuations equal to the ith derivative of the state variables x_i dot = f_i

a neessary condition similiar to EL is needed.
Pontryagin Maximum principle.
assuming piecwise smooth and bounded control functions.
Define the hamiltonian as the linear combination of phi functions and state equation functions

where the time derivatives of phi equal the ith state variable derivative of the hamiltonian

PMP is that such  vector of time dependent phi functions exists with the hamiltonian such that:
H = max when u = u* 
H ( phi*, x*, u*) = 0 , phi_0 <= 0 at t = t1 where phi* is the solution when u = u*.

H =0 and phi_0 <= 0 at each point on maximum trajectory.

Solving optimal control problems:

write out the state equations in terms of the DE condition which has been given (in terms of u).
construct the hamiltonian and the costate equations for phi
chosse phi_0 = -1. Find the values of the other phi values.
Take partial derivative of u wrt H and find values of u which maximize H (using 2nd deriv test).
this yields optimal control

Use the values from the end conditions to see if there are contradictions with the predicted end time (check for trivial cases).
Then we can find the cost value through direct substitution and integration.

Time optimal control to the origin:
construct the cost functional J as the integral of the function f_0 = 1 from t0 to t1 so the result is the change in time.

The solving of time optimal control for bounded magnitude of u gives u* = +- (K/m) (sign dependent on that of phi2). 
with a phi2 vector which is linear and can only switch values once.

The family of solution cuves can then be found by intregrating to find the state variables with respect to each other from the state equtaions.
The values of phi can then be correlated with regions on the plot and behaviour of the control can be determined.
*e.g. u = -K/m while on or above POQ*.
the switching curve the curve where phi2 = 0

In order to find the minimum time, define the switching time as eta. solve for this switching time from x_2 and general switching value s. 
Then use the intersections with the switching curve parabola to relate x1 and x2 and then find s. then get eta from there.

We can use this intersection method as a quicker alternative than finding the values of A, B and t1 which keep H = 0 for all t.

Example 3 glucose:

same steps as the last problem but when through examination of the switching function it was found that no switches could occur which 
restricted the number of cases to 2 possibilities.

Example 4 (fixed endpoint conditions):
when the end time is fixed, we do not need H=0 and end-points, the end-point coditions are enough. C not equal to 0 is a possibility.

construct hamiltonian (phi0 = -1) , derive H wrt u and find u maximum conditions. in terms of costate variables.
use the costate equations to relate state variables to optimal controls.
use end point conditions to find A and B constants. we are done.
MUCH SIMPLER.

Presentation of general solution of a linear optimal control problem:

A  = state equation matrix
l = control matrix
xdot = derivative of coordinate.
J = time optimal control
abs(u ) <= 1

phase plane analysis:
solution of xdot = A x is the linear combination of the eigenvectors to multiplied by the exponential of the eigenvalue

if eigenvalue:
real negaive (STABLE)
real positive (UNSTABLE)
real opposite (SADDLE POINT)

costate equations are phi dot = -A^T * phi
u = sgn ( l phi1 + m phi2)

controls pieceise cts as switching at zeros of S  = lphi1(t) + m phi2(t) 

BETWEEN TWO CONSECUTIVE ZEROS OF S, u* is CONSTANT.
so we can find the equilibrium points where xdot = 0. ( id detA neq 0)

now using our linear algebra, we can solve the costate equations by finding the eigenvalues and vectors of -A^T.
hence, we can also find the switching function 

if A has real eigenvalues, -A^T does as well.

IF EIGENVALUES OF A ARE REAL,  the switching function has at most one zero. (so maximum one switch occurs).

PMP IS BOTH NECESSARY AND SUFFICIENT FOR LINEAR TIME OPTIMAL CONTROL PROBLEMS.

Example 1: (stable node real eigenvalues).
find f0, f1, f2 from the DEs. write the hamiltonian. find the costate equations in matrix form. 
find the eigenvalues and eigenvectors of A and solve the general system using the method of undetermined coefficients for both u* = 1 and u* = -1.
Draw in the phase portrait for each case. Consider a starting point w and determine which curves actually go the desired end point (origin).

prune the family of C+ and C- curves to only the ones which go through the origin (if they are ridden after a switch).

does not appear to be any "region of controlability".

Solving systems of differential equations using the matrix exponential 

firstly, find diagonalize A by finding its eigenvalues then use e^tA = P e^tD P^(-1). and then you can solve the IVP using the formula
given in these notes here:
https://math.berkeley.edu/~conway/Teaching/old/summer2016-2552bc/exercises/NonhomoSys.pdf
The diagonal matrix is the eigenvalues of the matrix A along the leading diagonal.
The exponential of this matrix is the exponential of these eigenvalues down the diagonal.
 
using the method of undetermined coefficients, we can solve the system xdot = Ax + (l;m)*u (by using the method of undetermined coefficinets.
Note that because, in a linear optimal control system the u value is either +-1, we can use a constant undetermined coefficient and 
the satisfactory equations works out to be (for the particular solution) solving where system of linear equations is equal to its equilibirum point.

Hence, we are able to solve the homogenous case in general for these simple problems and then add on the equilibrium point (xdot =0)
at the end for each case u* = 1 and u* = 0.


http://tutorial.math.lamar.edu/Classes/DE/NonhomogeneousSystems.aspx

Example 2: (unstable node real eigenvalues)
region of controlability is the area of the starting point in which the origin is acutally reached. The region of controlability expands as the 
maximum magnitude of the value of the control force increases.

Example 3: (saddle point node)
region of controlability is an infinite strip, outside of which the control is impossible.

TRICK:
IN ORDER TO INSPECT THE GRADIENT OF THE PHASE PORTRAIT, use dx2/dx1 = x2dot /x1dot ( which can be found from the state equations).

Example 4: (determinant equal to 0).
no simgularity at origin but for all of x2. Hamiltonian construction and costate equation formation still apply although 
matrix methods cannot be used as singular.

COMPLEX EIGENVALUES:
Key differences:
With real eigenvalues we dont really need to find the switching function as there is at most one zero (switching point).

with complex eigenvalues, the system must be solved for phi to understand when the zeros occur as there can be any number of switches.
H is still piecewise continuous.

Example 1:
eigenvalues +- i. instead of linear comb of sine and cosine, represented as a sine with a constant offset to make the zero finding easier.
u*=1 and u*=-1 cases solved by recombining the x system into a 2nd order linear ode and quoting solution.
Other methods such as the method of undetermined coefficients can be used as well.

phase plane is a set of circles centre at (1,0) and (-1, 0) for u* = 1 , -1 respecitvely.
the result of the switching curve implies switches are regular occurances, pi apart in time. a semicircle is swept out in this time.

The final optimal control looks like a series of circles with progressively smaller radii 
The optimal control is som


