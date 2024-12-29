# Radial Menu
*If you want to add options into your radial menu for ox copy and paste the code below into your options script.*

```lua
	{
    	label = 'Check Fishing Area',
    	icon = 'magnifying-glass',
    	onSelect = function()
    		TriggerEvent('sl-fishing:client:checkFishingArea')
    	end
    },
	{
    	label = 'Revoke License',
    	icon = 'id-card',
    	onSelect = function()
    		TriggerEvent('sl-fishing:client:revokeFishingLicense')
    	end
    }
```

---