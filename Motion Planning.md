---
tags:
  - motionPlan
---
**Probabilistic Roadmap (PRM)**
- probabilistically complete
- much easier to identify if a sample is collision-free than to build a model for the free space
- Cons: edges might be invalid; some map might be difficult to get the right sample
**Rapid-exploring Random Trees (RRTs)**
- probabilistically complete
- just check collision, no need to construct configuration space
- just keep track of parent node, no need to do tree search
**RRT*: tree expansion with optimality**
- improve the path from RRT
![[Pasted image 20241029105846.png|500]]

___
**Workspace**: environment robot operates in
**Configuration**: specification of the position of every point on the object
**Configuration space**: set of all possible configurations
**DoF**: number of dimension of configuration space

___
**Kinematic constraint**: feasible states, allowable positions of the robot,
-  geometry of the robot in relation to obstacles but also self-collisions for robot arm for example
**Differential constrain**t: limit how state can change
- "holonomic"is there's no differential constraint, or "quasiholonomic"
**Dynamic constrain**t: how the states can change as a result of forces and torques
- acceleration, gravity, friction, ...

---
**References**
