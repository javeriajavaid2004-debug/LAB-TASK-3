# State Transition Table
| Current State | Event / Condition | Next State |
|---|---|---|
| IDLE | Delivery Request Received | NAVIGATING |
| NAVIGATING | Obstacle Detected | AVOIDING_OBSTACLE |
| AVOIDING_OBSTACLE | Obstacle Avoided | NAVIGATING |
| NAVIGATING | Destination Reached | DELIVERING |
| DELIVERING | Delivery Successful | RETURNING |
| NAVIGATING | Critical Battery | RETURNING |
| RETURNING | Warehouse Reached | IDLE |
## Verification
### Check 1  Invalid Transition
IDLE - DELIVERING
This transition is invalid because the robot must first receive a delivery request and navigate to the destination.
Correct path:
IDLE - NAVIGATING → DELIVERING
### Check 2  Missing Transition
If the robot moves from NAVIGATING to AVOIDING_OBSTACLE but cannot return to NAVIGATING, it cannot continue its delivery.
Required transition:
AVOIDING_OBSTACLE → NAVIGATING
### Check 3 Obstacle During Delivery
The robot must not move directly from AVOIDING_OBSTACLE to DELIVERING.
Correct path:
AVOIDING_OBSTACLE → NAVIGATING → DELIVERING

## Final Verification Result
- IDLE → DELIVERING: INVALID
- AVOIDING_OBSTACLE → DELIVERING: INVALID
- AVOIDING_OBSTACLE → NAVIGATING: VALID
- NAVIGATING → DELIVERING: VALID
- DELIVERING → RETURNING: VALID
- RETURNING → IDLE: VALID
All important transitions have been checked against the requirements.
