# the-Skamania-Hiker-s-GPS

The Skamania II GPS’s off-trail pathfinding feature needs to find the most hiker-friendly trail for an arbitrary terrain. The terrain is represented as a 3D surface discretized into uniformly spaced tiles. The hiker can move with chessboard motion across the XY plane of this surface with the “cost” per step being defined by the change in height for each step:
cost(h0, h1) = eh1-h0 = eΔh
Where h0 is the height of the current title and h1 is the height of the tile to be moved to. The cost surface can be visualized with the following surface:
The total path cost is defined as the sum of all of the individual step costs.
We are hoping to implement the A* algorithm for this task, but our team lacks the expertise to code this and design admissible heuristics to ensure that the optimal path is found. As such, the project has the following components:

Step 1 Designing Admissible Heuristics

Assuming the cost function for chess movement (all eight neighbors), create an admissible
heuristic, define it as a mathematical equation, and prove/show it is admissible. 

Step 2 Implement The A* Algorithm
a) You will now implement your own version of A*. We have provided you with a sample agent to demonstrate the inheritance process and show you how paths should be returned.
b) Implement your heuristic into code.

Step 3 Initial Testing 
We have prepared a series of randomly generated 500x500 test maps to ensure that your code is working properly. In your report, please record your output for seeds 1-5 (inclusive), and make sure the path cost is the same as the optimal path cost we have already calculated for you.
Seed 1 - 241.55253710831192 Seed 2 - 238.5060683830129 Seed 3 - 236.667690049357 Seed 4 - 422.01798243905006 Seed 5 - 254.34464507852198
Note that while failing to meet these costs would demonstrate a problem with your code, meeting these costs does not necessarily mean the heuristics are admissible - perhaps there is an issue with your heuristic which did not arise in testing. Since this project assumes many floating-point calculations, your results for this part of the assignment can be within a margin of 0.3.
Use the following command to run this part of the assignment: "python Main.py -AI a -seed x" with “a” being the appropriate AI module, and “x” being the seeds listed above.
Submission Requirements: For each execution record the cost of the shortest path and the number of nodes expanded as per the output of the program.

Step 4 Climbing Mt. St. Helens - A-Star Variants
As part of our coming demonstration, we will have a hiker use the Skamania II to climb to the top of Mt. St. Helens, located here in Skamania County. It is crucial that during this demonstration, hikers can get the optimal route quickly, so we want you to modify your A-Star approach from above to use an A-Star variant of your choosing. As long as you can demonstrate that this variant poses some benefit (eg more memory efficiency, faster) compared to the vanilla A* algorithm you implemented previously, that’s fine. You are free to use any variant you chose, and recommend the following resource. The optimal path cost for this route is [find].

Step 5 Presentation
