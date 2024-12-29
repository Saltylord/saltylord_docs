# Items
*Add the following items into your data/items.lua*

```lua
	['fishing_doc'] = {
		label = 'Banned Fish List',
		weight = 100,
		consume = 0,
		description = "A list of banned fish from the Los Santos government.",
		client = {
			image = "fishing_doc.png",
		},
		server = {
			export = 'sl-fishing.fishing_doc'
		}
	},

	['fishing_license'] = {
		label = 'Fishing License',
		weight = 100,
		consume = 0,
		client = {
			image = "fishing_license.png",
		}
	},

	['fishing_contract'] = {
		label = 'Fish Market Contract',
		weight = 100,
		consume = 0,
		buttons = {
			{
				label = 'Check Status',
				action = function(slot)
					TriggerServerEvent('sl-fishing:server:checkContractProgress')
				end
			},
		},
		client = {
			image = "fishing_contract.png",
		}
	},

	['crate'] = {
		label = 'Sealed Crate',
		weight = 100,
		consume = 0,
		description = "A sealed crate found in the waters of Los Santos. There might be something interesting inside..",
		client = {
			image = "crate.png",
		},
		server = {
			export = 'sl-fishing.crate'
		}
	},

	['shoe'] = {
		label = 'Old Shoe',
		weight = 100,
		stack = false,
		description = "A soggy old shoe.",
		client = {
			image = "old_shoe.png",
		}
	},

	['stick'] = {
		label = 'Stick',
		weight = 100,
		stack = false,
		description = "A soggy sticky.",
		client = {
			image = "stick.png",
		}
	},

	['fish'] = {
		stack = false,
		consume = 0,
		client = {
			image = "fish.png",
		},
		server = {
			export = 'sl-fishing.fish'
		},
		buttons = {
			{
				label = 'Release Fish',
				action = function(slot)
					exports['sl-fishing']:releaseFish(slot)
				end
			}
		},
	},

	['bait'] = {
		weight = 100,
		consume = 0,
		stack = true,
		server = {
			export = 'sl-fishing.bait'
		}
	},

	["fishing_rod"] = {
		weight = 500,
		consume = 0,
		stack = true,
		close = true,
		client = {
			image = "fishing-rod.png"
		},
		server = {
			export = 'sl-fishing.fishing_rod'
		},
		buttons = {
			{
				label = 'Check Current Rank',
				action = function(slot)
					TriggerServerEvent('sl-fishing:server:checkFishingLevel')
				end
			},
		},
	},

	['fishing_basket'] = {
		label = 'Fishing Basket',
		weight = 1000,
		stack = false,
		close = false,
		consume = 0,
		description = "A wicker basket for storing fish.",
		client = {
			image = "fishing_basket.png"
		},
	},
```

---