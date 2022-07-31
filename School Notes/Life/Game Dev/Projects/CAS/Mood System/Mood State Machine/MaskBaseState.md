# Mask Base State
---
###### Base state for all the masks:
Joy/Sad, Fear/Anger
Disgust/Trust, Surprise/Anticipation

###### Functionality:
- Joy/Sad, Fear/Anger

```cs
using UnityEngine;

public abstract class MaskBaseState
{
	public abstract void EnterState(maskmanager mask);

	public abstract void ExitState(maskmanager mask);

	public abstract void OnCollisionEnter(maskmanager mask);

}
```