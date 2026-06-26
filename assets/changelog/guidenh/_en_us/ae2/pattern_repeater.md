---
item_ids:
  - appliedenergistics2:item.ItemMultiPart:473
navigation:
  title: Patter Repeater
  parent: ae2.md
  icon: appliedenergistics2:item.ItemMultiPart:473
categories:
    - Applied Energistics 2
author: Skorched
date: 2026-06-26
---

# Pattern Repeater
The <Color id="GREEN">Pattern Repeater</Color> is a somewhat niche, but incredibly powerful tool if used well. Put simply, it allows recipes to be visible across networks.

If two networks are linked via pattern repeaters, you can have a pattern in one network (A) be visible in a subnetwork (B). This means that a machine living on network B can be requested from network A!

To set this up, just make 2 pattern repeaters facing into each other and use a wrench to toggle one to <Color id="BLUE">Provider</Color> mode, and the other to <Color id="RED">Accessor</Color> mode. <Color id="RED">Accessor</Color> side is where the original pattern will live, and the <Color id="BLUE">Provider</Color> side is the network that will get access to that pattern.

This allows the user to request the recipe that lives in network B from network A!
