# BzZzi

## BzZzi's Colored Weed Plants V2

*First change the Config.stages table to only 5 stages.*

```lua
    Config.stages = {
        0, -- 1
        20, -- 2
        50, -- 3
        70, -- 4
        90 -- 5
    }
```

---

*Replace the models and images tables with the ones below inside the menu.lua file.*

```lua
    models = {
        {
            label = 'Base',
            value = 'base'
        },
        {
            label = 'Blue',
            value = 'blue'
        },
        {
            label = 'Cyan',
            value = 'cyan'
        },
        {
            label = 'Green',
            value = 'green'
        },
        {
            label = 'Maroon',
            value = 'maroon'
        },
        {
            label = 'Nature',
            value = 'natur'
        },
        {
            label = 'Navy',
            value = 'navy'
        },
        {
            label = 'Purple',
            value = 'purple'
        },
        {
            label = 'Red',
            value = 'red'
        },
        {
            label = 'Romance',
            value = 'romance'
        },
        {
            label = 'Sea',
            value = 'sea'
        },
        {
            label = 'Sunny',
            value = 'sunny'
        },
        {
            label = 'Yellow',
            value = 'yellow'
        },
    },
    images = {
        {
            label = 'Green',
            value = 'green'
        },
        {
            label = 'Green 2',
            value = 'green_2'
        },
        {
            label = 'Green 3',
            value = 'green_3'
        },
        {
            label = 'Green 4',
            value = 'green_4'
        },
        {
            label = 'Green Orange',
            value = 'green_orange'
        },
        {
            label = 'Green Orange 2',
            value = 'green_orange_2'
        },
        {
            label = 'Green Orange 3',
            value = 'green_orange_3'
        },
        {
            label = 'Green Orange 4',
            value = 'green_orange_4'
        },
        {
            label = 'Green Orange 5',
            value = 'green_orange_5'
        },
        {
            label = 'Green Orange 6',
            value = 'green_orange_6'
        },
        {
            label = 'Green Orange 7',
            value = 'green_orange_7'
        },
        {
            label = 'Green Orange Blue',
            value = 'green_orange_blue'
        },
        {
            label = 'Green Purple Orange',
            value = 'green_purple_orange'
        },
        {
            label = 'Green Purple Orange 2',
            value = 'green_purple_orange_2'
        },
        {
            label = 'Green Purple Orange 3',
            value = 'green_purple_orange_3'
        },
        {
            label = 'Purple',
            value = 'purple'
        },
        {
            label = 'Purple Orange',
            value = 'purple_orange'
        },
        {
            label = 'Purple Orange',
            value = 'purple_orange_2'
        },
    }
```

---

*Replace the models with the ones below inside the models.lua file.*

```lua
    dead = {
        'bzzz_growing_freepot_a',
        'bzzz_growing_freepot_b',
        'bzzz_growing_freepot_c',
        'bzzz_growing_freepot_d'
    },
    base = {
        'bkr_prop_weed_01_small_01c',
        'bkr_prop_weed_01_small_01b',
        'bkr_prop_weed_med_01a',
        'bkr_prop_weed_lrg_01a',
        'bkr_prop_weed_lrg_01b'
    },
    blue = {
        'bzzz_plants_weed_blue_small',
        'bzzz_plants_weed_blue_medium',
        'bzzz_plants_weed_blue_big',
        'bzzz_plants_weed_blue_bud',
        'bzzz_plants_weed_blue_bud_big'
    },
    cyan = {
        'bzzz_plants_weed_cyan_small',
        'bzzz_plants_weed_cyan_medium',
        'bzzz_plants_weed_cyan_big',
        'bzzz_plants_weed_cyan_bud',
        'bzzz_plants_weed_cyan_bud_big'
    },
    green = {
        'bzzz_plants_weed_green_small',
        'bzzz_plants_weed_green_medium',
        'bzzz_plants_weed_green_big',
        'bzzz_plants_weed_green_bud',
        'bzzz_plants_weed_green_bud_big'
    },
    maroon = {
        'bzzz_plants_weed_maroon_small',
        'bzzz_plants_weed_maroon_medium',
        'bzzz_plants_weed_maroon_big',
        'bzzz_plants_weed_maroon_bud',
        'bzzz_plants_weed_maroon_bud_big'
    },
    natur = {
        'bzzz_plants_weed_natur_small',
        'bzzz_plants_weed_natur_medium',
        'bzzz_plants_weed_natur_big',
        'bzzz_plants_weed_natur_bud',
        'bzzz_plants_weed_natur_bud_big'
    },
    navy = {
        'bzzz_plants_weed_navy_small',
        'bzzz_plants_weed_navy_medium',
        'bzzz_plants_weed_navy_big',
        'bzzz_plants_weed_navy_bud',
        'bzzz_plants_weed_navy_bud_big'
    },
    purple = {
        'bzzz_plants_weed_purple_small',
        'bzzz_plants_weed_purple_medium',
        'bzzz_plants_weed_purple_big',
        'bzzz_plants_weed_purple_bud',
        'bzzz_plants_weed_purple_bud_big'
    },
    red = {
        'bzzz_plants_weed_red_small',
        'bzzz_plants_weed_red_medium',
        'bzzz_plants_weed_red_big',
        'bzzz_plants_weed_red_bud',
        'bzzz_plants_weed_red_bud_big'
    },
    romance = {
        'bzzz_plants_weed_romance_small',
        'bzzz_plants_weed_romance_medium',
        'bzzz_plants_weed_romance_big',
        'bzzz_plants_weed_romance_bud',
        'bzzz_plants_weed_romance_bud_big'
    },
    sea = {
        'bzzz_plants_weed_sea_small',
        'bzzz_plants_weed_sea_medium',
        'bzzz_plants_weed_sea_big',
        'bzzz_plants_weed_sea_bud',
        'bzzz_plants_weed_sea_bud_big'
    },
    sunny = {
        'bzzz_plants_weed_sunny_small',
        'bzzz_plants_weed_sunny_medium',
        'bzzz_plants_weed_sunny_big',
        'bzzz_plants_weed_sunny_bud',
        'bzzz_plants_weed_sunny_bud_big'
    },
    yellow = {
        'bzzz_plants_weed_yellow_small',
        'bzzz_plants_weed_yellow_medium',
        'bzzz_plants_weed_yellow_big',
        'bzzz_plants_weed_yellow_bud',
        'bzzz_plants_weed_yellow_bud_big'
    }
```