🏋️‍♂️ MS Power Fitness - Management System Prototype

Status: Live Demo
https://loki1512.github.io/gym-app-demo/

Tech Stack: HTML | Bootstrap 5 | JS
https://getbootstrap.com/

"Unleash Your Power."
A high-fidelity, static prototype for a modern Gym Management System.
This project demonstrates the UI/UX flow for Admins, Members, and the Renewal Logic.

------------------------------------------------------------

🚀 Live Demo & Access

Open the App:
https://loki1512.github.io/gym-app-demo/

Use these Demo Credentials (Password can be anything):

Role: 👑 Master Admin
Email: admin@gym.com
Experience: Full Control, Priority Lists, Approvals

Role: ✅ Active User
Email: user@gym.com
Experience: Standard Dashboard, Active Status

Role: ⚠️ Expiring User
Email: expiring@gym.com
Experience: Yellow Alert, Renewal Prompt, 3 Days Left

Role: ⛔ Expired User
Email: expired@gym.com
Experience: Red Alert, Access Denied, Payment Flow

------------------------------------------------------------

🔄 Application Workflow

1. Smart Login Routing

The system automatically detects user status and redirects them to the appropriate dashboard context.

Login Page -> Check Credentials
    admin@...     -> Admin Dashboard
    user@...      -> User Dashboard (Active)
    expiring@...  -> User Dashboard (Warning)
    expired@...   -> User Dashboard (Blocked)

------------------------------------------------------------

2. Admin Workflow: "The Retention Loop"

The Admin Dashboard is designed as an Action Center, not just a data dump.

Priority Call List (Smart Table)
- Default View: Shows top 7 users expiring soon.
- Action: Admin calls the user directly from the dashboard.
- Interactive Filters: Clicking the "Expired" tile swaps the table to show recent drop-outs.

Member Management
- Omni-Search: Filter by ID, Name, Email, or Phone instantly.
- View Mode: Opens a detailed profile card (Read-Only).
- Edit/Delete: Located safely at the bottom of the detailed view.

Payment Approvals
- Admins review manual payment screenshots (UPI/Cash).
- Approve or Reject transactions to update user status.

------------------------------------------------------------

3. User Renewal Flow

User logs in (Expired Status)
-> Dashboard shows RED Alert
-> User clicks "Reactivate Now"
-> Redirect to Payment Page
-> User selects plan (Yearly/Monthly)
-> User uploads UPI screenshot
-> "Payment Initiated"
-> Appears in Admin "Pending Approvals"

Payment Features
- Plan Selection: Monthly (₹800) or Yearly Gold (₹8,000)
- QR Integration: Placeholder for dynamic UPI QR generation
- Trust Signals: Users can view full Transaction History even if expired

------------------------------------------------------------

📂 Project Structure

/gym-app-demo
    index.html
    login.html
    admin-dashboard.html
    admin-members.html
    admin-approvals.html
    user-dashboard.html
    user-dashboard-expiring.html
    user-dashboard-expired.html
    payment.html

------------------------------------------------------------

🛠️ Features Implemented

- Bootstrap 5 Responsive Design
- Simulated RBAC (Role-Based Access Control)
- Dynamic Table Filtering (JS-based)
- Mock Payment Gateway UI
- "Smart Tiles" (Clicking dashboard tiles filters data)

------------------------------------------------------------

Made with love for MS Power Fitness.
