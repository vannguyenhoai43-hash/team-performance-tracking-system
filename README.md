# Team Performance Tracking System – Google Sheets

Read this in: **English** | [Tiếng Việt](README_VI.md)

## Project Overview

**Manual team tracking often fails when managers need to see execution status, KPI progress, and shop performance at the same time.** In practice, task updates, member KPIs, and shop results are often tracked separately, making recurring review slow, fragmented, and hard to act on.

This project builds a **Google Sheets-based performance tracking system** that connects **Task → Member → Shop** into one monitoring workflow. Instead of maintaining separate trackers, the system uses one input layer to update linked dashboards, KPI views, and forecast logic automatically.

Built for recurring team review, the system allows users to filter by **month, member, and shop**, while keeping one reporting structure across all views.

---

## System Scope

The system supports:

- **daily, weekly, and monthly task tracking**
- **individual and team KPI monitoring**
- **end-of-period KPI forecasting**
- **shop-level performance review**
- **dynamic filtering by month, member, and shop**

All data shown in the file is **simulated based on a real-world structure** and does not contain sensitive information.

---

## What I Built

- Built a **Google Sheets performance system** with one input layer and multiple linked dashboards
- Designed the tracking logic across **Task → Member → Shop**
- Set up automated KPI summaries, dashboard calculations, and forecast views using built-in formulas
- Built dashboard views for **team overview, task tracking, member KPI performance, KPI forecast, and shop-level performance**
- Added dynamic filtering so users can switch by **month, member, and shop** without changing formulas manually

---

## Analytical Logic

The system is built around three linked management questions:

### 1. Execution Control
At the **task level**, the system tracks progress, status, deadlines, priority, and workload so managers can quickly see what is delayed, overloaded, or off-track.

![task_tracker](images/task_tracker.png)

### 2. KPI Accountability
At the **member level**, the system compares KPI progress across PICs and the whole team, helping identify who is meeting targets, who is behind, and where the gap is coming from.

![pfm_PIC](images/pfm_pic_tracker.png)

### 3. Business Impact
At the **shop level**, the system connects team execution to business outcomes by showing whether assigned shops are performing well across key KPI areas such as **Orders, Ad GMV, Paid Ads, Livestream, and Video**.

![pfm_shop](images/pfm_shop.png)

This makes the file more than a task tracker: it becomes a **multi-layer monitoring system** that links execution visibility with business performance.

---

## Core Components

The system includes five main components:

- **Central Data Input**: one update layer for KPI and task data
- **Team & Task Monitoring**: progress, deadlines, workload, completion rate, and priority
- **Member KPI Performance**: KPI tracking by member, team, month, and quarter
- **KPI Forecast**: end-of-period achievement estimation based on run rate and recent trends
- **Shop-Level Performance**: KPI, channel, and sales views by selected shop and member

---

## Example Use Cases

- A member may stay on track in **task completion**, but still miss KPI because the assigned shop underperforms on **Paid Ads** or **Livestream**.
- A shop may show stable topline performance, while the forecast layer flags **end-of-period KPI risk** based on current run rate and remaining-day allocation.
- Team-level KPI gaps can be traced back to a specific combination of **execution delay, member performance, and shop performance** instead of being reviewed separately.

These use cases are what make the system more useful than a standard task tracker or static dashboard.

---

## Operational Impact

- Replaced fragmented tracking across **task, member, and shop** with one linked review structure
- Reduced dependence on manual follow-up by centralizing updates into a single input layer
- Improved visibility into **execution status, KPI gaps, and underperformance risk** within the same reporting flow
- Enabled recurring review through dynamic filtering by **month, member, and shop**, instead of rebuilding separate views

---

## Scope & Limitation

This project is designed for **performance tracking and operational monitoring**, not for advanced statistical forecasting or large-scale data processing.

Its strength lies in accessibility, transparency, and reusable review logic inside **Google Sheets**. The trade-off is that it is best suited for structured team tracking rather than high-volume data workflows.

---

## Deliverables

- **Google Sheets performance tracking system**
- **Team overview dashboard**
- **Task tracking dashboard**
- **Member KPI dashboard**
- **KPI forecast view**
- **Shop-level performance dashboard**

**FULL FILE** [HERE](https://docs.google.com/spreadsheets/d/1Yenltej4gWU9nJimhRiPbkxyMMUPeSArb9E1LzAAtMI/edit?gid=1802438500#gid=1802438500)
