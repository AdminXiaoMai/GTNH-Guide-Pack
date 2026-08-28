---
navigation:
  parent: /items-blocks-index.md
  title: ME输出总线
  icon: appliedenergistics2:item.ItemMultiPart:260
categories:
- devices
item_ids:
- appliedenergistics2:item.ItemMultiPart:260
- ae2fc:part_fluid_export
- thaumicenergistics:part.base:3
---

<Row>

<ItemImage id="appliedenergistics2:item.ItemMultiPart:260" scale="4" />

<ItemImage id="ae2fc:part_fluid_export" scale="4" />

<ItemImage id="thaumicenergistics:part.base:3" scale="4" />
</Row>


# ME流体输出总线

输出总线会从[网络存储](../ae2-mechanics/import-export-storage.md)中抽出物品和流体（以及附属添加的其他类型），并存入其所连接的容器。

为减少卡顿，输出总线会在近期未输出的情况下进入某种“睡眠模式”，此时其工作速度较慢，并会在其输出物品时被唤醒并逐渐进入正常状态（每秒传输4次）。

属于[线缆子部件](../ae2-mechanics/cables-subparts.md)。

## 过滤

默认情况下，输出总线不会输出任何东西。放入其过滤槽的物品会加入白名单，也即只会输出其中指明的事物。

可通过NEI将物品或流体直接拖入过滤槽（无需实际持有该物品）。

用流体容器（如铁桶或流体储罐）右击即可将流体设为过滤，而非铁桶和储罐物品。

## 升级

输出总线支持以下[升级](upgrade_cards.md)：

* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:27" /> 增加过滤槽数量
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:29" /> 提升单次操作传输量
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:31" /> 将过滤模式切换为黑名单
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:53" />：向[自动合成系统](../ae2-mechanics/autocrafting.md)发起合成请求，可配置优先使用现存物品或强制合成新物品
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:26" /> 添加红石控制（高电平激活/低电平激活/脉冲激活）

## 传输速率

| 加速卡数量 | 每次操作传输量 |
|:-----------|:--------------|
| 0          | 1             |
| 1          | 8             |
| 2          | 32            |
| 3          | 64            |
| 4          | 96            |

## 配方

<RecipeFor id="appliedenergistics2:item.ItemMultiPart:260" />