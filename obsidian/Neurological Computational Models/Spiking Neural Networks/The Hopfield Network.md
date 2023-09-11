**Brain memory**
Instead of retrieving a memory by its adress (how RAM memory works), give a incomplete version and the memory will auto-complete it. This is called *associative memory*.

Brains do not have a central CPU organizing memory adresses. *The Hopfield Network* aims to model the constant buzz of neurons in the brain, and replicate the associative memory. 
![[Pasted image 20230202222643.png]]

**The model specification**
1) Equation update - weighted sum of connected states. Apply int( *sum* ) to round to {-1, 1} to make neurons binary.
2. Learning - weights are updated using Hebbian Learning. It multiplies the connected states values.
3. Convergence - converge when learning one memory, not guaranteed for multiple memories.