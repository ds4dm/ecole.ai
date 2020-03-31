---
layout: page
title: About
---
## MILPs

The problems in discrete optimization are everywhere around us.
It appears in the form of deciding which route to follow to get to the destination (Shortest Path Problem), fitting luggage in the trunk of the car (Bin Packing Problem), or planning a multi-city trip to name a few.
Even when we are not the ones to handle them, we regularly interact with them indirectly.
For example, a "prime" customer from Amazon will have a direct impact on the package deliver route (Traveling Salesman Problem), or our shopping preference influences the items that a nearby supermarket stocks up.
Zooming out from our daily life, such problems arise naturally in many areas like computational biology, policy planning, supply chain management etc.
Thus, the organizations and researchers in these field rely on solving them on daily basis.

Most widely solved discrete optimization problems are linear in nature i.e. with linear objective function and linear constraints.
Even with such seemingly trivial conditions, discrete nature of decision variables make them non-convex, and therefore, NP-Complete.
This is in contrast to the continuous optimization problems where the continuity of decision variables enables a polynomial time search for the solution.
It must be mentioned that there are discrete problems like shortest path which lands themselves to polynomial time algorithms owing to the very nature of the problem.
For the discrete problems that are proven to be NP-Complete, there are two broad lines of research.
First, the design of approximation algorithms that uses domain specific knowledge for a smarter search for the solution with certain guarantees.
Second, the design of decisions in exact branch-and-bound (B&B) framework, which is implicitly a brute force search mechanism.

## Branch and Bound framework

The B&B framework proceeds by iteratively splitting the feasible region into two and evaluating the bounds of the new feasible regions.
Thus, one can easily note that there are two major decisions needed to be taken broadly - (i) how to split the region (ii) In which order to evaluate the regions.
Besides these major decisions, there are numerous other decisions that are taken which determines the search.
Given enough time, the framework is guaranteed to return an exact optimal solution with full certainty.
As is the nature of all NP-Complete problems, this means infinite amount of time.
Therefore, MILP researchers study these decisions in detail to learn their properties and enable faster search in B&B frameworks.
The commercially available solvers like Gurobi, SCIP, Cplex, etc. implement B&B with various decisions that have been well studied over the past 50 years.
For example, there are several branching strategies well studied in the field that decides how to split the region.

## Use of Machine Learning in branch and bound
Various decisions in B&B framework have been traditionally designed manually with expert knowledge, and the patter recognition techniques have enabled richer and complex modeling of these decisions.
For example, Khalil et al. learns a branching decision with the help of SVMs in an online fashion.
Gasse et al. uses GCNN to predict a good quality branching variable with higher accuracy.
more examples ...


## Need for reproducibility
Various designs are evaluated on a **class of problems** with respect to **metrics** like number of iterations, runtime, etc.
However, reproducibility has bee a major hinderance in OR research because of the multiple sources of randomness in the solver and machine learning component.
In addition to the source of randomness from within the solver, the methods are not exactly comparable with commercial solvers because of the highly optimized libraries and incomparable platforms. 
With the increasing number of publications in the field, it will only get more problematic to provide a fair comparison to the relevant methods.


## Platform école

### Features -
1. SCIP integration
2. Easy to install
3. Easy to use
4. Easy to customize
