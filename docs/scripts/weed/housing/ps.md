# Project Sloth

## ps-housing v1.0

*ps-housing/server/sv_property.lua*

```lua
	function Property:PlayerEnter(src)
	    local _src = tostring(src)
	    self.playersInside[_src] = true

	    TriggerClientEvent('qb-weathersync:client:DisableSync', src)
	    TriggerClientEvent('ps-housing:client:enterProperty', src, self.property_id)

	    if next(self.playersDoorbell) then
	        TriggerClientEvent("ps-housing:client:updateDoorbellPool", src, self.property_id, self.playersDoorbell)
	        if self.playersDoorbell[_src] then
	            self.playersDoorbell[_src] = nil
	        end
	    end

	    local citizenid = GetCitizenid(src)

	    if self:CheckForAccess(citizenid) then
	        local Player = QBCore.Functions.GetPlayer(src)
	        local insideMeta = Player.PlayerData.metadata["inside"]

	        insideMeta.property_id = self.property_id
	        Player.Functions.SetMetaData("inside", insideMeta)
	    end

	    local bucket = tonumber(self.property_id) -- because the property_id is a string
	    SetPlayerRoutingBucket(src, bucket)
	    Player(src).state:set('instance', bucket, true)
	    exports['sl-weed']:loadIndoorPlants(src) -- Best to place at the end
	end
```

```lua
	RegisterNetEvent('ps-housing:server:leaveProperty', function (property_id)
	    local src = source
	    local property = Property.Get(property_id)

	    if not property then return end

	    exports['sl-weed']:deleteIndoorPlants(src, Player(src).state.instance) -- Add before the routing bucket is reset back to 0
	    property:PlayerLeave(src)
	end)
```

---

## ps-housing v2.0

*ps-housing/server/sv_property.lua*

```lua
	function Property:PlayerEnter(src)
	    local _src = tostring(src)
	    local isMlo = self.propertyData.shell == 'mlo'
	    local isIpl = self.propertyData.apartment and Config.Apartments[self.propertyData.apartment].interior

	    self.playersInside[_src] = true

	    if not isMlo then
	        TriggerClientEvent('qb-weathersync:client:DisableSync', src)
	    end

	    TriggerClientEvent('ps-housing:client:enterProperty', src, self.property_id, isMlo, self.propertyData)

	    if next(self.playersDoorbell) then
	        TriggerClientEvent("ps-housing:client:updateDoorbellPool", src, self.property_id, self.playersDoorbell)
	        if self.playersDoorbell[_src] then
	            self.playersDoorbell[_src] = nil
	        end
	    end

	    local citizenid = GetCitizenid(src)

	    if self:CheckForAccess(citizenid) then
	        local Player = QBCore.Functions.GetPlayer(src)
	        local insideMeta = Player.PlayerData.metadata["inside"]

	        insideMeta.property_id = self.property_id
	        Player.Functions.SetMetaData("inside", insideMeta)
	    end

	    if not isMlo or isIpl then
	        local bucket = tonumber(self.property_id) -- because the property_id is a string
	        QBCore.Functions.SetPlayerBucket(src, bucket)
	    end

		exports['sl-weed']:loadIndoorPlants(src) -- Best to place at the end
	end
```

```lua
	RegisterNetEvent('ps-housing:server:leaveProperty', function (property_id)
	    local src = source
	    local property = Property.Get(property_id)

	    if not property then return end

    	exports['sl-weed']:deleteIndoorPlants(src, Player(src).state.instance) -- Add before the routing bucket is reset back to 0
	    property:PlayerLeave(src)
	end)
```