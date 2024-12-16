# NoLag

*Place under function "updatePlantData" inside sl-weed/server/planting.lua*

```lua
	RegisterNetEvent('nolag_properties:server:property:enter', function(propertyId)
	    local src = source
	    local instance = propertyId

	    for i = 1, #plants do
	        if (plants[i].metadata.instance ~= 0) and (plants[i].metadata.instance == instance) then
	            local model = models[plants[i].metadata.model][plants[i].metadata.stage]
	            local entity = CreateObjectNoOffset(model, plants[i].metadata.coords.x, plants[i].metadata.coords.y, plants[i].metadata.coords.z, true, true, false)
	            FreezeEntityPosition(entity, true)
	            SetEntityRoutingBucket(entity, plants[i].metadata.instance)

	            indoorPlants[#indoorPlants + 1] = {
	                id = plants[i].id,
	                instance = plants[i].metadata.instance,
	                coords = plants[i].metadata.coords,
	                model = plants[i].metadata.model,
	                entity = entity
	            }
	        end
	    end

	    if Config.debug then
	        TriggerClientEvent('table', src, indoorPlants)
	    end
	end)

	RegisterNetEvent('nolag_properties:server:property:exit', function (propertyId)
	    local src = source

	    for i = 1, #indoorPlants do
	        if indoorPlants[i].instance == propertyId then
	            local entity = indoorPlants[i].entity

	            DeleteEntity(entity)

	            if Config.debug then
	                print('deleteIndoorPlants: Deleted entity: ' .. entity)
	            end
	        end
	    end

	    indoorPlants = {}
	end)
```