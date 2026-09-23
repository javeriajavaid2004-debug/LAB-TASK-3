## Delivery Robot Requirements

| Req. ID | Requirement |
|---------|-------------|
| **R1** | The robot shall remain in **IDLE** when no delivery request is received. |
| **R2** | The robot shall start **NAVIGATING** when a delivery request is received. |
| **R3** | The robot shall continuously monitor its surroundings while navigating. |
| **R4** | The robot shall enter **AVOIDING_OBSTACLE** when an obstacle is detected. |
| **R5** | The robot shall return to **NAVIGATING** after successfully avoiding an obstacle. |
| **R6** | The robot shall enter **DELIVERING** when it reaches the destination. |
| **R7** | The robot shall enter **RETURNING** after the package is successfully delivered. |
| **R8** | The robot shall enter **RETURNING** when the battery becomes critically low during navigation. |
| **R9** | The robot shall enter **IDLE** after reaching the warehouse. |
| **R10** | The robot shall not enter **DELIVERING** directly from **IDLE** or while **AVOIDING_OBSTACLE**. |
