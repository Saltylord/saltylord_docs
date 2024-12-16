# QBCore

# **QBCore Install Instructions**

# Player Metadata
*Add the following metadata to your QBConfig.Player.PlayerDefaults inside the metadata table, located in you qb-core/config.lua*

```lua
	fishmarketpoints = 0,
	fishing = {
		exp = 0,
		level = 1
	},
```

---

# Fishing Licenses

*Include 'fishing' into your licenses metadata inside the QBConfig.Player.PlayerDefaults table*

```lua
	licences = {
        driver = true,
        business = false,
        weapon = false,
		fishing = false
    },
```