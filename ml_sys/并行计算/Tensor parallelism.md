# Tensor parallelism

随着模型的进一步增大，需要直接把参数分布在不同的设备上。当模型架构是transformer时，会在Attention和Feed Forward Network之前插入Identity-AllReduce（前向为Identity，不改变activation tensor，反向为AllReduce），在结束后插入AllReduce-Identity。
