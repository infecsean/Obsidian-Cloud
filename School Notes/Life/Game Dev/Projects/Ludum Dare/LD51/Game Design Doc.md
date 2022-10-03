# Ludum Dare 51
---
Theme: Every 10 Seconds

Every 10 seconds, a person dies
you have to save as many people as you can

Every 10 seconds, more traffic

### CustomerBaseState
- Target to pathfind
- Dialogue to show
- Waiting interval

### CustomerWalking
- Target -> chair | target = exit
- Dialogue = none
- Waiting interval = none


### CustomerSeated
- Target = none
- Dialogue = none
- Waiting interval = 10s

### CustomerOrdering
- Target = none
- Dialogue = objectpool.random
- Waiting interval = 10s

### CustomerEating
- Target = none
- Dialogue = none
- Waiting Interval = 10s

### CustomerPaying
- Target = none
- Dialogue = money
- Waiting interval = 10s

### DialogueBaseState
- sprite icon
- when clicked
- 
### DialogueOrderingState
- Show only ordering sprites
- when clicked, check if right things in hand
### Dialogue