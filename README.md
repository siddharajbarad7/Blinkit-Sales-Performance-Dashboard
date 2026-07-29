<div align="center">

# 📊 Blinkit Sales & Performance Dashboard

**An end-to-end Power BI analytics solution for sales, customer, product, territory, financial, and salesperson performance.**

[![Power BI](https://img.shields.io/badge/Power%20BI-Desktop-F2C811?style=flat-square&logo=powerbi&logoColor=black)](https://www.microsoft.com/en-us/power-platform/products/power-bi/downloads)
[![DAX](https://img.shields.io/badge/DAX-Data%20Analysis%20Expressions-217346?style=flat-square)](#)
[![Git LFS](https://img.shields.io/badge/Git%20LFS-enabled-orange?style=flat-square)](#file-size--git-lfs)
[![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)](#license)

</div>

---

## Overview

This repository contains a multi-page **Power BI** dashboard built to give stakeholders a single, drillable view into Blinkit's business performance — from executive KPIs down to salesperson-level detail. The report is organized into 7 purpose-built pages, each with consistent slicers, KPI cards, and interactive visuals for cross-filtering.

**Live artifact:** [`Dashboards/blinkit.pbix`](./Dashboards) · Power BI Desktop

---

## Table of Contents

- [Dashboard Pages](#dashboard-pages)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [File Size & Git LFS](#file-size--git-lfs)
- [Repository Structure](#repository-structure)
- [Roadmap](#roadmap)
- [License](#license)

---

## Dashboard Pages

| # | Page | Description |
|---|---|---|
| 1 | **Executive Overview** | Company-wide KPIs, sales trend, sales by category, top 10 products & customers, key insights panel |
| 2 | **Product Analytics** | Sales by subcategory, decomposition tree, new vs. returning product sales, top products by profit, units sold vs. unit price |
| 3 | **Customer Analytics** | Customer growth trend, customer distribution by territory, sales by subcategory and gender |
| 4 | **Sales Analytics** | Sales trend, sales by category/sub-category, sales by order channel, category-wise sales waterfall |
| 5 | **Territory Analytics** | Regional sales breakdown, top territories by profit, territory performance table, sales vs. profit, MoM growth waterfall |
| 6 | **Financial Analytics** | Profit vs. revenue, profit margin by category, cost breakdown, P&L-style table, margin % gauge |
| 7 | **Salesperson Analytics** | Sales by salesperson, individual performance trend |

Every page ships with a **Year slicer** and headline **KPI cards** for consistent, at-a-glance context regardless of which view a user lands on.

---

## Key Features

- 🔍 **Cross-page filtering** — click any visual to filter related charts on the same page
- 📈 **Trend analysis** — line and waterfall charts surfacing MoM/YoY movement in sales and profit
- 🧩 **Decomposition tree** — root-cause drill-down on product performance
- 🗺️ **Territory-level breakdowns** — regional and country-level performance comparisons
- 💰 **Financial modeling** — margin %, cost breakdown, and P&L-style reporting
- 🧮 **DAX-driven measures** — KPIs and growth metrics computed via custom DAX rather than static values

---

## Tech Stack

| Layer | Tool |
|---|---|
| Reporting & Visualization | Power BI Desktop |
| Data Modeling | Star-schema relationships (Sales, Product, Customer, Territory, Financial) |
| Calculations | DAX (Data Analysis Expressions) |
| Version Control | Git + Git LFS |

---

## Getting Started

### Prerequisites

- [Power BI Desktop](https://www.microsoft.com/en-us/power-platform/products/power-bi/downloads) (free, Windows only)
- [Git LFS](https://git-lfs.com/) — required to pull the `.pbix` file

### Installation

```bash
# Clone the repository
git clone https://github.com/siddharajbarad7/Blinkit-Sales-Performance-Dashboard.git
cd Blinkit-Sales-Performance-Dashboard

# Pull the LFS-tracked files
git lfs pull
```

Open `Dashboards/blinkit.pbix` in Power BI Desktop — it launches on the **Executive Overview** page by default.

> **Note:** Power BI Desktop is Windows-only. macOS/Linux users can view a published version via the [Power BI Service](https://app.powerbi.com) if published, or use a Windows VM.

---

## File Size & Git LFS

The `.pbix` file is tracked via **Git LFS** to keep the repository performant. If the file exceeds GitHub's free 1 GB LFS storage/bandwidth quota, consider a paid data pack or trimming unused data/images from the model.

```bash
git lfs install
git lfs track "*.pbix"
git add .gitattributes
git add Dashboards/blinkit.pbix
git commit -m "Add Blinkit Power BI dashboard"
git push -u origin main
```

---

## Repository Structure

```
.
├── README.md
├── .gitattributes         # Git LFS tracking rules
├── Dashboards/             # Power BI report file(s)
│   └── blinkit.pbix
├── Data/                   # Source/raw data used to build the model
└── Screensort/             # Dashboard screenshots / preview images
```

---

## Roadmap

- [ ] Publish to Power BI Service for browser-based access
- [ ] Add row-level security (RLS) for territory-restricted views
- [ ] Automate data refresh via scheduled gateway
- [ ] Embed screenshots from `Screensort/` into this README

---

## License

Distributed under the MIT License. See `LICENSE` for details.

---

<div align="center">

Built with Power BI · Maintained by [Your Name]

</div>
