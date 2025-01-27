# Let’s Verify Step by Step - 论文笔记

2024年9月12日，OpenAI发布了o1-preview模型，在大语言模型中引入了“慢思考”这一设计，大幅提高了模型推理能力，在code和math相关evaluation中表现惊艳。人们在追溯o1模型的技术发展时，发现OpenAI在过去一段时间已经发布了一系列论文，这些论文所包含的技术构建了o1模型的基石。而 *Let’s Verify Step by Step* 就是其中极为重要的一篇。

## 摘要

近年来，大型语言模型在复杂多步骤推理能力方面取得了显著进步。然而，即使是最先进的模型也经常产生逻辑错误。为了训练更可靠的模型，我们可以转向结果监督，它为最终结果提供反馈，或者过程监督，它为每个中间推理步骤提供反馈。鉴于训练可靠模型的重要性以及人类反馈的高成本，仔细比较这两种方法是必要的。最近的工作已经开始这种比较，但仍有许多问题有待解决。我们进行了自己的调查，发现过程监督显著优于结果监督，用于从具有挑战性的MATH数据集中解决问题。我们的过程监督模型解决了来自MATH测试集代表性子集的78%的问题。此外，我们还展示了主动学习显著提高了过程监督的有效性。为了支持相关研究，我们还发布了PRM800K，这是我们最佳奖励模型训练中使用的完整80万步级人类反馈标签数据集。

