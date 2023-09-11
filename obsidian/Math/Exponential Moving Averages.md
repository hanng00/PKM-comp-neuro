The difference equation of an exponential moving average filter is very simple:
$$y[n] = \alpha x[n] + (1-\alpha)y[n-1]$$
In this equation, $y[n]$ is the current output, $y[n-1]$ is the previous output, and $x[n]$ is the current input; $\alpha$ is a number between 0 and 1. If $\alpha=1$, the output is just equal to the input, and no filtering takes place.

The filter is called 'exponential', because the weighting factor of previous inputs decreases exponentially. This can be easily demonstrated by substituting the previous outputs:
$$y[n] = \alpha\sum^\alpha_{k=0}(1-\alpha)^kx[n-k]$$
