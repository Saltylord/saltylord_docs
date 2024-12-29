# Empty Plant Pots

## Death State / Empty Pots
*This script requires an empty plant pot model due to the plant death state. When a plant dies, instead of it going poof. It switches to an empty plant pot the player can interact with, confirming the plant has died. Sadly GTA does not have a empty plant pot model in the game. You will need to either use BzZzi's empty plant pots or find and configure a new one.*

---

## BzZzi
*BzZzi offers free high quailty empty plant pots you can download and use right away. Simply follow her installation instructions and sl-weed will work without any need for edititng.*

[BzZzi's Pots](https://forum.cfx.re/t/props-pots/5271865)

## Changing BzZzi Model
*Simply change the Config.emptyPlantPotIndex to match the index of the model you want to use stored inside the data/models.lua file.*

```lua
    Config.emptyPlantPotIndex = 1, 2, 3, or 4
```

---

## Custom Models

*First, remove BzZzi's models from the 'dead' table inside the data/models.lua file and replace them with your own. If you only have one model that's okay.*

```lua
    dead = {
        'your_empty_plant_pot'
    },
```

*Second, update the 'Config.emptyPlantPotIndex' to match your models index number inside the dead table.*

```lua
    Config.emptyPlantPotIndex = 1
```