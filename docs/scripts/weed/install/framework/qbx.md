# QBX

# **QBX Install Instructions**
*Enable '@qbx_core/modules/playerdata.lua' in the fxmanifest*

```lua
	client_scripts {
	    '@qbx_core/modules/playerdata.lua',
	    'bridge/**/client.lua',
	    'client/*.lua'
	}
```

*My script will automatically detect QBX if you are running v1.22.0+, so there is no additional installation steps for this framework. If you are running a version lower then 1.22.0 then you will need to follow the additional step below.*

---

# **Only Pre v1.22.0**
*Add the following metadata to the CheckPlayerData function in qbx_core\server\player.lua*

```lua
    playerData.metadata.weed = playerData.metadata.weed or {
        level = 0,
        exp = 0
    }
```