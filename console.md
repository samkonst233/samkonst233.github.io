# Server Console

Execute commands and view server logs directly from the dashboard.

## Accessing Console

Navigate to **Dashboard** → **Console**

## Features

### Real-Time Logs

View server logs as they happen with automatic scrolling.

### Log Types

Logs are color-coded by type:

- **Info** (Blue) - General information
- **Success** (Green) - Successful operations
- **Warning** (Yellow) - Non-critical warnings
- **Error** (Red) - Error messages

### Command Execution

Execute server commands directly from the dashboard.

## Common Commands

### Resource Management
```bash
# Restart a resource
restart resource_name

# Stop a resource
stop resource_name

# Start a resource
start resource_name

# List all resources
resources
```

### Server Information
```bash
# View server status
status

# List connected players
players

# Show server performance
perf
```

### Admin Commands
```bash
# Kick a player
kick [id] [reason]

# Set server variable
setr variable_name "value"

# Get server variable
get variable_name
```

## Using the Console

### Execute a Command

1. Type command in the input field
2. Press **Enter** or click **Execute**
3. View command output in logs

### Clear Logs

Click the **Clear** button to remove all logs from view.

### Refresh Logs

Click **Refresh** to reload logs from the server.

## Tips

- Commands execute immediately on the server
- Use caution with sensitive commands
- Console history is not saved between sessions
- Press Enter key as a shortcut to execute

## Security

Only grant console access to trusted admins. Console commands can:

- Modify server configuration
- Restart/stop resources
- Execute arbitrary code

Ensure the **View Console** permission is only given to administrators you fully trust.