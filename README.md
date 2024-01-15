# S~~ANS~~ Holiday-Hack-Challenge-2023
 
<img width="800" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/d051e195-083b-431e-903d-cc42be8bcb79">  

## Christmas Island: Orientation
### Holiday Hack Orientation
Difficulty: 🎄

Talk to Jingle Ringford on Christmas Island and get your bearings at Geese Islands

<img width="477" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/f446a59b-8aec-4e4f-9a3d-7220f1fc2821">

### Items Gathered
![image](https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/4147c58c-cb62-4135-80d1-ece769d27c12) <b> Fishing Pole - Just a humble rod and reel. Perfect for catching all manner of aquatic life. </b>

## Christmas Island: Frosty's beach

Hints: Synthesis is the True Ending
From: Santa
The AI revolution has begun. Some of the most prominent and useful tools born from the advent of powerful AI include ChatGPT, PlayHT, Midjourney, Dall-E 3, Bing AI, and Bard, and Grok.

### Snowball Fight
Difficulty: 🎄🎄

Visit Christmas Island and talk to Morcel Nougat about this great new game. Team up with another player and show Morcel how to win against Santa!

To win the game we have to defeat elves and the Santa but boy is it difficult. As the hint says we need a powerful player to team with us and defeat elves and santa, that would be the Dwarf. Hint is in the Javascript source code of the game as highlighted below.

### Code Analysis:
The code appears to introduce a character (Elf the dwarf, jokingly referred to as Jared) into the game when in single-player mode.First, a sound effect named 'elf_the_dwarf_is_here' is played if audio is enabled. Next, a toast message appears on the screen saying "Elf the dwarf has joined your team!" for a short duration. Finally, a new game sprite named 'jaredSprite' is created at a specific position. All indicating we need the Dwarf.

View the source code of the game 
<img width="739" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/53a6d875-2c45-47e0-bf53-4788b72f4158">

```
 // Check if it's single-player mode
    // jared ... I mean Elf the dwarf joins the fight when in single player mode
       if (singlePlayer === 'true') {
          setTimeout(() => {
            if (isaudio) {
              gameSceneObject.sound.play('elf_the_dwarf_is_here', { volume: 0.5 });
            }
            toastManager.showToast("Elf the dwarf has joined your team!", duration=500, delay=5000);
            jaredSprite = gameSceneObject.physics.add.sprite(starting_pos.x + 150, starting_pos.y, 'jaredSprite');
```
### Working towards Victory: 
We have to change singlePlayer parameter to true and reload game. 
> [!IMPORTANT]
> Do not play this game in a seperate tab or windows of your browser you have to complete this challenge in the same page with the help of developer tools console.

> https://hhc23-snowball.holidayhackchallenge.com/room/?username=<>&roomId=201e0e461&roomType=public&gameType=co-op&id=18fed30a-a96a-47c2-a697-86c6d3a4b0bb&dna=<>&singlePlayer=false

 <img width="1000" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/3fed0b55-4771-43a1-9045-076875fe1719">

##### Steps:
1. Open Developer console and change the frame to the game room
   
<img width="241" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/634c5fa8-78d0-4b6b-9a04-d4b4a50280cd">

2. Choose play game with random players and once the game room to loads check the current loaded URL "window.location.href"
   
3. Use the below javascript which changes the "SinglePlayer" parameter to true and loads the frame again.
  
4. Now you have Dwarf the elf on your team. Playing the game is made easier.

````
// Get the current URL
var url = new URL(window.location.href);

// Update the 'singlePlayer' parameter to 'true'
url.searchParams.set('singlePlayer', 'true');

// Reload the frame with the modified URL
window.location.href = url.href;
````
 







