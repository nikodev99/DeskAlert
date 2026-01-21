# DeskAlert

# Announcement System – Complete Overview

This is a **company-wide announcement system** designed for **Windows corporate environments**. It ensures that critical messages are seen by all employees without relying on email or user action.

---

## Core Functionality

### For Employees (End Users)

* Announcements automatically appear on their screen as a **scrolling banner above the taskbar**
* The banner **cannot be closed by users**, ensuring important messages are seen
* Supports **rich text formatting**:

  * **Bold**
  * *Italic*
  * Colored text
* Plays a **notification sound** when announcements appear
* Supports **multi-day announcements** that persist even if the computer restarts

---

### For Administrators

* Create and schedule announcements through a **dedicated admin application**
* Set **start and end times** for announcements (hours or multiple days)
* **Preview formatted text** before publishing
* View all **active announcements** company-wide
* **Deactivate announcements early** if needed
* Track **who created each announcement** for accountability

---

## How It Works

### 1. Windows Service (Background Monitor)

* Runs automatically on every employee’s computer
* Checks a **centralized database every 30 seconds** for new announcements
* When an active announcement is found, it launches the display window
* Automatically **resumes announcements after computer restarts**
* Runs as a **system service**, so employees cannot stop it

---

### 2. Display Window

* Displays as a **blue banner** spanning the full width of the screen
* Positioned **just above the Windows taskbar**
* Text scrolls continuously **from right to left**
* Window is **always on top** and cannot be closed until the announcement period ends
* Automatically checks every 30 seconds whether it should close based on the end time

---

### 3. Admin Application

* Secure login system for administrators
* Create announcements using simple formatting markup:

```text
**text**        → Bold
*text*         → Italic
[color=red]text[/color] → Colored text
```

* Schedule announcements with specific **start and end dates/times**
* Quick-set duration buttons (e.g. **2 hours**, **4 hours**, **All day**)
* **Live preview** of formatted text
* View, edit, and manage all announcements

---

### 4. Centralized Database

* **SQLite database** stored on a secure network share
* All employee computers access the **same database**
* Tracks:

  * Announcements
  * Administrators
  * Creation and modification history
* No need to deploy announcements to individual machines

---

## Use Cases

Perfect for:

* 🚨 Emergency notifications (evacuations, outages)
* 📢 Company-wide announcements (policy updates, events)
* 🛠 IT maintenance windows
* 👥 HR announcements
* ⚠️ Safety alerts
* 📅 Multi-day events or reminders

---

## Example Scenario

An administrator creates an announcement at **9:00 AM** saying:

> *"Server maintenance tonight from 8:00 PM to 10:00 PM"*

All employees see it immediately.

If an employee restarts their computer at **4:00 PM**, the announcement **reappears automatically** when they log back in — ensuring everyone sees the critical message.

---

## Key Benefits

* ✅ **Guaranteed Visibility** – Cannot be dismissed or ignored
* 🎯 **Centralized Management** – One admin reaches all employees
* 🔁 **Persistence** – Survives restarts and logouts
* ⏱ **Scheduling** – Set it once, runs automatically
* 🎨 **Rich Formatting** – Eye‑catching, readable announcements
* 🧾 **Accountability** – Full tracking of announcement creators

---

## Summary

This system ensures **critical company communications reach every employee**, regardless of whether they check email, are away from their desk, or restart their computer. It is ideal for enterprises that require **reliable, unavoidable, and centrally managed communication**.
