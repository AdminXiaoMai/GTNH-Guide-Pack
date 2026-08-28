---
navigation:
  parent: /ae2-mechanics-index.md
  title: 自动合成
  icon: appliedenergistics2:item.ItemMultiMaterial:52
---

# 自动合成

### 示例设施

<GameScene zoom="3" width="400" height="200" interactive={true}>
  <ImportStructure src="../assets/structures/autocraft_setup_greebles.snbt" />
  <Block id="minecraft:furnace" x="9" y="1" z="0" facing="north" />
  <IsometricCamera yaw="195" pitch="15" />
</GameScene>

自动合成是AE2的基础功能之一。ME系统可以按需合成物品、将合成产物输出到其他位置，也可以自动维持库存数量。它同样支持流体，以及附属模组加入的其他材料类型。

## 组成

自动合成设施由三部分组成：

- **请求源**：由玩家在终端中发起，或由安装合成卡的设备自动发起
- **合成CPU**：计算合成步骤并存放合成所需的材料和中间产物
- **ME样板供应器**：按照样板将材料送入相邻的机器

### 工作流程

1. **发起请求**  
   - 玩家在终端中请求可自动合成的物品
   - 输出总线或接口等安装合成卡的设备请求其配置的物品

   - （**重要：**使用绑定在“选取方块”（通常是鼠标中键）的按键以请求合成库存中已有的事物，可能与物品栏整理模组冲突）

2. **任务规划**  
   ME系统计算请求所需的材料与前置步骤，并将材料存入选定的合成CPU

3. **输出材料**
   ME样板供应器根据[样板](../items-blocks/patterns.md)输出材料：
   - 合成类配方：输送至<ItemLink id="appliedenergistics2:tile.BlockMolecularAssembler" />
   - 加工类配方：对接各类加工设备

4. **返回产物**
   通过输入总线、接口或样板供应器将产物送回网络
   **必须发生一次物品进入网络的操作，单纯存入连接存储总线的容器无效。**

5. **继续合成**
   若产物是其他步骤所需的中间产物，它会存入合成CPU并用于后续步骤

---

# 样板

<ItemImage id="appliedenergistics2:item.ItemEncodedUltimatePattern" scale="4" />

样板是在<ItemLink id="appliedenergistics2:item.ItemMultiPart:340" />中以空白样板制作而得的。

### 样板类型

* **合成样板**  
  编码工作台配方，可直接放入<ItemLink id="appliedenergistics2:tile.BlockMolecularAssembler" />，通常与ME样板供应器配合使用

***

* **锻造样板**  
  处理锻造台配方，工作逻辑与合成样板完全一致

***

* **切石样板**  
  对应切石机配方，三类基础样板可混用同一系统

***

* **处理样板**  
  用于工作台以外的加工流程：
  - 可对接任何模组机器
  - 只要求系统最终收到样板中设定的产物，不关心材料经历了何种处理
  - 支持批量处理（8圆石→8石头）

---

# 不需要输入材料的自动合成

安装合成卡的<ItemLink id="appliedenergistics2:item.ItemMultiPart:280" />可设置为发出红石信号以请求合成物品。它不定义输入材料，适合控制农场或圆石复制机等无需输入材料的生产设施。

---

# 合成CPU

<GameScene width="350" height="220" zoom="4" showBackground={false}>
  <ImportStructure src="../assets/structures/crafting_cpus.snbt" />
  <IsometricCamera yaw="195" pitch="15" />
</GameScene>

### 组成

- **合成存储器**（必需）：提供1k/4k/16k/64k/256k存储容量，存放合成材料和中间产物
- **并行处理单元**（可选）：提高材料批次的发送速度和可并行执行的步骤数量
- **合成监控器**（可选）：显示当前任务
- **合成单元**（可选）：填充多方块结构中的空隙

每个合成CPU一次只能处理一个任务。它可以设置为只接受玩家请求、只接受自动化设备请求，或接受全部请求。

---

# ME样板供应器

<Row>
   - <BlockImage id="appliedenergistics2:tile.BlockInterface" scale="4" /> 
   - <BlockImage id="ae2fc:fluid_interface" scale="4" />
<GameScene width="220" zoom="3" zoom="4" align="center" showBackground={false}>
  <ImportStructure src="../assets/structures/cable_pattern_provider.snbt" />
  <IsometricCamera yaw="30" pitch="30" />
</GameScene>
</Row>

### 变种

1. **普通型**
   - 全向推送材料
   - 接收各面输入
   - 提供网络连接

2. **定向型**（使用扳手调整）  
   - 单面推送
   - 屏蔽连接面网络
   - 适合构建子网

3. **面板型**（线缆子部件）
   - 多设备共线安装
   - 功能同定向型

### 设置

- **阻塞模式**：设备未清空前暂停推送
- **合成锁定**：红石条件控制
- **终端可见性**：配置<ItemLink id="appliedenergistics2:item.ItemMultiPart:480" />显示

多个样板能合成同一物品时，系统会优先使用优先级较高的样板供应器；若网络无法提供该样板所需的材料，则会尝试较低优先级的样板。

---

# 分子装配室

<ItemImage id="appliedenergistics2:tile.BlockMolecularAssembler" scale="4" />

<GameScene width="300" height="200" zoom="4" showBackground={false}>
<ImportStructure src="../assets/structures/assembler_tower.snbt" />
<IsometricCamera yaw="195" pitch="30" />
</GameScene>

### 功能

- 解析相邻样板供应器的指令
- 自动将成品推送至周边容器
- 支持直接插入合成/锻造/切石样板

样板供应器可将材料分发给相邻的多个分子装配室，从而并行完成合成。
