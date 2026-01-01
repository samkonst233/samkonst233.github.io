# Frequently Asked Questions

Quick answers to common questions.

## General Questions

**What is FiveMSecure?**

FiveMSecure is a comprehensive anti-cheat and monitoring platform for FiveM servers that provides real-time protection, player monitoring, and server management tools.

**How much does it cost?**

Visit [fivemsecure.com](https://fivemsecure.com) for current pricing and license options.

**Is there a free trial?**

Contact support@fivemsecure.com for trial information.

**Do I need a separate license per server?**

Yes, each FiveM server requires its own unique license.

## Compatibility

**Does it work with ESX?**

Yes, FiveMSecure is framework-agnostic and fully compatible with ESX, QBCore, and custom frameworks.

**Does it work with QBCore?**

Yes, FiveMSecure works with all FiveM frameworks.

**Will it conflict with other anti-cheats?**

Generally no, but running multiple anti-cheats is unnecessary. FiveMSecure provides comprehensive protection on its own.

**What FiveM version is required?**

Latest stable FiveM version is recommended. FiveMSecure supports all recent versions.

## Features

**Can I monitor multiple players at once?**

Yes, you can view up to 4 player streams simultaneously in the dashboard.

**Does monitoring affect performance?**

Minimal impact. Client-side capture uses ~5-10 FPS at configurable quality settings.

**Can I record player streams?**

Screenshot capture is available now. Video recording is planned for a future update.

**How accurate is the anti-cheat?**

FiveMSecure uses multiple detection methods for high accuracy. Start with Warn actions and monitor logs to tune for your server.

**Can I whitelist trusted players?**

Yes, through the dashboard or using Lua exports in your scripts.

## Administration

**Can I have multiple admins?**

Yes, add unlimited admins with customizable permissions for each.

**What can admins do?**

Admins can access features you grant them permissions for, from read-only viewing to full configuration control.

**Can admins access all my servers?**

No, admin access is per-license. Admins only see servers they're explicitly granted access to.

**How do I remove an admin?**

Navigate to **Admins** section and click Remove on the admin you want to remove.

## Technical

**What ports does FiveMSecure use?**

- HTTPS: 443 (API communication)
- UDP: 3001 (Streaming, configurable)

**Does it store player data?**

Only ban records and necessary identifiers for protection. No personal data is stored beyond what's needed for functionality.

**Is the connection encrypted?**

Yes, all API communication uses SSL/TLS encryption. Streams use secure WebRTC.

**Can I host the dashboard myself?**

No, the dashboard is cloud-hosted at fivemsecure.com for security and automatic updates.

## Billing & Licensing

**How long is a license valid?**

License duration depends on your purchase. Check your dashboard for expiration date.

**What happens when my license expires?**

FiveMSecure will stop functioning. Renew before expiration to avoid downtime.

**Can I transfer a license to another server?**

Contact support@fivemsecure.com for license transfer requests.

**Do you offer refunds?**

Refund policy is available at fivemsecure.com/refund-policy.

## Support

**How do I report a bug?**

Join our [Discord](https://discord.gg/UCjjX5hqwV) and post in #bug-reports with:
- Description of the issue
- Steps to reproduce
- Server console logs
- FiveMSecure version

**How fast is support response?**

- Discord: Usually within a few hours
- Email: Within 24 hours on business days

**Can I request features?**

Yes! We love feature requests. Post them in #suggestions on Discord.

**Where can I find update notes?**

Check #announcements on Discord or the dashboard for update notifications.