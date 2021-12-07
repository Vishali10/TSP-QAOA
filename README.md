# TSP-QAOA
Solving the Travelling Salesman Problem using QAOA (Quantum Approximate Optimization Algorithm). 

# The Problem
Given a set of cities and distance between every pair of cities as an adjacency matrix, the problem is to find the shortest possible route that visits every city exactly once and returns to the starting point.

# QAOA Algorithm
1. The algorithm works as follows:
2. Choose the wiwi and wijwij in the target Ising problem. In principle, even higher powers of Z are allowed.
3. Choose the depth of the quantum circuit mm. Note that the depth can be modified adaptively.
4. Choose a set of controls θθ and make a trial function |ψ(θ)⟩|ψ(θ)⟩, built using a quantum circuit made of C-Phase gates and single-qubit Y rotations, parameterized by the components of θθ
5. Evaluate
C(θ)=⟨ψ(θ) |H| ψ(θ)⟩=∑iwi⟨ψ(θ) |Zi| ψ(θ)⟩+∑i<jwij⟨ψ(θ) |ZiZj| ψ(θ)⟩C(θ)=⟨ψ(θ) |H| ψ(θ)⟩=∑iwi⟨ψ(θ) |Zi| ψ(θ)⟩+∑i<jwij⟨ψ(θ) |ZiZj| ψ(θ)⟩
by sampling the outcome of the circuit in the Z-basis and adding the expectation values of the individual Ising terms together. In general, different control points around θθ have to be estimated, depending on the classical optimizer chosen.

6. Use a classical optimizer to choose a new set of controls.

7.Continue until C(θ)C(θ) reaches a minimum, close enough to the solution θ∗θ∗.

8. Use the last θθ to generate a final set of samples from the distribution |⟨zi |ψ(θ)⟩|2∀i|⟨zi |ψ(θ)⟩|2∀i to obtain the answer.


# OUTPUT
Adjacency matrix and graph representation:
![image](https://user-images.githubusercontent.com/35892971/144970727-c294dd2d-e6b4-476d-a4fc-869385d07ba0.png)

Quantum Approach:
![image](https://user-images.githubusercontent.com/35892971/144970780-8ab5f5ba-236a-4bbd-b8cb-451424ddbe76.png)

Brute Force Approach:
![image](https://user-images.githubusercontent.com/35892971/144970808-55f00135-ab66-4170-b2be-d64f7237d3ad.png)


