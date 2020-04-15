# TF2 Persist Item

Provides some basic functionality to preserve currently equipped items.  Probably should be
gutting it for your own setups.

## Possibilities

- With some proper modifications in other core plugins, this allows custom weapon servers to not
have to detach / re-equip weapons, fixing a number of issues.
- Bots don't get their loadouts regenerated when hitting resupply.

## Caveats

- Persisted item currently must be valid for the given class / slot.  As-is, doesn't support
Randomizer-like plugins.
