# WCDP – Mobile & Windows Application (Workforce Management)

> **Client:** Dry Wall, West Coast, California, USA  
> **Domain:** Employee Mobile and Admin Desktop Application (Time Tracking, Attendance & Task Management)  
> **Author:** Sagarika Chakraborty — *Full Stack .NET Engineer | React.js | Web API | SQL Server*

**WCDP** is a cross-platform workforce management suite built with **Xamarin.Forms** (Android, iOS, Windows desktop) using **C#** and **MVVM**. It enables employees to punch timesheets, track timecards and attendance, and receive task assignments, while admins manage tasks, users, and reports on a Windows desktop app. The solution integrates with secure APIs, supports data synchronization, and uses **AWS** for CI/CD and hosting.

---

## ✨ Key Features
- **Mobile (Android/iOS)**: Punch in/out, timecards, attendance, assigned tasks, offline cache & sync.
- **Windows Admin App**: Task assignment/monitoring, workforce analytics dashboards, attendance and timecard reporting.
- **MVVM & XAML**: Clean separation, reusable styles/themes, converters & templates for consistent UI/UX.
- **Secure API Integration**: Auth tokens, role-based views; robust sync with conflict handling.
- **AWS CI/CD**: CodePipeline + CodeBuild for automated build/test/deploy; app distribution via Play Store, App Store, and S3 for desktop installers.
- **Ops**: IAM roles for least-privilege access; auto-scaling and load balancing to handle peak hours.

---

## 🧱 Technology Stack
- **UI/Framework**: Xamarin.Forms (Android, iOS, Windows) with MVVM
- **Language**: C#
- **Build & Release**: AWS CodePipeline, CodeBuild, CodeDeploy (where applicable)
- **Hosting**: AWS (EC2/App Runner/LB as applicable), Amazon S3 (desktop installer distribution), CloudFront (optional)
- **Auth & Security**: JWT/OAuth tokens, IAM roles, HTTPS
- **Data**: REST/GraphQL APIs; SQLite for local cache; SQL Server/PostgreSQL backend (pluggable)

---

## 📁 Repository Structure
```
.
├─ README.md
└─ docs
   ├─ HLD.md
   ├─ LLD.md
   └─ architecture.png
```

---

## 🚀 Quick Start (Dev)

1) **Mobile Solution (Xamarin.Forms)**
- Configure `appsettings.json` or platform secrets:
  ```json
  {
    "ApiBaseUrl": "https://api.example.com",
    "Auth": { "ClientId": "local-dev", "Scopes": ["timesheet.read", "timesheet.write"] }
  }
  ```
- Run from Visual Studio: select **Android**/**iOS**/**UWP/Win** targets.

2) **Windows Admin**
- Update `appsettings.Development.json` similarly and run WPF/UWP project.

3) **Backend API** (if running locally)
- Provide `.env`/appsettings with DB connection and JWT signing key.

---

## 🧭 Documentation
- **HLD**: [`/docs/HLD.md`](docs/HLD.md) — architecture, modules, flows, security, CI/CD
- **LLD**: [`/docs/LLD.md`](docs/LLD.md) — MVVM layers, page/viewmodel map, sync contracts, error codes
- **Diagram**: [`/docs/architecture.png`](docs/architecture.png)

---

## 📦 Distribution
- **Mobile**: Google Play Store, Apple App Store (via App Store Connect/TestFlight).
- **Desktop**: Installer published to **S3** and optionally served via **CloudFront**.

---

## 👩‍💻 Credits
**Sagarika Chakraborty** — Cross-platform development (Xamarin.Forms + MVVM), secure API integration & sync, AWS CI/CD, store releases, and admin desktop tooling.
