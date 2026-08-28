---
navigation:
  parent: /items-blocks-index.md
  title: ME输入总线
  icon: appliedenergistics2:item.ItemMultiPart:240
categories:
- devices
item_ids:
- appliedenergistics2:item.ItemMultiPart:240
- ae2fc:part_fluid_import
- thaumicenergistics:part.base
---

#ME输入总线

<Row>
<ItemImage id="appliedenergistics2:item.ItemMultiPart:240" scale="4"/>

<ItemImage id="ae2fc:part_fluid_import" scale="4"/>

<ItemImage id="thaumicenergistics:part.base" scale="4"/>

</Row>

# ME流体输入总线

<ItemImage id="ae2fc:part_fluid_import" />

输入总线会从其所连接的容器中抽出物品和流体（以及附属添加的其他类型），并存入[网络存储](../ae2-mechanics/import-export-storage.md)。

为减少卡顿，输入总线会在近期未输入的情况下进入某种“睡眠模式”，此时其工作速度较慢，并会在其输入物品时被唤醒并逐渐进入正常状态（每秒传输4次）。

该设备属于[线缆子部件](../ae2-mechanics/cables-subparts.md)。

## 过滤

默认情况下，输入总线会输入所有其能访问的事物。放入其过滤槽的物品会加入白名单，也即只会输入其中指明的事物。

即使未实际拥有某物品，仍可通过NEI将其拖入过滤槽。

用流体容器（如铁桶或流体储罐）右击即可将流体设为过滤，而非铁桶和储罐物品。

## 升级

输入总线支持以下[升级卡](upgrade_cards.md)：
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:27" /> 增加过滤槽数量
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:29" /> 提升单次操作传输量
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:31" /> 将过滤模式切换为黑名单
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:26" /> 添加红石控制（高电平激活/低电平激活/脉冲激活）

## 运行速度

| 加速卡数量 | 单次操作传输量 |
|:-----------|:--------------|
| 0          | 1             |
| 1          | 8             |
| 2          | 32            |
| 3          | 64            |
| 4          | 96            |

## 合成配方

<RecipeFor id="appliedenergistics2:item.ItemMultiPart:240" />