# Hudu Dashboard Generator

A standalone, offline-capable HTML tool for generating per-client Hudu company overview dashboards. Fill in a form, preview the result, copy the HTML directly into Hudu's source code editor.

**Live tool:** [hudu-dashboard-generator](https://eclipticprime558.github.io/hudu-dashboard-generator/varay-dashboard-generator.html)

---

## How It Works

1. Open `varay-dashboard-generator.html` in any browser — no server, no install
2. Fill in the client's environment details across all sections
3. Toggle which security stack tools are active for this client
4. Click **⚡ Generate Dashboard HTML**
5. Use the **Preview** tab to verify the output looks correct
6. Click **Copy HTML** and paste into Hudu: Company → Overview → Edit → Source Code
7. Click **📥 Export JSON** and save the file to Egnyte in the client's folder

---

## Form Sections

### Environment at a Glance
| Field | Description |
|-------|-------------|
| Firewall Management | Local Managed or Cloud Managed |
| MFA Policy Enforcement | Enforcement level for the client |
| Server Host / Hypervisor | e.g. Hyper-V, VMware, None |
| VPN Type | e.g. SSLVPN, BOVPN, Both |
| Active Directory Type | Hybrid, On-Prem, or Cloud Only |

### Security Stack Toggles
Click to activate — inactive tools are hidden from the generated dashboard.

`SentinelOne` · `Huntress` · `Cove – Servers` · `Cove – SaaS` · `Avanan` · `Phin` · `ConnectSecure` · `AuthPoint` · `DNSFilter`

### Network & Infrastructure
Primary ISP · Backup ISP · Firewall Model · Network Notes · ISP Link URL · Firewall Creds URL · Network Diagram URL

### Power & Hardware
Power Provider · UPS Managed · UPS Model · iDRAC Deployed · iDRAC URL · Power Map URL · UPS Portal URL

### Cloud & Identity
M365 Tenant Domain · M365 Admin URL · AD Sync Server · Password Writeback · Sync Creds URL · AuthPoint URL

### Operations & Contacts
Primary Contact · IT Contact · Applications in Use · Contact Link URL · Onboarding URL · Applications URL

---

## Importing an Existing Client

1. Open `varay-dashboard-generator.html`
2. Click **📤 Import JSON** and select the client's saved `.json` file
3. All fields repopulate automatically
4. Make changes, regenerate, and copy back into Hudu

---

## Security Note

- Client `.json` files are excluded from this repo via `.gitignore` — they are never committed
- Store all client JSON files in Egnyte under each client's folder
- The HTML files contain no credentials, passwords, or client-specific data
