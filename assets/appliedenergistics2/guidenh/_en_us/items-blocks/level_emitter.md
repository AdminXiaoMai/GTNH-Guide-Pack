---
navigation:
  parent: /items-blocks-index.md
  title: ME Level Emitter
  icon: appliedenergistics2:item.ItemMultiPart:280
categories:
- devices
item_ids:
- appliedenergistics2:item.ItemMultiPart:280
---

# Level Emitter

<ItemImage id="appliedenergistics2:item.ItemMultiPart:280" scale="4" />

The level emitter emits a redstone signal based on the amount of an item in [network storage](../ae2-mechanics/import-export-storage.md). A variant emits according to the network's [energy](../ae2-mechanics/energy.md) level. Items and fluids can be dragged into the filter slot from JEI/REI, or a fluid can be selected by right-clicking with a fluid container.

Level emitters are [cable subparts](../ae2-mechanics/cables-subparts.md) and, unlike most [devices](../ae2-mechanics/devices.md), do not require a [channel](../ae2-mechanics/channels.md).

## Settings

* The emitter supports “greater than or equal to” and “less than” modes.
* With <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:53" />, it can emit while an item is being crafted or emit a signal to craft the item.

## Upgrades

* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:29" /> enables fuzzy matching and NBT-ignoring filters.
* <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:53" /> enables crafting functionality.

## Crafting Functionality

With the crafting card installed, the emitter enters crafting mode. “Emit while crafting” turns on redstone while [autocrafting](../ae2-mechanics/autocrafting.md) is making the filtered item through an <ItemLink id="appliedenergistics2:tile.BlockInterface" />. “Emit to craft item” creates a virtual [pattern](patterns.md) with no ingredients; requesting that item emits redstone from this emitter. Do not also place a real pattern for the same item in an interface.

This is useful for infinite farms or machines with probabilistic output, and for [recursive recipes](../tricks-example/recursive-crafting-setup.md) such as “1 cobblestone = 2 cobblestone”.

## Recipe

<RecipeFor id="appliedenergistics2:item.ItemMultiPart:280" />


