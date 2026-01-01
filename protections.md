# Protection Categories

FiveMSecure organizes anti-cheat features into 9 categories.

## Movement Protection

Detects abnormal player movement.

| Protection | Description |
|------------|-------------|
| **Anti Noclip** | Prevents flying through walls |
| **Anti Super Jump** | Blocks unrealistic jumping |
| **Anti Freecam** | Stops freecam scouting |
| **Anti Teleport** | Prevents unauthorized teleportation |

## Player Protection

Monitors player integrity and health.

| Protection | Description |
|------------|-------------|
| **Anti Invisibility** | Detects invisible players |
| **Anti One-Punch** | Prevents instant kill melee |
| **Heal/Armor Check** | Monitors health/armor modifications |

## Vehicle Protection

Controls vehicle spawning and modifications.

| Protection | Description |
|------------|-------------|
| **Anti Vehicle Repair** | Blocks instant vehicle repair |
| **Blacklisted Vehicles** | Ban specific vehicle models |

## Explosion Protection

Prevents griefing with explosions.

| Protection | Description |
|------------|-------------|
| **Anti Explosions** | Blocks unauthorized explosions |

## Aim Protection

Detects aim assistance cheats.

| Protection | Description |
|------------|-------------|
| **Anti Aimbot** | Detects aimbot software |

## Weapon Protection

Controls weapon usage.

| Protection | Description |
|------------|-------------|
| **Blacklisted Weapons** | Ban specific weapons |

## Ped Protection

Controls player models.

| Protection | Description |
|------------|-------------|
| **Blacklisted Peds** | Ban specific player models |

## Cheat Detection

Detects known cheat menus.

| Protection | Description |
|------------|-------------|
| **Anti Eulen** | Detects Eulen cheat menu |

## Injector Protection

Blocks unauthorized events.

| Protection | Description |
|------------|-------------|
| **Protect Triggers** | Block specific trigger events |

## Actions

When a protection detects a violation:

- **Ban** - Permanently bans the player
- **Kick** - Kicks the player from server
- **Warn** - Logs a warning only
- **None** - No action taken

## Example Configuration

Recommended starter setup:

- **Movement**: All enabled, action = Kick
- **Player**: All enabled, action = Warn
- **Vehicle**: Repair enabled, action = Kick
- **Explosion**: Enabled, action = Ban
- **Aim**: Enabled, action = Ban