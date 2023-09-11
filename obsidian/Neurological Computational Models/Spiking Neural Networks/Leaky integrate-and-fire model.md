### Basic Idea
* A common model of the neuron membrane potential. The membrane potential increases when recieving spikes but decays with time. 

![[Pasted image 20230220125325.png]]
* The idea is that neurons fires sparsely, so spikes are *integrated* and then *leaked*. The membrane voltage is then discretized and defined recursively.
![[Pasted image 20230220125502.png]]
* The neuron then fires and resets once a threshold is met. This configuration is encapsulated into a LIF-neuron.
![[Pasted image 20230220125630.png]]

### Mathematical implementation
