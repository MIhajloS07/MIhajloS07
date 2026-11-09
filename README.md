<div align="center">

<img src="https://capsule-render.vercel.app/api?type=venom&color=0:0d1117,40:1f3a5f,100:2563eb&height=260&section=header&text=Mihajlo%20Stoiljkovi%C4%87&fontSize=56&fontColor=ffffff&fontAlignY=40&animation=twinkling&desc=Backend%20%C2%B7%20Embedded%20%C2%B7%20Software%20Engineering&descSize=20&descAlignY=62" width="100%" alt="Header"/>

<a href="https://github.com/MIhajloS07">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=22&duration=2800&pause=800&color=58A6FF&center=true&vCenter=true&width=760&height=50&lines=Electrical+Engineering+%26+Computing+%40+ELFAK+Ni%C5%A1;I+build+REST+APIs+with+ASP.NET+Core+%26+Redis;I+build+desktop+apps+with+C%2B%2B+%26+Qt;I+build+IoT+systems+with+Arduino;Open+to+internships+%26+junior+roles+%F0%9F%9A%80" alt="Typing animation"/>
</a>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mihajlo-stoiljkovic-aa1560355/)
[![GitHub](https://img.shields.io/badge/GitHub-MIhajloS07-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/MIhajloS07)
[![University](https://img.shields.io/badge/Faculty%20of%20Electronic%20Engineering-Ni%C5%A1-1f3a5f?style=for-the-badge)](https://www.elfak.ni.ac.rs/)
![Open to work](https://img.shields.io/badge/Open%20to-Internships%20%26%20Junior%20roles-2ea44f?style=for-the-badge)

<sub>
<a href="#featured-projects">🌟 Projects</a> &nbsp;·&nbsp;
<a href="#tech-stack">🧰 Tech stack</a> &nbsp;·&nbsp;
<a href="#courses--certificates">📜 Courses</a> &nbsp;·&nbsp;
<a href="#competitions">🏆 Competitions</a> &nbsp;·&nbsp;
<a href="#github-stats">📊 Stats</a> &nbsp;·&nbsp;
<a href="#lets-connect">🤝 Contact</a>
</sub>

</div>

## In 10 seconds

<table>
<tr>
<td align="center" width="25%"><b>1st-year student</b><br/><sub>Electrical Engineering & Computing, University of Niš</sub></td>
<td align="center" width="25%"><b>Backend</b><br/><sub>ASP.NET Core · EF Core · SQL Server · Redis · Docker · NodeJs · Flask</sub></td>
<td align="center" width="25%"><b>Embedded & IoT</b><br/><sub>Arduino · Raspberry Pi ·C++ · UART · WebSocket · KiCad · Linux</sub></td>
<td align="center" width="25%"><b>Competitor</b><br/><sub>National C++ (ZETSS), Game Jam, STEAM & more</sub></td>
</tr>
</table>

## About me

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

<img src="assets/pipeline.svg" width="100%" alt="hardware, firmware, backend, UI"/>

### Education

| # | Institution | Field |
|:--:|:--|:--|
| 01 | **Faculty of Electronic Engineering, University of Niš** *(current)* | Electrical Engineering & Computing |
| 02 | **Technical School "Rade Metalac", Leskovac** *(graduated)* | Computer Engineering Technician |

<img src="assets/divider.svg" width="100%" alt=""/>

## Featured projects

<table>
<tr>
<td width="33%" valign="top">

**[Finance & Subscription Tracker API](https://github.com/MIhajloS07/Personal-Finance-Subscription-Tracker-Web-API)**<br/>
<sub>ASP.NET Core · EF Core · SQL Server · Redis · Docker</sub><br/>
REST API with Redis caching, 54 passing tests and one-command Docker setup.

</td>
<td width="33%" valign="top">

**[WorkSphere](https://github.com/MIhajloS07/WorkSphere)**<br/>
<sub>C++17 · Qt Widgets · SQL Server · CMake</sub><br/>
Desktop workforce management app with live dashboard and dark/light themes.

</td>
<td width="33%" valign="top">

**[Smart City Infrastructure](https://github.com/MIhajloS07/Smart-City-Infrastructure-Smart-Street-Lighting-Smart-Traffic-Light)**<br/>
<sub>Arduino · C++ · C# · .NET MAUI · WebSocket</sub><br/>
IoT street lighting and smart traffic light, built as a team project.

</td>
</tr>
</table>

### 01 · Personal Finance & Subscription Tracker API

<img src="https://img.shields.io/badge/.NET-10-512BD4?style=flat-square&logo=dotnet&logoColor=white"/> <img src="https://img.shields.io/badge/C%23-12-239120?style=flat-square&logo=csharp&logoColor=white"/> <img src="https://img.shields.io/badge/SQL%20Server-2022-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white"/> <img src="https://img.shields.io/badge/Redis-7-DC382D?style=flat-square&logo=redis&logoColor=white"/> <img src="https://img.shields.io/badge/Docker-Compose-2496ED?style=flat-square&logo=docker&logoColor=white"/> <img src="https://img.shields.io/badge/Tests-54%2F54%20passing-4CAF50?style=flat-square"/>

A production-style **REST API** for tracking users and recurring subscriptions: multi-currency, categories, payment dates and filtering. It uses **cache-aside with Redis**, **EF Core migrations**, DTOs, health checks and Swagger docs. The whole stack starts with **one command** (`docker compose up`).

<details>
<summary><b>What's inside · animated request flow (click to expand)</b></summary>

<img src="assets/api-flow.svg" width="100%" alt="Cache-aside request lifecycle: cache miss then cache hit"/>

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

- **Architecture:** controllers → services → data layer, dependency injection, DTO pattern, SOLID
- **Data:** SQL Server 2022 with EF Core migrations, unique-email constraints, foreign keys and cascading deletes
- **Performance:** async I/O and a Redis caching layer with invalidation on updates
- **Testing:** **54 tests** (xUnit, Moq, FluentAssertions, EF Core InMemory) across services and controllers
- **DevOps:** multi-stage Dockerfile, Docker Compose (API + SQL Server + Redis), health checks, `/health` endpoint
- **API docs:** OpenAPI / Swagger UI

</details>

[![Repo](https://img.shields.io/badge/View%20repository-181717?style=flat-square&logo=github)](https://github.com/MIhajloS07/Personal-Finance-Subscription-Tracker-Web-API)

### 02 · WorkSphere: Desktop workforce management

<img src="https://img.shields.io/badge/C%2B%2B-17-00599C?style=flat-square&logo=cplusplus&logoColor=white"/> <img src="https://img.shields.io/badge/Qt-Widgets-41CD52?style=flat-square&logo=qt&logoColor=white"/> <img src="https://img.shields.io/badge/SQL%20Server-Express-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white"/> <img src="https://img.shields.io/badge/CMake-build-064F8C?style=flat-square&logo=cmake&logoColor=white"/>

A modern **C++17 / Qt** desktop app for managing **employees, projects and assignments**, backed by **Microsoft SQL Server**. It has a live dashboard (headcount, active projects, payroll), a polymorphic domain model (`Worker` / `Manager`), validated forms and a **dark/light theme** driven by one QSS template.

<details>
<summary><b>Highlights · animated request flow (click to expand)</b></summary>

<img src="assets/worksphere-flow.svg" width="100%" alt="WorkSphere request lifecycle"/>

```mermaid
flowchart LR
    UI[Qt Widgets UI<br/>dashboard · forms · themes] --> M[Domain model<br/>Employee → Worker / Manager]
    UI --> Q[Qt SQL · ODBC]
    Q --> DB[(SQL Server Express)]
    UI -.-> ST[QSettings<br/>theme · currency · date]
    style UI fill:#41CD52,color:#000
    style DB fill:#CC2927,color:#fff
```

- Animated circular dashboard widgets, live search and a context-aware action bar
- Two employee types with polymorphic display, edit and payroll logic
- Projects with **auto Active/Inactive status** derived from the deadline
- Employee ↔ project assignments with duplicate detection and a live team panel
- Settings for currency (EUR, USD, RSD, BAM), date format and theme, remembered between sessions
- Parameterized queries and T-SQL; CMake build

</details>

[![Repo](https://img.shields.io/badge/View%20repository-181717?style=flat-square&logo=github)](https://github.com/MIhajloS07/WorkSphere)

### 03 · Smart City Infrastructure: Street Lighting & Traffic Light

<img src="https://img.shields.io/badge/Arduino-R4%20WiFi%20%2B%20R3-00979D?style=flat-square&logo=arduino&logoColor=white"/> <img src="https://img.shields.io/badge/C%2B%2B-Firmware-00599C?style=flat-square&logo=cplusplus&logoColor=white"/> <img src="https://img.shields.io/badge/C%23-Admin%20app-239120?style=flat-square&logo=csharp&logoColor=white"/> <img src="https://img.shields.io/badge/.NET%20MAUI-Mobile-512BD4?style=flat-square&logo=dotnet&logoColor=white"/> <img src="https://img.shields.io/badge/WebSocket-Dashboard-F7DF1E?style=flat-square&logo=javascript&logoColor=black"/>

A **team project (Team Smartanci)**: an IoT system where **four HC-SR04 ultrasonic sensors** detect vehicles and an **Arduino Uno R4 WiFi** creates a *moving corridor of light* that follows traffic, saving energy. A second **Arduino Uno R3** runs a smart traffic light over **UART**. It includes a **live web dashboard hosted on the Arduino**, a **C# admin app** and a **.NET MAUI feedback app**. It also has 3D-printed models of the traffic light and street mockup.

<details>
<summary><b>How it works · animated light logic (click to expand)</b></summary>

<img src="assets/smart-street.svg" width="100%" alt="Cascading street light animation"/>

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

- **Cascading light logic:** a vehicle at HC1 lights segments S1+S2, HC2 lights S2+S3, and so on, so light follows the car and stays off elsewhere
- **Protocol:** newline-terminated ASCII messages over UART (`LIGHT,S1,200`, `SENSOR,HC1,120`), with `ACK` / `ERR` handling
- **Reliability:** if WiFi drops, the traffic light falls back to a safe local timing cycle
- **Admin app (C#):** live sensor feed, manual segment control, UART monitor, event log
- **Dashboard:** street visualization, detection history, UART log viewer, AUTO / MANUAL / MAINTENANCE modes
- **Hardware design:** schematics in KiCad, assembly diagram, 3D-printed housing

</details>

[![Repo](https://img.shields.io/badge/View%20repository-181717?style=flat-square&logo=github)](https://github.com/MIhajloS07/Smart-City-Infrastructure-Smart-Street-Lighting-Smart-Traffic-Light)
[![Website](https://img.shields.io/badge/Team%20website-Live-2563eb?style=flat-square&logo=netlify&logoColor=white)](https://statuesque-pudding-4a326c.netlify.app/)

### More from my GitHub

<table>
<tr>
<td width="33%" valign="top">

**[QtUDPServerClient](https://github.com/MIhajloS07/QtUDPServerClient)**<br/>
<sub>C++ · Qt · Winsock2</sub><br/>
UDP client-server app with a GUI and command-based communication.

</td>
<td width="33%" valign="top">

**[LibrarySystem-Java](https://github.com/MIhajloS07/LibrarySystem-Java)**<br/>
<sub>Java 21 · SQLite · JUnit 5 · Maven · Docker</sub><br/>
MVC library management system with automated tests.

</td>
<td width="33%" valign="top">

**[Monastery-Web-API](https://github.com/MIhajloS07/Monastery-Web-API)**<br/>
<sub>Python · Flask · MySQL · Swagger · Docker</sub><br/>
CRUD REST API with unit tests.

</td>
</tr>
</table>

<img src="assets/divider.svg" width="100%" alt=""/>

## Tech stack

<div align="center">

<img src="https://skillicons.dev/icons?i=cs,cpp,c,java,python,js,html,css,dotnet,qt,flask,nodejs&theme=dark" alt="Languages and frameworks"/>
<br/>
<img src="https://skillicons.dev/icons?i=mysql,sqlite,redis,docker,postman,arduino,raspberrypi,git,github,npm,vscode,visualstudio,linux,windows,figma&theme=dark" alt="Data and tools"/>

</div>

<details>
<summary><b>What I use each for (click to expand)</b></summary>

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

<img src="assets/divider.svg" width="100%" alt=""/>

## Courses & certificates

<sub>Click a thumbnail to open the full certificate or badge.</sub>

<table>
<tr><th colspan="3" align="left">Cisco Networking Academy</th></tr>
<tr>
<td align="center" width="110"><a href="https://www.credly.com/badges/01959a62-f5e1-42ae-a7ef-ec5340e15fe8/public_url"><img src="assets/cisco-cpp-essentials-1.png" width="90" alt="C++ Essentials 1"/></a></td>
<td><b>C++ Essentials 1</b><br/><sub>Verified digital badge · syntax, data types, control flow, functions</sub></td>
<td align="center" width="170"><a href="https://www.credly.com/badges/01959a62-f5e1-42ae-a7ef-ec5340e15fe8/public_url"><img src="https://img.shields.io/badge/Verify%20on-Credly-FF6B00?style=flat-square" alt="Verify on Credly"/></a></td>
</tr>
<tr><th colspan="3" align="left">Singidunum University</th></tr>
<tr>
<td align="center"><a href="assets/singidunum-java-1.png"><img src="assets/singidunum-java-1.png" width="90" alt="Java 1"/></a></td>
<td><b>Java</b> <sub>(1/2)</sub><br/><sub>Singidunum University · certificate</sub></td>
<td align="center"><a href="assets/singidunum-java-1.png"><img src="https://img.shields.io/badge/View-certificate-1f3a5f?style=flat-square" alt="View certificate"/></a></td>
</tr>
<tr>
<td align="center"><a href="assets/singidunum-java-2.png"><img src="assets/singidunum-java-2.png" width="90" alt="Java 2"/></a></td>
<td><b>Java</b> <sub>(2/2)</sub><br/><sub>Singidunum University · certificate</sub></td>
<td align="center"><a href="assets/singidunum-java-2.png"><img src="https://img.shields.io/badge/View-certificate-1f3a5f?style=flat-square" alt="View certificate"/></a></td>
</tr>
<tr>
<td align="center"><a href="assets/singidunum-javascript.png"><img src="assets/singidunum-javascript.png" width="90" alt="JavaScript"/></a></td>
<td><b>JavaScript</b><br/><sub>Singidunum University · certificate</sub></td>
<td align="center"><a href="assets/singidunum-javascript.png"><img src="https://img.shields.io/badge/View-certificate-1f3a5f?style=flat-square" alt="View certificate"/></a></td>
</tr>
<tr><th colspan="3" align="left">SoloLearn</th></tr>
<tr>
<td align="center"><sub>SoloLearn</sub></td>
<td><b>All completed courses</b><br/><sub>Full list of finished courses and certificates on my public profile</sub></td>
<td align="center"><a href="https://www.sololearn.com/en/profile/30513559"><img src="https://img.shields.io/badge/Open-profile-149EF2?style=flat-square" alt="SoloLearn profile"/></a></td>
</tr>
</table>

<img src="assets/divider.svg" width="100%" alt=""/>

## Competitions

<div align="center">

| # | Competition | Field |
|:--:|:--|:--|
| 01 | **ZETSS** (national) | C++ programming |
| 02 | **Global Game Jam** (Metropolitan) | Game development under a deadline |
| 03 | **Galaksija Cup** | Technical challenges |
| 04 | **STEAM Challenge** | Interdisciplinary team project |
| 05 | **Business Challenge** | Teamwork & idea development |

</div>

<img src="assets/divider.svg" width="100%" alt=""/>

## GitHub stats

<div align="center">

<picture>
  <source media="(prefers-color-scheme: light)" srcset="https://www.gitskins.com/api/section/story-timeline?username=mihajlos07&mode=light" />
  <img src="https://www.gitskins.com/api/section/story-timeline?username=mihajlos07&mode=dark" width="100%" alt="Contributions week by week, with my longest streak" />
</picture>
<br>
<p align="center">
<picture>
  <source media="(prefers-color-scheme: light)" srcset="https://www.gitskins.com/api/section/heatmap?username=mihajlos07&theme=github-dark&avatar=https%3A%2F%2Favatars.githubusercontent.com%2Fu%2F251505713%3Fu%3D75476ca5c6c6768ac9dd8758d3420d3a860d8c0d%26v%3D4&v=recruiter-heatmap-1&mode=light" />
  <img src="https://www.gitskins.com/api/section/heatmap?username=mihajlos07&theme=github-dark&avatar=https%3A%2F%2Favatars.githubusercontent.com%2Fu%2F251505713%3Fu%3D75476ca5c6c6768ac9dd8758d3420d3a860d8c0d%26v%3D4&v=recruiter-heatmap-1&mode=dark" width="100%" alt="Mihajlo Stoiljković contribution activity" />
</picture>
</p>

<sub>Language stats show detected code in repositories, not proficiency.</sub>

</div>

## Currently learning

<div align="center">

![ASP.NET Core](https://img.shields.io/badge/ASP.NET%20Core-API%20design-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![EF Core](https://img.shields.io/badge/Entity%20Framework-Data%20modeling-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![Algorithms](https://img.shields.io/badge/Algorithms-%26%20Data%20Structures-2563eb?style=flat-square)
![Docker](https://img.shields.io/badge/Docker-Deployment-2496ED?style=flat-square&logo=docker&logoColor=white)
![Embedded](https://img.shields.io/badge/Embedded-HW%2FSW%20interaction-00979D?style=flat-square&logo=arduino&logoColor=white)

</div>

<img src="assets/divider.svg" width="100%" alt=""/>

## Let's connect

I'm looking for an **internship or junior role** where I can learn from experienced engineers, ship real features and grow in **backend/embedded/software** engineering/development.

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Message%20me-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mihajlo-stoiljkovic-aa1560355/)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/MIhajloS07)

**Build it. Test it. Containerize it. Learn from it.**
</div>
