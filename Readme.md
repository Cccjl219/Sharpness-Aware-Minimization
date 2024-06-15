# Sharpness-Aware Minimization
## Imporving Efficiency
- An Adaptative Policy To Empoly Sharpness-Aware Minization [[ICLR2023]](https://arxiv.org/abs/2304.14647) 为了提高SAM的效率，本文提出一种在训练过程中根据loss lanscape的sharpness自适应地选择SAM或ERM的策略。直觉上，SAM跟适用于sharp的区域，SGD更适用于flat的区域。如何measure这种flatness？本文利用**随机梯度的范数平方**，假设其服从正太分布，利用指数移动平均来计算分布的参数。

## Improving Effectiveness 
SAM关键的部分在于利用一步梯度上升寻找邻域内最大loss的点，但是由于这一步是对于实际寻找最大loss的近似，很多SAM的后续工作都是改进这里。
- Random Sharpness-Aware Minimization [[NeurIPS 2022]](https://arxiv.org/abs/2304.14647) 
