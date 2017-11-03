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








