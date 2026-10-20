---
homework: 02
week: 2
title: "Heuristic Evaluation of Amap (Gaode Maps) & The 'BusAssistant' Zero-Tap Redesign"
due: 2026-10-18
status: submitted
participants: [Self-Audit, Commuter Workflow]
tags: [homework, week/02, heuristic-evaluation, usability, amap, bus-assistant, calm-technology]
---

<p style="font-size: 0.8em; text-transform: uppercase; letter-spacing: 2px; opacity: 0.6; margin-bottom: 2px;">
HCI HOMEWORK 02 · HEURISTIC EVALUATION & SYSTEM REDESIGN
</p>

# HW02 — Heuristic Evaluation of Amap (高德地图) & The *BusAssistant* Zero-Tap Redesign

> **Course:** Stanford CS147 / HCI Core Curriculum ([[week-02]])  
> **Reference Theory:** [[nielsen-heuristics]], [[severity-rating]], [[Conceptual Model, System Image and Real usage|Conceptual Models]], [[constraints]], [[mapping]]  
> **Prototype Repository:** [github.com/SaidimM/BusAssistant](https://github.com/SaidimM/BusAssistant) (`/home/ubuntu/projects/BusAssistant`)

---

## 1. Tool Selection & Rationale

- **Target Application:** **Amap (Gaode Maps / 高德地图)** — China's dominant mobile navigation, transit, and location super-app.
- **Why This Tool (The "Free for a Reason" Super-App Paradox):**
  Most commuters and drivers rely on Amap for three foundational spatial tasks: **point-to-point routing**, **location checking**, and **real-time bus arrival status**. However, because Amap operates as a free consumer traffic funnel, it has evolved from a spatial navigation instrument into a bloated monetization platform packed with splash-screen shake-ads (`开屏摇一摇`), ride-hailing aggregators (`打车`), micro-loans (`借钱`), hotel group-buying, voice-pack stores, and AI mascots.
- **HCI Research Premise:**
  Evaluating Amap exposes a critical failure mode in modern software engineering: **what happens when a safety- and time-critical spatial tool (used while driving a car at 60 km/h or rushing to catch a morning bus) is hijacked by e-commerce and fintech dark patterns?** Furthermore, this audit directly motivates our functional Jetpack Compose redesign prototype, **[BusAssistant](https://github.com/SaidimM/BusAssistant)**—a single-purpose, `<500ms` zero-tap habitual transit dashboard.

---

## 2. Defined Realistic Tasks

We walked through two high-frequency real-world tasks twice (Pass 1: flow & context; Pass 2: screen-by-screen inspection against [[nielsen-heuristics|Nielsen's 10 Heuristics]]):

- **Task 1 (Habitual Morning Bus Commute — Multi-Line Corridor Check):**
  > *Scenario:* It is 8:15 AM on a weekday. You step out of your apartment walking toward your neighborhood bus stop. Three interchangeable bus lines (**Line 33, Line 12, and Line 84**) all serve the corridor to your transfer station. Your urgent goal is to find out **which of those candidate buses will arrive at your stop first right now** so you know whether to run (`⚡`) or walk calmly.
- **Task 2 (Safety-Critical In-Vehicle / Street Quick Route & Arrival Check):**
  > *Scenario:* Cold-launch the app while driving (or walking across a busy intersection) to verify live vehicle position along the route and receive a timely alert one stop before arrival.

```text
┌─────────────────────────────────────────────────────────────────────────┐
│      AMAP'S 7-STEP TORTURE PIPELINE (~10–15s Every Single Morning)      │
├─────────────────────────────────────────────────────────────────────────┤
│  [1. Cold Launch] ──► [2. 5s Splash Ad] ──► [3. Heavy 3D SDK Freeze]    │
│                                                       │                 │
│  [6. Defaults to Cab/Car!] ◄── [5. Type Dest] ◄── [4. Tap Search Bar]   │
│         │                                                               │
│         ▼                                                               │
│  [7. Switch to Bus Tab & Open Line 1... then Back... then Line 2...]    │
├─────────────────────────────────────────────────────────────────────────┤
│  VS. BUSASSISTANT REDESIGN (<500ms, 0 Taps):                            │
│  [1. Open App / Glance at Widget] ──► Side-by-side live countdown for   │
│      Line 33 (2 min), Line 12 (6 min), Line 84 (14 min) immediately!    │
└─────────────────────────────────────────────────────────────────────────┘
```

---

## 3. Heuristic Violations Table (8 Violations)

| # | Screen / State | Heuristic Violated | Description of Usability Problem & Cognitive/Motor Breakdown | Severity (0–4) & Multiplier Justification | Visual / Architectural Evidence |
|---|---|---|---|---|---|
| **1** | **Cold Launch Splash Screen (`开屏摇一摇广告`)** | **H3: User Control & Freedom**<br>*(+ H5: Error Prevention)* | **Splash-Screen Ad & Gyroscope Hijack:** Launching the app displays a 3–5s full-screen ad with a microscopic corner `"Skip (跳过)"` target and an ultra-sensitive gyroscope listener. While driving a car (or walking briskly), a slight vehicle vibration triggers the gyroscope and yanks the user out of the map app into Taobao/JD shopping pages—a documented cause of real-world driving distraction incidents. | **4 (Usability Catastrophe)**<br>• *Frequency:* High (every cold launch)<br>• *Impact:* **Severe safety hazard** while driving; total task derailment<br>• *Persistence:* High (cannot be avoided without third-party tools) | `SplashAdActivity` / Gyroscope intent redirect |
| **2** | **App Initialization & Map Canvas Bootstrap** | **H1: Visibility of System Status**<br>*(Response Latency Law)* | **~10-Second Startup Freeze:** Before the user can interact with the search bar, Amap initializes heavy 3D vector map engines, mini-program containers, promotional skins, and fintech SDKs. The main UI thread stutters or freezes for 5–10s, shattering Jakob Nielsen's **1.0s flow-of-thought limit** when the user only needs a 2 KB JSON bus ETA payload. | **3 (Major Usability Problem)**<br>• *Frequency:* High (daily cold launch)<br>• *Impact:* High (10s delay while walking to catch a bus can cause missing the bus)<br>• *Persistence:* High (hardware/SDK bloat) | Cold-start trace: `150–300 MB` footprint vs. `<500 ms` target |
| **3** | **Home Screen Search Bar (Morning Routine)** | **H7: Flexibility & Efficiency of Use**<br>*(+ H6: Recognition > Recall)* | **Zero Habitual Commute Memory (The 6-Tap Daily Tax):** Even though 90%+ of weekday launches at 8:15 AM near the user's apartment are for the exact same `Home → Work` commute, Amap forces the user through a novice 6-step search flow (Tap Search → Input/Select Destination → Plan Route → Select Tab → Pick Line) every single day instead of auto-surfacing the habitual departure board. | **3 (Major Usability Problem)**<br>• *Frequency:* Very High (twice daily every weekday)<br>• *Impact:* Moderate-High (repetitive motor/cognitive waste)<br>• *Persistence:* Permanent across sessions | Home Screen empty search prompt |
| **4** | **Route Planning Results — Mode Tabs** | **H2: Match Between System & Real World**<br>*(+ H3: User Control)* | **Commercial Ride-Hailing (`打车`) Default Bias:** After entering a destination, Amap frequently defaults to—or injects prominent cards for—**Ride-Hailing (Cab)** or **Driving** rather than honoring the commuter's consistent **Public Transit (公交/地铁)** habit. Because Amap earns commission on cab aggregation, its System Image prioritizes commercial conversion over the user's real-world mode preference. | **3 (Major Usability Problem)**<br>• *Frequency:* High (every route query)<br>• *Impact:* Moderate (forces extra modal tab-switching & causes mode slips)<br>• *Persistence:* High (commercial dark pattern) | Route Planner header tabs (`打车` vs. `公交地铁`) |
| **5** | **Public Transit Route Candidates List** | **H6: Recognition Rather Than Recall** | **Single-Line Silos Block Multi-Line Corridor Comparison:** When three bus lines (e.g., **Line 33, Line 12, Line 84**) serve the exact same stop-to-station corridor, Amap buries each option inside separate vertical route cards. To find out which bus arrives first, the user must tap into Card 1, memorize `"6 mins"`, navigate back, tap into Card 2, memorize `"2 mins"`, and compare in working memory. | **3 (Major Usability Problem)**<br>• *Frequency:* High (multi-line corridors are standard in cities)<br>• *Impact:* High (overloads 4-chunk working memory while walking)<br>• *Persistence:* High | Transit Route List accordion silos |
| **6** | **Home Viewport & Bottom Tab Bar (`我的` / Wallet)** | **H8: Aesthetic & Minimalist Design**<br>*(Tufte Data-Ink Ratio)* | **Fintech Mini-Loans & E-Commerce Pollution:** The bottom navigation bar, map overlays, and profile drawer are cluttered with completely unrelated financial modules (`借钱` consumer loans, credit cards, insurance), hotel coupons, and red notification badges (`●`). Every non-spatial pixel lowers the Data-Ink Ratio and competes with primary navigation signifiers. | **2 (Minor Usability Problem)**<br>• *Frequency:* Constant visual presence<br>• *Impact:* Low-Moderate (visual clutter & banner blindness, though bypassable)<br>• *Persistence:* High | Bottom navigation & `个人中心` fintech grid |
| **7** | **Live Bus Real-Time Map View** | **H1: Visibility of System Status**<br>*(Calm Feedforward)* | **Visual Polling Burden vs. Ambient Notification:** Once a user checks a bus line, monitoring its approach requires keeping the phone unlocked and repeatedly staring at a miniature bus icon moving along a 2D map. Lack of a one-tap ambient countdown widget or proactive *"1 stop away"* lock-screen alert forces continuous visual attention while walking in traffic. | **2 (Minor Usability Problem)**<br>• *Frequency:* Moderate-High<br>• *Impact:* Moderate (steals visual attention from physical street hazards)<br>• *Persistence:* Moderate | Real-Time Bus Map detail view |
| **8** | **Commute History & Account Settings** | **H3: User Control & Freedom**<br>*(Data Autonomy)* | **Cloud-Coupled Surveillance of Commute Trajectories:** Saving frequent destinations or enabling smart commute cards requires authenticating a cloud profile that uploads granular daily GPS trajectories to remote advertising servers, with no local-only SQLite option or transparent 1-tap habit wipe. | **2 (Minor Usability Problem)**<br>• *Frequency:* Continuous background telemetry<br>• *Impact:* Moderate (privacy erosion; reflective distrust)<br>• *Persistence:* High | Account Sync & Privacy Settings |

---

## 4. Top 3 Usability Problems & Concrete Redesign Proposals (*BusAssistant*)

Rather than stopping at paper wireframes, we engineered a functional Android prototype—**[BusAssistant](https://github.com/SaidimM/BusAssistant)** (Kotlin, Jetpack Compose, Material 3, Room SQLite)—that directly resolves the top three structural breakdowns identified above.

---

### Problem 1: The 7-Step Daily Re-Search & Single-Line Silos (Violations #3 & #5 — Severity 3)
- **Why Amap Fails:** Amap treats every app launch as an uncontextualized search query (`Where do you want to go today?`), and isolates interchangeable bus lines (`Line 33`, `Line 12`, `Line 84`) into separate sub-screens that violate **H6 (Recognition over Recall)** and **H7 (Efficiency of Use)**.
- **Concrete Redesign (*BusAssistant* Context Engine + Route Corridors):**
  1. **Zero-Tap Context Prediction (`HomeViewModel` + `BehaviorLogEntity`):** On launch, *BusAssistant* evaluates `Time of Day (8:15 AM)` × `Day of Week (Weekday)` × `Geofence Proximity (Near Apartment)` against its local Room SQLite frequency matrix and automatically displays the user's inferred commute corridor (**0 taps required**).
  2. **Interchangeable Route Corridor Card:** Instead of hiding lines in separate tabs, all candidate buses serving `Apartment ➔ Central Station` are aggregated into a single glanceable card, ranked dynamically by earliest arrival with semantic urgency badges (`tertiaryContainer` green for `⚡ RUN!`).

```text
┌─────────────────────────────────────────────────────────────────────────┐
│  8:15 AM (Weekday) · 📍 Near Apartment                     [↻]   [⚙️]  │
│  👉 Inferred Corridor: [Apartment Stop] ➔ [Central Station]             │
├─────────────────────────────────────────────────────────────────────────┤
│  🚌 Line 33   [██████████████░░░░]  1 stop away  · ~2 min   [⚡ RUN! ]  │
│  🚌 Line 12   [████████░░░░░░░░░░]  3 stops away · ~6 min   [ On Time]  │
│  🚌 Line 84   [███░░░░░░░░░░░░░░░]  7 stops away · ~14 min  [Queued  ]  │
├─────────────────────────────────────────────────────────────────────────┤
│  🚶 +10 min walk to Workplace after alighting at Central Station        │
└─────────────────────────────────────────────────────────────────────────┘
```

---

### Problem 2: Splash-Screen Gyro Ad Hijack & 10-Second Startup Freeze (Violations #1 & #2 — Severity 4 & 3)
- **Why Amap Fails:** Loading a 300 MB bundle of splash ads, gyroscope listeners, and 3D map textures when a user simply wants to know *"How many minutes until my bus?"* violates **H3 (User Control)**, **H5 (Error Prevention)**, and **H1 (Latency < 1.0s)**.
- **Concrete Redesign (*BusAssistant* 1D Linear Progress Canvas + Native AppWidget):**
  1. **Zero-Ad, Map-Free 1D Topology (`< 500 ms` Cold Start):** Commuters riding a familiar bus do not need a 2D geographic satellite map; they need a **1D topological progress bar** (like Harry Beck's iconic 1931 London Underground diagram). Replacing the 300 MB 3D map SDK with a custom 48 dp Jetpack Compose `Canvas` progress bar cuts APK size to `< 20 MB` and launch time to **under 500 milliseconds**.
  2. **Android Home Screen AppWidget & Ongoing Notification:** By surfacing live multi-line countdowns directly on the Android Home Screen widget and Lock Screen notification 15 minutes before the user's habitual departure window, the user gets instant feedforward without even launching the app.

---

### Problem 3: Commercial Mode Bias & Cloud Telemetry Lock-In (Violations #4, #6 & #8 — Severity 3 & 2)
- **Why Amap Fails:** Amap's System Image pushes high-commission ride-hailing (`打车`) tabs and mini-loans (`借钱`), while harvesting daily location trajectories to cloud servers.
- **Concrete Redesign (*BusAssistant* Local-First SQLite & Emergency Exit):**
  1. **100% On-Device Habit Learning (`Room SQLite`):** All commute logs (`BehaviorLogEntity`) and line configurations (`BusLineEntity`) remain strictly on-device with zero network analytics SDKs.
  2. **Explicit User Control (`H3`):** The `HabitInsightsScreen` makes the system's learned model completely transparent to the user, and `Settings -> Clear Learning Data` provides an immediate, deadbolt-confirmed (`AlertDialog`) 1-tap reset of all local commute memory.

---

## 5. Reflection: Where Amap's Conceptual Model Clashes with the User's Mental Model

In Don Norman's triad ([[Conceptual Model, System Image and Real usage]]), the user's **Mental Model** of a transit/navigation app is a **Calm Spatial Instrument**—like a wristwatch or a compass. When a commuter steps out the door at 8:15 AM or glances at a dashboard while driving, they are operating under severe environmental and cognitive constraints: their eyes and hands are needed in the physical world, so they expect the tool to answer a single spatial question (*"Where is my bus / turn?"*) in under **1.0 second** and then disappear into the periphery (Mark Weiser's **[[ubiquitous-computing|Calm Technology]]**).

Amap's **Design Model (and resulting System Image)**, however, is engineered around **Attention Extraction and Super-App Monetization**. Because the product is funded by advertising, ride-hailing commissions, and fintech lead generation, its System Image treats the user as an idle consumer with unlimited visual attention—intercepting cold launches with gyroscope-triggered splash ads, defaulting route queries to commercial cab tabs, and burying habitual bus ETAs six taps deep behind a 10-second 3D engine load. This fundamental clash between **User Need (minimum dwell time, zero taps)** and **Business Model (maximum dwell time, commercial conversion)** is why incremental UI tweaks inside a super-app cannot fix the problem—and why decoupling habitual transit into a dedicated, local-first calm instrument like **[BusAssistant](https://github.com/SaidimM/BusAssistant)** narrows both the [[gulf-of-execution]] (from 6 taps to 0 taps) and the [[gulf-of-evaluation]] (from 15 seconds of multi-screen recall to a 1-second glance).
