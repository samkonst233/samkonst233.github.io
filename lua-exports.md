# Lua Exports

Use FiveMSecure functions in your own resources.

## Client Exports

### Check if Player is Banned
```lua
local isBanned = exports['fivemsecure']:IsPlayerBanned()
```

Returns `true` if the current player is banned.

### Get Player Protection Status
```lua
local protections = exports['fivemsecure']:GetProtectionStatus()
```

Returns a table with enabled protections.

## Server Exports

### Ban a Player
```lua
exports['fivemsecure']:BanPlayer(source, reason, duration)
```

**Parameters:**
- `source` - Player server ID
- `reason` - Ban reason (string)
- `duration` - Duration in minutes (0 for permanent)

**Example:**
```lua
-- Permanent ban
exports['fivemsecure']:BanPlayer(1, "Cheating", 0)

-- 24 hour ban
exports['fivemsecure']:BanPlayer(1, "Trolling", 1440)
```

### Kick a Player
```lua
exports['fivemsecure']:KickPlayer(source, reason)
```

**Parameters:**
- `source` - Player server ID
- `reason` - Kick reason (string)

**Example:**
```lua
exports['fivemsecure']:KickPlayer(1, "AFK")
```

### Check if Player is Whitelisted
```lua
local isWhitelisted = exports['fivemsecure']:IsPlayerWhitelisted(identifier)
```

**Parameters:**
- `identifier` - Player identifier (Steam, License, Discord)

**Returns:** `true` if whitelisted, `false` otherwise

### Add to Whitelist
```lua
exports['fivemsecure']:AddToWhitelist(identifier)
```

### Remove from Whitelist
```lua
exports['fivemsecure']:RemoveFromWhitelist(identifier)
```

## Events

### Player Banned
```lua
AddEventHandler('fivemsecure:playerBanned', function(source, reason, duration)
    print(('Player %s banned for: %s'):format(source, reason))
end)
```

### Player Kicked
```lua
AddEventHandler('fivemsecure:playerKicked', function(source, reason)
    print(('Player %s kicked for: %s'):format(source, reason))
end)
```

### Protection Triggered
```lua
AddEventHandler('fivemsecure:protectionTriggered', function(source, protectionType)
    print(('Protection %s triggered by %s'):format(protectionType, source))
end)
```