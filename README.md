This acts as a host to the models created for my MSci project on modelling metabolism in microbial communities.

The first model solves a linear programming problem at every time step. 
It is very inefficient, but it is more likely to be accurate since it is very simple.

The second model implements the more advanced algorithm. 
In this model, we only change the bounds on our variables, but we check primal feasibility at each time step instead of solving the linear system.
This is significantly more efficient and can be checked by comparing results with the simple model

The third model extends the second model by allowing us to change the coefficients in the objective function.
To do this, we also need to check dual feasibility at each time step.
