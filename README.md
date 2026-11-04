<div align="center">

# Hamid Rizvi

**Forward Deployed Engineer · AI Engineer · NYU '26 · NYC**

*AI reads. Code decides. Humans confirm.*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-hamid--rizvi-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/hamid-rizvi)
[![Portfolio](https://img.shields.io/badge/Portfolio-hamidrizvi.vercel.app-FF4A1C?style=flat-square&logo=vercel&logoColor=white)](https://hamidrizvi.vercel.app)
[![Email](https://img.shields.io/badge/Email-hamidrizvi%40stern.nyu.edu-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:hamidrizvi@stern.nyu.edu)

</div>

---

## How I build

I build AI systems for work where a wrong answer costs something: legal deadlines, tax filings, support tickets that touch billing or security.

My rule is simple. **Model output is untrusted input.**

- **The LLM reads, classifies and drafts.** That's where it's genuinely better than code.
- **Deterministic code owns anything consequential.** Deadlines, money, routing decisions. Versioned, testable, auditable.
- **A human confirms before anything becomes real.** AI proposals stay inert until someone approves them.
- **Nothing is "done" until it's measured.** Evals, real workloads, real billing data. I publish the results I didn't want too.

---

## What I've shipped

### 🎯 Claude API Support Triage Agent
> *Auto-resolve what the docs can answer. Escalate what a human should own.*

A RAG agent built on a **raw tool calling loop with 5 tools and no framework**, so every step is visible and testable. It classifies developer support tickets, retrieves grounded context, drafts a citable answer and routes the ticket. **A rules-based routing engine, not the model, makes the final call.** Billing, security, sales and bug tickets always go to a human, whatever the model's confidence. Every tool call is logged as an audit trail.

**What I verified, not assumed**
- Ran a **7-point external review** and checked every finding against the live system. 3 of 7 were worse than reported, including **Row-Level Security disabled on all 6 tables**. Fixed it, confirmed the fix live and documented it.
- Added test coverage around the logic that had caused two earlier bugs.
- Ran a **free vs. paid model test on the same 40 tickets**. Incomplete runs dropped from **50% to 7.5% for $0.25**, verified against billing data. Both results are published.

`TypeScript` `Next.js` `Supabase` `pgvector` `OpenRouter` `Tool Calling` `RAG`

[![Live Demo](https://img.shields.io/badge/Live-agenttriage.vercel.app-000000?style=flat-square&logo=vercel&logoColor=white)](https://agenttriage.vercel.app)
[![Case Study](https://img.shields.io/badge/Case_Study-Read_the_writeup-FF4A1C?style=flat-square)](https://hamidrizvi.vercel.app/projects/triage/narrative)
[![Repo](https://img.shields.io/badge/GitHub-claude--support--triage--agent-181717?style=flat-square&logo=github)](https://github.com/hamidrizvi4/claude-support-triage-agent)

---

### 🏢 ResidenceOS · NYC Property Compliance Platform
> *The AI never computes a legally binding date.*

A compliance platform for NYC property managers. Before writing the deadline logic I checked the city's own source and found that **Local Law 152 deadlines follow DOB's rotating community district schedule, not "date + 4 years."** The obvious implementation would have produced the wrong legal deadline for **two of three seeded buildings**.

- Deadline logic is **deterministic, versioned config in TypeScript** that **fails closed** when district data is missing.
- AI extraction produces **schema-validated, inert proposals** that wait for human review.
- Wrote a **threat model** that treats LLM output as untrusted input, covering prompt injection signals (surfaced, never silently dropped), Stripe webhook signature verification, replay idempotency and secret redaction.

`TypeScript` `Next.js` `Supabase` `Stripe` `LLM Extraction` `Threat Modeling`

[![Live](https://img.shields.io/badge/Live-residencesystem.vercel.app-000000?style=flat-square&logo=vercel&logoColor=white)](https://residencesystem.vercel.app)

---

### 🧾 QuadTax · AI Tax Compliance Engine
> *The model reads the forms. It never touches the math.*

Tax prep for nonresident alien filers. An OCR and structured outputs pipeline parses **W-2, 1042-S and I-94** forms, and every calculation runs in deterministic logic, so the model can't invent a number. Generates **IRS Form 843** to help recover FICA taxes that were wrongly withheld. Cut filing time from **35 minutes to under 10**.

`Python` `FastAPI` `Next.js` `OpenAI Structured Outputs` `Pydantic` `Tesseract` `pdfplumber`

[![Repo](https://img.shields.io/badge/GitHub-QuadTax-181717?style=flat-square&logo=github)](https://github.com/hamidrizvi4/QuadTax)

---

### Earlier builds

| Project | What it does | Stack |
|---|---|---|
| **[Squirrel AI](https://github.com/hamidrizvi4/Squirrel-AI)** | Ask any public GitHub repo questions in plain English. Extracts code structure across 10+ languages and answers with source file references. | `React` `FastAPI` `OpenAI` `RAG` |
| **[Purchase Analytics AI](https://github.com/hamidrizvi4/Purchase-Analytics-AI)** · [demo](https://analyticsai.streamlit.app/) | Turned a 4 hour reporting task into a 5 minute dashboard. 110K+ transactions, RFM segmentation across 96K+ customers, churn model at AUC 0.82. | `Python` `Pandas` `Streamlit` `Gemini` |

---

## Production experience

**LexTrack AI** · AI/ML Product Engineering Intern · Feb – May 2026
- Designed **LLM-as-judge evals** and a deterministic testing framework to benchmark **GPT-4, Claude and Gemini**. The results chose the production model.
- Built and tuned production **RAG** systems with a **3-layer fallback architecture**, cutting inference cost **40%** at **sub-2s p95 latency** and **99.5% uptime**.

**LexTrack AI** · Capstone Project, Lead AI Developer · Sep – Dec 2025
- Ran **25+ customer interviews**, then led 3 engineers and 1 designer to **50+ active users in 8 weeks** at **85% weekly retention**.
- Hybrid architecture of deterministic rules plus a Gemini LLM cut merchant onboarding **80% (30 min → 5 min)** and cost **70%**.

---

## Toolkit

**AI systems** · Tool calling agents · RAG · LLM-as-judge evals · Model benchmarking · Structured outputs · Human-in-the-loop design · Prompt injection mitigation · Cost and latency optimization

**Engineering** · Python · TypeScript · SQL · Next.js · React · FastAPI · Node.js · Supabase/Postgres · pgvector · Row-Level Security · Stripe webhooks · Docker · AWS · Git

**Field skills** · Customer discovery · Scoping vague asks into shippable work · Threat modeling · Writing it down so the next person doesn't need me

**Certifications** · CSPO · CSM · Google Project Management

---

## Off the clock

Studying chess openings (1272 on Chess.com, working toward 1400 with the Najdorf Sicilian) and photographing NYC streets. Street photography taught me the habit I bring to engineering: notice what's actually happening, not what you expected to see.

---

<div align="center">

*NYU M.S. '26 · Open to Forward Deployed Engineer and AI Engineer roles · NYC, open to relocate*

**[See the full case studies →](https://hamidrizvi.vercel.app)**

</div>
