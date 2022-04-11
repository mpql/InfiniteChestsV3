# InfiniteChestsV3-mpql

This is the collection of ongoing compatibility and bug fixes I've written for [Zaicon/InfiniteChestsV3](https://github.com/Zaicon/InfiniteChestsV3) from 2020-2022, as that seems to be abandoned.

If anyone wants to tackle any issues, please feel free to send PRs. I am not a C#-, or even a software programmer, so I cannot guarantee I'll make any updates / bugfixes myself unless I'm actively playing and happen to have the motivation to hunt something down.

You can find the latest release available for download at [mpql/InfiniteChestsV3/releases](https://github.com/mpql/InfiniteChestsV3/releases).


## Changelog

Note: I'm changing the versioning scheme with 1.6.0-mpql to be more in line with [semver](https://github.com/semver/semver).

### 1.6.0-mpql
- Updated for TShock 4.5.17 / Terraria 1.4.3.6
- Chest naming is still broken

### 1.3.0.0-mpql.2
- Updated for  TShock 4.5.4 / Terraria 1.4.2.3

### 1.3.0.0-mpql.1
- Fixes [#6 Corrupted Chest Bug After Spawning Mimic](https://github.com/Zaicon/InfiniteChestsV3/issues/6)
- Fixes [#10 Key of Light / Dark - Multiple Issues](https://github.com/Zaicon/InfiniteChestsV3/issues/10)
	- Mimics spawned outside of Corruption or Crimson will randomly spawn as either Corrupted or Crimson, so you can access mimics from outside your world's evil without having to build a corresponding section of the world.
- Fixes [#11 Raise chest limit to 8000](https://github.com/Zaicon/InfiniteChestsV3/issues/11)

---


# Original Readme

## InfiniteChestsV3

### Plugin Features:
- Saves chests to database, allowing more than 8,000 chests per map.
- Allows conversion of chest storage to/from database at will.
- Allows chests to be "claimed" (protected) by users.
- Allows chests to be "public" (other users can edit but not destroy).
- Allows chests to "refill" (chest contents are restored at a specified interval).
- Allows players to destroy all empty chests automatically.
- Allows players to allow only certain users and/or groups to access protected chests.
- Allows players to search the entire chest database for specific items.
- Supports usage of Key of Light/Key of Night items.

### Things this plugin will not do (as of now):
* Chest name support. Chest names are stored in tile data, which would be very costly to implement.

### Commands
```
/chest claim - Protects a chest via user account.
/chest unclaim - Unprotects a chest.
/chest info - Displays X/Y coordinates and account owner.
/chest search <item name> - Searches chests for a specific item.
/chest allow <player name> - Gives user access to chest.
/chest remove <player name> - Removes chest access from user.
/chest allowgroup <group name> - Gives players with that group access to chest.
/chest removegroup <group name> - Removes group access to chest.
/chest public - Toggles the 'public' setting of a chest, allowing others to use but not destroy the chest.
/chest refill <seconds> - Sets the interval in which chests refill items.
/chest cancel - Cancels any of the above actions.
/convchests [-r] - Converts any "real" chests to database chests (or reverse with `-r`).
/prunechests - Permanently removes empty chests from the world and database.
/transferchests - Converts the database from InfiniteChests V1 or V2 to InfiniteChestsV3.
```

###Permisisons
```
ic.use - Enables use of /chest
ic.claim - Enables use of /chest claim, unclaim
ic.info - Enables use of /chest info
ic.search - Enables use of /chest search
ic.public - Enables use of /chest public
ic.protect - Players with this permission will have their chests automatically protected via user account.
ic.refill - Enables use of /chest refill
ic.edit - Allows player to edit any chest regardless of chest protection.
ic.convert - Enables use of /convchests
ic.prune - Enables use of /prunechests
ic.transfer - Enables use of /transferchests
```
