## Delivery Robot Requirements

| Requirement | Description                                                                                     | Priority |
| ----------- | ----------------------------------------------------------------------------------------------- | -------- |
| **R1**      | The robot shall remain in **IDLE** when no delivery request is received.                        | High     |
| **R2**      | The robot shall start **NAVIGATING** when a delivery request is received.                       | High     |
| **R3**      | The robot shall continuously monitor its surroundings while navigating.                         | High     |
| **R4**      | The robot shall enter **AVOIDING_OBSTACLE** when an obstacle is detected.                       | High     |
| **R5**      | The robot shall return to **NAVIGATING** after successfully avoiding an obstacle.               | High     |
| **R6**      | The robot shall enter **DELIVERING** when it reaches the destination.                           | High     |
| **R7**      | The robot shall enter **RETURNING** after the package is successfully delivered.                | High     |
| **R8**      | The robot shall enter **RETURNING** when the battery becomes critically low during navigation.  | High     |
| **R9**      | The robot shall enter **IDLE** after reaching the warehouse.                                    | Medium   |
| **R10**     | The robot shall not enter **DELIVERING** directly from **IDLE** or while **AVOIDING_OBSTACLE**. | High     |
