# Autonomous Delivery Robot — State Model

## States

| State ID | State |
|---|---|
| S1 | IDLE |
| S2 | NAVIGATING |
| S3 | AVOIDING_OBSTACLE |
| S4 | DELIVERING |
| S5 | RETURNING |

## Events / Conditions

| Event ID | Event / Condition |
|---|---|
| E1 | Delivery Request Received |
| E2 | Destination Reached |
| E3 | Delivery Successful |
| E4 | Warehouse Reached |
| E5 | Obstacle Detected |
| E6 | Obstacle Avoided |
| E7 | Critical Battery |

## State Flow

IDLE  
↓ Delivery Request Received  
NAVIGATING  

NAVIGATING  
↓ Obstacle Detected  
AVOIDING_OBSTACLE  

AVOIDING_OBSTACLE  
↓ Obstacle Avoided  
NAVIGATING  

NAVIGATING  
↓ Destination Reached  
DELIVERING  

DELIVERING  
↓ Delivery Successful  
RETURNING  

NAVIGATING  
↓ Critical Battery  
RETURNING  

RETURNING  
↓ Warehouse Reached  
IDLE
