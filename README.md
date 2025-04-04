This acts as a host to the models created for my MSci project on modelling metabolism in microbial communities.

The first model solves a linear programming problem at every time step. 
This is known as the direct method and is very simple to implement but has numerical instabilities.

The second model implements the Harwood et. al algorithm in a simple way, using discrete integration. 
In this model, we only change the bounds on our variables, but we check primal feasibility at each time step instead of solving the linear system.
This still has numerical instabilities since we are not taking advantage of the rootfinding function capabilities of continuous integration.

The third model extends the Harwood et. al algorithm by allowing us to change the coefficients in the objective function.
To do this, we also need to check dual feasibility at each time step, but again we still have numerical instabilities.

The fourth model is the same as the second model, but it applies sundials to integrate continuously instead of using runge-kutta discretely.

The fifth model is the same as the third model, but integrates continuously.

The examples folder holds the specific examples shown in the paper.
Direct Toy Models 1, 2 and 3 show the direct method applied to the toy models 1, 2 and 3 respectively.
Harwood Toy Model 1 shows the Harwood et. al method applied to the first toy model.
Extension Toy Models 2 and 3 show the extended algortihm applied to the second and third toy models.
