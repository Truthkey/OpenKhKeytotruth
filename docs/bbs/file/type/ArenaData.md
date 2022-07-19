# ARENADATA Format

This file stores a list missions on Mirage Arena and parameters related to them.

This file is contained within `arc/system/common_vs.arc` named `ArenaData.bin`.

## Arena Mission Order

| Name  | Description
|-------|------------
| BATTLE_TYPE_JUDGE   | Day of Reckoning
| BATTLE_TYPE_CURSE   | Wheels of Misfortune
| BATTLE_TYPE_TREASURE   | Risky Riches
| BATTLE_TYPE_RUN   | Weaver Fever
| BATTLE_TYPE_PRISON   | Sinister Sentinel
| BATTLE_TYPE_DAZZLE   | Dead Ringer
| BATTLE_TYPE_TYRANT   | Combined Threat
| BATTLE_TYPE_DESIRE   | Treasure Tussle
| BATTLE_TYPE_CRIME   | Harsh Punishment
| BATTLE_TYPE_BLIZZARD   | A Time to Chill
| BATTLE_TYPE_MAGICIAN   | Copycat Crisis
| BATTLE_TYPE_ARENA_OWNER   | Keepers of the Arena
| BATTLE_TYPE_WHALE   | Monster of the Sea
| BATTLE_TYPE_CONQUEROR   | Villains' Vendetta
| BATTLE_TYPE_LIGHT_MASTER   | Light's Lessions
| BATTLE_TYPE_DARKNESS   | Peering into Darkness

## Arena Data 1

This section is read until a completely NULL section is found. 

| Offset | Type  | Description
|--------|-------|------------
| 0x0     | uint32   | CTD ID
| 0x4     | int8     | Area
| 0x5     | int8     | Rank
| 0x6     | int8     | Level
| 0x7     | int8     | Extra
| 0x8     | uint16   | Medal Reward
| 0xA     | uint16   | Data (Arena Data 2 offset)
| 0xC     | int8     | Rounds Count
| 0xD     | int8     | Text ID
| 0xE     | int8     | Area Data
| 0xF     | int8     | Area Count

## Arena Data 2

This section has a list of bytes representing the OLO being used on each round.