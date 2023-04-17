
拓展

Co-scale conv-attentional image transformer https://blog.csdn.net/qq_43733107/article/details/127374336

Factorized Attention Mechanism和传统注意力机制的主要优缺点如下：

Factorized Attention Mechanism的优点：

计算效率高：Factorized Attention Mechanism将注意力计算分解为多个子空间的计算，每个子空间的计算独立进行，从而减少了计算量和内存消耗，提高了计算效率。

可扩展性强：由于计算量和内存消耗的减少，Factorized Attention Mechanism可以更好地适应较大的输入特征和较多的注意力头数目，具有较强的可扩展性。

泛化能力强：Factorized Attention Mechanism将输入特征分解为多个子空间，每个子空间都计算一组注意力权重，可以更好地捕捉输入特征中的多个方面和上下文信息，增强模型的泛化能力。

交互性强：Factorized Attention Mechanism可以使用跨头或跨通道的交互方式来进一步提高模型的性能和准确性，这种交互方式可以将不同子空间之间的信息进行整合和传递，从而更好地利用输入特征中的全局信息。

传统注意力机制的优点：
注意力权重可解释性强：传统注意力机制可以计算每个输入位置的注意力权重，从而可以更好地解释模型的决策和预测结果。

更加通用：传统注意力机制可以应用于各种类型的数据，例如文本、图像、音频等，具有更加通用的性质。

Factorized Attention Mechanism的缺点：

模型复杂度高：Factorized Attention Mechanism需要对输入特征进行分解和组合，导致模型的复杂度相对较高。

注意力权重可解释性相对较弱：由于Factorized Attention Mechanism将输入特征分解为多个子空间并计算每个子空间的注意力权重，因此对于单个输入位置的注意力权重解释性相对较弱。

传统注意力机制的缺点：

计算量和内存消耗较大：传统注意力机制需要计算每个输入位置的注意力权重，导致计算量和内存消耗较大，可能无法适应较大的输入特征和较多的注意力头数目。

可扩展性相对较弱：由于计算量和内存消耗的限制，传统注意力机制的可扩展性相对较弱，可能无法适应较大的输入特征和较多的注意力头数目。

论文的前作网络大致概要：https://blog.csdn.net/wumenglu1018/article/details/95949039

Davit代码：https://github.com/dingmyu/davit

概要博文推荐：

重点翻译：https://blog.csdn.net/qq_45128278/article/details/124491495

要点总结：https://zhuanlan.zhihu.com/p/500202422

额外总结：

![image](https://user-images.githubusercontent.com/118878610/232385824-e09dd40a-d82e-41be-b5e4-f454afa41fca.png)


1.双注意力模块在每个阶段持续提升性能。   

2.第二阶段的双重注意力提高最多，因为早期阶段需要更多的全局信息。第一阶段相对较小的改进是局部纹理特征主导了网络的浅层部分。

3.在所有四个阶段都 添加双重注意力时取得了最好的结果。

![image](https://user-images.githubusercontent.com/118878610/232386075-1f091580-7db7-4221-ba5c-4fcbd19b6f34.png)

可以看出先window注意力 后 channel  注意力效果最好






