# General Install Instructions

## General
- *Drag and drop the sl-weed folder into your resources folder*
- *Run the sl_weed.sql file located the in the install folder*
- *Add ensure sl-weed in your resource.cfg*
- *Copy and paste the items and shops into your inventory*
- *Copy and paste the images from the images folder into your inventory*
- *Download and install any empty plant pot model*
- *Follow additional steps located in Empty Plant Pots, Items, Shops, Genetics Tracking, and Framework*
- *Please read through each section below*

---

## Remove Other Weed Scripts
*For my script to function correctly. You need to remove past weed scripts, items related to these scripts, and database tables related to these scripts. Failure to do this will likely result in start up errors, plants not loading, or general server errors.*

---

## Frameworks
*My script will automatically detect QBCore and ESX so there is no additional installation steps for these frameworks. For QBX users please head to the Framework section and follow the extra steps.*

---

## Indoor Planting
*Indoor planting requires a properties system that uses instances. Below are a list of housing scripts that are supported and have installation instructions included in the Housing section. If you are using a custom housing system you can find exports inside the Exports section. Add those into you housing system for indoor planting support.*

| Scripts                 | Support                       |
| ----------------------- | ----------------------------- |
| `ps-housing v1.0`       |   ✔️   Supported               |
| `ps-housing v2.0`       |   ✔️   Supported               |
| `nolag_properties`      |   ✔️   Supported               |


---

## Genetics Tracking / FiveManage
*With genetics tracking enabled, if you want to use the Genetics Book and see the images of the strains. You will need to set up a FiveManage account. Once you've set one up or if you already have one created. Then you can head to the Genetics Tracking section in the Docs.*

---

## Spawning Seeds for testing using /spawnSeed
*You **CAN NOT** use /giveitem to spawn seeds due to the seeds metadata. You MUST use the provided admin command /spawnSeed to spawn seeds correctly*

---

## Creating / Using Joints
*To make joints you must complete the growing and drying process and use the finished product due to metadata*

- Right click on a strain and select "Roll Joint"
- For joints larger then 1 gram. Have between 1 and your configured maxGramsPerJoint moved into another slot, right click, and select "Roll Joint".
