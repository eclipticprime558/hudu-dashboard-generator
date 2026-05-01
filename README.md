# Hudu Dashboard Generator

A standalone offline tool for generating per-client Hudu company overview dashboards.

## Files

| File | Purpose |
|------|---------|
| `varay-dashboard-generator.html` | Form-based generator — fill in client details, toggle security stack, generate and copy HTML |

## How to Use — Generator

1. Open `varay-dashboard-generator.html` in any browser (no server needed — fully offline)
2. Fill in the client name and all environment details
3. Toggle the security stack tools that are active for this client
4. Click **⚡ Generate Dashboard HTML**
5. Click **Copy HTML** and paste into Hudu: Company → Overview → Edit → Source Code
6. Click **📥 Export JSON** and save the `.json` file to Egnyte in the client's folder

## How to Use — Import Existing Client

1. Open `varay-dashboard-generator.html`
2. Click **📤 Import JSON** and select the client's saved `.json` file
3. All fields repopulate automatically
4. Make changes, regenerate, copy back into Hudu

## Security Note

- Client JSON files are **never committed** to this repo (`.gitignore` excludes all `.json`)
- Store client JSON files in Egnyte under each client's folder
- No passwords, credentials, or sensitive data are stored — only descriptions and Hudu password record URLs

## Environment at a Glance Fields

- Firewall management type (Local / Cloud Managed)
- MFA Policy enforcement level
- Server Host / Hypervisor
- VPN type
- Active Directory type (Hybrid / On-Prem / Cloud Only)

## Security Stack Toggles

SentinelOne · Huntress · Cove — Servers · Cove — SaaS · Avanan · Phin · ConnectSecure · AuthPoint · DNSFilter
