# Troubleshooting

Common issues and solutions.

## Installation Issues

### Resource Won't Start

**Symptoms**: FiveMSecure doesn't appear in server console

**Solutions**:
1. Check folder name is exactly `fivemsecure`
2. Verify `ensure fivemsecure` in server.cfg
3. Check for syntax errors in server.cfg
4. Restart server completely

### Connection Failed

**Symptoms**: "Failed to connect to API" error

**Solutions**:
1. Verify license key is correct
2. Check server can reach api.fivemsecure.com
3. Confirm firewall isn't blocking port 443
4. Test with: `curl https://api.fivemsecure.com`

## Dashboard Issues

### Can't Login

**Solutions**:
1. Clear browser cache and cookies
2. Try incognito/private browsing
3. Check Discord account is verified
4. Try different browser

### No Servers Showing

**Solutions**:
1. Verify license is active
2. Check server is running FiveMSecure
3. Confirm Discord ID matches license owner

### Configuration Not Saving

**Solutions**:
1. Click "Save Config" button
2. Wait for success notification
3. Check browser console for errors
4. Verify you have edit permissions

## Monitoring Issues

### Black Screen

**Solutions**:
1. Check player has game window focused
2. Verify WebGL is enabled
3. Restart the stream

### Stream Won't Connect

**Solutions**:
1. Check firewall allows UDP on streaming port
2. Verify port 3001 is open
3. Restart FiveMSecure resource

### Laggy Stream

**Solutions**:
1. Lower frame rate in config
2. Reduce stream quality
3. Use smaller resolution

## Protection Issues

### False Positives

**Solutions**:
1. Lower protection sensitivity
2. Use "Warn" action instead of "Ban"
3. Check logs for patterns
4. Whitelist legitimate players

### Not Detecting Cheats

**Solutions**:
1. Verify protection is enabled
2. Check action is not set to "None"
3. Update to latest version
4. Review configuration

## Getting Help

If you still need help:

1. Check [FAQ](faq.md)
2. Join [Discord](https://discord.gg/UCjjX5hqwV)
3. Email support@fivemsecure.com

Include this information:
- Server console logs
- Browser console errors
- Steps to reproduce
- FiveMSecure version