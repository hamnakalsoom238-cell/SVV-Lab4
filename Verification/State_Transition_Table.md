# State Transition Table & Verification

## State Transition Table

| Current State | Event / Condition | Next State | Action / Description |
| :--- | :--- | :--- | :--- |
| IDLE | Delivery Request Received | NAVIGATING | Robot starts moving to destination |
| NAVIGATING | Obstacle Detected | AVOIDING_OBSTACLE | Pauses navigation, enters avoidance mode |
| AVOIDING_OBSTACLE | Obstacle Avoided | NAVIGATING | Resumes navigation to destination |
| NAVIGATING | Destination Reached | DELIVERING | Starts package delivery process |
| DELIVERING | Delivery Successful | RETURNING | Begins journey back to warehouse |
| NAVIGATING | Critical Battery | RETURNING | Cancels journey, heads back to warehouse |
| RETURNING | Warehouse Reached | IDLE | Ready for next request |

## Verification Checks

### Check 1 — Invalid Transition (IDLE → DELIVERING)
- **Can it happen?** No.
- **Explanation:** The robot cannot deliver without receiving a request and navigating first.
- **Violated Requirements:** R2 and R7.

### Check 3 — Obstacle During Delivery (AVOIDING_OBSTACLE → DELIVERING)
- **Can it move directly?** No.
- **Explanation:** It must first avoid the obstacle and resume navigation to reach the destination.
- **Violated Requirements:** R5, R6, and R7.
