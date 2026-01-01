# Admin System

Grant dashboard access to trusted users with customizable permissions.

## Adding an Admin

1. Navigate to **Dashboard** → **Admins**
2. Click **Add Admin**
3. Enter the admin's Discord ID
4. Enter an admin display name
5. Configure permissions (see below)
6. Click **Add Admin**

## Finding Discord IDs

To get someone's Discord ID:

1. Enable Developer Mode in Discord (User Settings → Advanced)
2. Right-click the user
3. Click "Copy User ID"

## Permission Types

### View Permissions

- **View Dashboard** - Access to home page and server overview
- **View Analytics** - Access to ban statistics and charts
- **View Players** - See active player list
- **View Monitoring** - Access live player streaming
- **View Bans** - See ban list and details
- **View Console** - Access server console logs
- **View Resources** - See server resources
- **View Logs** - Access webhook configuration

### Action Permissions

- **Edit Settings** - Modify anti-cheat protection configuration
- **Use Master Actions** - Import, export, or restore configurations
- **Manage Admins** - Add, edit, or remove other admins

## Editing Admin Permissions

1. Navigate to **Admins**
2. Click **Edit** button on the admin
3. Toggle permissions as needed
4. Click **Save Changes**

## Removing an Admin

1. Navigate to **Admins**
2. Click **Remove** button on the admin
3. Confirm the removal

Removed admins immediately lose all dashboard access.

## Permission Best Practices

### Full Admin Access

Grant all permissions to co-owners or head administrators.

### Moderator Access

Typical moderator permissions:
- View Dashboard
- View Players
- View Monitoring
- View Bans
- View Console

### Support Staff

Limited permissions for support team:
- View Dashboard
- View Players
- View Bans

### Developer Access

For developers working on your server:
- View Console
- View Resources
- Edit Settings

## Security Considerations

**Discord ID Verification**  
Always verify Discord IDs before adding admins. Incorrect IDs grant access to the wrong person.

**Regular Audits**  
Review your admin list monthly and remove inactive or untrusted users.

**Least Privilege**  
Only grant permissions that admins actively need. You can always add more later.

**Owner Account**  
The license owner always has full access and cannot be removed.

## Admin Activity

All admin actions are logged:

- Configuration changes
- Ban/kick actions
- Resource management
- Admin additions/removals

Logs are viewable in the dashboard's activity section.