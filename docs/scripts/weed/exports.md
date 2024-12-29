# Exports

## **loadIndoorPlants**

Loads active indoor plants off the client's current instance

```lua
    exports['sl-weed']:loadIndoorPlants(src)
```

| arg    | type   |
| ------ | ------ |
| `src`  | `int` |


---

## **deleteIndoorPlants**

*Must be used before the client's instance is reset back to 0.*

Delete active indoor plants off the client's current instance

```lua
    exports['sl-weed']:deleteIndoorPlants(src, instance)
```

| arg         | type   |
| ------      | ------ |
| `src`       | `int` |
| `instance`  | `int` |
