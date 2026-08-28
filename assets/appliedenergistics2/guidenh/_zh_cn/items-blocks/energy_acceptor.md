---
navigation:
  parent: /items-blocks-index.md
  title: 能源接收器
  icon: appliedenergistics2:tile.BlockEnergyAcceptor
categories:
- network infrastructure
item_ids:
- appliedenergistics2:tile.BlockEnergyAcceptor
---

# 能源接收器

<Row gap="20">
<BlockImage id="appliedenergistics2:tile.BlockEnergyAcceptor" scale="4" /> 
</Row>

能源接收器会将其他科技模组的常见能量系统转换为AE2内部使用的[能量](../ae2-mechanics/energy.md)，AE。虽然<ItemLink id="appliedenergistics2:tile.BlockController" />也能做到这一点，但控制器的面非常珍贵，一般还是推荐使用能源接收器。

能量转化比例为：
*   2 FE = 1 AE (Forge)
*   1 E  = 2 AE (Fabric)

转化速率完全取决于网络可存储的AE能源上限，具体原理详见[能源机制说明](../ae2-mechanics/energy.md)。

## 形态变体

能源接收器提供两种形态：
- 标准形态
- 扁平化/[线缆子部件](../ae2-mechanics/cables-subparts.md)形态

两种形态可通过合成网格自由转换，便于构建紧凑型系统。

## 配方

<RecipeFor id="appliedenergistics2:tile.BlockEnergyAcceptor" />
