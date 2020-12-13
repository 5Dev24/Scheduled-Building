**Scheduled Building** allows for prefabs to be spawned on a schedule.



## Permissions

* `scheduledbuilding.getposition` -- Allows players to use /getposition

## Commands

* `/getposition` -- Prints out the player's position on rotation

## Configuration

```json
{
  "Prefabs": [
    {
      "Location": "0 0 0",
      "Rotation": "0 0 0 0",
      "Prefab": "assets/bundled/prefabs/autospawn/resource/loot/loot-barrel-1.prefab",
      "Spawn rate (in seconds)": 5,
      "Check for previous": true,
      "Should save": false
    }
  ],
  "Version": "0.0.0"
}
```

## For Developers

### Hooks

An extra check ran before spawning a prefab
```csharp
bool CanSpawnScheduledPrefab(Vector3 position, Quaternion rotation, string prefab, uint interval, bool check, bool save)
```

Notifies that a prefab has been spawned

Note: entity can be null
```csharp
void SpawnedScheduledPrefab(GameObject obj, BaseEntity entity)
```

## Credits

- **JackReigns**, came up with the idea
