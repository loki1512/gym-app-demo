Markdown
# 🏋️‍♂️ MS Power Fitness - Management System Prototype

[![Status](https://img.shields.io/badge/Status-Live_Demo-success?style=for-the-badge)](https://loki1512.github.io/gym-app-demo/)
[![Tech Stack](https://img.shields.io/badge/Stack-HTML_|_Bootstrap_5_|_JS-blue?style=for-the-badge)](https://getbootstrap.com/)

> **"Unleash Your Power."** A high-fidelity, static prototype for a modern Gym Management System.  
> This project demonstrates the UI/UX flow for Admins, Members, and the Renewal Logic.

---

## 🚀 Live Demo & Access

**[👉 Click Here to Open the App](https://loki1512.github.io/gym-app-demo/)**

To explore the different roles and logic states, use these **Demo Credentials** (Password can be anything):

| Role | Email | Experience |
| :--- | :--- | :--- |
| **👑 Master Admin** | `admin@gym.com` | Full Control, Priority Lists, Approvals |
| **✅ Active User** | `user@gym.com` | Standard Dashboard, Active Status |
| **⚠️ Expiring User** | `expiring@gym.com` | **Yellow Alert**, Renewal Prompt, 3 Days Left |
| **⛔ Expired User** | `expired@gym.com` | **Red Alert**, Access Denied, Payment Flow |

---

## 🔄 Application Workflow

We have designed a logic-driven flow that handles member retention automatically. Below are the visual workflows for the system.

### 1. Smart Login Routing
The system automatically detects user status and redirects them to the appropriate dashboard context.

```mermaid
graph TD
    A[Login Page] -->|Input Email| B{Check Credentials}
    B -->|admin@...| C[Admin Dashboard]
    B -->|user@...| D[User Dashboard (Active)]
    B -->|expiring@...| E[User Dashboard (Warning)]
    B -->|expired@...| F[User Dashboard (Blocked)]
    
    style C fill:#212529,stroke:#fff,color:#fff
    style D fill:#198754,stroke:#fff,color:#fff
    style E fill:#ffc107,stroke:#333,color:#000
    style F fill:#dc3545,stroke:#fff,color:#fff
2. Admin Workflow: "The Retention Loop"
The Admin Dashboard is designed as an Action Center, not just a data dump.

<details> <summary><strong>🔍 Click to expand Admin Logic Details</strong></summary>

Priority Call List (Smart Table)

Default View: Shows top 7 users expiring soon.

Action: Admin calls the user directly from the dashboard.

Interactive Filters: Clicking the "Expired" tile swaps the table to show recent drop-outs.

Member Management

Omni-Search: Filter by ID, Name, Email, or Phone instantly.

View Mode: Opens a detailed profile card (Read-Only).

Edit/Delete: Located safely at the bottom of the detailed view.

Payment Approvals

Admins review manual payment screenshots (UPI/Cash).

Approve or Reject transactions to update user status.

</details>

3. User Renewal Flow
How a user goes from "Blocked" to "Active" without staff intervention.

Code snippet
sequenceDiagram
    participant User
    participant Dashboard
    participant PaymentPage
    participant Admin

    User->>Dashboard: Logs in (Expired Status)
    Dashboard-->>User: Shows RED Alert ⛔
    User->>Dashboard: Clicks "Reactivate Now"
    Dashboard->>PaymentPage: Redirects
    PaymentPage->>PaymentPage: Select Plan (Yearly/Monthly)
    PaymentPage->>PaymentPage: Upload UPI Screenshot
    PaymentPage->>User: "Payment Initiated"
    User->>Admin: Appears in "Pending Approvals"
<details> <summary><strong>💳 Click to see Payment Features</strong></summary>

Plan Selection: Users can choose between Monthly (₹800) or Yearly Gold (₹8,000).

QR Integration: Placeholder for dynamic UPI QR generation.

Trust Signals: Users can view their full Transaction History even if their account is expired.

</details>

📂 Project Structure
Plaintext
/gym-app-demo
├── index.html                 # Landing Page (Public)
├── login.html                 # Auth Simulation
├── admin-dashboard.html       # Main Admin Hub (Stats + Priority List)
├── admin-members.html         # Full Member List with Search/Filter
├── admin-approvals.html       # Payment Verification Page
├── user-dashboard.html        # Active Member View
├── user-dashboard-expiring.html # Warning View (Yellow)
├── user-dashboard-expired.html  # Restricted View (Red)
└── payment.html               # Checkout/Renewal Page
🛠️ Features Implemented
✅ Bootstrap 5 Responsive Design

✅ Simulated RBAC (Role-Based Access Control)

✅ Dynamic Table Filtering (JS-based)

✅ Mock Payment Gateway UI

✅ "Smart Tiles" (Clicking dashboard tiles filters data)

Made with ❤️ for MS Power Fitness.