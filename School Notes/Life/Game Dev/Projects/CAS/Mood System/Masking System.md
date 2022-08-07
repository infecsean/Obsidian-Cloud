# Masking System planning
---
###### Stuff about the masking system
---

Main-mood: Joy/Sad, Fear/Anger
Alt-mood: Disgust/Trust, Surprise/Anticipation

### Table Excluding Feelings with Alt-moods
| Human Feelings                  | Emotions             | Opposite Feelings               | Emotions               |
| ------------------------------- | -------------------- | ------------------------------- | ---------------------- |
| ==Optimism, courage==           | Anticipation + Joy   | ==Disapproval, Disappointment== | Surprise + Sadness     |
| ==Hope, Fatalism==              | Anticipation + Trust | ==Unbelief, Shock==             | Surprise + Disgust     |
| ==Anxiety, Dread==              | Anticipation + Fear  | ==Outrage, Hate==               | Surprise + Anger       |
| ==Love, Friendliness==          | Joy + Trust          | ==Remorse, Misery==             | Sadness + Disgust      |
| Guilt, Excitement               | Joy + Fear           | Envy, Sulleness                 | Sadness + Anger        |
| ==Delight, Doom==               | Joy + Surprise       | ==Pessimism==                   | Sadness + Anticipation |
| ==Submission, Modesty==         | Trust + Fear         | ==Contempt, Scorn==             | Disgust + Anger        |
| ==Curiosity==                   | Trust + Surprise     | ==Cynicism==                    | Disgust + Anticipation |
| ==Sentimentality, Resignation== | Trust + Sadness      | ==Morbidness, Derisiveness==    | Disgust + Joy          |
| ==Awe, Alarm==                  | Fear + Surprise      | ==Aggressiveness, Vengeance==   | Anger + Anticipation   |
| Despair                         | Fear + Sadness       | Pride, Victory                  | Anger + Joy            |
| ==Shame, Prudeness==            | Fear + Disgust       | ==Dominance==                   | Anger + Trust          |                                 |                      |                                 |                        |

### Table Excluding Feelings with Only Alt-moods
| Human Feelings              | Emotions             | Opposite Feelings           | Emotions               |
| --------------------------- | -------------------- | --------------------------- | ---------------------- |
| Optimism, courage           | Anticipation + Joy   | Disapproval, Disappointment | Surprise + Sadness     |
| ==Hope, Fatalism==              | Anticipation + Trust | ==Unbelief, Shock==             | Surprise + Disgust     |
| Anxiety, Dread              | Anticipation + Fear  | Outrage, Hate               | Surprise + Anger       |
| Love, Friendliness          | Joy + Trust          | Remorse, Misery             | Sadness + Disgust      |
| Guilt, Excitement           | Joy + Fear           | Envy, Sulleness             | Sadness + Anger        |
| Delight, Doom               | Joy + Surprise       | Pessimism                   | Sadness + Anticipation |
| Submission, Modesty         | Trust + Fear         | Contempt, Scorn             | Disgust + Anger         |
| ==Curiosity==                   | Trust + Surprise     | ==Cynicism==                    | Disgust + Anticipation |
| Sentimentality, Resignation | Trust + Sadness      | Morbidness, Derisiveness    | Disgust + Joy          |
| Awe, Alarm                  | Fear + Surprise      | Aggressiveness, Vengeance   | Anger + Anticipation   |
| Despair                     | Fear + Sadness       | Pride, Victory              | Anger + Joy            |
| Shame, Prudeness            | Fear + Disgust       | Dominance                   | Anger + Trust          | 

### Table with emotions I need in the game
| Human Feelings              | Emotions             | Opposite Feelings           | Emotions               |
| --------------------------- | -------------------- | --------------------------- | ---------------------- |
| Optimism, courage           | Anticipation + Joy   | ==Disapproval, Disappointment== | Surprise + Sadness     |
| Hope, Fatalism              | Anticipation + Trust | ==Unbelief==, Shock             | Surprise + Disgust     |
| ==Anxiety, Dread==              | Anticipation + Fear  | Outrage, Hate               | Surprise + Anger       |
| ==Love, Friendliness==          | Joy + Trust          | Remorse, Misery             | Sadness + Disgust      |
| ==Guilt, Excitement==           | Joy + Fear           | Envy, Sulleness             | Sadness + Anger        |
| Delight, Doom               | Joy + Surprise       | Pessimism                   | Sadness + Anticipation |
| Submission, Modesty         | Trust + Fear         | Contempt, Scorn             | Disgus + Anger         |
| ==Curiosity==                   | Trust + Surprise     | Cynicism                    | Disgust + Anticipation |
| ==Sentimentality==, Resignation | Trust + Sadness      | Morbidness, Derisiveness    | Disgust + Joy          |
| ==Awe==, Alarm                  | Fear + Surprise      | Aggressiveness, Vengeance   | Anger + Anticipation   |
| ==Despair==                     | Fear + Sadness       | Pride, Victory              | Anger + Joy            |
| ==Shame==, Prudeness            | Fear + Disgust       | Dominance                   | Anger + Trust          | 


### Discussion
- Q: Can I remove alt-moods?
	- A: Yes. All the necessary feelings can be isolated to the main moods, but curiosity
	- A: Potentially. The only feeling thats important that is also purely alt-mood is curiosity
		- Q: What to do with curiosity?
			- A: Make it a central theme
			- A: Make it a default advantage (stand out against other students, why noah is mc)
			- A: Make it a diminishing feature (tell story of how school kill curiosity)
- Q: Problem with 3 negative emotions but only one positive (joy)
	- A: A challenge for the player to keep him happy
		- Q: Delibrate scheme to be cynical
			- A: Not if the player actively sabotages him
			- ==C: No Problem ;)==
- Q: What to do with alt moods?
	- A: Hide its presense (Determine the ending or something?)
		- Q: Come off as weird when only main moods are shown when being loved
			- A: Yeah probably
	- A: Show its presense but not as masks
		- Clarification: Trust, disgust, surprise, and anticipation all seem dependent on subject.
		- Trust: You might trust your parents but not your teacher
		- Disgust: Kind of specific. It should be clear whether or not something is disgusted
		- Surprise: Used by ***awe*** and ***disappointment***, probably used by other 
		- Anticipation: Maybe use as an extension that depends on player's actions.
		- Surprise/Anticipation: A bool value i guess. Controls whether or not an emotion happens.
			- Example: If you were informed of what to expect at school, which you cannot fully, cus scripted, you wont feel anxious
		- ==C: Trust/Disgust will be based on subjects. Surprise/Anticipation will be a bool based on information and choices made by the player.==

Alt-moods will scale the severity of the pair if it is paired with a main mood.


### Conclusion
