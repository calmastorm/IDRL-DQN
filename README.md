# IDRL-DQN

用于IDRL课程的DQN代码。

02/21/2023

- 去除了源代码中的测试函数和渲染函数，目前阶段只需要训练函数提供的结果。

02/23/2023

- 重新添加了测试函数，修改代码去除了渲染函数。



## 比较方法

<u>每个或每组参数</u>调节完毕后，经过训练自动生成20次测试的分数及其平均数。尽管我们已经固定了大部分随机数，但仍有可能存在由硬件或未知变量引起的随机训练结果。因此我们会将上述的过程运行十次，然后计算其平均数和标准差。平均值能体现该组参数在这个模型上的综合表现，标准差能体现模型表现的离散程度，离散程度大表明表现不稳定，但不排除随机性带来的影响。

## 可调节的参数

训练次数：num_frames

经验回放尺寸：ReplayBuffer

神经网络结构：Network（子参数可以结合调整）

- Number of layers
- Number of dimensions

GAMMA

学习率：LearningRate

单次训练样本数：batch_size（和learning rate高度相关 可以结合调整）[参考链接](https://www.sciencedirect.com/science/article/pii/S2405959519303455#:~:text=There%20is%20a%20high%20correlation,size%20with%20low%20learning%20rate.)
