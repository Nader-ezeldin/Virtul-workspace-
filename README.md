📊 Workspace Dashboard – All‑in‑One Management Platform
https://img.shields.io/badge/Google%2520Apps%2520Script-4285F4?logo=googleapps&logoColor=white
https://img.shields.io/badge/Google%2520Sheets-34A853?logo=googlesheets&logoColor=white
https://img.shields.io/badge/Alpine.js-8BC0D0?logo=alpine.js&logoColor=white
https://img.shields.io/badge/Chart.js-FF6384?logo=chart.js&logoColor=white

A fully functional, secure, and extendable workspace management system built on Google Sheets, Google Apps Script, and a modern frontend. Manage tasks, budgets, assets, file requests, chat, calendars, and much more – all from your Google Sheet.

🚀 Live Demo
Since this is a Google Apps Script web app, you can deploy your own copy in minutes (see Installation).

✨ Key Features
User Management & Roles – Admin, Manager, Staff, Viewer with granular permissions.

Task Pipelines – Kanban board with drag‑and‑drop, Gantt chart view, priority and status filters.

Assets Management – Track hardware/software, assign to users, schedule maintenance, generate QR codes, and view full asset history.

File Requests Hub – Request and share files with advanced statuses (Pending, In Review, Approved, Rejected, Fulfilled, Partially Fulfilled). Add comments and set expiry dates.

Budget & Finance – Record income and expenses, visualise by category, export to CSV/PDF.

Calendar & Events – Synchronise with Google Calendar, add meetings, deadlines, and events.

Weekly Planner – Define weekly objectives and plan daily tasks.

Real‑time Team Chat – Global chat with automatic polling for new messages.

Dashboard Analytics – Interactive charts (tasks by status, expenses, cashflow) and recent activity feed.

Advanced Search – Filter any table with persistent search across modules.

Export / Import – Export any table as CSV or PDF, export/import all data (except Users) as JSON for backup or migration.

Backup to Google Drive – One‑click backup of all data to a dedicated Drive folder.

Email Notifications – Automatic emails on task assignment, file requests, and status changes (fully configurable).

Audit Log – Every sensitive action is logged for full traceability.

Session Management – Automatic session timeout (configurable) with visual countdown bar.

Dark / Light Theme – Auto‑detects system preference, manually toggle.

Multilingual – Full support for English and Arabic (right‑to‑left layout).

🛠️ Technology Stack
Backend: Google Apps Script (V8 runtime)

Database: Google Sheets (with dynamic column mapping)

Frontend: HTML5, CSS3 (Tailwind CSS), JavaScript (ES6)

Frameworks / Libraries:

Alpine.js – reactive UI

Chart.js – dashboard charts

Lucide – icons

jsPDF + autoTable – PDF export

Google Charts – Gantt charts

Tailwind CSS – utility-first styling

🔧 Installation & Deployment
Prerequisites
A Google account (free or Workspace)

Basic familiarity with Google Sheets and Apps Script

Steps
Create a copy of the spreadsheet

Download the provided .gs .json and .html files (from the repository) or use the link to the template sheet.

Open the spreadsheet, go to Extensions > Apps Script.

Copy the code

Paste the entire Code.gs content into the Code.gs file in the Apps Script editor.

Paste the entire index.html content into a new HTML file (create one via File > New > HTML).

Enable V8 runtime

Go to Run > Enable V8 runtime (if not already enabled).

Set up OAuth scopes (optional but recommended)

Create a file named appsscript.json with the following content Deploy as web app

Click Deploy > New deployment.

Choose Web app.

Set Execute as to "Me" (owner).

Set Who has access to "Anyone" (or "Anyone with link" for restricted use).

Click Deploy and copy the generated URL.

Open the URL – you will be prompted to authorize the app (grant all requested permissions). After authorization, the app will create the necessary sheets automatically.

🧑‍💻 Usage Guide
Login
First login with any email and PIN creates an Admin account.

Subsequent logins require an existing account with the correct PIN.

Roles & Permissions
Role	Capabilities
Admin	Full control: manage users, settings, backup, import/export, reset database, view audit log.
Manager	Manage tasks, budgets, assets, file requests, events, planner, and chat. Cannot manage users or system settings.
Staff	Same as Manager, except they cannot manage other users' tasks? (Actually they can assign tasks to anyone but cannot change user roles).
Viewer	Read‑only access to all modules (no create/update/delete).
Note: All actions are logged in the AuditLog sheet.

Modules Overview
Dashboard – KPI cards, charts, recent activity.

Tasks – Kanban board with drag‑and‑drop (no drag yet – future improvement), Gantt chart, filters, export.

Assets – Full CRUD, QR code generation, maintenance scheduling, history trail.

File Requests – Request files from colleagues, track with status, add comments, set expiry dates, receive email notifications.

Budgets – Record income/expenses, categorise, visualise.

Calendar – Create events, sync with Google Calendar, view monthly grid.

Planner – Weekly objectives and daily planning items.

Chat – Real‑time team messaging.

Office – View your office details (if configured).

Users (Admin) – Add/remove users, change roles and statuses.

Settings (Admin) – Configure email notifications (enable/disable, sender email/name).

Danger Zone (Admin) – Reset specific tables or wipe all non‑user data.

📧 Email Notifications
The app can send automatic emails for:

Task assignment (when a user is assigned a task)

New file request (to the target user)

File request status change (to the requester)

Email settings can be configured under Settings (Admin only). You must provide a valid Gmail or Google Workspace email as the sender (or leave blank to use the current user’s email).

🔒 Security & Privacy
All data resides in your own Google Sheets – we never see or store your data.

Session tokens are stored in the Users sheet and validated on each request.

All actions are logged for audit purposes.

You can disable email notifications at any time.

🤝 Contributing
Contributions are welcome! If you have ideas for new features or improvements, please open an issue or submit a pull request.

How to contribute
Fork the repository.

Create a feature branch.

Commit your changes.

Push and open a PR.

📄 License
This project is licensed under the MIT License – see the LICENSE file for details.

🙏 Acknowledgements
Inspired by real‑world team collaboration needs.

Built with love for open‑source tools.
