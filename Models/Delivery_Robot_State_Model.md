# Autonomous Delivery Robot - System States & Events

## System States
1. **IDLE**: The robot is powered on, parked at the warehouse, and waiting for a delivery request.
2. **NAVIGATING**: The robot is moving towards the destination or returning to the warehouse under normal path conditions.
3. **AVOIDING_OBSTACLE**: The robot has detected an obstruction and is executing an evasion maneuver.
4. **DELIVERING**: The robot has arrived at the destination and is performing the package drop-off process.
5. **RETURNING**: The robot is navigating back to the warehouse after a successful delivery or due to a critical low battery event.

## System Events & Trigger Conditions
- **Delivery Request Received**: Signal generated when a new delivery task is assigned.
- **Obstacle Detected**: Sensor detection of an obstacle in the navigation path.
- **Obstacle Avoided**: Confirmation that the obstruction is cleared and safe pathing is restored.
- **Destination Reached**: GPS/Sensor confirmation of arrival at the delivery destination.
- **Delivery Successful**: Package handoff completed successfully.
- **Critical Battery**: Battery level drops below safety threshold (≤ Low Battery limit).
- **Warehouse Reached**: GPS/Sensor confirmation of arrival back at base station.
