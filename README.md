# Traffic Simulation
## General
The paper examines the behavior and the traffic flow of 1-lane and 2-lane traffic models. The traffic on the single-lane roads being simulated is represented by a one dimension cellular automaton with a periodic boundary. For the double-lane roads, we use two one dimensional cellular automata, with the same velocity update rules as the single-lane but with an additional update rule for the lane change.
## Update rules
### General assumptions
All the cars move and stop simultaneously
All the car drivers follow the traffic rules
If there is a change in the lane of a car, it updates its velocity according to the situation in the new lane
### Velocity update rules
(1) Acceleration: If the empty space ahead is greater than the current velocity, and the current velocity is smaller than the maximum velocity, increase the velocity by 1.
(2) Slowing down: If the empty space ahead is smaller than the current velocity, decrease the velocity to the empty space.
(3) Random slowing down: A number between 0 and 1 is drawn, if it is smaller than the slowing down probability, the car slows down by 1.
This random deceleration is necessary because in real life, a car may slow down due to random incidents such as the driver startled or a hole on the road.
These rules are for both models. For 2-lane model, we will need to apply lane update rule before we can apply the velocity update rules above
## Results
There are some very nuanced differences between the flow of 1-lane and 2-lane models. Specifically, both of them peaked at a density of around 0.08 with the maximal value of flow being just above 0.5. If we take a closer look at the flow trend around this peak, we can see that with a density between 0.08 and 0.4, the flow on 2-lane roads is a bit higher.
Hence, it is fair to conclude that 2-lane roads do allow more traffic flow than 1-lane roads, even though the difference is very small. From this result, we can also predict that multiple-lane roads such as 3-lane, 4-lane roads will also allow more traffic flow given the same traffic density.
