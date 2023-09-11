[[Video link]](https://www.youtube.com/watch?v=zldal7b7sJ4&t=597s&ab_channel=iCASLab)
### Two methods that are highly debatable:
* **Rate codes** - information is stored in the spike count or firing rate. High-intensity spiking corresponds to a bright pixel, yieldign high frequency.
* **Temporal codes** - information is stored in the timing of a spike, where a high intensity spike is encoded as a quick spike.

### Empirical data:
* A paper conjectures that 85% of the brain must use **temporal code**, otherwise all energy would be used to encoding.
* But rates are better for error and noise tolerance, enabling faster convergence when using backprop.
* Timing is better for power efficiency and latency.

### Decoding outputs
* **Rate codes** - which output neuron has the highest firing rate?
* **Temporal encoding** - which output neuron fires first?
Thus, one could have a rate code input but a temporal output.
![[Pasted image 20230220124539.png]]