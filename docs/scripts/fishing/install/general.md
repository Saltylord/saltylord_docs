# General Install Instructions

## General
- *Drag and drop the sl-fishing folder into your resource folder*
- *Add ensure sl-fishing to your resource.cfg*
- *Run the sl-fishing.sql file*
- *Copy and paste the images from the images folder into your inventory*

## Fishing Basket Container
*Add this code in the /modules/items/containers.lua in ox_inventory*

```lua
	setContainerProperties('fishing_basket', {
		slots = 25,
		maxWeight = 35000,
		whitelist = { 'fish' }
	})
```

## Radial Menu Options

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

## Items
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

## Shop

```lua
    Fishing = {
		name = 'Fishing Shop',
		blip = {
			id = 59, colour = 67, scale = 0.8
		},
		inventory = {
			{name = 'fishing_rod', price = 100, metadata = {
				label = 'Wooden Rod',
				description = "Rarity: Starter \n\n Difficulty: Hard \n\n Rod Sensitivity: +8% \n\n A wooden fishing rod made by hand. Provides different bonuses while fishing.",
				rarity = 'common',
				sensitivity = 8,
				time = 3,
				presses = 15
			}},
			{name = 'fishing_rod', price = 200, metadata = {
				label = 'Fiberglass Rod',
				description = "Rarity: Competent \n\n Difficulty: Hard \n\n Rod Sensitivity: +12% \n\n A fiberglass fishing rod. Provides different bonuses while fishing. ",
				rarity = 'uncommon',
				sensitivity = 12,
				time = 4,
				presses = 15
			}},
			{name = 'fishing_rod', price = 500, metadata = {
				label = 'Metal Rod',
				description = "Rarity: Expert \n\n Difficulty: Medium \n\n Rod Sensitivity: +16% \n\n A fishing rod made from mixed metals. Provides different bonuses while fishing.",
				rarity = 'rare',
				sensitivity = 16,
				time = 5,
				presses = 15
			}},
			{name = 'fishing_rod', price = 750, metadata = {
				label = 'Graphite Rod',
				description = "Rarity: Professional \n\n Difficulty: Medium \n\n Rod Sensitivity: +20% \n\n A fishing rod made from mixing graphite and carbon fiber by hand. Provides different bonuses while fishing.",
				rarity = 'epic',
				sensitivity = 20,
				time = 4,
				presses = 10
			}},
			{name = 'fishing_rod', price = 1000, metadata = {
				label = 'Carbon Fiber Rod',
				description = "Rarity: Master \n\n Difficulty: Easy \n\n Rod Sensitivity: +24% \n\n A fishing rod made from pure carbon fiber by hand. Provides different bonuses while fishing.",
				rarity = 'legendary',
				sensitivity = 24,
				time = 3,
				presses = 8
			}},


			{name = 'bait', price = 25, metadata = {
				label = 'Live Fishing Bait',
				description = "Rarity: Starter \n\n Bonus Fish: +12% \n\n Catching Speed: +10% \n\n Lure Power: +8% \n\n Live fishing bait commonly used in rivers. Provides different bonuses while fishing.",
				image = 'live_bait',
				rarity = 'common',
				type = 'live',
				extra = 12,
				speed = 10,
				power = 8
			}},
			{name = 'bait', price = 50, metadata = {
				label = 'Live Fishing Bait',
				description = "Rarity: Competent \n\n Bonus Fish: +18% \n\n Catching Speed: +15% \n\n Lure Power: +12% \n\n Live fishing bait commonly used in rivers. Provides different bonuses while fishing.",
				image = 'live_bait',
				rarity = 'uncommon',
				type = 'live',
				extra = 18,
				speed = 15,
				power = 12
			}},
			{name = 'bait', price = 75, metadata = {
				label = 'Live Fishing Bait',
				description = "Rarity: Expert \n\n Bonus Fish: +24% \n\n Catching Speed: +20% \n\n Lure Power: +16% \n\n Live fishing bait commonly used in rivers. Provides different bonuses while fishing.",
				image = 'live_bait',
				rarity = 'rare',
				type = 'live',
				extra = 24,
				speed = 20,
				power = 16
			}},
			{name = 'bait', price = 100, metadata = {
				label = 'Live Fishing Bait',
				description = "Rarity: Professional \n\n Bonus Fish: +35% \n\n Catching Speed: +25% \n\n Lure Power: +20% \n\n Live fishing bait commonly used in rivers. Provides different bonuses while fishing.",
				image = 'live_bait',
				rarity = 'epic',
				type = 'live',
				extra = 35,
				speed = 25,
				power = 20
			}},
			{name = 'bait', price = 150, metadata = {
				label = 'Live Fishing Bait',
				description = "Rarity: Master \n\n Bonus Fish: +50% \n\n Catching Speed: +30% \n\n Lure Power: +24% \n\n Live fishing bait commonly used in rivers. Provides different bonuses while fishing.",
				image = 'live_bait',
				rarity = 'legendary',
				type = 'live',
				extra = 50,
				speed = 30,
				power = 24
			}},


			{name = 'bait', price = 25, metadata = {
				label = 'Lure Fishing Bait',
				description = "Rarity: Starter \n\n Bonus Fish: +12% \n\n Catching Speed: +10% \n\n Lure Power: +8% \n\n A type of lure bait commonly used in fresh water lakes. Provides different bonuses while fishing.",
				image = 'lure_bait',
				rarity = 'common',
				type = 'lure',
				extra = 12,
				speed = 10,
				power = 8
			}},
			{name = 'bait', price = 50, metadata = {
				label = 'Lure Fishing Bait',
				description = "Rarity: Competent \n\n Bonus Fish: +18% \n\n Catching Speed: +15% \n\n Lure Power: +12% \n\n A type of lure bait commonly used in fresh water lakes. Provides different bonuses while fishing.",
				image = 'lure_bait',
				rarity = 'uncommon',
				type = 'lure',
				extra = 18,
				speed = 15,
				power = 12
			}},
			{name = 'bait', price = 75, metadata = {
				label = 'Lure Fishing Bait',
				description = "Rarity: Expert \n\n Bonus Fish: +24% \n\n Catching Speed: +20% \n\n Lure Power: +16% \n\n A type of lure bait commonly used in fresh water lakes. Provides different bonuses while fishing.",
				image = 'lure_bait',
				rarity = 'rare',
				type = 'lure',
				extra = 24,
				speed = 20,
				power = 16
			}},
			{name = 'bait', price = 100, metadata = {
				label = 'Lure Fishing Bait',
				description = "Rarity: Professional \n\n Bonus Fish: +35% \n\n Catching Speed: +25% \n\n Lure Power: +20% \n\n A type of lure bait commonly used in fresh water lakes. Provides different bonuses while fishing.",
				image = 'lure_bait',
				rarity = 'epic',
				type = 'lure',
				extra = 35,
				speed = 25,
				power = 20
			}},
			{name = 'bait', price = 150, metadata = {
				label = 'Lure Fishing Bait',
				description = "Rarity: Master \n\n Bonus Fish: +50% \n\n Catching Speed: +30% \n\n Lure Power: +24% \n\n A type of lure bait commonly used in fresh water lakes. Provides different bonuses while fishing.",
				image = 'lure_bait',
				rarity = 'legendary',
				type = 'lure',
				extra = 50,
				speed = 30,
				power = 24
			}},


			{name = 'bait', price = 25, metadata = {
				label = 'Deep Sea Fishing Bait',
				description = "Rarity: Starter \n\n Bonus Fish: +12% \n\n Catching Speed: +10% \n\n Lure Power: +8% \n\n Deep sea fishing bait commonly used in oceans and salt water fishing areas. Provides different bonuses while fishing.",
				image = 'deepsea_bait',
				rarity = 'common',
				type = 'deepsea',
				extra = 12,
				speed = 10,
				power = 8
			}},
			{name = 'bait', price = 50, metadata = {
				label = 'Deep Sea Fishing Bait',
				description = "Rarity: Competent \n\n Bonus Fish: +18% \n\n Catching Speed: +15% \n\n Lure Power: +12% \n\n Deep sea fishing bait commonly used in oceans and salt water fishing areas. Provides different bonuses while fishing.",
				image = 'deepsea_bait',
				rarity = 'uncommon',
				type = 'deepsea',
				extra = 18,
				speed = 15,
				power = 12
			}},
			{name = 'bait', price = 75, metadata = {
				label = 'Deep Sea Fishing Bait',
				description = "Rarity: Expert \n\n Bonus Fish: +24% \n\n Catching Speed: +20% \n\n Lure Power: +16% \n\n Deep sea fishing bait commonly used in oceans and salt water fishing areas. Provides different bonuses while fishing.",
				image = 'deepsea_bait',
				rarity = 'rare',
				type = 'deepsea',
				extra = 24,
				speed = 20,
				power = 16
			}},
			{name = 'bait', price = 100, metadata = {
				label = 'Deep Sea Fishing Bait',
				description = "Rarity: Professional \n\n Bonus Fish: +35% \n\n Catching Speed: +25% \n\n Lure Power: +20% \n\n Deep sea fishing bait commonly used in oceans and salt water fishing areas. Provides different bonuses while fishing.",
				image = 'deepsea_bait',
				rarity = 'epic',
				type = 'deepsea',
				extra = 35,
				speed = 25,
				power = 20
			}},
			{name = 'bait', price = 150, metadata = {
				label = 'Deep Sea Fishing Bait',
				description = "Rarity: Master \n\n Bonus Fish: +50% \n\n Catching Speed: +30% \n\n Lure Power: +24% \n\n Deep sea fishing bait commonly used in oceans and salt water fishing areas. Provides different bonuses while fishing.",
				image = 'deepsea_bait',
				rarity = 'legendary',
				type = 'deepsea',
				extra = 50,
				speed = 30,
				power = 24
			}},

			{ name = 'fishing_basket', price = 2000 },
		},
		locations = {
			vec3(-3411.86, 964.23, 8.35)
		},
		targets = {

		}
	},
```