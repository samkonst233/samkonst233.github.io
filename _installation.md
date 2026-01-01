# Installation

This guide will help you install FiveMSecure on your FiveM server.

## Prerequisites

- FiveM server (latest version recommended)
- Valid FiveMSecure license key
- Server file access

## Step 1: Download

Download the latest release from your dashboard at [fivemsecure.com](https://fivemsecure.com).

## Step 2: Extract Files

Extract the downloaded archive to get the `fivemsecure` folder.

## Step 3: Install Resource

Copy the `fivemsecure` folder to your server's `resources` directory:

## Step 4: Configure Server

Add these lines to your `server.cfg`:
```cfg
ensure fivemsecure

setr fivemsecure:api_url "https://api.fivemsecure.com"
setr fivemsecure:server_secret "YOUR_LICENSE_KEY"
```

> Replace `YOUR_LICENSE_KEY` with your actual license key from the dashboard.

## Step 5: Restart Server

Restart your FiveM server to load the resource.

## Verification
If you see these messages, installation was successful.

## Next Steps

- [Configure protection settings](configuration.md)
- [Access the dashboard](dashboard.md)
- [Add admin users](admins.md)

## Troubleshooting

**Resource won't start**

Check that:
- Folder name is exactly `fivemsecure`
- `ensure fivemsecure` is in server.cfg
- No syntax errors in server.cfg

**Connection failed**

Verify:
- License key is correct
- Server can reach api.fivemsecure.com
- Firewall isn't blocking connections