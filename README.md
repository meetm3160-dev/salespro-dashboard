# SalesPro – Smart Sales Dashboard

A modern, high-performance, fully responsive **Sales Analytics Dashboard Website** built with **React**, **Tailwind CSS**, **Recharts**, and **Lucide Icons**. Inspired by world-class SaaS analytics platforms (Stripe, Linear, Datadog), SalesPro features a dynamic KPI engine, interactive charting, full sales management with CSV export, customer & product analytics, dark/light mode toggle, and real-time filtering.

---

## 🚀 Quick Start Guide

### 1. Prerequisites
Ensure **Node.js** (v18+) and **npm** are installed on your machine.

### 2. Installation
Clone or navigate to the project directory:
```bash
cd dashboard
npm install
```

### 3. Start Local Development Server
Run the local Vite server:
```bash
npm run dev
```
Open **[http://localhost:5173](http://localhost:5173)** in your browser.

### 4. Build for Production
To create an optimized production build:
```bash
npm run build
```
To preview the production build locally:
```bash
npm run preview
```

---

## 🌟 Key Features

### 1. Overview Dashboard
- **Dynamic KPIs**:
  - **Total Revenue**: Calculated in real-time from active sales records.
  - **Total Sales**: Completed fulfillment orders.
  - **Total Orders**: All pipeline transactions.
  - **Total Customers**: Count of unique active client accounts.
  - **Average Order Value (AOV)**: Revenue per transaction.
  - **Revenue Growth Rate**: Dynamic comparison indicator.
- **Sales Velocity Area Chart**: Monthly revenue trajectory with gradient shading.
- **Category Donut Chart**: Breakdown of portfolio contributions with interactive hover.
- **Recent Transactions Widget**: Latest incoming payments with instant navigation.

### 2. Interactive Charts
- **Monthly Sales Line & Area Chart**: Multi-metric toggle (Revenue, Revenue + Net Profit, Order Volumes).
- **Revenue by Product Bar Chart**: Ranked horizontal bars for top-selling SKUs with monetary and unit volume toggles.
- **Sales by Category Donut Chart**: Proportional distribution with center summary and segment progress bars.
- **Profit & Margin Analysis Chart**: Composed chart evaluating Gross Revenue vs COGS with dynamic Net Margin % line overlay.
- **Regional Sales Distribution**: Global geographical breakdown across North America, Europe, Asia Pacific, Latin America, and Middle East.

### 3. Sales Management
- **Searchable Sales Ledger**: Instant multi-attribute search across Order ID, Customer Name, Product, and Category.
- **Column Sorting**: Sort by Date, Amount, Quantity, Customer Name, and Order ID in ascending/descending order.
- **Multi-Level Filters**: Quick status pills (`All`, `Completed`, `Pending`, `Refunded`, `Failed`).
- **Pagination**: Configurable page size (5, 10, 20, 50 rows per page) and jump-to-page navigation.
- **CSV Export**: Clean one-click export with UTF-8 BOM encoding for Excel compatibility.
- **View Order Details Modal**: Inspect comprehensive customer profiles, line item receipts, and fraud checks.
- **Add New Order Modal**: Interactive order creation with real-time recalculation of all KPIs and charts, complete with celebratory confetti.

### 4. Product Analytics
- **Best-Selling Products**: Ranked performance list with units sold, ratings, and revenue.
- **Low-Performing Product Alerts**: Low-turnover warnings with actionable 20% promotional discount triggers.
- **Product Profit Matrix**: Full unit economics table displaying SKU cost, price, units sold, total revenue, net profit, and profit margin %.

### 5. Customer Analytics
- **Customer KPI Overview**: Total accounts, New vs Returning ratio, Average Customer LTV, and Retention Health.
- **Top Enterprise Clients Table**: Ranked by lifetime spend (LTV) with membership tiers (`VIP Enterprise`, `Gold`, `Regular`).
- **Purchase History Modal**: Click any customer to view their complete transactional audit trail.

### 6. Global Interactive Filters
- **Date Range Filter**: `Last 7 Days`, `Last 30 Days`, `Last 3 Months`, `This Year`, `All Time`, and `Custom Date Range` pickers.
- **Timeframe Selector**: Monthly, Weekly, and Yearly analysis toggles.
- **Category Filter**: Filter dynamically across Electronics, Software & SaaS, Accessories, Office Furniture, and Smart Devices.
- **Region Filter**: Filter across global geographic markets.
- **Reset Button**: One-click reset to default view.

### 7. Modern UI / UX & Additional Features
- **Dark Mode & Light Mode**: Seamless theme toggle with persistent `localStorage` memory and smooth Tailwind classes.
- **Executive Reports & Audits**: Export CSV ledgers, printable executive summaries, and raw JSON audits.
- **Notification Drawer**: Interactive notifications with unread badge counter, mark-as-read, and clear actions.
- **Profile Menu**: User status, organization details, quick settings, and sign-out simulation.
- **Responsive Layout**: Desktop collapsible sidebar and mobile-friendly slide-over drawer.

---

## 🛠️ Tech Stack

- **Framework**: React 18+ (Hooks, Context API, useMemo)
- **Styling**: Tailwind CSS 3.4+ (Dark mode, custom brand palette, glassmorphism)
- **Charts**: Recharts (ResponsiveContainer, AreaChart, BarChart, ComposedChart, PieChart)
- **Icons**: Lucide React
- **Celebration Effects**: Canvas Confetti
- **Build Tool**: Vite

---

## 📂 Project Architecture

```
src/
├── components/
│   ├── layout/
│   │   ├── Sidebar.jsx            # Desktop collapsible & mobile drawer navigation
│   │   ├── TopNavbar.jsx          # Header with search, theme switch, notifications, & profile
│   │   └── QuickFilterBar.jsx     # Global date, category, region, & timeframe filter bar
│   ├── overview/
│   │   ├── MetricCards.jsx        # 6 core dynamic KPI cards
│   │   └── RecentTransactionsWidget.jsx
│   ├── charts/
│   │   ├── MonthlySalesLineChart.jsx
│   │   ├── ProductRevenueBarChart.jsx
│   │   ├── SalesCategoryChart.jsx
│   │   ├── ProfitAnalysisChart.jsx
│   │   └── RegionalSalesChart.jsx
│   ├── sales/
│   │   ├── SalesTable.jsx         # Full ledger with search, sort, pagination, CSV export
│   │   ├── OrderDetailsModal.jsx   # Line item receipt & customer modal
│   │   └── CreateOrderModal.jsx   # Add order modal with live state updates & confetti
│   ├── products/
│   │   ├── BestSellingProducts.jsx
│   │   ├── LowPerformingAlerts.jsx
│   │   └── ProductProfitMatrix.jsx
│   ├── customers/
│   │   ├── CustomerStats.jsx
│   │   ├── TopCustomersTable.jsx
│   │   └── CustomerHistoryModal.jsx
│   ├── reports/
│   │   └── ReportsGenerator.jsx   # CSV, Print Preview, and JSON audit exporter
│   └── settings/
│       └── SettingsView.jsx       # Admin profile, currency, and notifications settings
├── context/
│   └── DashboardContext.jsx       # Central state management & dynamic calculation hooks
├── data/
│   └── mockData.js                # Realistic sales, products, customers, and notifications
├── utils/
│   ├── calculations.js            # KPI metrics, monthly trends, margins, & aggregates
│   ├── formatters.js              # Currency, compact numbers, percentages, dates
│   └── exportCsv.js               # CSV generator & browser download trigger
├── App.jsx                        # Master application shell & tab router
├── index.css                      # Tailwind base, utilities, & custom scrollbars
└── main.jsx                       # Application entry point
```

---

## 📄 License
This project was built for the SalesPro Analytics Platform.
