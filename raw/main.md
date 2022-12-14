# 哈士奇项目文书中文版

Husky工程是关于新一代的AI和新一代的编程。
具体地说，我们正在实现在计算机视觉领域用更强大高效的模型取代深度学习，辅助把事情拓展到其它领域。

## 不同AI方法之间的比较

Husky与以上诸多方法主要不同在于

- 不预先限制推理时计算的形式

- 从最开始就考虑推理时的计算效率

- 尽可能用完全可解释而且高效的程序解决问题

- 利用新一代编程工具实现"Human in the loop"

- 数学上更正确

详细见[不同AI方法之间的比较](comparison.md)

## Motivation

Observation: The most natural hypothesis class can be statistically simple but computationally hard.

Give examples in MNIST

DL and Traditional machine learning deal with statistical and computational challenge using the same

## 组织

本项目完全开放，将持续多年（ImageNet将16个月搞定，接下来继续做NLP等其他领域），欢迎随时加入，可以自由安排工作时间和工作量，每个人的贡献会被科学合理的记录下来，其中做出创造性贡献的会被加入文章的作者列表，工程贡献也会在文章或者文档中被记录下来。大家可以先参与比较大的项目，比如ImageNet，来学习掌握Huksy的用法和核心思想，然后大家可以随意组队或者单独用Husky做自己感兴趣的东西，我们将会全力提供支持。

深度学习是非常重要的科研方向，但是有很严重的一些问题，它缺乏理论支持，在很多方向已经很难有重大突破，例如图像分类，神经网络架构搜索等。即使有突破，往往建立在大量算力的基础上，在业界也不容易做到，更不用说学界。另外进行深度学习科研并不真正需要研究者很高的素质，调参五年很难真正学到一辈子都受用的技能。

但是在我们这个项目中，我们是真正意义上的计算机工程，它涉及到了计算机科学的诸多方面，包括硬件、软件工程、理论、编程语言设计、前端可视化、算法。几乎没有黑盒子存在，所有方面都有机的结合在一起。参与这种很多是国内外名校的本科生以及博士，以及业界有丰富经验的科研与开发人员。每个人都有机会学到各个领域最前沿的知识，而且这些知识对于科研本身是非常关键的，因为我们并不是通过调参，而是通过科学的方法来得到模型

## 子项目

### ImageNet
ImageNet将会被分解成1000个小任务，其中每个任务是判断图片是否属于其中一个类。每个人可以专注一个或者数个类，也可以研究比较通用的特征或者自动化的方法，最后会把所有人的结果整合起来得到一个远比现有深度学习优越的模型。

### 编译机制
Husky编程语言需要在编译方面做重大创新，Husky将会有Python一样的启动速度，有Rust一样的运行速度，用户可以或者通过用户，或者通过语言自身来决定哪些函数需要被完全编译，哪些函数会以更弱的形式编译，这一切可以根据不同的应用场景进行调整。

例如，在前端应用中，大部分的函数在开发过程中用解释的形式运行就足够了，这个时候最重要的就是修改代码后结果更新的速度。比如Rust在这方面就很难令人满意。而在图像识别里，我们的计算不在基于矩阵，需要根据实际情况设计有良好几何意义的函数的编程实现，这些需要被完全编译，使得可以很快在训练接上更新计算结果。总而言之，一个真正意义上通用的语言应该能够在不同场景下使用不同的编译机制，而现有的语言，如Rust, Julia, C/C++, Java, JavaScript, Lean, Ocaml, Python, Golang, Swift, Zig, Nim, Kotlin, C#, R, Matlab, Mathematica, Ruby, Scala, TypeScript等主推一种编译模式的语言都难以满足这些要求。

### Debugger前端设计

### Human in the loop for business data
我们会比Snorkel做得好得多

### 机器学习理论
这里有相当多可以研究的问题，很多事情背后都有严格的理论，很容易验证泛化性和鲁棒性

反观现有的深度学习理论，由于深度学习严重缺乏数学结构，过于一般，缺乏与具体领域的联动，很难从数学上严格有效的论证它的优越性（我们将会用事实证明它也并不优越）。以图像识别为例，在机器学习领域，基本上没有对数据分布的一个好的刻画（不能简单假设高斯分布，否则根本不可能得到有意义的结果）。

而在我们的项目中，我们可以几何上严格论证泛化性和鲁棒性，这是在深度学习理论难以想象的。

### 强化学习的正确框架
现有的强化学习理论框架与实际相差过远，而以深度学习为主的实验模型完全缺乏理论支持，严重依赖算力，我们将会在接下来的若干年里，探索一种全新的方式，[rl](rl.md)

### 科学上的应用
思路和深度学习在科学上的应用差不多，但是我们会做得更好，原因是Husky比深度学习探索的空间更大