---
navigation:
  parent: ../tricks_example_index.md
  title: 自动时运矿石机
  icon: minecraft:raw_iron
---

# 自动化时运挖掘矿石

<ItemLink id="appliedenergistics2:item.ItemMultiPart:300" />接受所有镐魔咒，包括时运，因此其常见用途之一便是给几个面板附上时运，并让<ItemLink id="appliedenergistics2:item.ItemMultiPart:320" />和<ItemLink id="appliedenergistics2:item.ItemMultiPart:300" />迅速放置和破坏矿石。

注意，<ItemLink id="appliedenergistics2:item.ItemMultiPart:240" />的运行速度会“缓慢增加”：此设施在启动时较慢，并会在几秒后达到最大速度。

<GameScene zoom="6" interactive={true}>
  <ImportStructure src="../assets/structures/ore_fortuner.snbt" />

  <BoxAnnotation color="#dddddd" min="2.7 0 2" max="3 1 3">
        （1）输入总线：装有若干加速卡。
<ItemImage id="appliedenergistics2:item.ItemMultiMaterial:30" scale="2" />
  </BoxAnnotation>

  <BoxAnnotation color="#dddddd" min="0 0 2" max="2 1 2.3">
        （2）成型面板：默认配置。
  </BoxAnnotation>

  <BoxAnnotation color="#dddddd" min="0 0 0.7" max="2 1 1">
        （3）破坏面板：无可用GUI，但可附有时运。
  </BoxAnnotation>

  <BoxAnnotation color="#dddddd" min="2.7 0 0" max="3 1 1">
        （4）存储总线：默认配置。
  </BoxAnnotation>

<DiamondAnnotation pos="3.5 0.5 2.5" color="#00ff00">
        输入
    </DiamondAnnotation>

<DiamondAnnotation pos="3.5 0.5 0.5" color="#00ff00">
        输出
    </DiamondAnnotation>

<DiamondAnnotation pos="4 0.5 1.5" color="#00ff00">
        至主网络
    </DiamondAnnotation>

  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

## 配置

*   <ItemLink id="appliedenergistics2:item.ItemMultiPart:240" />（1）中装有若干<ItemLink id="appliedenergistics2:item.ItemMultiMaterial:23" />。阵列内成型面板越多则所需加速卡也越多，可使总线一次性拿取更多物品。
*   <ItemLink id="appliedenergistics2:item.ItemMultiPart:320" />（2）处于默认配置。
*   <ItemLink id="appliedenergistics2:item.ItemMultiPart:300" />（3）没有GUI且无法配置，附有时运。
*   <ItemLink id="appliedenergistics2:item.ItemMultiPart:220" />（4）处于默认配置。

## 工作原理

1.  绿色子网络上的<ItemLink id="appliedenergistics2:item.ItemMultiPart:240" />将方块从第一个木桶中输入[网络存储](../ae2_mechanics/import_export_storage.md)。
2.  绿色子网络上的存储位置仅有<ItemLink id="appliedenergistics2:item.ItemMultiPart:320" />，它们会放置方块。
3.  橙色子网络上的<ItemLink id="appliedenergistics2:item.ItemMultiPart:300" />用于破坏方块，需给它们附上时运。
4.  橙色子网络上的<ItemLink id="appliedenergistics2:item.ItemMultiPart:220" />将破坏产物存入第二个木桶。
