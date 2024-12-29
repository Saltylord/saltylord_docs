# Empty Plant Pots

## BzZzi's Models

*The script is already configured to work with BzZzi's empty plant pots. If you still want to use BzZzi's models but just want to change which one appears when a plant dies. Simply change the Config.emptyPlantPotIndex to match the index of the model you want to use stored inside the data/models.lua file.*

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