# Fulfill'd

> Because America doesn't have a food production problem. It has a "we throw away 40% of it" problem.

**Fulfill'd, Inc.** — Anonymized B2B marketplace for perishable food distributors. Built on [Frappe Framework](https://github.com/frappe/frappe) + [ERPNext](https://github.com/frappe/erpnext), white-labeled top to bottom.

---

## What Is This

A custom [Frappe app](https://frappeframework.com/docs/user/en/basics/apps) that extends ERPNext with marketplace functionality for perishable food distribution. Vendors list inventory anonymously. Buyers search, add to cart (15-minute hold), and checkout via Stripe. Vendor identity is revealed only after payment clears. The system prioritizes products by nearest expiry date (FIFO) to reduce food waste.

### Key Features

- **Anonymized Marketplace** — Vendor identity hidden until payment confirms
- **15-Minute Cart Hold** — Products reserved on add-to-cart, auto-released on timeout
- **FIFO by Expiry** — Nearest-to-expire products surface first
- **Stripe Connect** — Marketplace payment splits (we take a transaction fee)
- **Read-Only ERP Integration** — Syncs inventory from vendor ERPs (Canopy, MYOB) without writing back
- **Full White-Label** — Zero Frappe/ERPNext branding visible to end users
- **PWA Mobile** — Save-to-homescreen, no native app needed

---

## Tech Stack

| Component | Technology |
|---|---|
| Framework | Frappe v16.x + ERPNext v16.9.0 |
| Database | MariaDB 10.6+ |
| Cache/Queue | Redis 7.x |
| Payments | Stripe Connect (via Frappe Payments) |
| Containers | Podman (rootless) |
| Cloud | AWS EC2 + S3 |
| Email | AWS SES |
| SSL | Let's Encrypt |

---

## Repository Structure

```
fulfilld/
├── .agent/workflows/         # Development workflows
├── .github/workflows/        # CI/CD
├── docs/
│   ├── original/             # Preserved 2020-2021 documentation
│   │   ├── core/             # Business docs, data model, architecture
│   │   ├── workflows/        # Customer, supplier, partner setup workflows
│   │   ├── pitch-decks/      # Pitch deck versions v1-v3
│   │   └── screenshots/      # Reference screenshots
│   └── architecture/         # Technical architecture docs
├── docker/
│   ├── Containerfile         # Multi-stage production build
│   ├── apps.json             # Frappe apps to install
│   ├── .env.example          # Environment template
│   └── scripts/              # Backup/restore helpers
├── fulfilld/                 # Custom Frappe App
│   ├── hooks.py              # App hooks and branding
│   ├── modules.txt           # Module definitions
│   ├── marketplace/          # Core marketplace logic
│   │   └── doctype/
│   │       ├── marketplace_listing/
│   │       ├── cart_item/
│   │       ├── marketplace_order/
│   │       └── transaction_fee/
│   ├── vendor_management/    # Vendor onboarding
│   ├── integration/          # ERP connectors
│   ├── public/               # CSS/JS/images (white-label assets)
│   ├── templates/            # Jinja templates (login, print formats)
│   └── www/                  # Portal pages
├── tests/                    # Unit tests
├── setup.py                  # Python package config
├── requirements.txt          # Python deps
└── package.json              # Node deps
```

---

## DocTypes

| DocType | Module | Purpose |
|---|---|---|
| **Marketplace Listing** | Marketplace | Anonymized inventory listing with FIFO expiry |
| **Cart Item** | Marketplace | 15-minute cart hold/reservation |
| **Marketplace Order** | Marketplace | Order lifecycle: placed → delivered → completed |
| **Transaction Fee** | Marketplace | Fee calculation and recording |
| **Vendor Profile** | Vendor Management | Vendor onboarding and config |
| **ERP Connector** | Integration | Canopy/MYOB API configuration |

---

## Quick Start (Development)

```bash
# 1. Clone
git clone https://github.com/Archimedes-Solutions/fulfilld.git
cd fulfilld

# 2. Set up Frappe development environment (see .agent/workflows/dev-environment.md)

# 3. Inside Frappe container:
bench get-app fulfilld /path/to/this/repo
bench --site fulfilld.localhost install-app fulfilld
bench start
```

See [`.agent/workflows/dev-environment.md`](.agent/workflows/dev-environment.md) for full setup instructions.

---

## Deployment Phases

| Phase | Timeline | Key Deliverables |
|---|---|---|
| **0: Foundation** | Weeks 1-2 | Cloud infra, Podman, base ERPNext, backups |
| **1: Core + White-Label** | Weeks 3-6 | All apps, Stripe, email, full branding |
| **2: Customization** | Weeks 7-12 | Marketplace logic, portals, custom app |
| **3: Integrations** | Weeks 13-16 | Canopy API, scanning, analytics, security |
| **4: Pilot** | Weeks 17-20 | 5 Portland vendors live |

---

## Team

| Role | Who |
|---|---|
| CEO/CRO | Bryan Thyken |
| Acting CTO | Patrick Ryan |
| Senior Engineer | Lucas Ragaglia |

---

## License

GNU General Public License v3.0 — see [LICENSE](LICENSE).

Built on [Frappe Framework](https://github.com/frappe/frappe) and [ERPNext](https://github.com/frappe/erpnext).
