## MG1

### Devlog (Updated)
<hr>

PROMPT: Write about how the plan you wrote in the MG1 break-down activity connects to the code you wrote. 
Cite specific class names and method names in the code and GameObjects in your Unity Scene.

### Programming:
- The plan for my MG-1 breakdown activity included the objects Text, Player, and Seed.
- Coding for this, I created one central script to manage the interaction between all 3 of these objects.
- I made this descision due to the limited number of objects and the iteration speed this would give me.
  - I also had planend for this descision in my breakdown by indicating my player is my single source of truth.
- I opted to use old input system syntax cause its very quick and easy to use
- I created 2 polling methods, 1 for Moving, and 1 for spawning the seeds in `Update()` These covered the actions on the Player Object's `Move` and `StopMove`
  - This meant that the `Player` retained the attributes of Number of Seeds Planted and Number of Seeds Left.
  - Which is sent as an action to the UI as `Updates` action in the breakdown called `UpdateUI`
- I made sure to correctly setup my variable attributes with ReadOnly if they werent settings
- And also add [Required] for references. (These are ODIN attributes), This is a best practice for me
- I opted to use OnEnable for the setup, updating the UI and setting the current seeds count
- I also extracted out the update ui code in its own UpdateUI() method cause it appeared twice, (once in the seed placement and once in OnEnable)
- Thus my flow was very similar to my breakdown with the `Player` object branching out to the UI and the Seeds, Which functioned very similar to the Unity Implementation

### [MG-1 Seed Planting Game Build 0.0.1](https://starnightstudios.itch.io/ga208-mg1-assignment-game)

### Open Source Assets

- [Player Sprite](https://www.clipartmax.com/middle/m2i8i8A0A0H7A0Z5_free-bunny-in-overalls-front-view-overall-clip-art/)
- [Seed Sprite](https://www.vecteezy.com/png/15082209-sapling-sprouting-from-soil)

<hr>
