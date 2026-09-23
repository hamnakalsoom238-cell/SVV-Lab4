# Functional & Behavioral Requirements

| Req. ID | Requirement Description |
| :--- | :--- |
| **R1** | The system shall initialize in the IDLE state upon system power-on and wait for incoming delivery requests. |
| **R2** | Upon receiving a valid delivery request, the system shall transition from IDLE to NAVIGATING state and move toward the target destination. |
| **R3** | While in NAVIGATING state, if an obstacle is detected, the system shall transition to AVOIDING_OBSTACLE state and pause normal navigation. |
| **R4** | Upon successfully clearing an obstacle, the system shall transition from AVOIDING_OBSTACLE back to NAVIGATING state. |
| **R5** | Upon reaching the designated destination coordinates, the system shall transition from NAVIGATING to DELIVERING state. |
| **R6** | Upon completing package handoff successfully, the system shall transition from DELIVERING to RETURNING state. |
| **R7** | If the battery level drops to or below the critical threshold during navigation, the system shall abort the current mission and transition to RETURNING state. |
| **R8** | Upon arriving at the warehouse location, the system shall transition from RETURNING to IDLE state. |
| **R9** | The system shall enforce a restriction prohibiting direct transition from IDLE to DELIVERING state without prior navigation. |
| **R10** | The system shall enforce a restriction prohibiting direct transition from AVOIDING_OBSTACLE to DELIVERING state without returning to navigation first. |
