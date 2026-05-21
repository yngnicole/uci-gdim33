# GDIM 33 In-Class Activities
## W1
### Activity 1
[Inspo Board](https://pin.it/4Ttro2VCF)

1. Some patterns that are emerging from my inspiration sources are
- 2d pixel or 2d illustration artstyle
- 2d isometric camera 
- Table tennis with cats and spades on a card
- Stats like health, coins
- Dialogue options
- Cats
- Spooky area
- Interesting 2d map that works with perspectives 

2. My table mate's is interested in building a game that looks visually nice. Our personal styles and interests are similar in that I was also looking at a lot of visual artstyles and
how I should develop my game in that aspect becasue I have the most experience in art. We also talked about wanting to make a 2D game because the scope might be easier and it will look better

3. My table's LA taste in game are FPS games. It is similar to mines as I play some fps games like Valorant but that is it...

### Activity 2
The genre that I want to use is combining 2D survival/exploration horror where the core mechanic and gameplay loop is trying to find items to survive like food and water and taming cats to
fight and protect you from ghosts. 
<img width="1439" height="804" alt="image" src="https://github.com/user-attachments/assets/538ef4a3-d6a0-432c-ba72-74129a389920" />



## W3
### Activity 1
<img width="1502" height="1130" alt="Screenshot 2026-04-15 174035" src="https://github.com/user-attachments/assets/2ee0ca5a-c3ee-44ec-bb94-cc643b156aae" />

### Activity 2
- It is advantageous to save the event name for the explore-to-dialogue state transitions as Scene variable because then other graphs can access this variable.
For example, the Walrus graph needed to access the variable to trigger the game state transition to occur. 
- I used a Debug.Log() to test if my transition from the two state machines worked. It helped me because I realized that I had problems with how the graph was set up that 
didn't allow the transition to occur. This saved me the problem of figuring out what in my graphs are not working later. 
- The Set Cursor Lock State is  relevant to my Vertical Slice because the camera movement will not be used with the mouse cursor so the mouse cursor is not needed at all. The 
set cursor Lock state lets me lock the cursor so the player cannot access it. 
- A game state is relevant to my Vertical Slice because I will be having different states for the enemies and cat gameobject where they have the states: idle or following player, provoked, and attacking. 



## W4
### Activity 1
- What is playable in my build right now is the most basic mechanic for player movement and cat attack. 
- My playtesting goals is to find bugs and areas that I should fix.
- Playtest Team Member: Hajin Lee, Romarick Anderson, Nicole Yang
- Playtest notes: 
	- Cat falls after the ghost disappears
	- No indication of how to attack the ghost 
	- No indication of the ghost taking damage

### Activity 2
- The writer could add more dialogue to this setup without writing any code because they can write the dialogue nodes in the ScriptableObject which does not require them to write code. They can also "code" the dialogue to work through visual scripting.
- The limit to the number of dialogue nodes that a writer could create without writing code depends on if the writer is creating any dialogue systems in the game. For example, if the writer needs to make dialogue buttons that branch off to existing dialogue, they may need to code it as visual scripting will get too messy. 
- - The purpose of the "Regenerate Nodes" button is that it recieves the custom made nodes you create and also recieves any nodes that were not originally there. 

## W5
### Activity 1 
My Unity tool choice is ScriptableObject

Big Step:
- Create ScriptableObjects to save data for items
- Write a script to implement how the data from SO will act on Player and Cat

Small steps:
1. Create a SO script with variables, Health, Hunger, Powerup and test if the shortcut menu appears in Unity.
2. Create a SO from the shortcut menu in Unity with the data, Health: 20 and everything else zero
3. Attach the SO with a medicine sprite I have. 
4. Create an Item script that reads player input (v) to consume the SO. Test if the SO is consumed if it disappears when consumed. 
5. Write additional code so that when the Item is consumed, Cat will gain 20 health. 
### Activity 2 
I created ScriptableObject script and added variables: Health, Hunger, Powerup and sprite icon. I created a SO object in Unity and attached my medicine sprite to it. I hooked up the
SO on the medicine gameobject and in the item script, I changed my original event of OnConsumeMedicine?.Invoke(_medicinestat); to 
OnConsumeMedicine?.Invoke(_scriptableObject.plusHealth); to get the variable plusHealth from _scriptableObject instead. My medicine item successfully disappears once consumed and 
gives health back to the Cat gameObject.

## W6
### Activity 1
- What is new in my build is that the Cat goes towards the enemy when they are in attack state, cat and enemy health is indicated in the top left and also new items are in the game. 
- My playtesting goal is to see whether or not my cat mechanic is engaging, and working.
[Itch](https://yngnicole.itch.io/gdim-33-playtest)
- Playtesting notes: 
- Visual indication of what button to press to consume items
- Cat doesn't lock onto the enemy but rather goes past it. 
- All items are consumed at once

### Activity 2 
1. Multiply setting of the Blend node make the resulting color darker and less saturated than the input colors because it multiplies two color inputs. When two color inputs are mulitplied,
the resulting value gets smaller and smaller towards 0. Color that are closer to 0 are darker while colors that are closer to 1 are brighter. Thus mulitply makes color darker. 
2. If we use Multiply to combine Alpha values, the resulting value be more translucent than either of the original values because the values are closer to 0 and alpha levels
that are closer to 0 are more translucent. 
3. I think the shader is getting the UV values from the mesh renderer on the Shiba gameobject.
4. I think manipulating colors with math sounds interesting but intimidating.

## W7
1. The data for the Vertex Color node in step 3 came from the Shiba mesh
2. The color on our shiba in step 3 is blended at the edges of different regions of color because vertex color is a vertex data and when they are attached to the
fragment shader, they're interpolated across the adjacent vertices. 
3. The shiba from step 3 is less detailed than the shiba we rendered with a texture because vertex color is only colored at the vertex and then smoothed out over the polygons whereas
textures are made from many pixels that are rendered at each pixel point. Since vertex color generally results in a less detailed color application, I think a vertex color can be useful for creating textures on objects that are meant to be 
less detailed and blurry like perhaps soft lighting. 
4. Based on the color of the shiba in step 4, it looks like the mesh's vertex normals on part of the shiba's leg is wrong because the rest of the shiba color is smooth but then
there is a sudden lighter area that does not match the rest.
5. One other piece of vertex data we can test with a debug shader are UV coordinates. The specific color can correspond to the U and V coordinates to see if they are mapped properly.
6. There is an error in the lighting in step 5 on the back of the shiba because the vertex normal is pointing away from the shiba but the light direction vector is pointed towards 
the shiba. This is because when two vectors point in opposite direction, it results in a negative dot product result. 
7. We set the Blend Mode to Addictive for the fire effect in step 6 because it adds the color on the top layer to the texture on the bottom layer. This combines the orange with
the noise texture, and increases the lighter areas because colors are being added and getting closer to 1. 

## W8
# Act 1 
- What is new in my build since Milestone 2 is that I implemented a hungar bar, a food item, and fixed some bugs like the health text on the screen will go negative. 
- [Itch](https://yngnicole.itch.io/gdim-33-playtest)
- My playtesting goals is to see if my controls are intuitive. 
- Playtest Notes: I got feedback that I need to add more features and a map to my game. It seems like my controls are pretty intuitive. Also that I should think about improving my UI like
adding a health bar or hunger bar.

# Act 2 
- I did activity 2c
1.
2. When the lerp is set to 0, there is no post processing effect on the screen at all. When the lerp is set to 0.5, there is a faint effect, and when the lerp is set to 1, the effect is super apparant. 
3. The sreen looks like that based on those different Lerp value because lerp finds the given x value based on the two original values which are the BlitTexture and the multiplied texture. So if the 
lerp value is closer to 1, then the color will be darker and more opaque, whereas if the lerp value is closer to 0, the effect will be more transparent. 