# Mask Manager
---
Manager of [[MaskBaseState|moods]]:
![[MaskBaseState#Base state for all the masks]]
Features:
- Connect to UI System (HUD)
- Connect to dialogue system

```cs
using system.something;
using system.something.somethingelse;
using UnityEngine;

public class maskmanager: monobehaviour
{
	MaskBaseState currentState;
	JoyMaskState JoyMask = new JoyMaskState();

}
```

![[uhhhhh.png]]