# 🗒️ config.yaml

### ⚙️ Config YAML Overview

The **config.yaml** file serves as the primary configuration for the Capture the Flag event, defining global settings and zone-specific parameters. It consists of the following key components:

* **minPlayersRequired**: (integer) The minimum number of players required to start the event. Must be a non-negative integer.
* **startupWaitTime**: (integer) The time (in seconds) to wait before starting the event after the required number of players has joined. Must be a non-negative integer.
* **nextEventWaitTime**: (integer) The time (in seconds) to wait before the next event begins after the current event ends. Must be a non-negative integer.
* **zone**: (object) This section contains configuration settings specific to the zone, including:
  * **flagClassName**: (string) The class name of the flag used in the zone. Must be at least one character long.
  * **returnRadius**: (integer) The radius (in meters) within which the flag can be returned. Must be a positive integer.
  * **captureTime**: (integer) The time (in seconds) required to capture the flag. Must be a positive integer.
  * **captureRadius**: (integer) The radius (in meters) within which players must remain to capture the flag. Must be a positive integer.
  * **recaptureRadius**: (integer) The radius (in meters) within which the flag must be recaptured if dropped. Must be a positive integer.
  * **recaptureTime**: (integer) The time (in seconds) required to recapture the flag. Must be a positive integer.
  * **broadCastRadius**: (integer) The radius (in meters) within which the flag carrier's status is visible to other players. Must be a positive integer.
  * **beepSoundName**: (string) The name of the sound played when the flag is picked up or dropped. Must be at least one character long.
  * **zombieConfig**: (object) Configuration settings for zombies in the zone, including:
    * **numWaves**: (integer) The number of zombie waves that will spawn. Must be a non-negative integer.
    * **min**: (integer) Minimum number of zombies in each wave. Must be a non-negative integer.
    * **max**: (integer) Maximum number of zombies in each wave. Must be a non-negative integer.
    * **zombieTypes**: (array of strings) The types of zombies that can spawn in this zone.

This configuration structure allows for detailed customization of gameplay mechanics, enabling the event to be tailored to the desired player experience while ensuring essential gameplay rules are clearly defined.

### 🗺️ Example Configuration

Below is an example configuration for the **zone** object within the `config.yaml` file:

```yaml
zone:
  flagClassName: RaulexCTFFlagV2        # Class name of the flag
  returnRadius: 5                       # Radius (in meters) for returning the flag
  captureTime: 300                      # Time (in seconds) to capture the flag
  captureRadius: 5                      # Radius (in meters) for capturing the flag
  recaptureRadius: 5                    # Radius (in meters) for recapturing the flag
  recaptureTime: 300                    # Time (in seconds) to recapture the flag
  broadCastRadius: 60                   # Radius (in meters) for broadcasting the carrier's position
  beepSoundName: CTFFlagBeepSound       # Sound played when the flag is picked up or dropped
  beepInterval: 5                       # Interval (in seconds) for the beep sound
  zombieConfig:                         # Configuration for zombie waves
    numWaves: 2                         # Number of zombie waves
    min: 2                               # Minimum number of zombies in each wave
    max: 5                               # Maximum number of zombies in each wave
    zombieTypes:                        # List of zombie types
      - ZmbM_NBC_Yellow                 # First zombie type
      - ZmbM_NBC_Grey                   # Second zombie type
      - ZmbM_Mummy                       # Third zombie type
minPlayersRequired: 0                   # Minimum players required to start the event
startupWaitTime: 60                     # Wait time (in seconds) before the event starts
nextEventWaitTime: 120                  # Wait time (in seconds) between events
```
