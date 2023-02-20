[Source](https://pubmed.ncbi.nlm.nih.gov/23356781/)

Implements a mechanism which self-regulates the activity of a [[Reservoir Computing]] to critical branching. This is done by enabling and disabling synapses in order to keep the local branching ratio $\sigma_i$ close to 1. 

* This is straightforward for **excitatory** neurons with excitatory axonal synapses.
* For **inhibitory** neurons, the state *blamed/unblamed* is introduced, denoting  if a spike has been blamed for branching into one or more spikes. Then, with some probability it is enabled or disabled.