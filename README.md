# Lambda SABR

## Time-discretization
In this section, we use time discretization method to perform Monte Carlo simulations on the $\lambda -SABR$ model. For the choice of methods, we use the Euler scheme and the Milstein scheme respectively. Regarding the drift term in the expansion, we substitute it with two types of means to compare the overall effects. This is then compared with the results from Conditional MC. After obtaining the trajectories of the underlying assets, we calculate the implied volatility using various methods.

* For $\lambda-SABR$ model, we have volatility $\sigma_{t}$ obeying such process:
$$d \sigma_{t}=\lambda\left(\theta-\sigma_{t}\right) d t+\nu \sigma_{t} d Z_{t}$$
* We derived the Oular / Milstein scheme for $\sigma_{t}$ as:

$$ \sigma_{t+\Delta t}=\sigma_{t}+\lambda\left(\theta-\sigma_{t}\right) \Delta t+\nu \sigma_{t} Z \sqrt{\Delta t}+\frac{\nu^{2}}{2} v_{t}\left(Z^{2}-1\right) \Delta t$$

* We apply two approaches to cauculate $E\left(\sigma_{t+\Delta t}\mid \sigma_{t} \right)$:
* First, We define $y_{t}:=\left(\sigma_{t} - \theta \right )e^{\lambda t}$ and easily get $y_{t}$ is a martingale and we have:
$E\left (\sigma_{t+\Delta t} \mid  \sigma_{t} \right)=\theta + \left(\sigma_{t} - \theta \right )e^{-\lambda \Delta t}$
* Second, we use the exact mean and variance to do so, we have $E\left (\sigma_{t+\Delta t}\mid  \sigma_{t}\right)=\theta \left ( 1-e^{-\lambda \Delta t}\right) + \sigma_{t}e^{-\lambda \Delta t}$










