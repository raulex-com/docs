---
cover: ../../.gitbook/assets/CoverPage.webp
coverY: 179.55199999999996
layout:
  cover:
    visible: true
    size: hero
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# ⛳ Capture The Flag

## 🏁 Capture the Flag

In this exciting event mod, a flag 🏳️ spawns at a designated location on the map. Players must **control the area** for a set time to successfully capture it. Once captured, the **flag carrier** must transport it to a **hidden destination** (visible only to the carrier). However, the **enemy team** 👥 can track the carrier's position once the flag is picked up.

If the carrier is killed, the flag is dropped and must be **recaptured** after holding the area for a brief period. The flag carrier **cannot use vehicles** 🚶 and must travel on foot. Upon **successfully reaching the target location**, the carrier is rewarded with loot 🎉.\
\


## ⚙️ Configuration Overview

The configuration for the **RaulexCTF** system is divided into four key components:

* **📝 config.yaml**\
  The main configuration file where global settings for the Capture the Flag event are defined.
* **🌍 zones/\<zoneName>.yaml**\
  Each zone has its own configuration file. These files define the specific settings for the different zones in the map, such as spawn locations and capture times.
* **🎁 loot-pool/\<lootpoolName>.yaml**\
  These files define the loot pool for the event, detailing what rewards players can receive upon successfully completing the objective.
* **📦 editor-imports/\<editorexportFile>.dze**\
  These files contain exported data from the editor, allowing for map-specific configurations and settings to be imported easily.
