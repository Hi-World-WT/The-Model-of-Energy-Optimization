# The-Model-of-Energy-Optimization

## Training Completion Time Model

For a specific training task (e.g., a particular DNN model), the time required to finish an training epoch on different devices is totally different. The training completion time is highly correlated with the following factors. First, since different devices can have different number of data objects to be trained, the training completion time can be determined by the amount of data objects $d_{i}$. Second, different clients can have totally different training platforms (e.g., CPU, GPU), thus the training completion time can also depend on different training platforms. Third, for a certain training platform, the hardware configuration can be different (e.g., number of cores, core frequency). Thus, we model the training completion time for one epoch as follows:
\begin{equation}
t_{i} = \frac{\theta * d_{i}}{c^{\alpha}f^{\beta}}
\end{equation}
$\theta$ represents the coefficient which is different for different training platforms and devices. $d_{i}$ represents the number of data objects required to be trained in this training epoch. $c$ represents the number of cpu cores adopted during the training process. $f$ represents the core frequency. $\alpha$ and $\beta$ are the corresponding coefficients that can be obtained through the system identification process. We can find that the more data objects need to be trained, the longer time it requires to complete the training. The more number of cpu cores and high core frequency can help accelerate the training process.
