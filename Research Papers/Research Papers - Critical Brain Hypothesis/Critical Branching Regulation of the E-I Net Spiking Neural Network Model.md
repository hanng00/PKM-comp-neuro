[Link](http://www.diva-portal.se/smash/get/diva2:1371426/FULLTEXT01.pdf)

### Takeaway
The paper tries to extend the [[E-I Net model]] model with a cirtical branching mechanism. Experiments hints at critical replication, but some experiments fail. It concludes that it is not clear how to properly extend the original E-I Net model.

### Background
Neural networks near criticality shows optimal information processing capabilities. If criticality can be robustly implemented and used, more energy efficient sensors and systems can be designed.

### Aim
The aim is to:
* **implement** a critical branching method based on [[C. Kello's model for critical branching NN]].
* **to tune** the dynamics of the [[E-I Net model]] to critical branching.

### Method
**Input model**
It models a [[Leaky integrate-and-fire model]]:
![[Pasted image 20230220131848.png]]
* $u_i^C$ is the membrane potential of each cell $i$ is updated at time step t.
* $i,j$ refers to cells in the postsynaptic and presynaptic populations $C, C^*$
* $n$ is the simulation step, $t$ the membrane potential decay rate.
* $\beta$ is the coupling constant, $-1$ if it is *inhibitory* and $1$ if it is *excitatory*.
* $Z^{C^*}$ represents the spike state of each cell in the presynaptic population with values {1, 0}.
* $W^{C^* -> C}_{i,j}$ is a weight matrix resemlbing the contribution of membrane potential cause by presynaptic spikes.

**Output model**
* The neuron fires if it reaches a threshold $\theta$, and then resets to its resting potential $u_r$.

**Learning rule**
The paper mentions [[Hebbian-Oja's learning rule]], [[Földiáks rule]] and [[Correlation Measuring (CM) rule]] - all used in the proposed [[E-I Net model]].

**Critical branching**
* The branching ratio $\sigma$ is defined as (output spikes)/(input cell spikes). Below 1 -> information decays, and above 1, information dissipates. Critical branching occurs when $\sigma=1$
* This paper alters [[C. Kello's model for critical branching NN]] by updating synaptic weights instead of enabling or disabling synaptic connections:
![[Pasted image 20230220154621.png]]
* Combining the above critical branching mechanism with the E-I Net's threshold regulation does not function as expected. The solution was to  set connections in *blue* to a constant threshold, and keep *red* unchanged. 
![[Pasted image 20230220155136.png]]

**Measuring criticality**
The paper used the following methods, see more in [[Measuring criticality]]:
1. Study of neural avalanches
2. Allan factor

**Branching ratio**
Measurement of the networks susceptibiliy to spikes. Here, measured by the numebr of spikes in the inhibitory population per spike in the excitory population.
![[Pasted image 20230220205711.png]]

### Results
