---
title: "Why Checking My Morning Bus Takes 10 Seconds and 7 Taps: A Heuristic Audit of Amap (And Why I Built BusAssistant)"
type: homework-report
status: ready
week: 2
source_notes:
  - "[[20-notes/homework/hw02-heuristic-evaluation/submission]]"
  - "[[20-notes/concepts/nielsen-heuristics]]"
  - "[[20-notes/concepts/severity-rating]]"
  - "[[20-notes/concepts/Conceptual Model, System Image and Real usage]]"
wp_category: HCI
tags: [post, week-02, heuristic-evaluation, nielsen, amap, bus-assistant, calm-technology]
---

# Why Checking My Morning Bus Takes 10 Seconds and 7 Taps: A Heuristic Audit of Amap (And Why I Built BusAssistant)

## Hook

Every weekday morning at 8:15 AM, I walk out of my apartment toward the same bus stop to catch one of three buses that head toward my transfer station. 

I only have one urgent question: **"Which of those three buses is arriving first right now, so I know whether to run or walk?"**

Answering that question requires about 2 kilobytes of data. Yet when I pull out my phone and open a mainstream super-app map like **Amap (高德地图)**, here is what actually happens:

1. **Cold Launch (`0.0s`):** A full-screen splash advertisement appears (`开屏摇一摇`). If I walk too briskly—or worse, if a driver hits a bump on the road—the phone's gyroscope triggers and yanks the screen straight into a shopping app.
2. **Engine Freeze (`3.0s – 8.0s`):** The app initializes a 300 MB bundle of 3D vector map textures, mini-programs, voice-pack stores, and consumer microloan banners (`借钱`).
3. **Manual Re-Search (`8.0s – 11.0s`):** Even though I have taken the exact same commute five days a week for months, the app greets me with a blank search bar. I have to tap Search, pick my destination, and wait for route calculation.
4. **Commercial Hijack (`11.0s – 13.0s`):** Instead of showing my bus, the route planner defaults to **Ride-Hailing (`打车`)**—because the platform takes a commission on cab rides.
5. **Single-Line Silos (`13.0s – 18.0s`):** When I finally switch to the Public Transit tab, the three bus lines that serve my stop (Lines 33, 12, and 84) are locked inside separate vertical cards. I have to tap into Card 1, memorize `"6 minutes"`, tap Back, tap into Card 2, and compare them in my head while crossing the street.

Why does a modern smartphone—a supercomputer in our pocket—make a daily 1-second question take 15 seconds and 7 taps?

To find out, I put Amap on the operating table for a formal **Heuristic Evaluation** using Jakob Nielsen's 10 Usability Heuristics, and then built a open-source Android alternative: **[BusAssistant](https://github.com/SaidimM/BusAssistant)**.

---

## The Diagnosis: When the System Image Fights the User's Mental Model

In *The Design of Everyday Things*, Don Norman explains that designers and users never speak directly; they communicate solely through the **System Image** (the interface, feedback, and behavior on screen).

```text
┌────────────────────────────────────────────────────────────────────────┐
│              THE SUPER-APP MENTAL MODEL CLASH                          │
├──────────────────────┬─────────────────────────────────────────────────┤
│ User's Mental Model  │ "I am walking in traffic or driving at 60 km/h. │
│ (Calm Instrument)    │  Give me my bus ETA in < 1.0s and disappear."   │
├──────────────────────┼─────────────────────────────────────────────────┤
│ Super-App System     │ "You are a monetizable eyeballs funnel! Here    │
│ Image (Attention Tax)│  are gyro ads, cab promos, and mini-loans."     │
└──────────────────────┴─────────────────────────────────────────────────┘
```

When I audited Amap across my morning commute workflow against **Nielsen's 10 Usability Heuristics** and scored each issue on his **0–4 Severity Scale** (`Frequency × Impact × Persistence`), three major structural failures stood out:

### 1. Violation of H3 (User Control & Freedom) & H5 (Error Prevention) — Severity 4 Catastrophe
A splash-screen ad with a microscopic `"Skip"` button and a hair-trigger gyroscope listener is not an accidental bug; it is a **hostile constraint**. When used inside a moving vehicle, hijacking a driver's navigation screen into an e-commerce store steals the locus of control during a safety-critical task. Regulators had to intervene after real-world driving incidents, yet "shake-to-jump" dark patterns keep creeping back.

### 2. Violation of H7 (Flexibility & Efficiency of Use) — Severity 3 Major
Nielsen's 7th Heuristic states that interfaces should provide **accelerators** for frequent, expert users. A tourist visiting a city for the first time needs a 2D map and a search bar. A daily commuter at 8:15 AM on a Monday does **not** need a search bar—they need their habitual departure board immediately. Forcing a daily commuter through a 6-tap novice search flow every morning is like forcing a homeowner to fill out a guest registration form every time they unlock their front door.

### 3. Violation of H6 (Recognition Rather Than Recall) — Severity 3 Major
Human working memory holds roughly 4 chunks of information and decays rapidly when distracted by street traffic. Burying interchangeable bus lines (Lines 33, 12, and 84) inside separate sub-screens forces the user to play a memory matching game instead of presenting all candidate arrivals side-by-side.

---

## The Redesign: How I Built *BusAssistant* for Zero-Tap Calm Commuting

Instead of complaining about super-app bloat, I asked an HCI engineering question: **What happens if we strip away 100% of the ads, fintech modules, cloud tracking, and even the 2D map itself—leaving only a pure, habit-driven commute instrument?**

I built **[BusAssistant](https://github.com/SaidimM/BusAssistant)** in Kotlin and Jetpack Compose (Material 3) around three HCI principles:

```text
+-------------------------------------------------------------------------+
|  8:15 AM (Weekday) • Location: Near Apartment                           |
|  👉 Inferred Commute: [Apartment] ➔ [Central Bus Station]               |
+-------------------------------------------------------------------------+
|  🚌 Line 33   | 🟢 Arriving in 2 min (1 stop away)   ⚡ RUN!           |
|  🚌 Line 12   | 🟡 Arriving in 6 min (3 stops away)                     |
|  🚌 Line 84   | ⚪ Arriving in 14 min (7 stops away)                    |
+-------------------------------------------------------------------------+
|  🚶 Walking to workplace: ~10 mins after arrival at Central Station     |
+-------------------------------------------------------------------------+
```

### 1. From 7 Taps to 0 Taps (On-Device Context Prediction)
Using a local Room SQLite database (`BehaviorLogEntity`), *BusAssistant* learns your commute patterns across **Time of Day × Day of Week × Geofence Proximity**. When you open the app at 8:15 AM near your apartment, it automatically predicts your `Home ➔ Station` commute and renders the live arrival board in **under 500 milliseconds**—zero typing, zero taps.

### 2. Interchangeable Route Corridors (Recognition Over Recall)
Instead of isolating bus lines in separate tabs, *BusAssistant* groups all buses that serve the same segment of your commute into a single **Route Corridor**. You see Line 33 (`2 min`), Line 12 (`6 min`), and Line 84 (`14 min`) ranked side-by-side on one screen, with a high-contrast semantic badge (`⚡ RUN!`) when your fastest option is approaching.

### 3. Map-Free 1D Topology & 100% Local Privacy
When you take the same bus every day, you already know where the streets are—you don't need a 300 MB 3D satellite map. By replacing the 2D map with a clean 1D linear progress canvas and an **Android Home Screen AppWidget**, the entire app weighs `< 20 MB`, launches in `< 0.5s`, and stores 100% of your commute history strictly on your device with a 1-tap `Clear Learning Data` emergency exit.

---

## Takeaways for Builders

1. **"Free" apps charge in cognitive load:** When a tool's business model relies on maximizing screen dwell time, it will inevitably sabotage workflows that require sub-second glanceability.
2. **Design for the 90% habit, not just the 10% exception:** If your users perform the exact same query at the exact same time every day, don't make them type it—predict it locally and surface it at launch.
3. **Calm Technology respects human attention:** As Mark Weiser wrote in 1991, the best technology whispers what you need in a 1-second glance and lets you get back to walking down the street.

*Check out the open-source prototype here: [github.com/SaidimM/BusAssistant](https://github.com/SaidimM/BusAssistant).*
