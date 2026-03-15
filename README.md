<p align="center">
  <img src="https://img.shields.io/badge/Fulfill'd-Reducing%20Food%20Waste-22c55e?style=for-the-badge&labelColor=0f172a" alt="Fulfill'd — Reducing Food Waste" />
</p>

<h1 align="center">Fulfill'd, Inc.</h1>

<p align="center">
  <strong>Anonymized B2B Marketplace for Perishable Food Distribution</strong><br/>
  <em>Because America doesn't have a food production problem. It has a "we throw away 40% of it" problem.</em>
</p>

<p align="center">
  <a href="https://fulfilld.com"><img src="https://img.shields.io/badge/Website-fulfilld.com-0ea5e9?style=flat-square&logo=safari&logoColor=white" alt="Website" /></a>
  <img src="https://img.shields.io/badge/Status-Active%20Development-22c55e?style=flat-square" alt="Status" />
  <img src="https://img.shields.io/badge/License-GPLv3-6366f1?style=flat-square" alt="License" />
</p>

---

## 🥬 Our Mission

Every year, the United States discards **~80 million tons** of food — roughly 40% of the total supply — while millions face food insecurity. Most of that waste happens in the gap between distributors: perfectly good product expires on warehouse floors because there's no fast, trusted way to move short-dated inventory between businesses.

**Fulfill'd** is a B2B marketplace that connects perishable food distributors through an anonymized trading platform. Vendors list short-dated inventory. Buyers find it by category, proximity, and expiry window. Products are surfaced **nearest-expiry-first**, ensuring the food most at risk of waste gets moved first.

Vendor identity stays hidden until payment clears — eliminating pricing bias, protecting supplier relationships, and letting the product sell on merit.

## 🏗️ What We're Building

| | |
|---|---|
| **Anonymized Marketplace** | Vendor identity revealed only after payment confirms |
| **FIFO by Expiry** | Products surfaced nearest-expiry-first to maximize waste reduction |
| **15-Minute Cart Hold** | Inventory reserved instantly — no double-selling, no stale carts |
| **Stripe Connect** | Marketplace payment splits with transparent transaction fees |
| **ERP Integration** | Read-only sync from vendor systems (Canopy, MYOB) — no write-back risk |
| **Full White-Label** | Our own brand, end to end — no third-party branding visible |
| **Mobile-First PWA** | Save-to-homescreen, works on any device, no app store needed |

## 🧰 Tech Stack

<p align="center">
  <img src="https://img.shields.io/badge/Frappe-v16-0089FF?style=flat-square&logo=python&logoColor=white" alt="Frappe" />
  <img src="https://img.shields.io/badge/ERPNext-v16.9-0089FF?style=flat-square&logo=python&logoColor=white" alt="ERPNext" />
  <img src="https://img.shields.io/badge/MariaDB-10.6+-003545?style=flat-square&logo=mariadb&logoColor=white" alt="MariaDB" />
  <img src="https://img.shields.io/badge/Redis-7.x-DC382D?style=flat-square&logo=redis&logoColor=white" alt="Redis" />
  <img src="https://img.shields.io/badge/Stripe-Connect-635BFF?style=flat-square&logo=stripe&logoColor=white" alt="Stripe" />
  <img src="https://img.shields.io/badge/Docker-Podman-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/AWS-EC2%20%2B%20S3-FF9900?style=flat-square&logo=amazonaws&logoColor=white" alt="AWS" />
</p>

Built as a custom [Frappe](https://github.com/frappe/frappe) application extending [ERPNext](https://github.com/frappe/erpnext) — the world's most popular open-source ERP — white-labeled from the ground up.

## 📦 Repositories

| Repository | Description |
|---|---|
| [`fulfilld`](https://github.com/Fulfilld-Inc//fulfilld) | Core marketplace application — Frappe custom app, Docker configs, CI/CD |
| [`fulfilld-docs`](https://github.com/Fulfilld-Inc//fulfilld-docs) | External documentation — user guides, API reference, onboarding *(coming soon)* |

## 🗺️ Roadmap

| Phase | Timeline | Milestone |
|---|---|---|
| **0 — Foundation** | Weeks 1–2 | Cloud infrastructure, containerized ERPNext, backups |
| **1 — Core + White-Label** | Weeks 3–6 | All apps installed, Stripe live, full branding |
| **2 — Customization** | Weeks 7–12 | Marketplace logic, vendor/buyer portals, custom app |
| **3 — Integrations** | Weeks 13–16 | Canopy API, barcode scanning, analytics |
| **4 — Pilot** | Weeks 17–20 | 5 Portland-area vendors live on platform |

## 👥 Team

| Role | Who |
|---|---|
| CEO / CRO | Bryan Thyken |
| Acting CTO | Patrick Ryan |
| Senior Engineer | Lucas Ragaglia |

## 📫 Contact

- **General:** TBD
- **Engineering:** TBD
- **Website:** TBD

---

<p align="center">
  <sub>🌱 Every transaction on Fulfill'd means less food in landfills and more food on tables.</sub>
</p>

## License

GNU General Public License v3.0 — see [LICENSE](LICENSE).

Built on [Frappe Framework](https://github.com/frappe/frappe) and [ERPNext](https://github.com/frappe/erpnext).

Built on [Frappe Framework](https://github.com/frappe/frappe) and [ERPNext](https://github.com/frappe/erpnext).
