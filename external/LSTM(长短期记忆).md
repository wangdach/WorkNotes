#### [LSTM(长短期记忆)](https://www.nvidia.cn/developer/discover/lstm/)

> 长短期记忆 (LSTM) 是一种[递归神经网络](https://developer.nvidia.com/discover/recurrentneuralnetwork)，专用于防止给定输入的[神经网络](https://developer.nvidia.com/discover/artificialneuralnetwork)输出在通过反馈回路循环时发生衰减或爆炸。反馈回路可以使递归网络比其他神经网络更出色地进行模式识别。输入过去的记忆对于攻克[序列学习](https://developer.nvidia.com/discover/recurrentneuralnetwork#sequence-learning)任务至关重要，与其他 RNN 结构相比，长短期记忆网络可以通过缓解所谓的梯度消失问题，进而提供更卓越的性能。
>
> 由于 LSTM 具有学习长期依赖关系的能力，因而适于解决众多序列学习问题，其中包括语言建模和翻译、语音声学建模、语音合成、语音识别、音频和视频数据分析、手写识别和生成、序列预测和蛋白质二级结构预测。

##### 长短期记忆网络结构

>  长短期记忆网络结构由自连接线性单元（权重为常数  1.0）组成。这使得流入该自循环单元的值（向前推算）或梯度（向后推算）可以保持不变，且随后可在所需的时间步进行回调。乘以单元乘数之后，前一时间步的输出或误差仍与下一时间步的输出相同。该自循环单元（即记忆单元）能够存储包含过去十几个时间步的信息。这对许多任务都极其有效。例如，对于文本数据，LSTM 单元能够存储前一段落中包含的信息，并能将此信息应用于当前段落的句子中。 

 ![lstm](pic/LSTM(长短期记忆).assets/lstm.png) 