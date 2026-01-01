# Protection Categories

FiveMSecure organizes anti-cheat features into nine logical categories.

## Movement Protection

Prevents exploits related to player movement.

### Anti Noclip

Detects and prevents noclip/fly cheats that allow players to pass through walls and objects.

**How it works**: Monitors player position changes and collision states to detect impossible movement patterns.

**Recommended action**: Kick or Ban

### Anti Super Jump

Prevents super jump cheats that allow players to jump unrealistically high.

**How it works**: Tracks jump velocity and height to detect modifications.

**Recommended action**: Kick

### Anti Freecam

Prevents freecam exploitation that allows players to scout areas without being visible.

**How it works**: Monitors camera position relative to player position.

**Recommended action**: Ban

### Anti Teleport

Prevents unauthorized teleportation to any location on the map.

**How it works**: Detects instant position changes beyond normal game mechanics.

**Recommended action**: Ban

## Player Protection

Monitors player integrity and prevents health-related cheats.

### Anti Invisibility

Prevents invisibility cheats that make players undetectable to others.

**How it works**: Checks player visibility states and alpha values.

**Recommended action**: Warn (can have false positives with some scripts)

### Anti One-Punch

Prevents one-punch kill cheats that instantly kill other players with melee attacks.

**How it works**: Monitors melee damage output for unrealistic values.

**Recommended action**: Ban

### Heal/Armor Check

Monitors and detects unauthorized health and armor modifications.

**How it works**: Tracks health and armor changes for impossible increases.

**Recommended action**: Ban

## Vehicle Protection

Controls vehicle spawning and modifications.

### Anti Vehicle Repair

Blocks instant vehicle repair cheats that restore vehicle health instantly.

**How it works**: Monitors vehicle health changes for instant repairs.

**Recommended action**: Kick

### Blacklisted Vehicles

Block specific vehicle models from being spawned on your server.

**Configuration**: Click settings to add vehicle spawn names.

**Common blacklisted vehicles**:
- RHINO (tank)
- LAZER (military jet)
- HYDRA (fighter jet)
- BUZZARD (attack helicopter)

**Recommended action**: Kick

## Explosion Protection

Prevents griefing with explosions.

### Anti Explosions

Prevents unauthorized explosions caused by cheat menus and exploits.

**How it works**: Monitors explosion events and validates their source.

**Recommended action**: Ban

## Aim Protection

Detects aim assistance cheats.

### Anti Aimbot

Detects aimbot software that automatically targets and tracks other players.

**How it works**: Analyzes aim snap speed, targeting patterns, and precision.

**Recommended action**: Ban

## Weapon Protection

Controls weapon usage on your server.

### Blacklisted Weapons

Block specific weapons from being used on your server.

**Configuration**: Click settings to add weapon hashes.

**Common blacklisted weapons**:
- WEAPON_RAILGUN
- WEAPON_MINIGUN  
- WEAPON_RPG
- WEAPON_FIREWORK

**Recommended action**: Kick

## Ped Protection

Controls player models.

### Blacklisted Peds

Block specific ped models from being used on your server.

**Configuration**: Click settings to add ped model names.

**Common blacklisted peds**:
- s_m_y_swat_01 (SWAT)
- s_m_y_cop_01 (Police)
- Various animal models

**Recommended action**: Kick

## Cheat Detection

Detects known cheat menus.

### Anti Eulen

Specifically detects and blocks the Eulen cheat menu.

**How it works**: Scans for Eulen menu signatures and behavior patterns.

**Recommended action**: Ban

## Injector Protection

Blocks unauthorized events and code injection.

### Protect Triggers

Blocks unauthorized trigger events from being executed by clients.

**Configuration**: Click settings to add event names to block.

**Common protected triggers**:
- esx:giveInventoryItem
- qb-admin:server:giveItem
- adminmenu:giveWeapon

**Recommended action**: Ban

## Tuning Your Configuration

### For Strict Servers

Enable all protections with Ban actions for zero tolerance.

### For Casual Servers

Use Warn and Kick actions to give players warnings before banning.

### For RP Servers

Be selective with vehicle and ped blacklists to allow roleplay scenarios.

## Understanding False Positives

Some protections may trigger on legitimate actions:

**Anti Invisibility**  
Can trigger with some admin scripts or game bugs. Start with Warn.

**Anti Vehicle Repair**  
May conflict with mechanic job scripts. Configure accordingly.

**Heal/Armor Check**  
Can trigger with hospital scripts or admin healing. Monitor closely.

## Next Steps

- [Set up live monitoring](monitoring.md)
- [Configure webhooks](dashboard.md#webhooks)
- [Add admin users](admins.md)