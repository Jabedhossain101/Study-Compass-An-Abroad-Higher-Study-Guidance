# 🧭 Study Compass — Higher Education Discovery & Management Prototype

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/Markup-HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5)
[![CSS3](https://img.shields.io/badge/Styling-CSS3-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![Responsive](https://img.shields.io/badge/Layout-Responsive-success.svg)](#-responsive-breakpoints)

A modular, highly responsive, multi-view front-end prototype engineered with semantic HTML5 and a token-driven modern CSS3 architecture. **Study Compass** unifies global university search, application lifecycle monitoring, peer-to-peer discourse, and administrative controls into a single, high-performance static evaluation harness.

---

## 📌 Executive Overview

Study Compass streamlines the fragmented workflow international students navigate when planning higher education. Rather than distributing screens across static multi-page files, this repository consolidates 6 essential operational views into a unified environment toggled by a lightweight, top-anchored prototype control bar:

1. **Public Landing Page:** Strategic value proposition, institutional metrics, curated program tracks, and registration entry points.
2. **Student Dashboard:** Visual progress metrics, impending deadlines, document verification checklists, and algorithm-matched universities.
3. **University Search & Discovery:** Filterable catalog cards, acceptance rate projections, tuition metrics, and program comparison tags.
4. **Application Tracker:** Visual pipeline tracking admissions milestones (Drafting, Submission, Committee Review, Visa Processing).
5. **Community Forum:** Threaded peer-to-peer discussions, country-specific admissions channels, and mentor query sections.
6. **Admin Dashboard:** Platform-wide telemetry, institutional verification controls, user governance, and data analytics.

---


---

## 📂 Repository Layout

```text
study-compass/
│
├── index.html          # All 6 operational view containers and prototype nav engine
├── css/
│   └── style.css       # Token definitions (:root), layout systems, and responsive rules
└── README.md           # Engineering documentation and customization guidelines
🚀 Quick Start GuideThis project requires zero external build dependencies, package installations, or local servers to execute.1. Clone the RepositoryBashgit clone [https://github.com/your-username/study-compass.git](https://github.com/your-username/study-compass.git)
cd study-compass
2. Launch InterfaceStandard File Execution: Double-click index.html or open it directly in any modern desktop or mobile browser.VS Code Live Server (Recommended): Right-click index.html inside VS Code and select "Open with Live Server" to enable real-time style reloads upon saving.⚙️ Design Token System & CustomizationThe layout leverages CSS custom properties declared inside :root at the top of css/style.css. Adjusting these variables propagates site-wide changes instantly without altering individual component rules.CSS:root {
  /* Brand Palette */
  --primary: #1e3a8a;          /* Deep institutional navy */
  --primary-accent: #3b82f6;   /* Active selection highlight */
  --gold: #d97706;             /* Accents, metrics, and badges */
  --background: #f8fafc;       /* Canvas foundation */
  --surface: #ffffff;          /* Card and container background */


 
}
🧭 Multi-Screen Prototype ArchitectureAll platform screens exist within dedicated section elements:HTML<section class="screen" id="screen-[view-name]">
  <!-- Isolated View Content -->
</section>
The top prototype navigation bar (.proto-bar) binds to an inline showScreen(screenId) script that toggles the .active CSS display class.Migrating to Production / Single Page Apps (SPA)To convert this prototype into production-ready modular routes (e.g., React, Next.js, or Vue):Delete the <header class="proto-bar"> element from index.html.Delete the inline <script> at the bottom containing showScreen().Extract each <section class="screen"> container into its respective page or route component.📱 Responsive BreakpointsLayouts are fully adaptive, reflowing structures across standard viewports using discrete breakpoint boundaries:ViewportTarget Device ProfileReflow Mechanics> 980pxDesktop / UltrawideMulti-column grids, fixed vertical navigation sidebars≤ 980pxTabletsFlexible two-column layout, compact sidebar modes≤ 720pxMobile DevicesSidebars collapse to horizontal top navigation; cards stack vertically≤ 480pxSmall SmartphonesConsolidated padding, full-width inputs, streamlined utility headersAll media queries are logically grouped at the base of css/style.css.🗺️ Engineering Roadmap[ ] Extract UI elements into reusable components for Next.js and Tailwind CSS.[ ] Implement browser state persistence (localStorage) for the Application Tracker steps.[ ] Build automatic dark/light theme switching via @media (prefers-color-scheme: dark).[ ] Audit full keyboard focus traversal and screen-reader semantics (WCAG 2.1 AA compliance).
