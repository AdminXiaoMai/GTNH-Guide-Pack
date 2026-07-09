---
navigation:
  title: 共享勘探
  parent: qol.md
  icon: gregtech:gt.detrav.metatool.01:100
categories:
    - Quality Of Life
author: Skorched
date: 2026-05-16
---

# 共享勘探

Visual Prospecting 在多人游戏里的工作方式这次做了大幅体验优化。新发现的勘探结果现在会立刻共享给同一队伍里的所有成员（准确说，是同一个 [GTNH Team](../misc/gtnh_teams.md) 的成员）。

以前用过 <Color id="RED">Shared Prospecting</Color> 的玩家，功能逻辑可以理解成差不多，但这次是正式整合、可用而且经过优化的版本。

另外，为了让地下流体勘探结果更容易区分，现在每种流体都会带有彩色覆盖层，颜色与高阶探矿工具里显示的颜色保持一致。

作为这次重构的一部分，还加入了下面这些命令：

| Command | Permission Level | Effect |
| --------------- | --------------- | --------------- |
| `/vp_client_cache_reset` | - | 重置客户端本地勘探缓存 |
| `/vp team info [detailed]` | 0 | 显示你所在队伍的信息 |
| `/vp_team_info <player> [detailed]` | 2 | 显示目标玩家所在队伍的信息 |
| `/vp_admin team upload <player>` | 2 | 将一名玩家本地缓存里的勘探结果上传到队伍数据 |
| `/vp_admin team clear` | 2 | 清空队伍勘探数据 |
| `/vp_admin servercache rebuild all` | 4 | 在服务端重建全部缓存 |
| `/vp_admin servercache rebuild spawn` | 4 | 在服务端重建出生点区块的缓存 |
