# BowTie Artifacts
This repo shows the artifacts of the paper [Stopping Silent Sneaks: Defending against Malicious Mixes with Topological Engineering](https://arxiv.org/abs/2206.00592). We developed two tools: ***mixnets topology generator (MTG)*** to produce the reference and 
mixnet topologies and ***routesim*** to evaluate the topologies on their expected security metrics of 
typical dynamic email-like usage.

## Tools
### [routesim](https://github.com/frochet/routesim)
To enable our evaluation of time to first compromise metric based on realistic Mixnets usage, we 
implement 
***routesim*** in rust to support the dynamic, multi-message 
user scenario, aiming at estimating user's resilience against client enumeration. It takes the output of the ***MTG*** as the input data, and evaluates the security level of clients over time.

### [MTG](https://github.com/sus0pid/MTG-Simulator)
We implemented a scalable Mixnet topology generator incorporating the four mixnet construction algorithms in Python. It generates the mixnet topological configuration and the amount of fully compromised traffic that the adversary can see. 