# QBX

# **QBX Install Instructions**

**(WILL BE DEPRECIATED SOON) QBX SUPPORT WILL REMAIN BUT YOU WILL NOT LONGER NEED TO EDIT THE CORE**

# Player Metadata
*Add the following code to the CheckPlayerData function inside qbx_core/server/player.lua*

```lua
    playerData.metadata.fishmarketpoints = playerData.metadata.fishmarketpoints or 0
	playerData.metadata.fishing = playerData.metadata.fishing or {
        level = 0,
        exp = 0
    }
```

---

# Fishing Licenses

*Include 'fishing' into your licenses metadata inside the CheckPlayerData function*

```lua
	playerData.metadata.licences = playerData.metadata.licences or {
        id = true,
        driver = true,
        weapon = false,
        fishing = false
    }
```