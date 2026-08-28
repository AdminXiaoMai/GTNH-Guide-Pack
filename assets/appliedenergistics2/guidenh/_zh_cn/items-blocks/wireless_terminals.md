---
navigation:
  parent: /items-blocks-index.md
  title: 无线终端
  icon: appliedenergistics2:item.ToolWirelessTerminal
categories:
- tools
item_ids:
- appliedenergistics2:item.ToolWirelessTerminal
- ae2fc:wireless_interface_terminal
- ae2fc:wireless_fluid_pattern_terminal
- ae2fc:wireless_level_terminal
- ae2wct:wirelessCraftingTerminal
- ae2fc:wireless_ultra_terminal
---

# 无线终端

<Row>
  <ItemImage id="appliedenergistics2:item.ToolWirelessTerminal" scale="4" />
  <ItemImage id="ae2wct:wirelessCraftingTerminal" scale="4" />
  <ItemImage id="ae2fc:wireless_ultra_terminal" scale="4" />
</Row>

<Row>
  <ItemImage id="ae2fc:wireless_interface_terminal" scale="4" />
  <ItemImage id="ae2fc:wireless_fluid_pattern_terminal" scale="4" />
  <ItemImage id="ae2fc:wireless_level_terminal" scale="4" />
</Row>

无线终端是普通有线[终端](terminals.md)的便携版本。它们的UI完全一致，不过无线终端只有[升级卡](upgrade_cards.md)槽，而无<ItemLink id="appliedenergistics2:item.ItemViewCell" />槽。

可将终端放入<ItemLink id="appliedenergistics2:tile.BlockWireless" />右上角槽位（带有无线终端图标且下方有箭头）以与访问点所在的网络配对。

需处于<ItemLink id="appliedenergistics2:tile.BlockWireless" />的信号范围内方可使用，可在<ItemLink id="appliedenergistics2:tile.BlockCharger" />（充能器）中补充能量。

# 基础无线终端

<ItemImage id="appliedenergistics2:item.ToolWirelessTerminal" scale="4" />

基础终端，但是是便携版！可在<ItemLink id="appliedenergistics2:tile.BlockWireless" />范围内任何地方访问[网络存储](../ae2-mechanics/import-export-storage.md)，或是向[自动合成](../ae2-mechanics/autocrafting.md)设施发送请求。

## 界面

见[终端](terminals.md)。

## 配方

<RecipeFor id="appliedenergistics2:item.ToolWirelessTerminal" />

# 无线合成终端

<ItemImage id="ae2wct:wirelessCraftingTerminal" scale="4" />

在基础无线终端功能上增加合成网格，可自动从[网络存储](../ae2-mechanics/import-export-storage.md)补充材料。Shift+点击输出槽需谨慎！

## 界面

见[终端](terminals.md)。

## 升级

支持以下[升级卡](upgrade_cards.md)：
* <ItemLink id="ae2wct:infinityBoosterCard" />：在任意世界
* <ItemLink id="ae2wct:magnetCard" />：提升电池容量


## 配方

<RecipeFor id="ae2wct:wirelessCraftingTerminal" />
