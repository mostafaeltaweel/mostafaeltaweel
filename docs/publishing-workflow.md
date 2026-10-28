# Sustainable Daily LinkedIn Publishing System
**Mostafa Eltaweel | Applied AI & Workflow Automation | Data Analytics & BI | ERP Systems**

A sustainable, repeatable engineering workflow connecting daily technical work to recruiter reach:
$$\text{Project Work} \longrightarrow \text{Documentation} \longrightarrow \text{Visual Asset} \longrightarrow \text{LinkedIn Post} \longrightarrow \text{GitHub Link} \longrightarrow \text{Tracker}$$

---

## 1. The Core Publishing Philosophy

1. **Proof Over Polishing:** Recruiters and engineering leads value real screenshots, actual error messages, and tangible architectural decisions far more than generic motivational quotes.
2. **Decompose, Don't Fabricate:** You do not need to build a brand new multi-tier project every 24 hours. A substantial project (such as your 119K-record Hotel Booking Analytics or n8n Multi-Agent CRM) yields 5 to 7 high-value, distinct technical posts.
3. **Always Ground in GitHub:** Every post must link to a real repository, documentation page, or live demonstration where readers can verify your work.

---

## 2. The Standard 8-Part Post Template

Use this structure for every technical post. It takes ~15 minutes to write when following this formula:

```markdown
[1. HOOK: 1-2 lines stating the commercial friction or counter-intuitive technical reality]
Most Power BI dashboards show what happened yesterday, but fail to explain why revenue leaked.

[2. CONTEXT: The specific business or operational scenario]
While analyzing 119,390 hotel booking transactions, we noticed overall cancellation rates hovering near 37%. But looking at aggregate averages was hiding the real financial culprit.

[3. THE IMPLEMENTATION: What you actually engineered]
Instead of building standard time charts, I segmented the data across lead-time bins (0–30d, 31–90d, 91–180d, 180d+) and crossed it with deposit policies. 

[4. TECH STACK: Clear, scannable tags]
🛠️ Stack: Power BI Desktop | DAX Measures | Python (Pandas) | Star-Schema Modeling

[5. REAL EVIDENCE: Key insight, finding, or result]
Key Finding: Bookings made >90 days in advance had a 42% cancellation probability, compared to only 14% for bookings made under 30 days. More critically, the "Non-Refund" deposit policy was almost exclusively utilized by high-risk agency segments rather than direct bookings.

[6. VISUAL: Real screenshot or architecture diagram]
(Attached: Unaltered screenshot of the lead-time variance matrix in Power BI)

[7. GITHUB REPOSITORY LINK]
Explore the full data model and DAX library on GitHub:
👉 https://github.com/mostafaeltaweel/hotel-booking-analytics

[8. CONVERSATIONAL CLOSING: Authentic discussion prompt]
How does your team handle cancellation forecasting in seasonal commercial datasets? Let's discuss in the comments.

#DataAnalytics #PowerBI #BusinessIntelligence #Python #DataModeling
```

---

## 3. The 5-Day Content Rotation Framework

How to extract 5 days of high-value content from **one** core project:

| Day | Post Focus | Content Angle | Required Visual Asset |
| :--- | :--- | :--- | :--- |
| **Day 1: The Executive Overview** | Business Problem & High-Level Architecture | Explain the commercial problem, who cares about it, and how your system is structured end-to-end. | High-level system architecture diagram or full dashboard overview. |
| **Day 2: Deep Technical Breakdown** | Code, DAX, or Pipeline Mechanics | Zoom into one specific calculation (e.g. DAX time-intelligence, SQL CTE with window functions, or n8n webhook routing). | Syntax-highlighted code snippet or specific workflow node. |
| **Day 3: Data Hygiene & Edge Cases** | Real-world dirty data & troubleshooting | Detail how you handled missing records, null values, invoice synchronization discrepancies, or API rate limits. | Before-and-after data sample or Power Query M-code step. |
| **Day 4: Key Insights & Business Findings** | Data Storytelling & Strategic Takeaways | Share the actual actionable recommendations derived from the data (e.g. deposit policy yield adjustments). | Highlighted KPI chart with callout annotations. |
| **Day 5: Lessons Learned & What's Next** | Engineering reflection & future roadmap | Honest discussion of model limitations, trade-offs, and what you would build next (e.g. adding real-time streaming). | Clean terminal output or GitHub project roadmap screenshot. |

---

## 4. Reusable Visual Post Specification

To ensure visual consistency that reinforces your personal brand:

### Canvas Specifications:
- **Dimensions:** `1200 x 1200 px` (Square 1:1, best for mobile feed) or `1200 x 627 px` (Landscape 1.91:1).
- **Format:** High-quality PNG.

### Layout Geometry:
```
┌─────────────────────────────────────────────────────────────┐
│ [TOP BRAND HEADER - 120px]                                  │
│  MOSTAFA ELTAWEEL · APPLIED AI & BI                         │
│  Project: Hotel Booking Cancellation Diagnostics            │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│ [BODY AREA - 940px]                                         │
│                                                             │
│  Unaltered, high-resolution screenshot of:                  │
│  • Power BI Matrix / Visual                                 │
│  • n8n Workflow Canvas                                      │
│  • SQL Server ERD Diagram                                   │
│  • Python / LangChain Execution Log                         │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│ [FOOTER BAR - 140px]                                        │
│  [Python 3.12] [Power BI PL-300] [Star-Schema]              │
│  github.com/mostafaeltaweel                                 │
└─────────────────────────────────────────────────────────────┘
```

### Color Rules:
- Header & Footer Background: Deep Navy `#101827`
- Accents & Highlights: Mint `#5EEAD4` and Teal `#0D9488`
- Border: 1px Muted Slate `#334155`
- Never use generic decorative 3D stock art when reporting technical results; real software UI builds 10x more recruiter trust.

---

## 5. Daily Publishing Progress Tracker Schema

Maintain a local log in `docs/publishing-log.md` with this markdown schema:

```markdown
# Publishing Log & Pipeline Tracker

| Date | Project Featured | Topic / Focus | Visual Asset | LinkedIn Post URL | GitHub Repo Linked | Feedback / Leads |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 2026-10-29 | Hotel Analytics | Day 1: Architecture & Lead Time Risk | `hotel-dashboard-full.png` | [Pending] | `mostafaeltaweel/hotel-booking-analytics` | - |
| 2026-10-30 | Hotel Analytics | Day 2: DAX Time-Intelligence Breakdown | `dax-code-snippet.png` | [Pending] | `mostafaeltaweel/hotel-booking-analytics` | - |
| 2026-10-31 | AI Lead System | Day 1: n8n + Groq Pipeline Overview | `n8n-workflow-full.png` | [Pending] | `mostafaeltaweel/ai-lead-qualification-agent` | - |
| 2026-11-01 | AI Lead System | Day 2: JSON Schema Validation & Prompts | `groq-schema-prompt.png` | [Pending] | `mostafaeltaweel/ai-lead-qualification-agent` | - |
| 2026-11-02 | Financial Fraud BI | Day 1: 1M Transaction Audit & Star-Schema | `fraud-star-schema.png` | [Pending] | `mostafaeltaweel/sales-financial-bi-audit` | - |
```
