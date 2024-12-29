# Items

*Copy and paste the following items into your item list*

```lua
	['weed_seed'] = {
		weight = 100,
		consume = 0,
		stack = true,
		client = {
			image = "weed_seed.png",
			export = 'sl-weed.weed_seed'
		},
		buttons = {
			{
				label = 'Weed Rank',
				action = function(slot)
					TriggerServerEvent('sl-weed:server:checkCurrentRank')
				end
			}
		},
	},

	['weed'] = {
		weight = 1,
		consume = 0,
		stack = true,
		buttons = {
			{
				label = 'Roll Joint',
				action = function(slot)
					exports['sl-weed']:rollJoint(slot)
				end
			},
		},
	},

	['joint'] = {
        consume = 0,
        stack = true,
        client = {
            image = "joint.png",
			export = 'sl-weed.joint'
        }
    },

	['wet_weed'] = {
		consume = 0,
		stack = true,
		client = {
			image = "wet_weed.png"
		},
		server = {
			export = 'sl-weed.wet_weed'
		},
	},

	['plant_nutrition'] = {
		label = 'Plant Fertilizer',
		weight = 1000,
		consume = 0,
		stack = true,
		description = "Fertilizer for various plants.",
		client = {
			image = "plant_fertilizer.png",
		}
	},

	['plant_water'] = {
		label = 'Plant Water',
		weight = 1000,
		consume = 0,
		stack = true,
		description = "Mineral water for various plants.",
		client = {
			image = "plant_nutrition.png",
		}
	},

	['plant_cure'] = {
		label = 'Plant Cure',
		weight = 1000,
		consume = 0,
		stack = true,
		description = "A chemcial used to cure plants from various diseases.",
		client = {
			image = "plant_cure.png",
		}
	},

	['plant_pot'] = {
		label = 'Plant Pot',
		weight = 1000,
		consume = 0,
		stack = true,
		description = "A plant use for various plants.",
		client = {
			image = "plant_pot.png",
		}
	},

	['rolling_papers'] = {
		label = 'Rolling Papers',
		weight = 100,
		consume = 0,
		stack = true,
		description = "Rolling papers used for rolling joints",
		client = {
			image = "rolling_papers.png",
		}
	},

	['genetics_book'] = {
		label = 'Plant Genetics Book',
		weight = 100,
		consume = 0,
		stack = true,
		client = {
			image = "genetics_book.png",
			export = 'sl-weed.genetics_book',
		},
	},
```

---