# cs ia criterion d script
---

###### Reqs
- 6 Minutes
- 

### Intro (~30 Secs)
- hello my student code is 051721-0036
- This is the video documentation for my computer science internal assessment cri D
- my product is a weather system package made for Unity 3D
- This product is made for my client Mark, who is an Environment Designer
- This weather system is going to enable my client to create customizable environments including grass, trees, weathers like rain and wind, and atmosphere like the sun and sky
- Throughout the video, i will be referring to this notepad on the left which includes my success criteria from criterion A, the test plan from criterion B, E and record of tasks.

### Actual Video
- So since this is a Unity 3D package, things will have to be done within unity, so lets open the project in unity
- This requires a bit of knowledge of the program if unfamiliar but since my client is, this should be intuitive

- In unity, we can see in the file hierarchy, my package contains
	- a shader for the grass
	- a shader for the trees
	- a particle system object for the rain
	- central weather controller script
	- Optionally, a movement script that handles the movement for the character, this should be replaced by whatever my client's game is using

So how this works is that the artist, which in this case, is my client Mark, creates a grass mesh in their preferred software, and import the 3D model, then attach a material with this shader on the object, and the animation will be applied

As shown in my first point which is test plan 6, the shader uses lambert shading, as seen here

Also, throughout the video, I will be entering play mode with the stats turned on to show the performance impact on the screen while I operate the scripts, this fulfills test plan number 5

So to set up the central weather controller script, simply add a new empty object to the scene, then attach the script to it.

Drag the rain particle system into the scene, and reference it in the script component in the inspector. Now to test it. As you can probably see, the user is able to control the amount of rain and how heavy the rain it. That fulfills test plan number 1

Next, as a demonstration, drag a grass model with the shader material attached to it, and drag the object reference to the central weather controller script to allow it to control all grass that uses this shader. Same thing with the tree and its shader. Now we can control all trees and grass in the scene using this central weather controller as you can see. This fulfills test plan 3.

Next, as the light is, as a default, already set to be unity's lighting system, so the lighting should be able to be controlled directly in the central weather contrller without any referencing. The grass and tree both requires an object to sample the material to get the shared materials in the scene. Now the colors can be changed as you can see. This fulfills test plan 2 and 7.

Next, I have prepared 5 different meshes for test plan 4, testing its compatbility over different meshes and not just my particular mesh. As you can see, it is working flawlessly. Test plan 4 is fulfilled.

Finally, to test its compatibility with unity's terrain system, simply set it up as a Detail mesh object. The shader i wrote allows it to use gpu instancing and it should work with unity's terrain system like so.

That concludes the demonstration video thanks for watching