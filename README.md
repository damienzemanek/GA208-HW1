## MG1

### Devlog
<hr>

PROMPT: Write about how the plan you drew for the MG2 break-down activity connects to the code you wrote. 
Cite specific class names and method names in the code and GameObjects in your Unity Scene.

[Itch Build 0.0.1](https://starnightstudios.itch.io/ga208-mg1-assignment-game)

Asset Procurement: In order to meet my breakdown's requirements for its sprites I needed sprite assets. So:
  - I looked online for an image of a bunny and a sapling, collected, and imported them
  - I made a new folder called W1 in the main directory, and inside that a folder called `Assets` and in a folder in that called `Sprites`
  - I set them to `Single` for their sprite mode, and their compression to `High Quality` then Applied.

Scene Setup:
- I added 2 Square 2D GameObjects and changed their Sprite Renderer Sprite asset to the respective assets, and named them accordingly
- I created a new folder in W1 called `Scripts` and created a `Player` Script
- I added that script to the Player GameObject
- Before editing the script I added another 2D Square GameObject named it `Ground` and sized it to fit the scene

Programming:
- I opted to use old input system syntax cause its very quick and easy to use
- I created 2 polling methods, 1 for Moving, and 1 for spawning the seeds
- I put both in Update()
- I then added FixedUpdate() and put the Translate in there with a isMoving guard clause before it
- I made sure to correctly setup my variable attributes with ReadOnly if they werent settings
- And also add [Required] for references. (These are ODIN attributes), This is a best practice for me
- I opted to use OnEnable for the setup, updating the UI and setting the current seeds count
- I extracted out the update ui code in its own UpdateUI() method cause it appeared twice, (once in the seed placement and once in OnEnable)

Scene Completing Setup:
- I then imported the TMPro package requirements and added the text, and added them as references
- I had 4 TMPro texts, 2 labels, and 2 number trackers so I didnt have to add any string literals into the code (Just a preference), plus it looks better in the canvas
- I added in all my references, including making a Prefab out of the seed sprite, and mades its OrderInLayer to be behind the player

Building:
- I added the Web build package. And tried building.
- The build failed twice due to scripts `MaterialRandomizer` and `MaterialRandomizerScript` being editor scripts trying to include themselves
- I added the `#if UNITY_EDITOR ... #endif` compiler checks to remove them from the build
- After that the build worked.
- I zipped up my files and uploaded it to Itch.


### Open Source Assets

- [Player Sprite](https://www.clipartmax.com/middle/m2i8i8A0A0H7A0Z5_free-bunny-in-overalls-front-view-overall-clip-art/)
- [Seed Sprite](https://www.vecteezy.com/png/15082209-sapling-sprouting-from-soil)

<hr>
