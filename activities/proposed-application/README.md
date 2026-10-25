# Proposed Application: Linya

| | |
|---|---|
| **Student name** | Dela Vega, Winchester |
| **Section** | [Section] |
| **GitHub username** | AikawaKun9 |
| **Date submitted** | 2026-10-24 |

---

## 1. Problem Statement

### 1.1 Background

Students experience long waiting times when requesting important documents, such as the Transcript of Records (TOR), and processing other registrar-related transactions. The process can be inconvenient because students may spend hours waiting, standing in line, and going through multiple procedures before their requests are accommodated. This becomes more challenging during enrollment periods when the number of students seeking assistance increases. Although waiting areas with benches are available, students may still need to stand in line for their turn, raising concerns about the efficiency and organization of the queueing process.

### 1.2 Evidence from research

| Method | Who / where | Key finding |
|---|---|---|
| Observation | Registrar's office waiting area, while requesting my own TOR | Students waited for extended periods. Benches were available, but many still stood in line for their turn. |
| Interview | Student who had been told "you will be called when your turn comes" | Waited a long time without knowing how many people were ahead or how long it would take, so did not dare leave the area. |
| Interview | Student waiting for a registrar transaction | Expressed frustration: *"Unsay purpose sa mga lingkoranan kung magbarog raman diay japon ta para molinya"* (roughly, "What is the point of the chairs if we end up standing in line anyway?"). |
| Document review | Posted steps or forms for TOR and other registrar transactions | Several procedures are required, and nothing tells the student their queue position or expected waiting time. |

### 1.3 Point-of-view (POV) statement

**Students who visit the registrar in person** need **to know their place in the queue and roughly when they will be served** because **without that information they must stay near the counter and stand in line for hours, even when seats are available.**

### 1.4 "How might we…?" question

How might we let students see their queue position and estimated waiting time so they can wait comfortably, giving them assurance while helping registrar staff keep service orderly during busy periods?

### 1.5 Self-check

- [x] Names a real user group
- [x] States a need, not a feature
- [x] Rests on an insight from research
- [x] Is narrow enough to act on and open enough to allow different ideas

---

## 2. Target-User Profile

### 2.1 Primary persona

*Fictional persona combining my own experience and what I observed from other students.*

| | |
|---|---|
| **Name, age** | EDDIE, 21 |
| **Role / background** | Graduating student who needs his TOR for job applications and clearance processing |
| **Goals** | Get a TOR ticket without missing class; sit down on the hallway benches while waiting for his number |
| **Frustrations / pain points** | Standing in line for hours despite benches being available; uncertainty about when his turn is coming, no queue number, extra waiting when several procedures are needed |
| **Context of use** | Android smartphone, limited mobile data, weak campus Wi-Fi at times, crowded hallway outside the registrar; uses the app while waiting at the office or nearby, especially during busy enrollment weeks |
| **Accessibility considerations** | Low-end phone and slow connection need a very light page; large, high-contrast queue number; simple wording in English or Filipino; students without a phone or data still need a way to get a number |
| **Current workaround** | Arrives early, stands near the counter, asks staff or other students how long the wait is, and skips meals or classes to hold a place in line |

### 2.2 User groups and stakeholders

| Group | Who | Relationship to the app |
|---|---|---|
| Primary users | Students visiting the registrar in person | Join the queue, see their position and estimated wait, get notified when their turn is near |
| Secondary users | Registrar staff | Call the next number, record the transaction type, and mark each student served or skipped |
| Stakeholders | Registrar (head of office), school administration, IT/MIS office, the student body | Approves and maintains the system, sets service policies, is affected by changes in crowding and service time |

### 2.3 Organizational needs

- Orderly and fair service, especially during enrollment periods, with a clear record of who was served and when.
- Compliance with the Data Privacy Act of 2012 (RA 10173): the queue ticket collects only the minimum needed (transaction type and an optional student number or nickname), is visible only to the student and authorized staff, and old queue data is deleted or anonymized after a set period.
- Low cost and low maintenance, since the office has limited IT staff and budget.
- Support for existing policies, including priority service for PWDs, senior citizens, and pregnant students.
- Simple reports (peak hours, average service time per transaction) to help with staffing.
- **Possible conflict:** students want to join from anywhere, but the registrar wants people physically present so the line stays fair. *Handling:* students join by scanning a QR code at or near the office, and a staff-assisted option issues numbers to students without phones or data.

---

## 3. Proposed Application

### 3.1 Concept

Linya is a mobile-friendly web app that replaces standing in line with a virtual queue. EDDIE scans a QR code at the registrar's office, picks his transaction (for example, TOR request), and gets a queue number. His phone shows the number currently being served, how many people are ahead of him, and an estimated waiting time. When his turn is near, the app alerts him so he can sit, eat, or wait elsewhere nearby instead of standing in line. Registrar staff use a simple dashboard to call the next number and mark transactions as served or skipped.

### 3.2 Value proposition

For **students who must visit the registrar in person** and **need to know when they will be served**, ***Linya*** is a **virtual queue and wait-time tracker** that **shows each student's queue position and estimated wait, and alerts them when their turn is near**. Unlike **the current line-up-and-wait process**, it **removes the need to stand in line and the uncertainty about when they will be called**.

### 3.3 Value Proposition Canvas

| User side | Product side |
|---|---|
| **Jobs:** Submit a TOR request or other transaction and be served within a reasonable time | **Features:** QR join, queue number by transaction type, live "now serving" display, estimated wait time |
| **Pains:** Standing in line for hours, no idea of the wait, being told "you will be called" with no updates, multiple procedures | **Pain relievers:** Live position and estimate on the phone; turn-near alert; separate queue types so students join the correct line |
| **Gains:** Less waiting stress, ability to rest or step away, a predictable visit, fairer service | **Gain creators:** "Your turn is near" alert; fair first-come numbering; staff-assisted tickets so no one is left out |

### 3.4 Existing applications (from your application analysis)

| Existing app | What it does well | Where it falls short | How your app differs |
|---|---|---|---|
| Current manual queue (line-up and call by staff) | Needs no technology and is familiar | No queue number or wait estimate, students must stand and stay close, hard to see who came first | Gives every student a number, live position, and estimate |
| Existing online registrar transactions | Reduce visits for some transactions | Do not help students who still must appear in person, and give no information about the in-person wait | Complements the online process by organizing the in-person visit |

### 3.5 Technology choice

**Options considered:** Progressive Web App (PWA) with QR join, SMS-based queue notifications, physical ticket-dispenser kiosk (IoT)

**Weighted decision matrix** (scores 1–5, higher is better):

| Option | Solves the problem ×3 | Team skills ×2 | Cost ×2 | Privacy ×2 | Time to MVP ×1 | Total /50 |
|---|---|---|---|---|---|---|
| PWA with QR join | 5 | 5 | 5 | 4 | 4 | **47** |
| SMS-based queue notifications | 4 | 3 | 2 | 3 | 3 | 31 |
| Ticket-dispenser kiosk (IoT) | 3 | 2 | 1 | 5 | 1 | 26 |

**Chosen technology and rationale:** A PWA with QR-code join. It works in any phone browser with no installation, needs one codebase for students and staff, costs almost nothing on a free hosting tier, and directly addresses the core pain: not knowing the queue position or waiting time. SMS adds per-message costs, and a ticket kiosk needs hardware and still keeps students standing near the machine, so no emerging technology is needed.

---

## 4. Preliminary Requirements

### 4.1 Functional requirements (user stories)

| ID | User story | Priority (MoSCoW) |
|---|---|---|
| FR-01 | As a **student**, I want to **join the queue for my transaction type by scanning a QR code** so that **I get a queue number without standing in line**. | Must |
| FR-02 | As a **student**, I want to **see the number now being served, my position, and my estimated waiting time** so that **I know when I will be served**. | Must |
| FR-03 | As a **registrar staff member**, I want to **call the next number and mark a ticket served or skipped** so that **the queue moves in order and stays up to date**. | Must |
| FR-04 | As a **student**, I want to **get an alert when my turn is near** so that **I can wait comfortably and return in time**. | Should |
| FR-05 | As a **registrar staff member**, I want to **issue a ticket for a student without a phone or data** so that **no one is excluded from the queue**. | Should |
| FR-06 | As a **registrar head**, I want to **see reports of peak hours and average service time** so that **I can plan staffing**. | Could |
| FR-07 | As a **student**, I want to **join the queue remotely before arriving** so that **I can save even more time**. | Won't (this time) |
| FR-08 ★ |	Staff assign a window when calling; the student sees “Go to Window 3” |	Should |
| FR-09	| Staff filter the waiting list by service | Must |
| FR-10	| Student can leave the queue |	Should |

### 4.2 Non-functional requirements

| ID | Category | Requirement |
|---|---|---|
| NFR-01 | Performance | The "now serving" number and the student's position update within 5 seconds of staff pressing "call next", and the page loads within 3 seconds on a 3G connection. |
| NFR-02 | Usability | A first-time student can join the queue in under 1 minute (no more than 3 screens) without help, and the queue number is readable at arm's length. |
| NFR-03 | Security / privacy | Only the minimum data is collected, per RA 10173; students see only their own ticket; staff pages require login; queue data is deleted or anonymized after 30 days; all traffic uses HTTPS. |
| NFR-04 | Compatibility | Works on the latest versions of Chrome on Android and desktop, with a responsive layout from 360 px width. |

### 4.3 MoSCoW summary

- **Must have:** QR join with queue number by transaction type, live "now serving" and position with estimated wait, staff dashboard to call and update tickets
- **Should have:** "Turn is near" alert, staff-issued tickets for students without phones, priority handling for PWD, senior, and pregnant students
- **Could have:** Peak-hour and service-time reports for the registrar
- **Won't have (this time):** Remote joining before arrival, SMS notifications, integration with the student information system

---

## 5. Minimum Viable Product (MVP)

### 5.1 MVP features

1. QR-code join with a queue number for a chosen transaction type (for example, TOR request, submit requirements, enrollment-related)
2. Live student status page showing the number now being served, the student's position, and the estimated waiting time
3. Registrar staff dashboard to call the next number and mark tickets as served or skipped

### 5.2 Out of scope

- Remote joining from home, because it makes the queue less fair and needs location or time checks that are beyond one semester.
- SMS notifications, because of cost; the in-browser alert is used instead.
- Integration with the existing registrar or student information system, because it needs approvals from the school's IT office. The MVP keeps its own small database.
- Processing or approving the actual documents; Linya only organizes who is served and when.

### 5.3 Constraints and assumptions

- **Constraints:** One semester, solo developer, free hosting tier, no budget for SMS or hardware.
- **Assumptions:** Most students have a smartphone with a browser and some mobile data; the registrar agrees to a pilot and staff will press "call next" consistently; a printed QR code can be posted at the office; staff can issue tickets for students without phones.

### 5.4 Feasibility check (TELOS)

| Dimension | Key question | Your assessment |
|---|---|---|
| Technical | Can I build it with my skills and tools? | It would be possible to build a web app with a QR link, a live-updating status page, a staff dashboard, and a small database with guidance and tutorials, using the tools and skills i will aqcquire in this course. |
| Economic | Do the benefits justify the costs? | Maybe?. Costs are near zero (free tier, my own time), while benefits include less waiting for students and a more orderly office for staff. |
| Legal | Does it comply with law and policy (e.g., RA 10173)? | Feasible with care: minimal data, a short privacy notice at join, role-based access, and automatic deletion of old queue records. The hosting location and retention period should be confirmed with the school. |
| Operational | Will people use it, and can it be run? | Likely, since joining takes one QR scan. The main risk is inconsistent staff updates, which I would address with a one-button "call next" interface and a short orientation. Students without phones are served by staff-issued tickets. |
| Schedule | Can I deliver the MVP this semester? | Will Try. Three core features sharing one database are achievable within the semester, including a small on-site pilot test, if time is |

**Verdict:** Feasible if the scope stays limited to the three MVP features.

---

## Submission Checklist

- [x] File saved as `activities/proposed-application/README.md` in my CCC181 repository
- [x] All `[bracketed placeholders]` replaced and guidance blockquotes removed
- [x] Sections 1–5 complete
- [ ] Images (if any) placed in `images/` and displaying correctly on GitHub
