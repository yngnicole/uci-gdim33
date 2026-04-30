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
ScriptableObject:
Big steps:
1. Create ScriptableObjects to save data for items
2. Write a script to implement how the data from SO will act on Player and Cat
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