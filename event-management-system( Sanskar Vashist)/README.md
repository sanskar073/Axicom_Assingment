# 🎪 Technical Event Management System

A comprehensive ERP-style web application for managing technical event equipment rentals, built with vanilla HTML, CSS, and JavaScript.

## 🚀 Features

### User Portal
- **Product Browsing** - Filter by Audio, Visual, Lighting categories
- **Shopping Cart** - Add products, view totals in INR (₹)
- **Checkout** - Cash/UPI payment options
- **Order Tracking** - 4-stage status (Pending → Approved → Processing → Completed)

### Vendor Portal
- **Add Products** - Upload images, set INR prices
- **Manage Inventory** - Track stock levels
- **Product Categories** - Audio, Visual, Lighting equipment

### Admin Portal
- **User Management** - Approve/manage users
- **Vendor Management** - Approve vendors, manage accounts
- **Order Management** - Update order statuses
- **Audit Trail** - Track all system actions

## 📁 Project Structure

```
event-management-system/
├── index.html          # Main landing page
├── flow-chart.html     # System architecture diagram
├── README.md           # This file
├── admin/              # Admin portal pages
│   ├── admin-login.html
│   ├── admin-dashboard.html
│   ├── maintain-user.html
│   ├── maintain-vendor.html
│   └── manage-orders.html
├── user/               # User portal pages
│   ├── user-login.html
│   ├── user-portal.html
│   ├── products.html
│   ├── cart.html
│   ├── checkout.html
│   └── order-status.html
└── vendor/             # Vendor portal pages
    ├── vendor-login.html
    ├── vendor-dashboard.html
    ├── vendor-page.html
    └── vendor-products.html
```

> **Note:** All CSS and JavaScript are embedded directly in HTML files for portability.

## 🔐 Login Credentials

| Portal | Username | Password |
|--------|----------|----------|
| **Admin** | `sanskar` | `admin123` |
| **User** | `sanskar1` | `password123` |
| **Vendor** | `soundtech` | `vendor123` |
| **Vendor** | `lightcraft` | `vendor123` |
| **Vendor** | `visualpro` | `vendor123` |

## 🛠️ How to Run

Simply open `index.html` in any browser, or use a local server:

```bash
# Using Node.js http-server
npx http-server . -p 8080

# Or Python
python -m http.server 8080
```

## 💰 Currency

All prices are displayed in **Indian Rupees (₹ INR)**.

## 🔄 Reset Data

To reset all data to defaults, run in browser console:
```javascript
localStorage.clear();
location.reload();
```

---

**Built with** ❤️ using HTML5, CSS3, and Vanilla JavaScript
