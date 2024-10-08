# Data parallelism

划分了输入数据的batch维，把数据（计算量）均衡地划分在了所有的设备上，每个设备计算出本地的梯度后调用AllReduce得到全局的梯度。
