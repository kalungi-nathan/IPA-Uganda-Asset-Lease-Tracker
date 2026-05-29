# IPA Asset Lease Tracker

A web-based asset management platform for Innovations for Poverty Action (IPA) Uganda, designed to track PDA/Tablet and Laptop leases across projects.

## Live Demo
Deploy to GitHub Pages — the `index.html` file is fully self-contained.

## Features

- **PDA & Laptop Inventory** — Track all assets with status (Available / Leased / Maintenance)
- **Auto-Billing** — UGX 5,000/PDA/day · UGX 20,000/Laptop/day
- **Booking Form** — Real-time cost calculator, project auto-fill, "Already assigned" error guard
- **Finance Review** — Monthly billing summaries per project
- **Reports** — Lease summary, utilization, project billing, depreciation
- **CSV Export** — All tables and reports downloadable as CSV
- **Print Support** — Browser-native print for any report
- **Depreciation Flags** — Uganda 4-year straight-line method; flags zero-book-value assets
- **CSV Import** — Bulk upload PDA/Laptop lists; bulk delete
- **Role-Based Access** — Admin · Finance · Project Manager · Field Manager · Research Associate
- **Alerts** — Expiry warnings, pickup-ready notifications

## Default Login Credentials

| Username | Password    | Role                |
|----------|-------------|---------------------|
| admin    | admin123    | System Admin        |
| finance  | finance123  | Finance Officer     |
| Obed     | O123       | Project Manager     |
| Gloria     | G123       | Project Manager       |
| Anthony     | A123       | Project Manager  |
| Emmanuel     | E123       | Field Manager     |
| Charity     | C123       | Field Manager       |
| Harod      | H123       | Field Manager  |
| Hassan      | Y123       | Field Manager     |

> **Change all passwords after first login via the Users page.**

## Role Permissions

| Feature                     | Admin | Finance | Proj Mgr | Field Mgr | Res. Assoc |
|-----------------------------|:-----:|:-------:|:--------:|:---------:|:----------:|
| Manage users                |  ✓    |         |          |           |            |
| Add/edit/delete inventory   |  ✓    |         |          |           |            |
| Add/edit/delete projects    |  ✓    |         |          |           |            |
| View finance & reports      |  ✓    |  ✓      |  ✓       |           |            |
| View & export leases        |  ✓    |  ✓      |  ✓       |           |            |
| Book PDAs & Laptops         |  ✓    |  ✓      |  ✓       |  ✓        |  ✓         |

## Depreciation Policy
Assets depreciate over **4 years** using Uganda's straight-line method (Income Tax Act). Book value flags appear in inventory and the dedicated Depreciation Report.

## CSV Import Format
```
AssetCode,Model,Serial,PurchaseDate,PurchasePrice,Status,Condition
PDA-010,Samsung Tab A8,SN-001,2023-01-15,850000,Available,Good
```

## Deployment to GitHub Pages

1. Create a new GitHub repository
2. Upload `index.html` to the root
3. Go to **Settings → Pages → Source: Deploy from branch → main / root**
4. Your site will be live at `https://yourusername.github.io/your-repo-name/`

## Data Storage
All data is stored in the browser's `localStorage`. For multi-user production use, connect to a backend API or use a cloud database (Airtable, Firebase, Supabase).

## Tech Stack
Pure HTML + CSS + JavaScript — no frameworks, no build step, no dependencies (except Google Material Icons CDN).
