---
navigation:
  parent: /ae2-mechanics-index.md
  title: 子网络
  icon: appliedenergistics2:item.ItemMultiPart:140
---

# 子网络

<GameScene width="600" height="400" zoom={4} rotateX={25} rotateY={-45} centerY={-15} centerZ={4.25}>
    <ImportStructure src="../assets/structures/subnet_demonstration.snbt" />

    <DiamondAnnotation pos="1.5 2.5 9.5" color="#00ff00">
            将分子装配室的产物运进木桶。
    </DiamondAnnotation>

    <DiamondAnnotation pos="1.5 2.5 8.5" color="#00ff00">
            将上方超级储罐中的流体运到下方储罐。
    </DiamondAnnotation>

    <DiamondAnnotation pos="1.5 2.5 7.5" color="#00ff00">
            红石 P2P 子网络，把红石块的信号 \
            传到红石灯。
    </DiamondAnnotation>

    <DiamondAnnotation pos="1.5 2.5 6.5" color="#00ff00">
            将木桶里的物品送进虚空储存元件。
    </DiamondAnnotation>

    <DiamondAnnotation pos="1.5 2.5 5.5" color="#00ff00">
            使用 ME接口 与 ME存储总线交互的子网络，\
            让主网络能够访问这一片本地子存储。
    </DiamondAnnotation>

    <DiamondAnnotation pos="2.5 0.5 3.5" color="#00ff00">
            工业高炉自动合成子网络，把样板里的材料 \
            送进工业高炉输入口，再从样板进入的同一接口 \
            把产物送回主网络。
    </DiamondAnnotation>
</GameScene>

“子网络”并没有特别严格的定义，但一般可以把它理解为：一个为[主网络](./me-network-connections.md)提供支持，或专门负责某个小任务的独立 [ME 网络](./me-network-connections.md)。

在前期，子网络通常规模较小，不一定需要控制器；但当你开始把多方块和复杂自动化接入 AE2 之后，这种情况很快就会改变。

子网络最常见的三种用途是：

* 限制某些[设备](./devices.md)能访问哪些存储。比如，你可能不希望矿处理子网络把产物直接倒进主网络，但又希望仍然能在主网络里看见这些产物。
* 节省主网络的频道。比如，把带样板的 ME接口 接到另一个接口，再由那个接口连多个机器上的 ME存储总线，这样主网络只占 1 个频道，而不是每台机器各放一个接口、各占 1 个频道。
* 节省致密线缆和空间。比如，把最多 32 个主网络频道打包进一个 [P2P](./p2p_tunnels.md) 载体子网络，只用 1 个频道长距离传输。

搭建子网络时，最重要的一点之一是时刻弄清楚[网络连接](./me-network-connections.md)。

很多人会把一堆接口、总线和别的部件随手拼在一起，以为这就成了子网络；但如果这些设备仍然通过各种整方块设备连在主网络上，那它们其实还是主网络的一部分。

> [!NOTE]
> 不同颜色的线缆和建立子网络本身没有直接关系；它们唯一的作用，只是彼此不会连接。

子网络的一些常见用途包括：

* <Color id="BLUE">抽象</Color>。把一套复杂合成流程的细节都放进子网络里处理，这样在主网络看来，整座工厂就像“一台机器”。
* <Color id="GREEN">并行化</Color>。把一台慢机器换成 10 台同样的慢机器并行工作；对主网络来说，行为并没有变化，而且通常也不需要额外频道。
* <Color id="YELLOW">多方块样板处理</Color>。在子网络里更轻松地把所有材料送进同一组总线或仓室。

具体例子包括：

* 用 ME输入总线 和 ME存储总线 组成一个“管道”子网络，在两个容器之间转移物品或流体。
* 用 ME破坏面板 和 ME存储总线 组成子网络，让破坏面板挖下来的东西只能进入指定存储，从而实现过滤。
* 用 ME接口 和 ME成型面板 组成子网络，让插进接口的东西自动被推到成型面板并放置/丢到世界中。
* 用一个专门的存储系统，通过特有的“ME接口 与 ME存储总线”交互接入主网络，用来存农场产物之类的内容，避免把主存储无限灌满。
* 以及更多类似方案。

<ItemLink id="appliedenergistics2:item.ItemMultiPart:140" showIcon="left" /> 对建立子网络非常有用。它能在不连接两个网络的前提下传递能量，因此你不需要到处额外摆放能源接收器和供电线缆，就能为子网络供能。
