# Loot Tables Docs

Loot Tables is JSON File use to handle loot from the entity, block, chest and certain gameplay like Piglin Barter and Fishing. 

## Create custom loot table

To create your custom loot table, create JSON file on `<BehaviorPack>/loot_tables/`. For entity loot, put on `loot_tables/entities/`,  and block put on `loot_tables/blocks/`

First thing you need is adding `"pools"` component. Inside that, add `rolls` to rolls how much item on `entries` drop. See example below (Or check my template)
```json
{
    "pools": [
        {
            "rolls": 1,
            "entries": []
        }
    ]
}
```

## Linking custom loot table for my custom entity/block

On your custom block/entity, use `minecraft:loot` to linking your custom loot table. 
```json
{
    "minecraft:loot": "loot_tables/path/to/your/file"
}
```