---
navigation:
  parent: /items-blocks-index.md
  title: 充能器
  icon: appliedenergistics2:tile.BlockCharger
categories:
- machines
item_ids:
- appliedenergistics2:tile.BlockCharger
---

# 充能器

<ItemImage id="appliedenergistics2:tile.BlockCharger" scale="4" />

充能器可以为兼容工具充能，也能将<ItemLink id="gregtech:gt.metaitem.01:8516" />转化为<ItemLink id="appliedenergistics2:item.ItemMultiMaterial:1" />。

需从顶部或底部为其供能，可以使用AE2线缆或其他模组的能源线缆。物品可从任意面输入或输出，且只有完成充能的产物才会被抽出，因此无需设置过滤。可用<ItemLink id="appliedenergistics2:item.ToolCertusQuartzWrench" />旋转充能器以配合自动化。

## 主要用途

* 制作充能水晶：<ItemImage id="gregtech:gt.metaitem.01:8516" /><ItemLink id="gregtech:gt.metaitem.01:8516" /> → <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:1" />
* 制作陨石罗盘：<ItemImage id="minecraft:compass" /><ItemLink id="minecraft:compass" /> → <ItemLink id="appliedenergistics2:tile.BlockSkyCompass" />
* 村民职业工作站

## 手动充能

~~在顶部/底部安装<ItemLink id="appliedenergistics2:item.ItemMultiMaterial:46" />，右键转动曲柄直至物品完成充能。~~

## 简单自动化

充能器可以通过调整朝向实现半自动化：

<GameScene zoom="4" showBackground={false}>
  <ImportStructure src="../assets/structures/charger_hopper.snbt" />
  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

## 配方

<RecipeFor id="appliedenergistics2:tile.BlockCharger" />
