[Original paper](https://pubmed.ncbi.nlm.nih.gov/23536063/)

### Definition
The E-I Net model consists of 
* a [[Leaky integrate-and-fire model]] 
* with the learning rule [[Correlation Measuring (CM) rule]] for $W_{i,j}$

The membrane potential is regulated as:
$$\Delta \theta_j^{C} \propto <Z_j^{C}> - p^{C} $$
Here $j$ denotes the cell number, $C$ denotes the cell’s population, $\theta$ is the threshold of the cell, $Z$ is the mean spike rate of the cell and $p$ is a predetermined spike rate constant.

It regulates the firing threshold of each cell, leading to a constant spike rate of the population. This phenomena is called [[Homeostasis]].

### Function
The network functions like this:
* A whitened image are used as input to the excitatory neurons (E) with weights adjusted by [[Hebbian-Oja's learning rule]].
* Spikes in (E) propagates to the inhibitory population (I) with weights adjusted by the [[Correlation Measuring (CM) rule]].
* Spikes in (I) propagates back into itself, and to (E) using [[Correlation Measuring (CM) rule]].
* The learned stimulus can the be reconstructed using "reverse engineering", tbd. 
The separation of (E) and (I) is what makes it differ from [[Reservoir Computing]]:
* (I) is used to decorrelate the (E) cells from responding together, forcing (E) cells to respond uniquely.
![[Pasted image 20230220151151.png]]