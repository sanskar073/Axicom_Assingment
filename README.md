# 🎉 Event Management System - Acxiom ERP

> A comprehensive Enterprise Resource Planning (ERP) Platform for Event Procurement & Logistics built with pure HTML, CSS, and JavaScript.

![Status](https://img.shields.io/badge/Status-Active-success)
![HTML](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

---

## 📋 Project Overview

This Event Management System is a fully functional web-based ERP solution designed for managing event procurement and logistics. The system features three distinct user portals (Admin, Vendor, and User) with role-based access control, audit trails, and SAP integration simulation.

### 🎯 Key Features

- **Role-Based Access Control (RBAC)** - Three distinct user roles with specific permissions
- **Audit Trail System** - Complete logging of all system activities
- **SAP ERP Integration Hooks** - Simulated integration with SAP S/4HANA
- **Business Rules Engine** - Automated validation and compliance checks
- **Data Export Utilities** - Export data to CSV/Excel formats
- **Modern UI/UX** - Glassmorphism design with responsive layouts

---

## 🏗️ System Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                    Event Management System                   │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│    ┌──────────────┐  ┌──────────────┐  ┌──────────────┐     │
│    │    Admin     │  │    Vendor    │  │     User     │     │
│    │   Portal     │  │   Portal     │  │   Portal     │     │
│    └──────┬───────┘  └──────┬───────┘  └──────┬───────┘     │
│           │                 │                 │              │
│    ┌──────▼─────────────────▼─────────────────▼──────┐      │
│    │              Core ERP Engine (erp.js)            │      │
│    │  • Audit System  • RBAC  • SAP Integration      │      │
│    │  • Business Rules  • Data Export                │      │
│    └──────────────────────────────────────────────────┘      │
│                                                              │
│    ┌──────────────────────────────────────────────────┐      │
│    │            LocalStorage Data Layer               │      │
│    │   Products | Vendors | Users | Orders | Logs    │      │
│    └──────────────────────────────────────────────────┘      │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

---

## 📁 Project Structure

```
event-management-system/
│
├── index.html              # Main entry point - Role selection
├── flow-chart.html         # System architecture visualization
│
├── admin/                  # Administrator Module
│   ├── admin-login.html        # Admin authentication
│   ├── admin-signup.html       # Admin registration
│   ├── admin-dashboard.html    # Main admin control panel
│   ├── maintain-vendor.html    # Vendor management
│   ├── maintain-user.html      # User management
│   ├── manage-orders.html      # Order management
│   ├── add-membership.html     # Add memberships
│   ├── update-membership.html  # Update memberships
│   ├── reports.html            # Business intelligence reports
│   ├── transactions.html       # Transaction logs
│   └── maintenance.html        # System maintenance
│
├── vendor/                 # Vendor Portal Module
│   ├── vendor-login.html       # Vendor authentication
│   ├── vendor-signup.html      # Vendor registration
│   ├── vendor-dashboard.html   # Vendor control panel
│   ├── vendor-page.html        # Vendor profile page
│   ├── vendor-products.html    # Product listing
│   ├── product-status.html     # Inventory status
│   └── update-item.html        # Product updates
│
└── user/                   # Procurement User Module
    ├── user-login.html         # User authentication
    ├── user-signup.html        # User registration
    ├── user-portal.html        # User dashboard
    ├── products.html           # Product catalog
    ├── cart.html               # Shopping cart
    ├── checkout.html           # Order checkout
    ├── order-status.html       # Order tracking
    ├── request-item.html       # Special item requests
    └── success.html            # Order confirmation
```

---

## 👥 User Roles & Default Credentials

### 🔐 Administrator
| Field | Value |
|-------|-------|
| Username | `sanskar` |
| Password | `admin123` |
| Permissions | Full system access, user management, vendor approval, reports |

### 🏪 Vendor
| Field | Value |
|-------|-------|
| Username | `soundtech` / `lightcraft` / `visualpro` |
| Password | `vendor123` |
| Permissions | Product management, inventory control, order fulfillment |

### 🛒 Procurement User
| Field | Value |
|-------|-------|
| Username | `sanskar1` |
| Password | `password123` |
| Permissions | Browse products, place orders, track shipments |

---

## 🚀 Getting Started

### Prerequisites
- Any modern web browser (Chrome, Firefox, Edge, Safari)
- No server installation required - runs entirely in the browser

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/sanskar073/Axicom_Assingment.git
   ```

2. **Navigate to the project**
   ```bash
   cd Axicom_Assingment
   ```

3. **Open `index.html`**
   - Double-click `index.html` to open in your browser
   - Or use a local server like Live Server extension in VS Code

---

## ⚙️ Core ERP Features

### 1. Audit Trail System
Tracks all user actions with timestamps, IP addresses, and detailed logs for compliance requirements.

### 2. Role-Based Access Control (RBAC)
```javascript
PERMISSIONS = {
    ADMIN:  ['CREATE_USER', 'DELETE_USER', 'APPROVE_VENDOR', 'VIEW_REPORTS', 'EXPORT_DATA', 'VIEW_AUDIT'],
    VENDOR: ['ADD_ITEM', 'UPDATE_OWN_ITEM', 'VIEW_OWN_STATS'],
    USER:   ['PLACE_ORDER', 'VIEW_ORDERS', 'REQUEST_ITEM']
}
```

### 3. SAP Integration Hooks
Simulated integration with SAP S/4HANA for:
- Vendor synchronization (BAPI_VENDOR_CREATEFROMDATA)
- Order posting to SAP FI/CO
- General Ledger entries

### 4. Business Rules Engine
- Minimum order value validation ($100)
- Vendor approval compliance (SOX)
- Automated order processing rules

### 5. Product Categories
- **Audio Equipment**: Microphones, Speakers, Mixers
- **Visual Equipment**: Projectors, LED Walls, Cameras
- **Lighting Equipment**: LED Panels, Spotlights, Laser Systems

---

## 🎨 Design Features

- **Glassmorphism UI** - Modern frosted glass effects
- **Dark Theme** - Professional dark mode design
- **Responsive Layout** - Works on desktop, tablet, and mobile
- **Smooth Animations** - CSS transitions and hover effects
- **Inter Font** - Clean, professional typography
- **Gradient Accents** - Purple/Pink/Indigo color scheme

---

## 💾 Data Storage

The application uses **LocalStorage** for data persistence:

| Key | Description |
|-----|-------------|
| `products` | Product catalog |
| `vendors` | Vendor information |
| `users` | Registered users |
| `admins` | Administrator accounts |
| `orders` | Order history |
| `auditLogs` | System audit trail |

---

## 📊 Sample Data

The system comes pre-loaded with sample data:

**12 Products** across three categories:
- Professional Audio Equipment (₹8,500 - ₹72,000)
- Stage Lighting Systems
- Visual Display Equipment

**3 Pre-approved Vendors**:
- SoundTech Pro (Audio)
- LightCraft Events (Lighting)
- VisualPro Solutions (Visual)

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| HTML5 | Structure & Semantics |
| CSS3 | Styling & Animations |
| JavaScript (ES6+) | Logic & Interactivity |
| LocalStorage | Client-side Data Persistence |
| Google Fonts (Inter) | Typography |

---

## 📝 Assignment Information

- **Project**: Event Management System
- **Type**: Web Development Assignment
- **Student**: Sanskar Vashist
- **Framework**: Acxiom ERP Concepts

---

## 📄 License

This project is created for educational purposes as part of an assignment.

---

## 🤝 Contributing

This is an academic project. For any queries or contributions, please contact the project author.

---

<p align="center">
  <b>Powered by Acxiom ERP Concepts • Secure Audit Trail Enabled</b>
</p>