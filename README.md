# Checkly: Attendance Management System

A mobile and web-based staff attendance management application, built during my Industrial Training internship at **SD Guthrie Research Sdn. Bhd.** (Carey Island, Selangor) under the Advanced Agricultural Technology & Data Sciences (AATDS) unit.

## 📋 About

The organization previously relied on manual attendance tracking (electronic punch cards), which was time-consuming, error-prone, and gave management no real-time insight into attendance trends. Checkly digitizes the entire process — staff check in/out electronically, and management gets real-time dashboards and reports.

The system supports **three user roles** with different access levels:

| Role | Access |
|---|---|
| **Staff** | Record daily attendance, view personal dashboard & reports |
| **Head of Department (HOD)** | All Staff features + department dashboard & reports |
| **Admin** | Full access to all departments' data, dashboards, reports, and user management |

## ✨ Key Features

- **Daily Check In/Out** with mandatory Work Mode selection (On-Site / Work From Home)
- **Location-based validation** — On-Site check-ins must be within 10KM of the office (GPS-verified)
- **Weekly quota enforcement** — max 3 On-Site days and 2 WFH days per week
- **Automatic Late Arrival labelling** for check-ins after 8:40 AM
- **Auto Mark Absent** — scheduled flow marks staff absent if no attendance is recorded by 5:30 PM (excludes weekends/public holidays)
- **Check-Out Reminder** — automated email reminder sent at 5:15 PM
- **Personal, Department, and Admin dashboards** with attendance KPIs and charts
- **CSV export** for attendance reports
- **User Management** — add/edit/delete staff records and public holidays (Admin only)

## 🛠️ Tech Stack

| Component | Platform | Role |
|---|---|---|
| Frontend | Microsoft Power Apps | User interface for all roles |
| Data Storage | Microsoft SharePoint Lists | Stores attendance, user, and holiday data |
| Automation | Microsoft Power Automate | Scheduled flows, email triggers, data import/export |

**SharePoint Lists:** `UsersList`, `AttendanceList`, `PublicHolidayList`

## 📸 Screenshots
[View the User Interface of the system](Checkly-Attendance-Management-System/blob/main/Checkly-Sytem-UI-Screenshots.pdf)

## 📂 Files in this Repository

- `Checkly.msapp` — exported Power Apps application file (open with Power Apps Studio)
- `docs/Checkly_Technical_Documentation.pdf` — full technical documentation (architecture, data flow, DAX-equivalent business rules, user guide, troubleshooting)
- `docs/Practical_Training_Report.pdf` — my full internship report covering both Checkly and its analytics dashboard

> **Note:** `.msapp` files can't be previewed directly on GitHub. To view or run the app, import it into [Power Apps Studio](https://make.powerapps.com) (requires a Microsoft/Power Platform account).

## 🔧 How It Works (Automation Flows)

| Flow | Trigger | Purpose |
|---|---|---|
| Auto Mark Absent | Scheduled, 5:30 PM daily | Marks staff absent if no attendance recorded (skips weekends/holidays) |
| Check-Out Reminder | Scheduled, 5:15 PM daily | Emails staff who haven't checked out |
| Export Attendance Report | Manual (Power Apps) | Exports HOD/Admin attendance data as CSV |
| Import Attendance/Users | Manual | Imports bulk data into SharePoint Lists |

## 👤 Author

**Ainaa Aqilah binti Hassan Nuddin**

Bachelor of Information Technology (Hons.), Universiti Teknologi MARA

IT Intern, SD Guthrie Research Sdn. Bhd. (March – July 2026)

[GitHub](https://github.com/ainaaqilah)

---
*Developed as part of Industrial Training (CST688), supervised by Madam Shahirah Shazana Binti A. Rahman (Executive, Software Developer Engineer).*
