---
navigation:
  parent: /items-blocks-index.md
  title: 石英纤维
  icon: appliedenergistics2:item.ItemMultiPart:140
categories:
- network infrastructure
item_ids:
- appliedenergistics2:item.ItemMultiPart:140
---
<ItemImage id="appliedenergistics2:item.ItemMultiPart:140" scale="4"/>


石英纤维可以附着在线缆任意面上，将附着的[线缆](./cables.md)与附着方向相邻的线缆分开，阻止它们互相传递频道，但是可以传递能量。常用于分隔不同网络或规划[频道路由](../ae2-mechanics/channels.md#频道路由)，也可以用于从某一网络提供能量给[自组织网络](../ae2-mechanics/channels.md#自组织网络)供能。

# 石英纤维

<GameScene zoom="8" showBackground={false}>
<ImportStructure src="../assets/structures/quartz_fiber.snbt" />
<IsometricCamera yaw="195" pitch="30" />
</GameScene>

石英纤维可在[网络](../ae2-mechanics/me-network-connections.md)之间传输能量而不会将其连接起来。也由此不用到处摆能源接收器和供能线缆就能给[子网络](../ae2-mechanics/subnetworks.md)供能了。它也能阻止线缆连接，不过使用异色线缆或者<ItemLink id="appliedenergistics2:item.ItemMultiPart:120" />更便宜也更有效。

该设备属于[线缆子部件](../ae2-mechanics/cables-subparts.md)。

## 配方

<RecipeFor id="appliedenergistics2:item.ItemMultiPart:140" />
