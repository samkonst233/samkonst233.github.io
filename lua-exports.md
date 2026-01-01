# Lua Exports

Use FiveMSecure functions in your custom resources.

## Client Exports

### IsPlayerBanned

Check if the current player is banned.
```lua
local isBanned = exports['fivemsecure']:IsPlayerBanned()
```

**Returns**: `boolean` - True if player is banned

**Example**:
```lua
if exports['fivemsecure']:IsPlayerBanned() then
    print("You are banned from this server")
end
```

### GetProtectionStatus

Get status of all protections.
```lua
local protections = exports['fivemsecure']:GetProtectionStatus()
```

**Returns**: `table` - Protection status data

**Example**:
```lua
local status = exports['fivemsecure']:GetProtectionStatus()
print("Noclip protection:", status.antiNoclip)
```

## Server Exports

### BanPlayer

Ban a player from the server.
```lua
exports['fivemsecure']:BanPlayer(source, reason, duration)
```

**Parameters**:
- `source` (number) - Player server ID
- `reason` (string) - Ban reason
- `duration` (number) - Duration in minutes (0 for permanent)

**Example**:
```lua
-- Permanent ban
exports['fivemsecure']:BanPlayer(1, "Cheating detected", 0)

-- 24-hour ban
exports['fivemsecure']:BanPlayer(1, "Excessive trolling", 1440)

-- 7-day ban
exports['fivemsecure']:BanPlayer(1, "Rule violation", 10080)
```

### KickPlayer

Kick a player from the server.
```lua
exports['fivemsecure']:KickPlayer(source, reason)
```

**Parameters**:
- `source` (number) - Player server ID
- `reason` (string) - Kick reason

**Example**:
```lua
exports['fivemsecure']:KickPlayer(1, "AFK timeout")
```

### IsPlayerWhitelisted

Check if a player is whitelisted.
```lua
local isWhitelisted = exports['fivemsecure']:IsPlayerWhitelisted(identifier)
```

**Parameters**:
- `identifier` (string) - Player identifier (Steam, License, or Discord)

**Returns**: `boolean` - True if whitelisted

**Example**:
```lua
local steamId = "steam:110000abcdef"
if exports['fivemsecure']:IsPlayerWhitelisted(steamId) then
    print("Player is whitelisted")
end
```

### AddToWhitelist

Add a player to the whitelist.
```lua
exports['fivemsecure']:AddToWhitelist(identifier)
```

**Parameters**:
- `identifier` (string) - Player identifier

**Example**:
```lua
exports['fivemsecure']:AddToWhitelist("steam:110000abcdef")
```

### RemoveFromWhitelist

Remove a player from the whitelist.
```lua
exports['fivemsecure']:RemoveFromWhitelist(identifier)
```

**Parameters**:
- `identifier` (string) - Player identifier

**Example**:
```lua
exports['fivemsecure']:RemoveFromWhitelist("steam:110000abcdef")
```

## Events

### playerBanned

Triggered when a player is banned.
```lua
AddEventHandler('fivemsecure:playerBanned', function(source, reason, duration)
    print(string.format('Player %s banned for: %s', source, reason))
end)
```

**Parameters**:
- `source` (number) - Player who was banned
- `reason` (string) - Ban reason
- `duration` (number) - Ban duration in minutes

### playerKicked

Triggered when a player is kicked.
```lua
AddEventHandler('fivemsecure:playerKicked', function(source, reason)
    print(string.format('Player %s kicked for: %s', source, reason))
end)
```

**Parameters**:
- `source` (number) - Player who was kicked
- `reason` (string) - Kick reason

### protectionTriggered

Triggered when any protection detects a violation.
```lua
AddEventHandler('fivemsecure:protectionTriggered', function(source, protectionType, action)
    print(string.format('Protection %s triggered by %s - Action: %s', protectionType, source, action))
end)
```

**Parameters**:
- `source` (number) - Player who triggered protection
- `protectionType` (string) - Type of protection (e.g., "antiNoclip")
- `action` (string) - Action taken ("ban", "kick", "warn", "none")

## Integration Example

Example admin command using exports:
```lua
RegisterCommand('adminban', function(source, args, rawCommand)
    -- Check if player is admin
    if not IsPlayerAceAllowed(source, 'admin') then
        return
    end

    local targetId = tonumber(args[1])
    local reason = table.concat(args, ' ', 2)

    if not targetId or not reason then
        TriggerClientEvent('chat:addMessage', source, {
            color = { 255, 0, 0 },
            multiline = true,
            args = {"Error", "Usage: /adminban [id] [reason]"}
        })
        return
    end

    -- Use FiveMSecure export to ban
    export