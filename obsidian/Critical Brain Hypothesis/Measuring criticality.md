**5 invariants for avalanches**
According to [[_Scaling properties of neuronal avalanches are consistent with critical dynamics]], there are five invariants which can be used to classify avalanches from criticality.

**Power-law distribution**. 
	* "Proven to work" in this [paper](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.108.208102)
	* However, it appears to show in random systems so it is more a feature of complex systems rather than criticality. [[_Power-law statistics and universal scaling in the absence of criticality]]

**Studying Avalanche** (Measuring power-law #2)
Used in [[_Critical Branching Regulation of the E-I Net Spiking Neural Network Model]] by studying avalanches S / time T. And Their distribution was given by $D(s)=k_sS^{-\beta}$ . Criticality would yield $\beta =1$. 
![[Pasted image 20230220175454.png]]

**Allan Factor** (Measuring power-law #2)
* Developed to measure stability in clocks. The Allan factor reflects the stability of the event variance in a time series by using the variance in number of events when binnign the time series. By varying the size of the bin, an estimate of how the time series evolves with time can be made.
![[Pasted image 20230220205052.png]]
* For brain criticality, we can divide the time series into bins and compute the Allan factor of the spike trains. This yields 
	* A(1) = 0.533, A(2) = 0.995, A(4) = 1.08, A(8) = 0.807
* The takeaway is that for larger time frames not much changes indicating a fractal structure.
![[Pasted image 20230220205336.png]]


**Susceptibility**, 
	* proposed in [[_Inferring collective dynamical states from widely unobserved systems]]. A function describing how sensitive a given system is to an incoming stimulus.