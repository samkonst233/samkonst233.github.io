# Configuration

Configure FiveMSecure through the web dashboard.

## Accessing Configuration

1. Go to [fivemsecure.com/dashboard](https://fivemsecure.com/dashboard)
2. Sign in with Discord
3. Navigate to **Settings**

## Protection Actions

Each protection can be assigned one of these actions:

| Action | Behavior |
|--------|----------|
| **Ban** | Permanently removes player from server |
| **Kick** | Temporarily removes player from server |
| **Warn** | Logs violation without punishment |
| **None** | Disables the protection |

## General Settings

### Whitelist Mode

When enabled, only whitelisted players can join your server.
```lua
Config.enableWhitelist = true
```

Use this for private servers or during maintenance.

### Advanced Ban Logic

Enables enhanced detection algorithms for improved accuracy and fewer false positives.
```lua
Config.advancedBanLogic = true
```

Recommended to keep this enabled.

## Protection Categories

### Movement
- **Anti Noclip** - Prevents flying through walls
- **Anti Super Jump** - Blocks unrealistic jumping
- **Anti Freecam** - Stops freecam scouting
- **Anti Teleport** - Prevents unauthorized teleportation

### Player
- **Anti Invisibility** - Detects invisible players
- **Anti One-Punch** - Prevents instant kill melee
- **Heal/Armor Check** - Monitors health modifications

### Vehicle
- **Anti Vehicle Repair** - Blocks instant repair
- **Blacklisted Vehicles** - Ban specific vehicle models

### Explosion
- **Anti Explosions** - Prevents unauthorized explosions

### Aim
- **Anti Aimbot** - Detects aim assistance software

### Weapon
- **Blacklisted Weapons** - Ban specific weapons

### Ped
- **Blacklisted Peds** - Ban specific player models

### Cheats
- **Anti Eulen** - Detects Eulen cheat menu

### Injector
- **Protect Triggers** - Blocks unauthorized event triggers

## Managing Blacklists

Click the settings icon next to any blacklist protection to manage items.

### Example: Blacklisted Vehicles