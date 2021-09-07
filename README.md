# TF2 Persist Item

Provides some basic functionality to preserve currently equipped, non-loadout items.

This is provided as a proof-of-concept; developers should probably should be gutting it for
their own projects.  (For a more complete implementation, see how it's integrated in my
[Custom Weapons X][] project.)

[Custom Weapons X]: https://github.com/nosoop/SM-TFCustomWeaponsX

## Possibilities

- With some proper modifications in other core plugins, this allows custom weapon servers to not
have to detach / re-equip weapons, fixing a number of issues.
- Bots don't get their randomized loadouts regenerated when hitting resupply.

## Caveats

- Persisted item currently must be valid for the given class / slot.  As-is, doesn't support
Randomizer-like plugins.

## Usage

Install the plugin.  Requires [dynhooks][] and [tf2wearables][].

Implement a global forward callback on `TF2_OnReplaceItem`:

```
public Action TF2_OnReplaceItem(int client, int item) {
	// return Plugin_Continue if the currently equipped `item` should be replaced with the
	// one that's in the player's active loadout
}
```

[dynhooks]: https://forums.alliedmods.net/showpost.php?p=2588686&postcount=589
[tf2wearables]: https://github.com/nosoop/sourcemod-tf2wearables/releases
