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



## W2
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
