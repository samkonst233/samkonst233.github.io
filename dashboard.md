# Dashboard Guide

The FiveMSecure dashboard is your central control panel for server management.

## Authentication

Access the dashboard at [fivemsecure.com/dashboard](https://fivemsecure.com/dashboard).

Click **Login with Discord** to authenticate. Your Discord account must be associated with a valid license.

## Navigation

### Dashboard (Home)

Overview of your server with key statistics:

- Server name and IP address
- License status and expiration
- Quick access cards

### Analytics

View ban statistics and trends:

- Total bans across all time periods
- Active vs expired bans
- Interactive charts with time filtering
- Options: 5min, 30min, 1hour, Today, 7 days, 30 days

### Players

Real-time player monitoring:

- View all connected players
- See health, armor, ping
- View player identifiers (Steam, Discord, License)
- Position coordinates
- Ban or kick players directly

### Monitoring

Live player screen streaming:

- Watch player screens in real-time via WebRTC
- View multiple streams simultaneously
- Capture screenshots

### Bans

Ban management interface:

- View all server bans
- Search by ban ID, reason, or Discord ID
- View detailed ban information
- Unban players

### Admins

Manage dashboard access:

- Add new admins by Discord ID
- Configure granular permissions
- Edit existing admin permissions
- Remove admin access

### Console

Server console access:

- View real-time server logs
- Execute server commands
- Filter by log type (info, error, warning, success)
- Auto-scrolling log viewer

### Resources

Server resource management:

- View all server resources
- See resource status (running/stopped)
- Start, stop, or restart resources
- Filter and search resources

### Settings

Anti-cheat configuration:

- Enable/disable protections by category
- Set actions for each protection
- Configure blacklists
- Manage general settings

### Master Actions

Configuration management:

- **Export** - Generate backup code
- **Import** - Load configuration from code
- **Restore** - Reset to default settings

### Logs

Webhook configuration:

- Join/leave event webhooks
- Ban event webhooks
- Screenshot webhooks
- Resource event webhooks

## Quick Actions

### Ban a Player

1. Navigate to **Players** or **Monitoring**
2. Click on the player
3. Click **Ban** button
4. Enter ban reason
5. Select duration (permanent, 1 day, 7 days, 30 days)
6. Click **Confirm Ban**

### Kick a Player

1. Navigate to **Players** or **Monitoring**
2. Click on the player
3. Click **Kick** button
4. Enter kick reason
5. Click **Confirm Kick**

### Unban a Player

1. Navigate to **Bans**
2. Find the ban using search
3. Click **Unban** button
4. Confirm the action

### Manage Resources

1. Navigate to **Resources**
2. Find the resource
3. Click **Start**, **Stop**, or **Restart**

## License Management

### Multiple Licenses

If you own multiple licenses:

1. Click **My Licenses** in the sidebar
2. Select the license you want to manage
3. Dashboard switches to that server's configuration

### Invited Configurations

If you're an admin on someone else's server:

1. Click **Invited Configs** in the sidebar
2. Select the configuration
3. Your available features depend on granted permissions

## Admin Permissions

When adding admins, you can grant these permissions:

- **View Dashboard** - Access to home page
- **View Analytics** - Access to ban statistics
- **View Players** - See active players
- **View Monitoring** - Access live streams
- **View Bans** - See ban list
- **View Console** - Access server console
- **View Resources** - See server resources
- **Edit Settings** - Modify protection configuration
- **Use Master Actions** - Import/export configs
- **View Logs** - Access webhook configuration
- **Manage Admins** - Add/edit/remove other admins

## Saving Changes

Always click **Save Config** after modifying:

- Protection settings
- Blacklists
- Webhook URLs
- General settings

Changes apply immediately without requiring a server restart.

## Tips

- Use the search function to quickly find specific settings
- Monitor logs regularly during the first week
- Start with Warn actions before enabling bans
- Test all configuration changes on a development server
- Keep webhook URLs secure and don't share them publicly