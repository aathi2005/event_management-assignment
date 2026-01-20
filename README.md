# Event Management System – Frappe Framework

A Frappe-based web application designed for a local event planning company to manage events, attendees, and ticket sales efficiently.  
The system focuses on simplicity and core functionality, assuming a single user role (event planner).

---

## 🚀 Features Implemented

### 1. Event Management
- Create, update, delete events
- Event fields:
  - Event Title
  - Description
  - Event Date
  - Location
  - Capacity
- Search and filter events by:
  - Event Title
  - Event Date

---

### 2. Attendee Management
- Register attendees for events
- Update attendee details
- View attendees mapped to each event
- **Event capacity validation** to prevent overbooking

---

### 3. Ticket Management
- Track tickets sold per event
- Track available tickets
- Auto-calculate remaining capacity
- Fixed ticket price assumption for simplicity

---

### 4. Capacity Validation (Business Logic)
- Implemented using **Frappe Server Script**
- Triggered **Before Insert** on Attendee
- Prevents registration when event capacity is exceeded

---

### 5. CSV Import
- Bulk import Event records using **Frappe Data Import**
- Supported CSV fields:
  - Event Title
  - Description
  - Event Date
  - Location
  - Capacity

---

## 🛠 Tech Stack
- **Framework:** Frappe Framework
- **Backend:** Python (Frappe ORM, Server Scripts)
- **Frontend:** Frappe Desk UI
- **Database:** MariaDB
- **Tools:** Git, GitHub, WSL (Linux)

---

## ⚙️ Project Setup

```bash
bench init frappe-bench
bench new-site event.local
bench new-app event_management
bench --site event.local install-app event_management
bench start
