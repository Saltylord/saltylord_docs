# Shops

*This shop does not include the 6 parent strains and is intended for gathering to be enabled*

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

---

*If you would like players to be able to purchase seeds from a store, use the shop below. I recommend disabling gathering if you choose to do this, but it is not required.*

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