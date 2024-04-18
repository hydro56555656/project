# Lambda SABR

## Time-discretization
这部分中，我们使用Time-discretization对 $\lambda -SABR$模型进行蒙特卡洛模拟。在方法选择上，会分别使用Oular method和Milstein method。针对展开式中的漂移项，我们使用两种均值做替代，对整体效果进行比较。并与Conditional MC中的结果对比。在获得标的资产的轨迹后，分别求几种方法下的隐含波动率。

For $\lambda-SABR$ model, we have volatility $\sigma_{t}$ obeying such process:
$$d \sigma_{t}=\lambda\left(\theta-\sigma_{t}\right) d t+\nu \sigma_{t} d Z_{t}$$
We derived the Oular / Milstein scheme for vt as:

$$\sigma _{t+\Delta t}=\sigma _{t}+\lambda\left(\theta-\sigma_{t}\right) \Delta t+\nu \sigma_{t} Z \sqrt{\Delta t}+\frac{\nu^{2}}{2} v_{t}\left(Z^{2}-1\right) \Delta t \quad \text { for } \quad Z \sim N(0,\sigma)$$


