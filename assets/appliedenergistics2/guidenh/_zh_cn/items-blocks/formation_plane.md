---
navigation:
  parent: /items-blocks-index.md
  title: ME成型面板
  icon: appliedenergistics2:item.ItemMultiPart:320
categories:
- devices
item_ids:
- appliedenergistics2:item.ItemMultiPart:320
---


 成型面板

<Row gap="20">
<ItemImage id="appliedenergistics2:item.ItemMultiPart:320" scale="4" />
<ItemImage id="ae2fc:part_fluid_formation_plane" scale="4" />
</Row>

成型面板用于放置方块和丢弃物品。其功能类似仅允许存入的<ItemLink id="appliedenergistics2:item.ItemMultiPart:220" />，当[设备](../ae2-mechanics/devices.md)（如<ItemLink id="appliedenergistics2:item.ItemMultiPart:240" />和<ItemLink id="appliedenergistics2:tile.BlockInterface" />）向[网络存储](../ae2-mechanics/import-export-storage.md)存入物品时触发放置/丢弃操作。

<GameScene width="220" height="150" zoom="4" interactive={true}>
  <ImportStructure src="../assets/structures/formation_plane_demonstration.snbt" />
  <IsometricCamera yaw="-30" pitch="30" />
</GameScene>

该[设备](../ae2-mechanics/devices.md)利用了[管道子网](../tricks-example/pipe-subnet.md)中存储总线的机制，若需要丢弃物品/放置方块而非运输物品，可用其替代存储总线。

成型面板属于[线缆子部件](../ae2-mechanics/cables-subparts.md)。

**请确保在领地插件中启用假玩家权限**

## 过滤设置

默认情况下会放置/丢弃所有物品。在过滤槽中放入物品将启用白名单模式，仅允许指定物品被放置。

即使未实际拥有某物品，仍可通过JEI/REI将其拖入过滤槽。

右键点击流体容器（如桶或储罐）可设置流体过滤器而非容器物品本身。

## 优先级

单击GUI右上角扳手图标以设置优先级。进入网络的物品会优先送至优先级最高的存储位置。

## 设置

* 成型面板可设置为放置方块或投出物品。

## 升级

成型面板支持以下[升级卡](upgrade_cards.md)：
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:27" />：增加过滤槽数量
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:29" />：支持按耐久度过滤或忽略物品NBT
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:31" />：将过滤模式从白名单切换为黑名单

## 合成配方

<RecipeFor id="appliedenergistics2:item.ItemMultiPart:320" />
