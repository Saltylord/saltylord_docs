# FAQ

## Do you plan to add support for other frameworks?

*I'm open to the idea but currently each release will only support ESX, QB, and QBX.*

---

## Do you plan to add support for other inventory systems?

*No. OX is free, secure, and feature rich. What more could you want?*

---

## Do I have to use Shoeshuffler's or BzZzi's models or can I use any model?

*Models can be changed and configured to whatever you want.*

---

## The property system we use is encrypted and there are no functions or events for entering / leaving the property. Can we use indoor planting?

*No. Without those functions or events you will not be able to load and unload the indoor models. The script works with instances, if the script can't track or see what instance the player is in and if its related to the property being entered. The indoor planting system will not work.*

*You can try contacting the developer of your housing script and asking if they can add entering and leaving exports or events. If they refuse, there is nothing I can do.*

---

## Script is displaying a client error similar to the one below.

*You can't use /giveitem to spawn seeds. You need to use the provided command /spawnSeed.*

```
MainThrd/ ^1SCRIPT ERROR: @sl-weed/client/main.lua:194: attempt to index a nil value (field '?')^7
MainThrd/ ^3> ref^7 (^5@sl-weed/client/main.lua^7:194)
MainThrd/ ^3> ref^7 (^5@ox_inventory/client.lua^7:448)
```

---

# When I place a plant down I can't interact with it (QBX ONLY).

*You need to follow the QBX install instructions and add '@qbx_core/modules/playerdata.lua' in the fxmanifest.lua*

```
MainThrd/ ^1SCRIPT ERROR: @sl-weed/bridge/qbx/client.lua:4: attempt to index a nil value (global 'QBX')^7
MainThrd/ ^3> getPlayerCitizenId^7 (^5@sl-weed/bridge/qbx/client.lua^7:4)
MainThrd/ ^3> cb^7 (^5@sl-weed/client/planting.lua^7:314)
MainThrd/ ^3> cb^7 (^5@ox_lib/imports/callback/client.lua^7:57)
MainThrd/ ^3> handler^7 (^5@ox_lib/imports/callback/client.lua^7:10)
```

---

## Script is displaying a client error similar to the one below.

*You will need to download and install an empty plant model since GTA does not have an empty plant pot model. There are links available for BzZzi's empty plant pots. I recommend this since its free.*

```
MainThrd/ ^1SCRIPT ERROR: @ox_lib/imports/requestModel/client.lua:10: attempted to load invalid model '-2091095138'^7
MainThrd/ ^3> requestModel^7 (^5@ox_lib/imports/requestModel/client.lua^7:10)
MainThrd/ ^3> handler^7 (^5@sl-weed/client/planting.lua^7:565)
```

---