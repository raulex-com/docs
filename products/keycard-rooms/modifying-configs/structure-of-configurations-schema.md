# 🏗️ Config Structure

## 🚪 Door Structure

```json
{
    "locationName": "VMC T5 Door", /* A unique name used as a reference. */
    "buildingName": "Land_KlimaX_T5Door", /* The classname of the building or the door*/
    "buildingPos": [
        3759.030029296875,
        316.5320129394531,
        8920.0302734375
    ], /* Position of the building */
    "buildingDir": [
        25.109928131103516,
        0,
        0
    ], /* Orientation of the building */
    "doorIndex": 0, /* The door to lock (Use DayZEditor or the converter tool to find this number.) */
    "openFor": 300, /* Time the door should be open for. */
    "openDelay": 5, /*  Time before the door is opened after a card swipe. */
    "closeOnRestart": true, /* Should the door be automatically closed after restart. */
    "onOpenNotificationMessage": "T5 Door at VMC has been opened!", /* Notification to be shown to all players once the door has been opened.*/
    "keyCards": [
        "RedemptionKeyCard_05",
        "Banana",
        "MyCustomKeyCard_01"
    ], /* The item(s) that can be used to open the door. */
    "crates": [
        {
            "crateName": "RedemptionMilitaryCrate", /* Storage Item classanme to spawn*/
            "cratePos": [
                3757.509033,
                316.549225,
                8922.211914
            ], /* Crate position*/
            "crateDir": [
                -45,
                0,
                0
            ], /* Crate Orientation*/
            "lootPool": [
                "Snipers",
                "Shotguns",
                "Keys"
            ] /* Loot Pools to spawn.*/
        },
        {
            "crateName": "RedemptionMilitaryCrate",
            "cratePos": [
                3759.509033,
                314.549225,
                8921.211914
            ],
            "crateDir": [
                90,
                0,
                0
            ],
            "lootPool": [
                "AssaultRifles",
                "SNAFU_Weapons",
                "Tier5Money"
            ]
        }
    ] /* Crate(s) to spawn once door is opened. */
}
```

## 📦 Loot Pool Structure

```json
{
    "randomRewards": { /* These items spawns 100% */
        "minItems": 2, /* Minimum number of items to choose from the entries. */
        "maxItems": 3, /* Maximum number of items to choose from the entries. */
        "entries": [
            {
                "itemName": "SVD", /* Classname of item*/
                "attachments": [
                    "PSO11Optic" /* Attachments to spawn with the item.*/
                ],
                "quantity": 1,
                "weight": 1000 /* 1000 -> very common */
            },
            {
                "itemName": "RPG", 
                "attachments": [],
                "quantity": 1,
                "weight": 100 /* 100 -> rare */
            },
            {
                "itemName": "ItemRuby",
                "attachments": [],
                "quantity": 1,
                "weight": 10 /* 10 -> very rare*/
            },
            {
                "itemName": "MoneyRuble100",
                "attachments": [],
                "quantity": 250,
                "weight": 500 /* Common */
        ]
    },
    "fixedRewards": { /* These items spawns 100% */
        "entries": [
            {
                "itemName": "Flashlight",
                "attachments": [
                    "Battery9V"
                ],
                "quantity": 1
            }
        ]
    },
    "lootPoolName": "Tier1" /* Name of this lootPool */
}
```

## ⚙️Global Config

```json
{
    "alarm": {
        "alarmName": "RaulexKeyCard_DoorAlarm", /* Name of alarm, this should reflect your definitions in config.cpp */
        "alarmRange": 500, /* How far(metres) should the alarm be played to. */
        "alarmDuration": 60 /* Time alarm will be played for. */
    },
    "closingAlarm": { /* Closing alarm if required. */
        "alarmName": "RaulexKeyCard_DoorAlarm",
        "alarmRange": 200,
        "alarmDuration": 30,
    },
    "numUses": 1 /* Number of times a keycard item can be used on the door. */
}
```
