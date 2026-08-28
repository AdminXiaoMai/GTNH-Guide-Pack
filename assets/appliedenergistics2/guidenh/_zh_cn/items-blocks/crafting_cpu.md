---
navigation:
  parent: /items-blocks-index.md
  title: 合成CPU多方块结构（合成存储器/并行处理单元/合成监控器/合成单元）
  icon: appliedenergistics2:tile.BlockSingularityCraftingStorage
categories:
- devices
item_ids:
- appliedenergistics2:tile.BlockCraftingUnit
- appliedenergistics2:tile.BlockCraftingMonitor
- appliedenergistics2:tile.BlockCraftingUnit:1
- appliedenergistics2:tile.BlockCraftingUnit:2
- appliedenergistics2:tile.BlockCraftingUnit:3
- appliedenergistics2:tile.BlockAdvancedCraftingUnit:0
- appliedenergistics2:tile.BlockAdvancedCraftingUnit:1
- appliedenergistics2:tile.BlockAdvancedCraftingUnit:2
- appliedenergistics2:tile.BlockAdvancedCraftingUnit:3
- appliedenergistics2:tile.BlockCraftingStorage
- appliedenergistics2:tile.BlockCraftingStorage:1
- appliedenergistics2:tile.BlockCraftingStorage:2
- appliedenergistics2:tile.BlockCraftingStorage:3
- appliedenergistics2:tile.BlockAdvancedCraftingStorage
- appliedenergistics2:tile.BlockAdvancedCraftingStorage:1
- appliedenergistics2:tile.BlockAdvancedCraftingStorage:2
- appliedenergistics2:tile.BlockAdvancedCraftingStorage:3
- appliedenergistics2:tile.BlockSingularityCraftingStorage
---

# 合成CPU多方块结构（合成存储器/并行处理单元/合成监控器/合成单元）

<GameScene width="350" height="220" zoom="4" showBackground={false}>
  <ImportStructure src="../assets/structures/crafting_cpus.snbt" />
  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

<Row>
  <BlockImage id="appliedenergistics2:tile.BlockCraftingStorage:1" scale="4" />

  <BlockImage id="appliedenergistics2:tile.BlockCraftingUnit:1" scale="4" />

  <BlockImage id="appliedenergistics2:tile.BlockCraftingMonitor" scale="4" />

  <BlockImage id="appliedenergistics2:tile.BlockCraftingUnit:0" scale="4" />
</Row>

合成CPU管理合成请求与合成任务。它们会在执行多步骤合成任务时将中间产物存于自身，并影响合成任务的大小上限，某种程度上也会影响这些任务的完成速度。详细信息见[自动合成](../ae2-mechanics/autocrafting.md)。

## 核心功能

* 存储合成过程的中间产物
* 通过右键点击查看合成进度
* 可配置接收玩家请求/自动化请求/二者兼有
* 最低配置：单个1k合成存储器

## 构造规则

必须构建为无空隙的实心长方体结构，至少包含1个合成存储器组件。

---

# 合成单元

<BlockImage id="appliedenergistics2:tile.BlockCraftingUnit" scale="4" />

（可选）合成单元仅用于填充CPU内空隙，以保证CPU的形状是实心长方形棱柱。没有其他组件时可用此填补。它们也是其他组件的合成材料。

<RecipeFor id="appliedenergistics2:tile.BlockCraftingUnit" />

---

# 合成存储器

<Row>
  <BlockImage id="appliedenergistics2:tile.BlockCraftingStorage:0" scale="4" />

  <BlockImage id="appliedenergistics2:tile.BlockCraftingStorage:1" scale="4" />

  <BlockImage id="appliedenergistics2:tile.BlockCraftingStorage:2" scale="4" />

  <BlockImage id="appliedenergistics2:tile.BlockCraftingStorage:3" scale="4" />

  <BlockImage id="appliedenergistics2:tile.BlockAdvancedCraftingStorage:0" scale="4" />

  <BlockImage id="appliedenergistics2:tile.BlockAdvancedCraftingStorage:1" scale="4" />

  <BlockImage id="appliedenergistics2:tile.BlockAdvancedCraftingStorage:2" scale="4" />

  <BlockImage id="appliedenergistics2:tile.BlockAdvancedCraftingStorage:3" scale="4" />
</Row>

（必需）合成存储器支持所有标准元件大小（1k、4k、16k、64k、256k）。它们会将与合成相关的材料和中间材料存于自身，因此处理所需材料更多的合成任务需要更大的或更多个合成存储器。

<Column>
  <Row>
    <RecipeFor id="appliedenergistics2:tile.BlockCraftingStorage:0" />

    <RecipeFor id="appliedenergistics2:tile.BlockCraftingStorage:1" />

    <RecipeFor id="appliedenergistics2:tile.BlockCraftingStorage:2" />

    <RecipeFor id="appliedenergistics2:tile.BlockCraftingStorage:3" />
  </Row>

  <Row>
    <RecipeFor id="appliedenergistics2:tile.BlockAdvancedCraftingStorage" />

    <RecipeFor id="appliedenergistics2:tile.BlockAdvancedCraftingStorage:1" />

    <RecipeFor id="appliedenergistics2:tile.BlockAdvancedCraftingStorage:2" />

    <RecipeFor id="appliedenergistics2:tile.BlockAdvancedCraftingStorage:3" />
  </Row>
</Column>

---

# 并行处理单元

<BlockImage id="appliedenergistics2:tile.BlockCraftingUnit:1" scale="4" />

（可选）提升<ItemLink id="appliedenergistics2:tile.BlockInterface" />的原料分发频率，适配高速处理设备（如被多个<ItemLink id="appliedenergistics2:tile.BlockMolecularAssembler" />环绕的样板供应器）。

<RecipeFor id="appliedenergistics2:tile.BlockCraftingUnit:1" />

---

# 合成监控器

<BlockImage id="appliedenergistics2:tile.BlockCraftingMonitor" scale="4" />

（可选）合成监控器会显示CPU当前正在处理的任务。其屏幕可用<ItemLink id="appliedenergistics2:item.ToolColorApplicator" />染色。

<RecipeFor id="appliedenergistics2:tile.BlockCraftingMonitor" />
