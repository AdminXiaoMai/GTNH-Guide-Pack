---
navigation:
  parent: /items-blocks-index.md
  title: 监控器
  icon: appliedenergistics2:item.ItemMultiPart:400
categories:
- devices
item_ids:
- appliedenergistics2:item.ItemMultiPart:400
- appliedenergistics2:item.ItemMultiPart:420
- ae2fc:part_fluid_storage_monitor
- ae2fc:part_fluid_conversion_monitor
- appliedenergistics2:item.ItemMultiPart:410
---

# ME监控器

<GameScene zoom="8" showBackground={false}>
<ImportStructure src="../assets/structures/monitors.snbt" />
<IsometricCamera yaw="195" pitch="30" />
</GameScene>

监控器可在不打开GUI的情况下展示单种物品或流体，并允许与其交互。

监控器会继承支持其的[线缆](cables.md)的颜色。

若安装在地面或天花板，可使用<ItemLink id="appliedenergistics2:item.ToolCertusQuartzWrench" />旋转方向。

该设备属于[线缆子部件](../ae2-mechanics/cables-subparts.md)。

# ME存储监控器

能显示单种物品或流体，以及其数量。在农场之类的设施旁放几个比较好……

*不需要*占用[频道](../ae2-mechanics/channels.md)。

操作指令：
* 右键持有物品/双击流体容器：设置监控物品
* 空手右键：清空监控目标
* Shift+空手右键：锁定当前配置

## 合成配方

<RecipeFor id="appliedenergistics2:item.ItemMultiPart:400" />

# ME交换监控器

在存储监控功能基础上，支持物品存取操作。当配置物品[可自动合成](../ae2-mechanics/autocrafting.md)且库存为零时，提取操作将触发合成界面。

*需要*占用[频道](../ae2-mechanics/channels.md)。

扩展操作指令：
* 左键点击：提取整组物品（库存不足时触发合成）
* 持有物品右键：存入物品
* 空手右键：存入背包中所有匹配物品

## 合成配方

<RecipeFor id="appliedenergistics2:item.ItemMultiPart:420" />
