---
navigation:
  parent: /items-blocks-index.md
  title: 能源元件
  icon: appliedenergistics2:tile.BlockDenseEnergyCell
categories:
- network infrastructure
item_ids:
- appliedenergistics2:tile.BlockEnergyCell
- appliedenergistics2:tile.BlockDenseEnergyCell
- appliedenergistics2:tile.BlockCreativeEnergyCell
- appliedenergistics2:item.ItemMultiPart:690
---

# 能源元件

<Row gap="20">
  <BlockImage id="appliedenergistics2:tile.BlockEnergyCell" scale="4" />

  <BlockImage id="appliedenergistics2:tile.BlockDenseEnergyCell" scale="4" />

  <BlockImage id="appliedenergistics2:tile.BlockCreativeEnergyCell" scale="4" />
</Row>

能源元件给予网络更大的[能量](../ae2-mechanics/energy.md)容量。一定量的能量缓存能减少大量输入输出造成的能量尖峰影响，更大的能量存储容量则使得网络能在脱离供电时（例如晚上的太阳能板阵列）运作，也可处理[空间存储](../ae2-mechanics/spatial-io.md)产生的巨量瞬时能量消耗。

## 填充条

<Row>
<BlockImage id="appliedenergistics2:tile.BlockEnergyCell" scale="4" />
</Row>

元件侧面的填充条对应其能量水平。

*   0 条：储能低于25%
*   1 条：储能25%-50%
*   2 条：储能50%-75%
*   3 条：储能75%-99%
*   4 条：储能99%以上

## 元件种类

*   <ItemLink id="appliedenergistics2:tile.BlockEnergyCell" />：基础型号，可存储20万AE能源，足以应对常规网络操作中的能耗波动
*   <ItemLink id="appliedenergistics2:tile.BlockDenseEnergyCell" />：致密型号，可存储160万AE能源，适用于依赖储能运行网络或处理大型[空间存储系统](../ae2-mechanics/spatial-io.md)的瞬时高负载
*   <ItemLink id="appliedenergistics2:tile.BlockCreativeEnergyCell" />：创造模式专用，提供无限能源

## 配方

<Row>
  <RecipeFor id="appliedenergistics2:tile.BlockEnergyCell" />

  <RecipeFor id="appliedenergistics2:tile.BlockDenseEnergyCell" />
</Row>
