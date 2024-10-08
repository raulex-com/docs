# 🌎 zone.yaml

### 🗺️ Zone Schema Overview

The **zone schema** defines the configuration for each zone within the Capture the Flag event. It consists of several key components:

* **zoneName**: (string) The name of the zone, which must be at least one character long.
* **zone**: (optional object) Contains specific settings related to the zone, including:
  * **flagClassName**: (string) The class name of the flag used in this zone.
  * **returnRadius**: (integer) The radius (in meters) within which the flag can be returned.
  * **captureTime**: (integer) The time (in seconds) required to capture the flag.
  * **captureRadius**: (integer) The radius (in meters) within which players must remain to capture the flag.
  * **recaptureRadius**: (integer) The radius (in meters) within which the flag must be recaptured if dropped.
  * **recaptureTime**: (integer) The time (in seconds) required to recapture the flag.
  * **broadCastRadius**: (integer) The radius (in meters) within which the flag capture progress is visible to other players.&#x20;
  * **beepSoundName**: (string) The sound played when the flag is picked up or dropped.
  * **timeToReturnFlag:** (integer) Time (in seconds) before mission times out if flag has not reached the destination after capture.
  * **zombieConfig**: (optional object) Configuration settings for zombies in the zone, including:
    * **numWaves**: (integer) The number of zombie waves that will spawn.
    * **min**: (integer) Minimum number of zombies in each wave.
    * **max**: (integer) Maximum number of zombies in each wave.
    * **zombieTypes**: (array of strings) The types of zombies that can spawn.
* **initialSpawnPoints**: (array) A list of initial spawn points, each with a position and optional editor file name.
* **returnPoints**: (array) A list of points where the flag can be returned, each with:
  * **pos**: (string) The position for returning the flag, which can also be a string representing coordinates or the string `"random"`.
  * **editorFileName**: (optional string) An optional file name for the DayZ Editor Exports.
  * **crates**: (array) A list of crates associated with the return point, each with:
    * **crateName**: (string) The name of the crate.
    * **cratePos**: (string) The position of the crate, which can also be a string representing coordinates or the string `"random"`.
    * **crateDir**: (string) The direction of the crate.
    * **makeStatic**: (optional boolean) Whether the crate is static.
    * **lootPool**: (array of strings) The loot pool names associated with the crate.

This schema ensures that each zone in the Capture the Flag event is properly configured with necessary settings for gameplay, including spawn points, flag mechanics, and potential zombie encounters.

### 🗺️ Example Zone YAML Configuration

Below is an example of a **zone.yaml** configuration file for the Capture the Flag event:

```yaml
zoneName: CTF Zone
zone:
  flagClassName: RaulexCTFFlagV2
  returnRadius: 5
  captureRadius: 30
  captureTime: 5
  recaptureRadius: 15
  recaptureTime: 10
  broadCastRadius: 60
  beepSoundName: CTFFlagBeepSound
  timeToReturnFlag: 3600                # Time (in seconds) before mission times out if flag has not reached the destination after capture.
  zombieConfig:
    numWaves: 2
    min: 2
    max: 5
    zombieTypes:
      - ZmbM_NBC_Yellow
      - ZmbM_NBC_Grey
      - ZmbM_Mummy
initialSpawnPoints:
  - pos: random
returnPoints:
  - pos: 8422.0 6.325613021850586 3002.80078125
    crates:
      - crateName: SeaChest | RedemptionMilitaryCrate
        cratePos: 8422.0 6.325613021850586 3002.80078125
        crateDir: 0 0 0
        makeStatic: false
        lootPool:
          - Default
```
