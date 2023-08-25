# Homework

## Accelerated Growth

1. **Calculate the degree exponent of the directed Barabási-Albert model with accelerated growth, assuming that the degree of the newly arriving nodes increases in time as m(t) = tΘ.**

## The t-Party Evolving Network Model

In the t-party gender play no role, hence each newcomer is allowed to invite only one other participants to a dance. However, attractiveness plays a role: More attractive participants are more likely to be invited to a dance by a new participant. The party evolves following these rules:

- Every participant corresponds to a node i and is assigned a time-independent attractiveness coefficient ηi.
- At each time step a new node joins the t-party.
- This new node then invites one already partying node to a dance, establishing a new link with it.
- The new node chooses its dance partner with probability proportional to the potential partner's attractiveness. If there are t nodes already in the party, the probability that node i receives a dance invitation is

Πi=ηi∑jηj=ηit⟨η⟩

where 〈η〉 is the average attractiveness.

1. **Derive the time evolution of the node degrees, telling us how many dances a node had.**
2. **Derive the degree distribution of nodes with attractiveness η.**
3. **If half of the nodes have η = 2, and the other half η = 1, what is the degree distribution of the network after a sufficiently long time?**

## Bianconi-Barabási Model

Consider the Bianconi-Barabási model with two distinct fitnesses, η = a and η = 1. To be specific, let us assume that the fitness follows the double delta distribution

ρ(η)=12δ(η−a)+12δ(η−1)with0≤a≤1

1. **Calculate the degree exponent, and its dependence on the parameter a.**
2. **Calculate the stationary degree distribution of the network.**

## 6.4. Additive Fitness

Assume that the growth of a network is governed by preferential attachment with additive fitness

Π(ki)∼ηi+ki

where a different ηi is assigned to each node, chosen from a ρ(η) fitness distribution.

1. **Calculate and discuss the degree distribution of the resulting network.**
