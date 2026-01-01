# Configuration

Configure FiveMSecure through the web dashboard at [fivemsecure.com/dashboard](https://fivemsecure.com/dashboard).

## Protection Actions

Each protection can be configured with one of these actions:

| Action | Behavior |
|--------|----------|
| **Ban** | Permanently bans the player |
| **Kick** | Removes player from server |
| **Warn** | Logs a warning (no action taken) |
| **None** | Disables the protection |

## General Settings

### Whitelist

Enable to allow only whitelisted players to join.

### Advanced Ban Logic

Uses enhanced detection algorithms for better accuracy.

## Protection Categories

Configure protections by category in the dashboard:

### Movement
- Anti Noclip
- Anti Super Jump
- Anti Freecam
- Anti Teleport

### Player
- Anti Invisibility
- Anti One-Punch
- Heal/Armor Check

### Vehicle
- Anti Vehicle Repair
- Blacklisted Vehicles

### Explosion
- Anti Explosions

### Aim
- Anti Aimbot

### Weapon
- Blacklisted Weapons

### Ped
- Blacklisted Peds

### Cheats
- Anti Eulen

### Injector
- Protect Triggers

## Blacklists

Add items to blacklists through the dashboard:

**Vehicles**

## Webhooks

Configure Discord webhooks for logging:

- Join/Leave logs
- Ban logs
- Screenshot logs
- Resource logs

Add webhook URLs in the **Logs** section of the dashboard.

## Recommended Settings

For new servers:
```lua
-- Movement protections
antiNoclip = true (action: kick)
antiSuperjump = true (action: kick)
antiTeleport = true (action: ban)

-- Player protections
antiinvis = true (action: warn)
antiOnePunch = true (action: ban)

-- Explosion protection
antiExplosion = true (action: ban)

-- Aim protection
antiAimbot = true (action: ban)
```

## Best Practices

1. Start with **Warn** actions to test
2. Monitor logs for false positives
3. Gradually increase severity to **Kick** then **Ban**
4. Test configuration changes on a development server first

## Next Steps

- [Learn about protection categories](protections.md)
- [Set up live monitoring](monitoring.md)
- [Add admin users](admins.md)