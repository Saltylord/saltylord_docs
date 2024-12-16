# General Install Instructions

## General
- *Drag and drop the sl-weed folder into your resources folder*
- *Run the sl_weed.sql file located the in the install folder*
- *Add ensure sl-weed in your resource.cfg*
- *Copy and paste the images from the images folder into your inventory*

## Spawning Seeds for testing using /spawnSeed
*You **CAN NOT** use /giveitem to spawn seeds due to the seeds metadata. You MUST use the provided admin command /spawnSeed to spawn seeds correctly*

## Creating and using Joints
*To make joints you must complete the growing and drying process and use the finished product due to metadata*

- Right click on a strain and select "Roll Joint"
- For joints larger then 1 gram. Have between 1 and your configured maxGramsPerJoint moved into another slot, right click, and select "Roll Joint".

## Items
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
        stack = true,
        client = {
            image = "joint.png"
        },
        server = {
            export = 'sl-weed.joint'
        },
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
```

## Shops
*If you want to use the gathering system*

```lua
	Weed = {
		name = 'Weed Shop',
		blip = {
			id = 59, colour = 67, scale = 0.8
		},
		inventory = {
			{name = 'plant_nutrition', price = 100},
			{name = 'plant_water', price = 100},
			{name = 'plant_cure', price = 100},
			{name = 'plant_pot', price = 100},
			{name = 'rolling_papers', price = 100},
		},
		locations = {
			vec3(-1174.14, -1573.76, 4.37)
		},
		targets = {

		}
	},
```

*If you want the seeds to be purchased from a shop*

```lua
	Weed = {
		name = 'Weed Shop',
		blip = {
			id = 59, colour = 67, scale = 0.8
		},
		inventory = {
			{name = 'weed_seed', price = 100, metadata = {
				label = 'OG Kush Seed',
				description = "Type: Sativa \n\n Sex: Female \n\n A seed for growing weed.",
				strain = 'OG Kush',
				type = 'sativa',
				sex = 'female',
				model = 'base',
				budImage = 'green_3'
			}},
			{name = 'weed_seed', price = 100, metadata = {
				label = 'OG Kush Seed',
				description = "Type: Sativa \n\n Sex: Male \n\n A seed for breeding new plant types.",
				strain = 'OG Kush',
				type = 'sativa',
				sex = 'male',
				model = 'base',
				budImage = 'green_3'
			}},

			{name = 'weed_seed', price = 100, metadata = {
				label = 'Sour Diesel Seed',
				description = "Type: Sativa \n\n Sex: Female \n\n A seed for growing weed.",
				strain = 'Sour Diesel',
				type = 'sativa',
				sex = 'female',
				model = 'base',
				budImage = 'green_orange_blue'
			}},
			{name = 'weed_seed', price = 100, metadata = {
				label = 'Sour Diesel Seed',
				description = "Type: Sativa \n\n Sex: Male \n\n A seed for breeding new plant types.",
				strain = 'Sour Diesel',
				type = 'sativa',
				sex = 'male',
				model = 'base',
				budImage = 'green_orange_blue'
			}},

			{name = 'weed_seed', price = 100, metadata = {
				label = 'Blue Dream Seed',
				description = "Type: Sativa \n\n Sex: Female \n\n A seed for growing weed.",
				strain = 'Blue Dream',
				type = 'sativa',
				sex = 'female',
				model = 'base',
				budImage = 'green_2'
			}},
			{name = 'weed_seed', price = 100, metadata = {
				label = 'Blue Dream Seed',
				description = "Type: Sativa \n\n Sex: Male \n\n A seed for breeding new plant types.",
				strain = 'Blue Dream',
				type = 'sativa',
				sex = 'male',
				model = 'base',
				budImage = 'green_2'
			}},

			{name = 'weed_seed', price = 100, metadata = {
				label = 'Purple Haze Seed',
				description = "Type: Indica \n\n Sex: Female \n\n A seed for growing weed.",
				strain = 'Purple Haze',
				type = 'indica',
				sex = 'female',
				model = 'base',
				budImage = 'purple_orange'
			}},
			{name = 'weed_seed', price = 100, metadata = {
				label = 'Purple Haze Seed',
				description = "Type: Indica \n\n Sex: Male \n\n A seed for breeding new plant types.",
				strain = 'Purple Haze',
				type = 'indica',
				sex = 'male',
				model = 'base',
				budImage = 'purple_orange'
			}},

			{name = 'weed_seed', price = 100, metadata = {
				label = 'Hindu Kush Seed',
				description = "Type: Indica \n\n Sex: Female \n\n A seed for growing weed.",
				strain = 'Hindu Kush',
				type = 'indica',
				sex = 'female',
				model = 'base',
				budImage = 'green_orange'
			}},
			{name = 'weed_seed', price = 100, metadata = {
				label = 'Hindu Kush Seed',
				description = "Type: Indica \n\n Sex: Male \n\n A seed for breeding new plant types.",
				strain = 'Hindu Kush',
				type = 'indica',
				sex = 'male',
				model = 'base',
				budImage = 'green_orange'
			}},

			{name = 'weed_seed', price = 100, metadata = {
				label = 'Gorilla Glue #4 Seed',
				description = "Type: Indica \n\n Sex: Female \n\n A seed for growing weed.",
				strain = 'Gorilla Glue #4',
				type = 'indica',
				sex = 'female',
				model = 'base',
				budImage = 'green_purple_orange'
			}},
			{name = 'weed_seed', price = 100, metadata = {
				label = 'Gorilla Glue #4 Seed',
				description = "Type: Indica \n\n Sex: Male \n\n A seed for breeding new plant types.",
				strain = 'Gorilla Glue #4',
				type = 'indica',
				sex = 'male',
				model = 'base',
				budImage = 'green_purple_orange'
			}},

			{name = 'plant_nutrition', price = 100},
			{name = 'plant_water', price = 100},
			{name = 'plant_cure', price = 100},
			{name = 'plant_pot', price = 100},
		},
		locations = {
			vec3(-1174.14, -1573.76, 4.37)
		},
		targets = {

		}
	},
```