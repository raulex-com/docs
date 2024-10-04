# 🎁 lootpool.yaml

### 🎁 Loot Pool YAML Schema Overview

The **lootpool.yaml** file defines the configuration for loot pools within the Capture the Flag event. It specifies how loot items are generated and distributed, ensuring players receive appropriate rewards. The schema consists of the following key components:

#### 🔑 Schema Components

* **lootPoolName**: (string) The name of the loot pool. This must be at least one character long.
* **inventory**: (optional array) A collection of loot items within the pool, each defined by the **inventorySchema**. The default value is an empty array if not specified. Each item in the inventory can have the following properties:
  * **min**: (number, optional) The minimum quantity of this item that can be awarded.
  * **max**: (number, optional) The maximum quantity of this item that can be awarded.
  * **item**: (string, optional) The name or identifier of the item being awarded.
  * **qty**: (number, optional) The specific quantity of this item that can be awarded.
  * **noDuplicates**: (boolean, optional) A flag indicating whether duplicate items are allowed in the loot. The default value is `false`.
  * **chance**: (number, optional) The probability of this item being awarded when loot is generated.
  *   **inventory**: (optional array) An array of further nested loot items, allowing for complex loot structures (e.g., loot bags containing multiple items).\
      \


      > **⚠️** If both **min** and **max** are not present for an item in the inventory, all items in that inventory will be spawned when the loot is generated.

#### 📜 Example of a Loot Pool Configuration

```yaml

lootPoolName: Default
inventory:
  - min: 1
    max: 2
    noDuplicates: true
    inventory:
      - item: SVD
        chance: 100
        inventory:
          - item: PSO11Optic
      - item: M4A1
        chance: 100
        inventory:
          - item: Mag_STANAG_60Rnd
  - noDuplicates: false
    inventory:
      - item: Flashlight
        inventory:
          - item: Battery9V
```
