# Troubleshooting

Solutions to common issues.

## Installation Problems

### Resource Won't Start

**Symptoms**: FiveMSecure doesn't appear in server console.

**Check**:
1. Folder name is exactly `fivemsecure` (lowercase, no spaces)
2. `ensure fivemsecure` is in server.cfg
3. No syntax errors in server.cfg
4. Resource files are not corrupted

**Solution**: Restart server completely, not just the resource.

### API Connection Failed

**Symptoms**: "Failed to connect to API server" error in console.

**Check**:
1. License key in server.cfg is correct
2. Server can reach api.fivemsecure.com
3. Firewall allows HTTPS (port 443)
4. No proxy blocking requests

**Test Connection**:
```bash
curl https://api.fivemsecure.com
```

Should return a response without errors.

## Dashboard Issues

### Can't Login

**Symptoms**: Discord login fails or infinite redirect.

**Solutions**:
1. Clear browser cache and cookies
2. Try incognito/private browsing mode
3. Verify Discord account is verified (check email)
4. Try a different browser
5. Disable browser extensions temporarily

### Empty Dashboard

**Symptoms**: No servers appear after logging in.

**Check**:
1. License is active and not expired
2. Server is running with FiveMSecure loaded
3. Discord ID matches license owner
4. Check "Invited Configs" section

**Solution**: Contact support if license should be active.

### Configuration Won't Save

**Symptoms**: Changes revert after clicking Save.

**Check**:
1. You have "Edit Settings" permission
2. Browser console for JavaScript errors (F12)
3. Network tab shows successful API response
4. Wait for success notification before leaving page

## Monitoring Issues

### Black Screen in Stream

**Symptoms**: Live monitoring shows black screen.

**Solutions**:
1. Player must have game window focused
2. Check config.lua has WebGL enabled
3. Ask player to alt-tab to game
4. Restart the stream
5. Check player's graphics settings

### Can't Connect to Stream

**Symptoms**: "Connection failed" error when starting stream.

**Check**:
1. Firewall allows UDP on streaming port (default 3001)
2. Port in server.cfg matches config.lua
3. WebSocket connection is active
4. Resource is started on server

**Firewall Check**:
```bash
# Linux
sudo ufw status | grep 3001

# Check if port is listening
netstat -an | grep 3001
```

### Laggy or Stuttering Stream

**Symptoms**: Stream is choppy or has low FPS.

**Solutions**:
1. Lower `frameRate` to 10-15 in config
2. Reduce `quality` to 0.5-0.6
3. Use 1280x720 resolution instead of 1080p
4. Check server and client bandwidth
5. Limit simultaneous streams to 2-3

## Protection Issues

### False Positive Detections

**Symptoms**: Legitimate players getting kicked or banned.

**Solutions**:
1. Change action from Ban to Warn
2. Monitor logs for patterns
3. Lower protection sensitivity if configurable
4. Whitelist specific players for testing
5. Report false positives on Discord

**Temporary Fix**:
```lua
-- Disable problematic protection
Config.antiNoclip = false
```

### Not Detecting Cheats

**Symptoms**: Known cheaters not being caught.

**Check**:
1. Protection is enabled in dashboard
2. Action is not set to "None"
3. FiveMSecure is latest version
4. No conflicting anti-cheat resources

**Solution**: Update to latest version and report on Discord.

## Performance Issues

### High Server CPU Usage

**Solutions**:
1. Reduce monitoring frameRate
2. Disable unused protections
3. Limit simultaneous streams
4. Check for conflicts with other resources

### High Bandwidth Usage

**Caused by**: Multiple active streams at high quality.

**Solutions**:
1. Lower stream quality setting
2. Reduce frameRate
3. Limit simultaneous viewers
4. Use smaller resolution

## Common Error Messages

### "Invalid license key"

Your license key in server.cfg doesn't match our records.

**Fix**: Copy license key exactly from dashboard.

### "License expired"

Your license has expired.

**Fix**: Renew license at fivemsecure.com.

### "WebSocket connection lost"

Server lost connection to FiveMSecure API.

**Fix**: 
1. Check server internet connection
2. Restart fivemsecure resource
3. Check firewall settings

### "Permission denied"

You don't have permission for this action.

**Fix**: Contact license owner to grant appropriate permissions.

## Getting Additional Help

If you still need assistance:

1. Check [FAQ](faq.md) for quick answers
2. Join [Discord](https://discord.gg/UCjjX5hqwV) for community help
3. Email support@fivemsecure.com with:
   - Server console logs
   - Browser console errors (F12)
   - Steps to reproduce the issue
   - FiveMSecure version