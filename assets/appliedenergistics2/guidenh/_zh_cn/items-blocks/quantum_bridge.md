---
navigation:
  parent: /items-blocks-index.md
  title: 量子环
  icon: appliedenergistics2:tile.BlockQuantumLinkChamber
categories:
- network infrastructure
item_ids:
- appliedenergistics2:tile.BlockQuantumRing
- appliedenergistics2:tile.BlockQuantumLinkChamber
---

<Row>
<ItemImage id="appliedenergistics2:tile.BlockQuantumRing" scale="4"/>

<ItemImage id="appliedenergistics2:tile.BlockQuantumLinkChamber" scale="4"/>
</Row>

量子环是AE的无线跨维度频道传输方案，具体机制参考[量子环](../ae2-mechanics/quantum-bridge.md)。

# 量子网桥

![已搭建完成的量子网桥](../assets/images/quantum_bridge_demonstration.png)

量子网桥能将[网络](../ae2-mechanics/me-network-connections.md)无限延伸，甚至能跨维度连接。它们能传输共32个频道（无论线缆连接方式如何），可视作无线的[致密线缆](cables.md#dense-cable)。

<GameScene width="400" height="300" zoom="4" showBackground={false}>
  <ImportStructure src="../assets/structures/quantum_bridge_internal_structure_1.snbt" />
  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

<GameScene zoom="4" showBackground={false}>
  <ImportStructure src="../assets/structures/quantum_bridge_internal_structure_2.snbt" />

  <BoxAnnotation color="#33dd33" min="1 1 1" max="6 2 3">
    两端之间的虚拟线缆连接
  </BoxAnnotation>

  <IsometricCamera yaw="195" pitch="30" />
</GameScene>

需要注意，**量子网桥的两端点均需区块加载**，假如两端距离很远，则必须使用<ItemLink id="appliedenergistics2:tile.BlockSpatialPylon" />或再加区块加载器。

# 量子环

<BlockImage id="appliedenergistics2:tile.BlockQuantumLinkChamber" scale="8" />

8个量子环围绕<ItemLink id="appliedenergistics2:tile.BlockQuantumRing" />可构建量子网络桥。仅4个与链接仓直接相邻的量子环可连接网络，角落的4个量子环无法连接线缆。

## 配方

<RecipeFor id="appliedenergistics2:tile.BlockQuantumLinkChamber" />

# 量子链接仓

<BlockImage id="appliedenergistics2:tile.BlockQuantumRing" scale="8" />

该方块被<ItemLink id="appliedenergistics2:tile.BlockQuantumLinkChamber" />环绕后形成量子网络桥。链接仓本身无法连接线缆，仅在完整结构建成后接入网络。

链接仓库存仅可存放1个<ItemLink id="appliedenergistics2:item.ItemMultiMaterial:48" />，支持自动化访问。

## 配方

<RecipeFor id="appliedenergistics2:tile.BlockQuantumRing" />
