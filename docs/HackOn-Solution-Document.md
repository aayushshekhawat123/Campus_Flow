# HackOn with Amazon | Solution Document

## A Universe of Opportunity
### 48-Hour Hackathon | Solution Document

---

| | |
|---|---|
| **Team Name** | The Hackers |
| **Hackathon Theme** | AI + Cloud + Intelligent Productivity |
| **Project** | CampusFlow — AI-Powered Academic Operating System for Students |
| **Date** | June 2026 |

---

## Team Members

| Name | College / University | Role | Email |
|------|---------------------|------|-------|
| [Member 1] | [College] | Full-Stack Developer | [Email] |
| [Member 2] | [College] | Full-Stack Developer | [Email] |

---

## 1. Problem Statement & Relevance

### The Problem

Indian colleges operate on a fragmented stack of disconnected tools: attendance is tracked in manual registers or legacy ERPs, notices are broadcast via WhatsApp groups that students mute, deadlines live in scattered PDFs, and study planning is left entirely to the student. The result is a systemic failure in academic communication that costs students semesters, not just grades.

**Quantified impact:**
- 67% of Indian students report missing at least one critical deadline per semester due to information fragmentation (NASSCOM Student Survey, 2024)
- Students interact with 5-7 disconnected platforms daily (college portal, WhatsApp, email, LMS, notice boards, Telegram)
- 38% of students fall below 75% attendance thresholds without realizing it until the registrar blocks their exam eligibility
- Faculty spend 4+ hours per week on administrative communication that could be automated

No existing system combines attendance intelligence, AI-assisted planning, proactive notifications, and productivity tooling into a single student-facing platform.

### Why It Matters

**260 million** students are enrolled in higher education in India alone (AISHE 2023-24). Every one of them faces the same fragmented information problem. Globally, the EdTech market is projected at $404B by 2025, yet productivity-layer solutions for campus operations remain a whitespace.

The cost of inaction:
- Students repeat semesters due to attendance shortfalls they could have prevented
- Placement opportunities are missed because notices go unread
- Academic stress and burnout escalate when students lack visibility into their own workload

CampusFlow addresses a problem that affects **every enrolled student at every institution** — this is not a niche vertical but a horizontal platform opportunity.

### Theme Alignment

CampusFlow sits precisely at the intersection of the three hackathon pillars:

| Pillar | CampusFlow Implementation |
|--------|--------------------------|
| **AI** | AWS Bedrock powers 7 distinct AI features: notice summarization, study plan generation, academic chatbot, Guardian AI risk analysis, smart scheduling, routine intelligence, and burnout detection |
| **Cloud** | Cloud-native architecture across 5 AWS services (Bedrock, SNS, Lambda, S3, EC2) enabling serverless event processing, managed AI inference, and scalable storage |
| **Intelligent Productivity** | Focus Zone (deep work sessions), Smart Scheduler (conflict resolution), Life Companion (wellness + expense + habit tracking), and proactive deadline automation |

The unique angle: We don't just use AI to answer questions — we use it to **proactively prevent academic failure** before students even know they're at risk.

### What Makes This Novel

**Existing solutions fail at the integration layer:**

| Platform | What It Does | What It Misses |
|----------|-------------|----------------|
| Moodle / Google Classroom | Course content delivery | No attendance intelligence, no proactive alerts, no AI planning |
| College ERP (SAP, Oracle) | Administrative record-keeping | Student-hostile UX, zero productivity features, no AI layer |
| Notion / Google Calendar | Personal organization | No institutional integration, no automated notice ingestion, no Guardian AI |
| StudySmarter / Forest | Single-feature productivity | Isolated tools with no campus context |

**CampusFlow's insight:** The problem isn't that individual tools don't exist — it's that no system combines institutional data (notices, attendance, events) with AI intelligence (risk detection, schedule optimization) and student productivity (focus sessions, habit tracking) into a unified experience that actually runs on the student's behalf.

We built the first **Academic Operating System** — a platform that doesn't just display data, but acts on it autonomously through scheduled cron jobs, event-driven notifications, and AI-powered planning.

---

## 2. Customer & Solution

### Target Customer

**Primary: The Overloaded Engineering Student (18-24)**

Arjun is a second-year B.Tech CS student managing 6 courses, a club position, exam prep, and a part-time internship. He checks 5 different platforms daily and still misses a library due date that delays his semester registration. He needs one system that watches his academic life and intervenes before things go wrong.

**Secondary: The College Administrator**

Dr. Mehta is an Academic Registrar who sends notices via email that go unread, posts PDFs to a portal nobody visits, and fields complaints from students claiming they "weren't informed." She needs a broadcast channel with proof of delivery and intelligent summarization.

### How We Solve It

CampusFlow delivers a unified intelligent layer across seven critical student workflows:

| # | Feature | Benefit |
|---|---------|---------|
| 1 | **Attendance Intelligence** | Real-time tracking with shortage prediction. Students see projected attendance for each subject and receive alerts before they drop below exam-eligibility thresholds. |
| 2 | **AI Notice Intelligence** | Every uploaded notice is auto-summarized by AWS Bedrock with extracted deadlines, urgency classification, and action items. Students read a 2-line summary instead of a 5-page PDF. |
| 3 | **Proactive Notification Cascade** | 72h → 24h → 1h automated reminders for exams and assignments. Push notifications via Service Worker deliver alerts even when the browser is closed. |
| 4 | **AI Study Planner** | Generates time-blocked study schedules respecting exam dates, sleep hours, meal times, and existing events. Powered by Bedrock Nova Lite. |
| 5 | **Guardian AI** | Weekly risk analysis that identifies unpreparedness, attendance drops, and workload overload before they become emergencies. |
| 6 | **Smart Scheduler** | Detects timeline conflicts, suggests optimal study blocks, tracks attendance recovery requirements, and balances workload across the week. |
| 7 | **Focus Zone + Life Companion** | Pomodoro-style deep work sessions with streak tracking, plus wellness logging, expense management, habit tracking, and burnout monitoring — all with AI-generated recommendations. |

### User Workflow

```
┌──────────────────────────────────────────────────────────────────┐
│                        STUDENT JOURNEY                             │
├──────────────────────────────────────────────────────────────────┤
│                                                                    │
│  Login ──▶ Dashboard ──▶ See Today's Schedule + AI Insights       │
│                │                                                   │
│                ├──▶ Notice Center (AI Summaries + Urgency Badges) │
│                ├──▶ Notification Center (Severity-Ranked Alerts)  │
│                ├──▶ Calendar (Conflict Detection)                  │
│                ├──▶ Study Plan (AI-Generated Time Blocks)         │
│                ├──▶ Guardian AI (Risk Report)                     │
│                ├──▶ Smart Scheduler (Optimization)                │
│                ├──▶ Focus Zone (Deep Work Sessions)               │
│                └──▶ Life Companion (Wellness + Expenses + Habits) │
│                                                                    │
├──────────────────────────────────────────────────────────────────┤
│                      ADMINISTRATOR JOURNEY                         │
├──────────────────────────────────────────────────────────────────┤
│                                                                    │
│  Login ──▶ Upload Notice (PDF/Image/Text)                         │
│                │                                                   │
│                ├──▶ AI Auto-Processes (Summary, Urgency, Dates)   │
│                ├──▶ Students See Instantly (Push Notifications)   │
│                └──▶ Manage History (View, Sort, Delete)           │
│                                                                    │
└──────────────────────────────────────────────────────────────────┘
```

### Working Prototype

**CampusFlow is fully deployed and operational on AWS EC2.**

| Screen | Description |
|--------|-------------|
| **Login** | JWT-authenticated entry with role-based routing (student → dashboard, admin → upload portal) |
| **Student Dashboard** | Unified view: today's events, upcoming deadlines, Guardian AI summary, quick actions |
| **Notice Center** | AI-summarized notices with urgency badges (critical/high/medium/low), category tags, and extracted dates |
| **Smart Scheduler** | Today's chronological plan, weekly workload meters, conflict warnings, attendance recovery tracking |
| **Life Companion** | Score cards for routine, wellness, budget, habits, and burnout — each with AI-powered recommendations |
| **Admin Portal** | Notice upload with drag-and-drop, previous notices management with sort and delete |

**🚀 Live Demo:** http://54.159.36.107:4000/login

| Credential | Email | Password |
|-----------|-------|----------|
| Student | student@campusflow.com | student123 |
| Administrator | admin@campusflow.com | admin123 |

---

## 3. Tech Architecture & Scaling

### Architecture Overview

```
┌─────────────────────────────────────────────────────────────────┐
│                    CLIENT LAYER                                    │
│  React 19 + Vite 8 + Tailwind CSS + Service Worker (Push)       │
└────────────────────────────┬────────────────────────────────────┘
                             │ HTTPS (REST API)
                             ▼
┌─────────────────────────────────────────────────────────────────┐
│                    APPLICATION LAYER (EC2)                        │
│  Express.js 5 + JWT Auth + Role Guards + Joi Validation         │
│                                                                   │
│  ┌─────────────┐  ┌──────────────┐  ┌────────────────────┐     │
│  │ 14 Route    │  │ Cron         │  │ AI Service Layer   │     │
│  │ Modules     │  │ Schedulers   │  │ (7 Bedrock calls)  │     │
│  └─────────────┘  └──────┬───────┘  └────────┬───────────┘     │
└────────────────────────────┼──────────────────┼─────────────────┘
                             │                  │
              ┌──────────────┼──────────────────┼────────────┐
              │              │                  │            │
              ▼              ▼                  ▼            ▼
    ┌──────────────┐  ┌───────────┐  ┌──────────────┐  ┌───────┐
    │ MongoDB Atlas│  │ AWS SNS   │  │ AWS Bedrock  │  │AWS S3 │
    │ 18 Collections│ │ Event Bus │  │ Nova Lite v1 │  │Notice │
    │              │  └─────┬─────┘  └──────────────┘  │Files  │
    └──────────────┘        │                           └───────┘
                            ▼
                    ┌──────────────┐
                    │ AWS Lambda   │
                    │ Push Consumer│
                    │ (Web Push)   │
                    └──────────────┘
```

### Tech Stack

| Layer | Technology | Why Chosen |
|-------|-----------|------------|
| **Frontend** | React 19 + Vite 8 | Latest concurrent rendering, sub-second HMR, optimal bundle splitting (18 lazy-loaded routes) |
| **Styling** | Tailwind CSS 3.4 | Utility-first for rapid prototyping; dark/light theme via CSS class toggling without runtime cost |
| **Backend** | Express.js 5 (Node.js 20) | Async/await native, ESM modules, mature ecosystem, sub-5ms route handling |
| **Database** | MongoDB Atlas (Mongoose 9) | Schema flexibility for 18 evolving collections; compound indexes for complex sorting; Atlas auto-scaling |
| **AI/ML** | AWS Bedrock (Nova Lite v1) | Managed inference — zero model hosting. Single API powers 7 features: summarization, planning, chat, risk analysis, scheduling, routines, burnout |
| **File Storage** | AWS S3 | Infinite capacity, pre-signed URLs for secure time-limited reads, $0.023/GB/month |
| **Event Bus** | AWS SNS | Decoupled pub/sub architecture. Server publishes; Lambda consumes. Never blocks the request path. |
| **Automation** | AWS Lambda | Serverless push delivery — scales to zero when idle, handles notification bursts without provisioning |
| **Deployment** | AWS EC2 | Full control for hackathon demo; App Runner / ECS path available for production auto-scaling |
| **Auth** | JWT + bcrypt (cost 12) | Stateless authentication with 8h expiry; no session store required for horizontal scaling |
| **Scheduling** | node-cron | Minute-resolution deadline scanning (24h, 1h windows) + 15-min 72h deadline sweep |
| **Push** | Web Push (VAPID) | Browser notifications without app install; works with tab closed via Service Worker |

### Key Algorithms & Complexity

| Algorithm | Implementation | Complexity |
|-----------|---------------|------------|
| **Deadline Cascade Scheduling** | Cron job scans events in [now+24h ± 1min] and [now+1h ± 1min] windows. Uses `Reminder` deduplication with compound index on `(eventId, triggerType)`. | O(n) per sweep where n = active events in window |
| **Notice Intelligence Pipeline** | Async pipeline: upload → S3 store → Bedrock invoke (extract title, summary, urgency, deadlines, actions, category) → MongoDB update. Retries 3x with 5s backoff. | O(1) per notice; Bedrock inference ~2-5s |
| **Attendance Prediction** | Projects future attendance % based on `logs.length`, calculates classes needed to reach 75% threshold: `needed = ceil((0.75 * (conducted + remaining) - attended))` | O(s) where s = subjects |
| **Smart Schedule Optimization** | Conflict detection via interval overlap check. Study block allocation uses greedy bin-packing into free time slots respecting sleep, meal, and travel buffers. | O(e log e) where e = events (sort + sweep) |
| **Guardian AI Risk Scoring** | Aggregates: events with no study coverage, exams within 48h without sessions, overlapping critical events. Passes structured data to Bedrock for natural-language risk report. | O(e + s) aggregate; O(1) Bedrock call |
| **Notification Deduplication** | Compound query on `(userId, alertType, deadline)` before insert prevents duplicate alerts across scheduler reruns. | O(1) indexed lookup per notification |
| **Budget Intelligence** | Real-time percentage calculation with daily spending rate projection: `predicted = dailyRate * remainingDays`. Triggers alerts at 80% and 100% thresholds. | O(t) where t = transactions in period |

### Scaling Strategy

| Dimension | Current (Hackathon) | Scale Path (100K Users) |
|-----------|---------------------|------------------------|
| **Compute** | Single EC2 instance | App Runner auto-scaling (1→20 instances) behind ALB |
| **Database** | MongoDB Atlas M0 (free) | Atlas M30+ with read replicas; shard on `userId` |
| **AI Inference** | Direct Bedrock calls | Queue-based async processing via SQS → Lambda → Bedrock |
| **File Storage** | S3 single bucket | CloudFront CDN for notice file delivery |
| **Notifications** | SNS → single Lambda | SNS → Lambda concurrency scaling (1000 concurrent) |
| **Real-Time** | 15s polling for unread count | WebSocket via API Gateway for instant delivery |
| **Caching** | None | Redis/ElastiCache for session data and hot queries |

**Key architectural decisions enabling scale:**
- Stateless backend (JWT, no server-side sessions) → horizontal scaling is trivial
- Event-driven notifications (SNS → Lambda) → push delivery is decoupled from API response time
- Bedrock managed inference → no GPU provisioning, no model versioning, no cold starts
- MongoDB document model → schema evolution without migrations, flexible per-feature collections

---

## 4. Future Vision

### Where This Goes

CampusFlow today solves the **student productivity problem** at a single campus. In 12 months, it becomes the **Academic Operating System** — the default intelligent layer between institutions and students, deployable across thousands of colleges with multi-tenant architecture.

In 36 months, the same AI + productivity + notification stack expands beyond education into **corporate learning, workforce onboarding, and professional skill development** — anywhere humans need to manage schedules, track progress, and receive intelligent guidance.

### Roadmap

| Horizon | Milestone | Impact |
|---------|-----------|--------|
| **0-3 months** | Multi-college deployment (5 pilot institutions), mobile PWA, WebSocket real-time updates | 5,000 active students |
| **3-6 months** | Multi-tenant SaaS architecture, LMS integrations (Moodle, Canvas), parent notification portal, analytics dashboard for faculty | 50,000 students across 20 institutions |
| **6-12 months** | Predictive grade modeling, placement readiness scoring, cross-campus collaboration, React Native mobile app, institutional API marketplace | 200,000 students, B2B revenue model active |

### Multi-Segment Expansion

| Phase | Segment | Adaptation |
|-------|---------|-----------|
| **Year 1** | Higher Education (India) | Current product — campus-focused academic OS |
| **Year 2** | K-12 Education | Parent-facing dashboard, simplified UX, guardian notifications |
| **Year 2** | Corporate L&D | Training deadline tracking, certification management, skill gap analysis |
| **Year 3** | Government Skill Missions | Integration with Skill India, NSDC — tracking lakhs of trainees across programs |
| **Year 3** | Healthcare Education | Clinical rotation scheduling, competency tracking, board exam prep |

### Value Impact

| Metric | Projected Impact |
|--------|-----------------|
| **Deadline compliance** | 40% reduction in missed submissions (from proactive cascade reminders) |
| **Attendance recovery** | 25% fewer students falling below 75% threshold (from predictive alerts) |
| **Study time optimization** | 3+ hours/week saved per student on manual scheduling |
| **Notice engagement** | 5x improvement in notice read-rates vs. email/WhatsApp broadcast |
| **Administrative load** | 60% reduction in "I wasn't informed" escalations to registrar |
| **Student wellness** | Measurable burnout risk reduction through early AI intervention |

At 200,000 students, CampusFlow saves **600,000 student-hours per week** in scheduling overhead alone — equivalent to 75,000 working days returned to academic pursuits every semester.

---

## Links

| Resource | URL |
|----------|-----|
| **Live Application** | http://54.159.36.107:4000/login |
| **GitHub Repository** | https://github.com/aayushshekhawat123/Campus_Flow |
| **Demo Video** | [Insert Demo Video Link] |

---

*Confidential — For Jury Evaluation Only*
