---
navigation:
  parent: /items-blocks-index.md
  title: 网络工具
  icon: appliedenergistics2:item.ToolNetworkTool
categories:
- tools
item_ids:
- appliedenergistics2:item.ToolNetworkTool
- appliedenergistics2:item.ToolAdvancedNetworkTool
---

# 网络工具

<ItemImage id="appliedenergistics2:item.ToolNetworkTool" scale="4" />

网络工具是修改版本的[扳手](wrench.md)，它能显示网络诊断信息，也能存储[升级卡](upgrade_cards.md)。它仍保留了扳手拆卸[子部件](../ae2-mechanics/cables-subparts.md)等事物的能力，但无法再旋转方块。

内置9个升级卡槽位，当工具在物品栏时，所有AE2设备界面均可访问这些升级卡。

右键点击网络任意部分将显示诊断窗口（类似右键<ItemLink id="appliedenergistics2:tile.BlockController" />），包含：
* 网络中已使用的频道数
* 全局能源单位切换（AE/E/FE）
* 网络存储的[能源](../ae2-mechanics/energy.md)量及最大容量
* 能源输入/消耗速率
* 网络中所有[设备](../ae2-mechanics/devices.md)和组件的列表

该窗口在调试[子网](../ae2-mechanics/subnetworks.md)时，可帮助确认不同线缆/设备是否属于同一网络。

## 隐藏伪装板

手持网络工具时，<a href="facades.md">伪装板</a>将被隐藏。

此时可以直接与隐藏的伪装板后方的方块交互，无需取下伪装板。

## 配方

<RecipeFor id="appliedenergistics2:item.ToolNetworkTool" />
