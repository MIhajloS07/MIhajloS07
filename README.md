<div align="center">

<img src="https://capsule-render.vercel.app/api?type=venom&color=0:0d1117,40:1f3a5f,100:2563eb&height=260&section=header&text=Mihajlo%20Stoiljkovi%C4%87&fontSize=56&fontColor=ffffff&fontAlignY=40&animation=twinkling&desc=Backend%20%C2%B7%20Embedded%20%C2%B7%20Software%20Engineering&descSize=20&descAlignY=62" width="100%" alt="Header"/>

<a href="https://github.com/MIhajloS07">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=22&duration=2800&pause=800&color=58A6FF&center=true&vCenter=true&width=760&height=50&lines=Electrical+Engineering+%26+Computing+%40+ELFAK+Ni%C5%A1;I+build+REST+APIs+with+ASP.NET+Core+%26+Redis;I+build+desktop+apps+with+C%2B%2B+%26+Qt;I+build+IoT+systems+with+Arduino;Open+to+internships+%26+junior+roles+%F0%9F%9A%80" alt="Typing animation"/>
</a>

<br/><br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mihajlo-stoiljkovic-aa1560355/)
[![GitHub](https://img.shields.io/badge/GitHub-MIhajloS07-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/MIhajloS07)
[![University](https://img.shields.io/badge/Faculty%20of%20Electronic%20Engineering-Ni%C5%A1-1f3a5f?style=for-the-badge)](https://www.elfak.ni.ac.rs/)
![Open to work](https://img.shields.io/badge/Open%20to-Internships%20%26%20Junior%20roles-2ea44f?style=for-the-badge)

<br/>

<sub>
<a href="#-featured-projects">🌟 Projects</a> &nbsp;·&nbsp;
<a href="#-tech-stack">🧰 Tech stack</a> &nbsp;·&nbsp;
<a href="#-competitions">🏆 Competitions</a> &nbsp;·&nbsp;
<a href="#-github-stats">📊 Stats</a> &nbsp;·&nbsp;
<a href="#-lets-connect">🤝 Contact</a>
</sub>

</div>

<br/>

## ⚡ In 10 seconds

<table>
<tr>
<td align="center" width="25%"><h3>🎓</h3><b>1st-year student</b><br/><sub>Electrical Engineering & Computing, University of Niš</sub></td>
<td align="center" width="25%"><h3>⚙️</h3><b>Backend</b><br/><sub>ASP.NET Core · EF Core · SQL Server · Redis · Docker · NodeJs · Flask</sub></td>
<td align="center" width="25%"><h3>🔌</h3><b>Embedded & IoT</b><br/><sub>Arduino · Raspberry Pi ·C++ · UART · WebSocket · KiCad · Linux</sub></td>
<td align="center" width="25%"><h3>🏆</h3><b>Competitor</b><br/><sub>National C++ (ZETSS), Game Jam, STEAM & more</sub></td>
</tr>
</table>

<br/>

## 👋 About me

I'm Mihajlo, a **Computer Electrical Technician** (graduate of *Rade Metalac*, Leskovac) and now a first-year student at the **Faculty of Electronic Engineering, University of Niš**.

I'm most interested in the places where layers meet: **hardware ↔ firmware ↔ backend ↔ UI**. I learn by building complete things, with tests, containers and documentation, not just code snippets.

```cs
var mihajlo = new Engineer
{
    Studies    = "Electrical Engineering & Computing @ ELFAK, Niš",
    Focus      = new[] { "Backend (ASP.NET Core)", "Embedded (Arduino)", "Desktop (C++/Qt)" },
    Philosophy = "Learn by building: with tests, containers and docs",
    Status     = "Open to internships & junior opportunities"
};
```

### 🎓 Education

| | Institution | Field |
|:--:|:--|:--|
| 🏛️ | **Faculty of Electronic Engineering, University of Niš** *(current)* | Electrical Engineering & Computing |
| 🏫 | **Technical School "Rade Metalac", Leskovac** *(graduated)* | Computer Engineering Technician |

<br/>

## 🌟 Featured projects

<div align="center">

<a href="https://github.com/MIhajloS07/Personal-Finance-Subscription-Tracker-Web-API">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=MIhajloS07&repo=Personal-Finance-Subscription-Tracker-Web-API&theme=tokyonight&hide_border=true" alt="Finance API"/>
</a>
<a href="https://github.com/MIhajloS07/WorkSphere">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=MIhajloS07&repo=WorkSphere&theme=tokyonight&hide_border=true" alt="WorkSphere"/>
</a>
<a href="https://github.com/MIhajloS07/Smart-City-Infrastructure-Smart-Street-Lighting-Smart-Traffic-Light">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=MIhajloS07&repo=Smart-City-Infrastructure-Smart-Street-Lighting-Smart-Traffic-Light&theme=tokyonight&hide_border=true" alt="Smart City"/>
</a>

</div>

<br/>

### 1️⃣ Personal Finance & Subscription Tracker API

<img src="https://img.shields.io/badge/.NET-10-512BD4?style=flat-square&logo=dotnet&logoColor=white"/> <img src="https://img.shields.io/badge/C%23-12-239120?style=flat-square&logo=csharp&logoColor=white"/> <img src="https://img.shields.io/badge/SQL%20Server-2022-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white"/> <img src="https://img.shields.io/badge/Redis-7-DC382D?style=flat-square&logo=redis&logoColor=white"/> <img src="https://img.shields.io/badge/Docker-Compose-2496ED?style=flat-square&logo=docker&logoColor=white"/> <img src="https://img.shields.io/badge/Tests-54%2F54%20passing-4CAF50?style=flat-square"/>

A production-style **REST API** for tracking users and recurring subscriptions: multi-currency, categories, payment dates and filtering. It uses **cache-aside with Redis**, **EF Core migrations**, DTOs, health checks and Swagger docs. The whole stack starts with **one command** (`docker compose up`).

```mermaid
flowchart LR
    C([Client / Swagger]) --> CT[Controllers]
    CT --> S[Services<br/>business logic]
    S <-->|cache-aside| R[(Redis 7)]
    S --> EF[EF Core]
    EF --> DB[(SQL Server 2022)]
    style C fill:#1f3a5f,color:#fff
    style R fill:#DC382D,color:#fff
    style DB fill:#CC2927,color:#fff
```

<details>
<summary><b>🔍 What's inside (click to expand)</b></summary>

<br/>

- **Architecture:** controllers → services → data layer, dependency injection, DTO pattern, SOLID
- **Data:** SQL Server 2022 with EF Core migrations, unique-email constraints, foreign keys and cascading deletes
- **Performance:** async I/O and a Redis caching layer with invalidation on updates
- **Testing:** **54 tests** (xUnit, Moq, FluentAssertions, EF Core InMemory) across services and controllers
- **DevOps:** multi-stage Dockerfile, Docker Compose (API + SQL Server + Redis), health checks, `/health` endpoint
- **API docs:** OpenAPI / Swagger UI

</details>

[![Repo](https://img.shields.io/badge/View%20repository-181717?style=for-the-badge&logo=github)](https://github.com/MIhajloS07/Personal-Finance-Subscription-Tracker-Web-API)

<br/>

### 2️⃣ WorkSphere: Desktop workforce management

<img src="https://img.shields.io/badge/C%2B%2B-17-00599C?style=flat-square&logo=cplusplus&logoColor=white"/> <img src="https://img.shields.io/badge/Qt-Widgets-41CD52?style=flat-square&logo=qt&logoColor=white"/> <img src="https://img.shields.io/badge/SQL%20Server-Express-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white"/> <img src="https://img.shields.io/badge/CMake-build-064F8C?style=flat-square&logo=cmake&logoColor=white"/>

A modern **C++17 / Qt** desktop app for managing **employees, projects and assignments**, backed by **Microsoft SQL Server**. It has a live dashboard (headcount, active projects, payroll), a polymorphic domain model (`Worker` / `Manager`), validated forms and a **dark/light theme** driven by one QSS template.

```mermaid
flowchart LR
    UI[Qt Widgets UI<br/>dashboard · forms · themes] --> M[Domain model<br/>Employee → Worker / Manager]
    UI --> Q[Qt SQL · ODBC]
    Q --> DB[(SQL Server Express)]
    UI -.-> ST[QSettings<br/>theme · currency · date]
    style UI fill:#41CD52,color:#000
    style DB fill:#CC2927,color:#fff
```

<details>
<summary><b>🔍 Highlights (click to expand)</b></summary>

<br/>

- Animated circular dashboard widgets, live search and a context-aware action bar
- Two employee types with polymorphic display, edit and payroll logic
- Projects with **auto Active/Inactive status** derived from the deadline
- Employee ↔ project assignments with duplicate detection and a live team panel
- Settings for currency (EUR, USD, RSD, BAM), date format and theme, remembered between sessions
- Parameterized queries and T-SQL; CMake build

</details>

[![Repo](https://img.shields.io/badge/View%20repository-181717?style=for-the-badge&logo=github)](https://github.com/MIhajloS07/WorkSphere)

<br/>

### 3️⃣ Smart City Infrastructure: Street Lighting & Traffic Light

<img src="https://img.shields.io/badge/Arduino-R4%20WiFi%20%2B%20R3-00979D?style=flat-square&logo=arduino&logoColor=white"/> <img src="https://img.shields.io/badge/C%2B%2B-Firmware-00599C?style=flat-square&logo=cplusplus&logoColor=white"/> <img src="https://img.shields.io/badge/C%23-Admin%20app-239120?style=flat-square&logo=csharp&logoColor=white"/> <img src="https://img.shields.io/badge/.NET%20MAUI-Mobile-512BD4?style=flat-square&logo=dotnet&logoColor=white"/> <img src="https://img.shields.io/badge/WebSocket-Dashboard-F7DF1E?style=flat-square&logo=javascript&logoColor=black"/>

A **team project (Team Smartanci)**: an IoT system where **four HC-SR04 ultrasonic sensors** detect vehicles and an **Arduino Uno R4 WiFi** creates a *moving corridor of light* that follows traffic, saving energy. A second **Arduino Uno R3** runs a smart traffic light over **UART**. It includes a **live web dashboard hosted on the Arduino**, a **C# admin app** and a **.NET MAUI feedback app**. It also has 3D-printed models of the traffic light and street mockup.

```mermaid
flowchart LR
    S[4 × HC-SR04<br/>sensors] --> SRV[Arduino Uno R4 WiFi<br/>lighting logic + web server]
    SRV -->|UART| CL[Arduino Uno R3<br/>smart traffic light]
    SRV -->|HTTP / WebSocket| W[Live web dashboard]
    SRV -->|WiFi| A[C# admin app]
    F[.NET MAUI<br/>feedback app] -.-> FS[Formspree]
    style SRV fill:#00979D,color:#fff
    style CL fill:#00979D,color:#fff
```

<details>
<summary><b>🔍 How it works (click to expand)</b></summary>

<br/>

- **Cascading light logic:** a vehicle at HC1 lights segments S1+S2, HC2 lights S2+S3, and so on, so light follows the car and stays off elsewhere
- **Protocol:** newline-terminated ASCII messages over UART (`LIGHT,S1,200`, `SENSOR,HC1,120`), with `ACK` / `ERR` handling
- **Reliability:** if WiFi drops, the traffic light falls back to a safe local timing cycle
- **Admin app (C#):** live sensor feed, manual segment control, UART monitor, event log
- **Dashboard:** street visualization, detection history, UART log viewer, AUTO / MANUAL / MAINTENANCE modes
- **Hardware design:** schematics in KiCad, assembly diagram, 3D-printed housing

</details>

[![Repo](https://img.shields.io/badge/View%20repository-181717?style=for-the-badge&logo=github)](https://github.com/MIhajloS07/Smart-City-Infrastructure-Smart-Street-Lighting-Smart-Traffic-Light)
[![Website](https://img.shields.io/badge/Team%20website-Live-2563eb?style=for-the-badge&logo=netlify&logoColor=white)](https://statuesque-pudding-4a326c.netlify.app/)

<br/>

### 🗂️ More from my GitHub

<table>
<tr>
<td width="33%" valign="top">

**📡 [QtUDPServerClient](https://github.com/MIhajloS07/QtUDPServerClient)**<br/>
<sub>C++ · Qt · Winsock2</sub><br/>
UDP client-server app with a GUI and command-based communication.

</td>
<td width="33%" valign="top">

**📚 [LibrarySystem-Java](https://github.com/MIhajloS07/LibrarySystem-Java)**<br/>
<sub>Java 21 · SQLite · JUnit 5 · Maven · Docker</sub><br/>
MVC library management system with automated tests.

</td>
<td width="33%" valign="top">

**⛪ [Monastery-Web-API](https://github.com/MIhajloS07/Monastery-Web-API)**<br/>
<sub>Python · Flask · MySQL · Swagger · Docker</sub><br/>
CRUD REST API with unit tests.

</td>
</tr>
</table>

<br/>

## 🧰 Tech stack

<div align="center">

<img src="https://skillicons.dev/icons?i=cs,cpp,c,java,python,js,html,css&theme=dark" alt="Languages"/>
<br/>
<img src="https://skillicons.dev/icons?i=dotnet,qt,flask,nodejs&theme=dark" alt="Frameworks"/>
<br/>
<img src="https://skillicons.dev/icons?i=mysql,sqlite,redis,docker,postman&theme=dark" alt="Data"/>
<br/>
<img src="https://skillicons.dev/icons?i=arduino,raspberrypi,git,github,npm,vscode,visualstudio,linux,windows,figma&theme=dark" alt="Tools"/>
</div>

<details>
<summary><b>📋 What I use each for (click to expand)</b></summary>

<br/>

| Area | Experience |
|:--|:--|
| **C# / .NET** | ASP.NET Core APIs, EF Core, WinForms, OOP, .NET MAUI basics |
| **C / C++** | Low-level fundamentals, STL, OOP, Qt Widgets, Arduino firmware |
| **Python** | Flask APIs, Raspberry Pi (`RPi.GPIO`), Pygame |
| **Java** | OOP, CRUD with database connectivity, JUnit |
| **Databases** | SQL Server (stored procedures), MySQL, SQLite, Redis caching |
| **Embedded** | Arduino, Raspberry Pi, UART, Wi-Fi / BLE, KiCad, PCB basics |
| **DevOps** | Docker, Docker Compose, Git / GitHub |
| **Game dev** | Pygame, Godot, Unity basics, GameMaker |
| **Networking & OS** | Cisco Packet Tracer, Linux / Windows administration, VMs |

*Proficiency varies across tools. This reflects hands-on projects and ongoing learning.*

</details>

<br/>

## 🏆 Competitions

<div align="center">

| | Competition | Field |
|:--:|:--|:--|
| 💻 | **ZETSS** (national) | C++ programming |
| 🎮 | **Global Game Jam** (Metropolitan) | Game development under a deadline |
| 🚀 | **Galaksija Cup** | Technical challenges |
| 🔬 | **STEAM Challenge** | Interdisciplinary team project |
| 💼 | **Business Challenge** | Teamwork & idea development |

</div>

<br/>

## 📊 GitHub stats

<div align="center">

<img height="170" src="https://github-readme-stats.vercel.app/api?username=MIhajloS07&show_icons=true&theme=tokyonight&hide_border=true&rank_icon=github" alt="Stats"/>
<img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=MIhajloS07&layout=compact&theme=tokyonight&hide_border=true&langs_count=7" alt="Top languages"/>

<img src="https://streak-stats.demolab.com?user=MIhajloS07&theme=tokyonight&hide_border=true" alt="Streak"/>

<img src="https://ghchart.rshah.org/2563eb/MIhajloS07" width="100%" alt="Contribution calendar"/>

<sub>Language stats show detected code in repositories, not proficiency.</sub>

</div>

<br/>

## 🌱 Currently learning

<div align="center">

![ASP.NET Core](https://img.shields.io/badge/ASP.NET%20Core-API%20design-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![EF Core](https://img.shields.io/badge/Entity%20Framework-Data%20modeling-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Algorithms](https://img.shields.io/badge/Algorithms-%26%20Data%20Structures-2563eb?style=for-the-badge)
![Docker](https://img.shields.io/badge/Docker-Deployment-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Embedded](https://img.shields.io/badge/Embedded-HW%2FSW%20interaction-00979D?style=for-the-badge&logo=arduino&logoColor=white)

</div>

<br/>

## 🤝 Let's connect

I'm looking for an **internship or junior role** where I can learn from experienced engineers, ship real features and grow in **backend or embedded** development.

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Message%20me-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mihajlo-stoiljkovic-aa1560355/)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/MIhajloS07)

<br/>

**Build it. Test it. Containerize it. Learn from it.** ✨

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2563eb,50:1f3a5f,100:0d1117&height=120&section=footer" width="100%" alt="Footer"/>

</div>
