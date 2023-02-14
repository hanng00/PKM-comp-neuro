Link: https://www.diva-portal.org/smash/get/diva2:1466428/FULLTEXT02

----
### Takeaway
Models the [[Reminiscence bump]] using Modular Attractor Neural Networks and BCPNN's and  Exponential Moving Averages.

**Aim and scope**
This paper aims at modelling the reminiscence bump from the [[Reminiscence bump]] to predict how biological parameters affect its form. 

The paper uses the [[BCPNN (Bayesian confidence propagation neural network)]] learning process, in a modular [[Attractor Network Model]], to study the effect of altering synaptic plasticity parameters.

It assumes long-term memory exists, and does not model the transfer from  short-term memory which the [[Memory Chain Model]] or [[AM-ART Model]] does.

**Data model**
In the model, a unit $\pi_{ii'}$ is a *minicolumn* which is a local group of neurons. Minicolumns are then organized into *hypercolumns*. The idea is that hypercolumns represents a feature of a memory (such as color), and the corresponding minicolumns represents the feature values (red, green, blue, yellow).
![[Pasted image 20230204182507.png]]
The network used here is an [[Attractor Network Model]] with [[BCPNN (Bayesian confidence propagation neural network)]] plasticity, having 12 hypercolumns with 12 minicolumns each (144 total units).

**Network dynamics**
The Network is governed by the following differential equations:
* The support of a unit $h_{ii'}$ is affected by the weighted contributions of presynaptic units added with its unit bias $\beta_{ii'}$ (3.1).
* The supports *per hypercolumn* is softmax normalized, yielding the unit activation $\pi_{ii'}$ (3.2)
* The unit activations are used to calculate [[Exponential Moving Averages]] in (3.3) and (3.4) for weights and biases, which are then transformed back to the "real" weights and biases in (3.5) and (3.6).
![[Pasted image 20230204190238.png]]
![[Pasted image 20230204190255.png]]

**Modelling the reminencese bump**
* $\alpha$ is a learning parameter, controlling the strength of each memory or how much it modifies the network's weights and biases. 
* By setting $\alpha=\alpha_0 e^{-\frac{t}{t_c}}+\alpha_{cst}$ , we can model the decrease of dopamine receptors combined with other aging phenomenas.

**Training and recalling memories**
* Training - Clamp the activation of each pattern for a certain duration, let the network's weights and biases evolve. 
* Recalling - Keep the network's weights and biases fixed, measure the memory and activation overlap
![[Pasted image 20230205115600.png]]

**Recency**
If $\alpha(t)$ stopped decaying at a certain age, such as proposed above, recency is achieved. Childhood [[Amnesia]] is also observed since recall from earlier memories are worsen. The model parameters used were,
* initial plasticicty $\alpha_0=0.25$ - increasing this shifts the bump to the right and a higher recency effect.
* constant plasticity $\alpha_{cst}=0.015$ - increasing this shifts the bump to the right and a higher recency effect.
* time constant of plasticity decay $tao_s=8$.
![[Pasted image 20230205115530.png]]

**Interpretation of results**
Two mechanisms underlies the reminiscence bump:
* The decrease of brain plasticity with aging due to dropping levels of dopamine receptors
* The pruning of synapses with aging
The recency curve is generated with this simple system. More complex systems like the  [[Memory Chain Model]] or [[AM-ART Model]] yields similar results. However, interactions between different areas of the brain aren't taken into account.