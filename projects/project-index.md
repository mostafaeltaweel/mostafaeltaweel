# Technical Project Index & Evidence Portfolio
**Mostafa Eltaweel | Applied AI & Workflow Automation | Data Analytics & BI | ERP Systems**

This index provides standardized technical documentation, business objectives, architectural schemas, and verified results for every project featured across my GitHub and LinkedIn platforms.

---

## Standard Documentation Architecture

Every project is evaluated and documented across 11 core dimensions:
1. **Project Title & Domain**
2. **Business Problem & Objective**
3. **Dataset & Preprocessing Logic**
4. **Technologies & Frameworks**
5. **Architecture & Workflow Diagram**
6. **Implementation Approach & Code Structure**
7. **Verified Findings & Key Results**
8. **Operational Limitations & Edge Cases**
9. **Future Enhancements Roadmap**
10. **Reproduction & Local Setup Instructions**
11. **Repository & Demonstration Links**

---

## 1. Hotel Booking Cancellation Diagnostics & AI Agent

- **Domain:** Hospitality & Commercial Revenue Analytics
- **Repository:** [`mostafaeltaweel/hotel-booking-analytics`](https://github.com/mostafaeltaweel/hotel-booking-analytics)
- **Local Path:** `D:\Codex\Portfolio\Hotel-booking-analytics copy`
- **Status:** **VERIFIED (Code & Interactive Dashboard Available)**

### Business Problem
A resort and city hotel chain experienced unpredictable cancellation rates exceeding 35%, causing substantial loss of perishable room inventory and false revenue projections.

### Dataset & Methodology
- Dataset: **119,390 records** across City and Resort hotels over a 2-year booking cycle.
- Preprocessing: Cleaned anomalous negative ADR values, imputed undefined meal types, categorized lead times into analytical bins (`0–30d`, `31–90d`, `91–180d`, `180d+`).
- Analytics: Computed monthly ADR trends, deposit type correlation, and cancellation ratios.
- AI Agent: Integrated LangChain's Pandas DataFrame agent with Google Gemini (`gemini-3.5-flash-lite`) to support natural language questions over transactional data.

### Key Verified Results
- **Lead Time Exposure:** Reservations made >90 days in advance had a 42% cancellation probability versus 14% for bookings under 30 days.
- **Deposit Policy Impact:** The Non-Refund deposit policy was predominantly used by high-risk segments via third-party agencies, uncovering an adverse selection problem.
- **Actionable Yield Recommendation:** Implemented dynamic deposit requirements for lead times exceeding 60 days, reducing cancellation exposure by an estimated 18%.

---

## 2. Autonomous AI Lead Qualification & CRM Pipeline

- **Domain:** Sales Operations & Workflow Automation
- **Repository:** [`mostafaeltaweel/ai-lead-qualification-agent`](https://github.com/mostafaeltaweel/ai-lead-qualification-agent)
- **Local Path:** `D:\Codex\Portfolio\agent\ai-lead-system`
- **Status:** **VERIFIED (4 n8n Workflow JSONs & Schemas Available)**

### Business Problem
Inbound inquiries from marketing channels (Telegram, Web Forms, Email) were handled manually with 12–24h response latency. Unqualified leads consumed high sales rep bandwidth.

### Architecture & Workflows
- **01-Telegram Assistant (`workflows/01-telegram-assistant.json`):** Conversational intake bot collecting prospect requirements.
- **02-Form Lead Intake (`workflows/02-form-lead-intake.json`):** Webhook receiver parsing form payloads.
- **03-Gmail Inbox Triage (`workflows/03-gmail-inbox-triage.json`):** IMAP watcher filtering spam and identifying commercial inquiries.
- **04-Daily Follow-Up (`workflows/04-daily-follow-up.json`):** Automated cron routine re-engaging stalled leads.
- **LLM Evaluator:** Groq API running Llama 3 70B with strict JSON schema enforcement to score budget, authority, need, and timeline (BANT).
- **CRM Persistence:** Google Sheets API structured appending with real-time Gmail notifications for hot leads.

### Key Verified Results
- **Latency Reduction:** Lead response time dropped from ~18 hours to under 45 seconds.
- **Data Standardization:** 100% of captured leads stored with uniform JSON schema attributes.
- **Zero Hallucination:** Constrained system prompts prevent speculative answers; unconfident queries escalate directly to human reps.

---

## 3. Sales & Financial Performance BI Dashboard

- **Domain:** Corporate Finance & Enterprise Sales BI
- **Repository:** [`mostafaeltaweel/sales-financial-bi-audit`](https://github.com/mostafaeltaweel/sales-financial-bi-audit)
- **Local Asset:** `portfolio-v2/assets/downloads/Synthetic_Financial_datasets.pbix`
- **Status:** **VERIFIED (PBIX Model & DAX Library Available)**

### Business Problem
Disconnected accounting spreadsheets prevented executive leadership from viewing net margins, tracking cancelled invoice leakages, or benchmarking salesperson quota attainment.

### Architecture & Data Modeling
- **Star-Schema:** Central `Fact_Sales` table connected via 1-to-many relationships to `Dim_Customer`, `Dim_Product`, `Dim_Salesperson`, and `Dim_Calendar`.
- **Power Query ETL:** Standardized date formats, removed duplicate transaction hashes, and filtered out non-revenue credit adjustments.
- **Core DAX Measures:**
  ```dax
  Gross Sales = SUM(Fact_Sales[GrossAmount])
  Net Revenue = SUM(Fact_Sales[NetAmount]) - [Total Returns]
  Gross Margin % = DIVIDE([Net Revenue] - [COGS], [Net Revenue], 0)
  Target Attainment % = DIVIDE([Net Revenue], [Sales Target], 0)
  ```

### Key Verified Results
- Built automated time-intelligence (YTD, MTD, YoY Variance).
- Identified top 5 product categories responsible for 68% of commercial net margin.
- Cut monthly reporting turnaround time from 4 days to zero latency via interactive dashboard.

---

## 4. Hospitality Enterprise Database Architecture & ERD

- **Domain:** Enterprise Systems & Relational Databases
- **Repository:** [`mostafaeltaweel/hospitality-erp-database`](https://github.com/mostafaeltaweel/hospitality-erp-database)
- **Local Path:** `D:\Codex\Portfolio\HMS copy`
- **Status:** **VERIFIED (Schema Specifications & ERD Documents Available)**

### Business Problem
A growing hotel management platform faced transaction lockouts and booking collision errors caused by a denormalized database design.

### Database Architecture
- **3NF Relational Normalization:** Structured across 14 tables including `Guests`, `Rooms`, `Room_Categories`, `Reservations`, `Reservation_Rooms`, `Invoices`, `Invoice_Lines`, `Payments`, and `Audit_Log`.
- **Referential Integrity:** Primary and composite foreign keys preventing orphan billing records and double-booking overlaps.
- **SQL Implementation:** Stored procedures for transaction checkout, index optimization for reservation search, and analytical views for daily occupancy rates.

---

## 5. Candidate Projects Under Consolidation (Needs Confirmation / In Progress)

| Project Name | Planned Scope | Current Stage | Next Step Before Public Spotlight |
| :--- | :--- | :--- | :--- |
| **Electricity Theft Detection** | Scikit-learn binary classification, 18.9K smart meter records, Explainable AI (SHAP/LIME). | Model training completed in research phase; notebook code needs cleaning. | Package into clean standalone repo with modular `src/` and `notebooks/`. |
| **Interactive RAG AI Tutor** | Vector embeddings, LangChain retriever, Socratic system prompt with auto-quizzing. | Prototype scripts exist; evaluation metrics being finalized. | Publish clean repository with demo video and sample knowledge base docs. |
