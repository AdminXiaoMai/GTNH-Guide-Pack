---
navigation:
  parent: /items-blocks-index.md
  title: 破坏面板
  icon: appliedenergistics2:item.ItemMultiPart:300
categories:
- devices
item_ids:
- appliedenergistics2:item.ItemMultiPart:300
- appliedenergistics2:item.ItemMultiPart:301
---

# ME破坏面板

<GameScene zoom="8" showBackground={false} interactive={false}>
<ImportStructure src="../assets/structures/annihilation_plane.snbt" />
</GameScene>

ME破坏面板具备破坏方块与收集物品的功能，其工作原理类似<ItemLink id="appliedenergistics2:item.ItemMultiPart:240" />，将物品存入[网络存储](../ae2-mechanics/import-export-storage.md)。物品需接触面板正面方可被收集，不作用于区域范围。

可为其附加镐类附魔：时运附魔可用于自动化矿物处理（需整合包支持）；精准采集按预期工作；效率降低能耗；耐久提供免耗能概率。

属于[线缆组件](../ae2-mechanics/cables-subparts.md)。

**请确保在领地插件中启用假人权限**

## 过滤

破坏面板只会在掉落物或物品能存入网络时破坏方块或捡起物品。也即*需要限制其网络中可存储物品的种类*才能过滤破坏面板，通常会将其放在[子网络](../ae2-mechanics/subnetworks.md)中。使用<ItemLink id="appliedenergistics2:item.ItemMultiPart:220" />或设置[分区](cell_workbench.md)的[元件](../items-blocks/storage_cells.md)可达成这一点。

<GameScene width="300" height="200" zoom="6" interactive={true}>
  <ImportStructure src="../assets/structures/annihilation_filtering.snbt" />

  <DiamondAnnotation pos="1 0.5 0.5" color="#00ff00">
    过滤目标方块的掉落物
  </DiamondAnnotation>

  <DiamondAnnotation pos=".5 0.5 2.5" color="#00ff00">
    对掉落物进行存储分区
  </DiamondAnnotation>

  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

破坏面板过滤的是*掉落物*。因此假如要设置仅破坏<ItemLink id="etfuturum:amethyst_cluster_2:6" />，则面板必须附有精准采集。未长成的紫晶芽什么都不会掉落，而网络永远能存下“空气”，因此普通的破坏面板会一直破坏它们。

## 合成配方

<RecipeFor id="appliedenergistics2:item.ItemMultiPart:300" />
