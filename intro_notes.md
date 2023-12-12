语言模型 (Language Model)，给令牌 (token) 序列分配概率：$p(x_{1:T}) = p(x_1, x_2, x_3, ..., x_T)$

自回归语言模型 $p(x_1, x_2, x_3) = p(x_1)p(x_2| x_1) p(x_3| x_2, x_1)$

从语言模型的概率分布中采样：用参数 $T$ 温度，控制样本的多样性

n-gram 模型：$p(x_i|x_{1: \ i-1}) = p(x_i|x_{i-1-n: \ i-1})$

神经网络模型：训练神经网络模型 $\text{nn}(\text{input}=x_{1:i-1}, \text{label}=x_{i})$ 去估计 $p(x_i|x_{1: \ i-1})$