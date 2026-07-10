# JobTrackr 

A full-stack job application tracking app that helps you manage your job search journey. Built with a clean architecture: IndexedDB (DB Layer), REST-style API (API Layer), and an event-driven UI (App Layer).

![JobTrackr Preview](https://via.placeholder.com/1200x600?text=JobTrackr+Dashboard)

---

##  Features

###  Dashboard Stats
- **Total Applications** — Track all your job applications at a glance
- **Status Breakdown** — See counts for Applied, Interview, Offer, Rejected, and Wishlist
- **Interview Rate** — Calculate your conversion rate (interviews + offers) ÷ (total applications)

###  Dual Views
- **Kanban Board** — Drag-and-drop applications across columns by status
- **List View** — Tabular view with sortable columns and detailed information

###  Search & Filter
- **Search** — Find applications by company name or job role
- **Filter by Status** — Wishlist, Applied, Interview, Offer, Rejected
- **Filter by Type** — Internship, Full-time, Contract, Remote, Hybrid
- **Sort Options** — Newest first, oldest first, company name (A–Z), or deadline

###  Data Persistence
- **IndexedDB Storage** — All data persists locally in your browser
- **No Server Required** — Works completely offline
- **Instant Sync** — Changes reflect immediately across all views

###  Full CRUD Operations
- **Create** — Add new job applications with detailed metadata
- **Read** — View applications in Kanban or list view
- **Update** — Edit applications and drag cards to new statuses
- **Delete** — Remove applications with confirmation

###  Rich Application Details
- Company name and job role
- Job type (Internship, Full-time, Contract, Remote, Hybrid)
- Application status with color-coded indicators
- Date applied and application deadline
- Location, salary/stipend, and source URL
- Internal notes for interview prep, contact info, or referral details

 Deadline Tracking
- Visual indicators for upcoming deadlines
- Warning labels for applications closing within 7 days
- Alert for expired deadlines

---

Quick Start

How to Use

1. **Open the App**
   - Download or clone this repository
   - Open `job tracker.html` in your web browser
   - No installation or build process required!

2. **Add Your First Application**
   - Click the **"Add Application"** button (top right)
   - Fill in required fields: Company & Role
   - Add optional details: location, salary, deadline, notes
   - Click **"Save Application"**

3. **Track Your Progress**
   - **Drag cards** between columns to update status
   - **Search** for specific companies or roles
   - **Filter** by status or job type
   - **Sort** applications by date or deadline

4. **Edit or Delete**
   - Hover over any card and click **✎** (edit) or **✕** (delete)
   - In list view, use the action buttons on the right

---

##  Architecture

This app demonstrates a **three-layer full-stack architecture**:

### Layer 1: Database (IndexedDB)
```javascript
const DB = {
  getAll(),      // Fetch all applications
  insert(),      // Add new application
  update(),      // Modify existing application
  delete(),      // Remove application
}
