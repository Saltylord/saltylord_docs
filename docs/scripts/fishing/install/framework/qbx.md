# QBX

# **QBX Install Instructions**

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