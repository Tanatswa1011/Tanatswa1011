<div align="center">

# Tanatswa Phil Muganga

**Systems & Product Engineer** | Berlin, Germany

Building reliable systems for high-complexity operational problems.

[![Portfolio](https://img.shields.io/badge/Portfolio-TanaPhil.com-555?style=flat-square)](https://TanaPhil.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-tanatswaphilmuganga16-0A66C2?style=flat-square)](https://www.linkedin.com/in/tanatswaphilmuganga16)
[![Email](https://img.shields.io/badge/Email-tanamuganga16@gmail.com-EA4335?style=flat-square)](mailto:tanamuganga16@gmail.com)

</div>

---

## Engineering Focus

**Core:** Automation systems · Data quality at scale · Operational reliability · Fail-closed architecture  
**Expertise:** Python systems engineering · Research-to-deployment workflows · State management · Testing infrastructure

---

## Projects

### [AITRADE](https://github.com/Tanatswa1011/Aitrade) — Systematic Trading Framework

**Problem:** Automated trading systems fail silently or execute orders under unsafe conditions. Research and production diverge.

**Solution:** Production-hardened Python framework for systematic strategies with deterministic validation, execution safeguards, and fail-closed defaults.

**Technical Depth:**
- **Architecture:** Signal pipeline → validation gates → risk checks → execution adapter → journal logging
- **Safety Design:** Execution disabled by default. Orders require operator consent + environmental checks + state verification.
- **State Management:** Corruption fails closed. Restart blocks until manual review.
- **Validation:** 419+ integration tests. Strategy hashes prevent accidental mutations.
- **Stale-data Protection:** Blocks entries on market data gaps exceeding threshold.
- **Position Safeguards:** Reads broker state on every submission. Refuses entry if position non-flat.

**Status:** Research and deployment preparation (paper trading). Live execution intentionally disabled.  
**Tech Stack:** Python · NinjaTrader ATI bridge · Databento · PostgreSQL

**Key Systems:**
- Frozen strategy configurations with SHA256 integrity hashes
- NQ Drift VWAP pullback engine (phase 30, backtested)
- GC VWAP mean reversion (phase 26, frozen)
- Prop-firm rule validator (generic framework)

---

### [ASK DAA](https://github.com/Tanatswa1011/DataAiAgent-) — Data Profiling & QA

**Problem:** Data quality issues go undetected. Column types misclassified. Anomalies buried in raw exports.

**Solution:** CSV profiler that surfaces dataset structure, quality signals, and type evidence in one deterministic interface.

**Technical Depth:**
- **Classification Pipeline:** Deterministic rules (boolean → numeric → datetime → categorical → text). Threshold-based, fully testable.
- **Quality Signals:** Mixed-type warnings · missing value density · cardinality analysis · sample data inspection
- **Architecture:** FastAPI backend + Next.js frontend. Multipart file uploads. Stateless processing (temporary). 
- **Testing:** Backend tests cover all classification rules and edge cases. Frontend tests for upload flow and component behavior.

**Status:** Stable, feature-complete for phase 2 scope  
**Tech Stack:** Python/FastAPI · Next.js · Pandas profiling · Pydantic

---

### [ORB Validity Analysis](https://github.com/Tanatswa1011/orb-validity-qqq) — Quantitative Research

**Problem:** Trading hypotheses lack statistical rigor. Backtests are irreproducible.

**Solution:** Production-grade research repository for testing Opening Range Breakout (ORB) strategy on QQQ with historical market data.

**Technical Depth:**
- **Reproducibility:** All data regenerated via script from Alpaca API. No committed raw data. Frozen requirements.
- **Structure:** Separation of raw → processed → features. Research lives in notebooks; pipelines are source-of-truth.
- **Data Integrity:** Data validation gates before feature engineering. Complete audit trail.

**Status:** Stable research framework  
**Tech Stack:** Python · Pandas · Alpaca API · Parquet storage

---

## Background

**Previous Role:** Data automation engineer  
**Impact:** Built systems processing ~1,000 structured documents/week using Python + SQL  
**Key Achievement:** Reduced 15-hour manual workflow to ~2-hour automated pipeline with quality gates

**Methodology from experience:**
1. Map the system (understand real workflow, not assumed workflow)
2. Identify the constraint (what takes the most time or causes most errors?)
3. Build deterministic guards (data quality gates prevent downstream failure)
4. Measure the output (what changed? By how much?)
5. Automate ruthlessly (remove humans from repetitive decisions)

---

## Technical Stack

| Category | Depth |
|----------|-------|
| **Systems** | Python · SQL · Event-driven architecture · State management · CI/CD |
| **Data** | Pandas · PostgreSQL · Data pipelines · Validation frameworks · Backtesting |
| **Infrastructure** | AWS · Linux · Git · Supabase · GitHub Actions |
| **Product** | TypeScript · React · Next.js · API design · Testing |
| **Workflow** | Deterministic validation · Frozen configurations · Audit logging · Reproducibility |

---

## How I Work

✅ **Constraint-driven:** Find the bottleneck, measure it relentlessly  
✅ **Deterministic:** Prevent human error through guards, not discipline  
✅ **Testable:** If it can break, it's tested. If it's frozen, it's hashed.  
✅ **Observable:** Comprehensive logging of decisions and state  
✅ **Operator-friendly:** Humans supervise. Systems enforce rules.  

---

## Open To

Senior systems engineering · Founding engineering roles · Infrastructure for reliable automation · Teams prioritizing data quality and deployment safety

**Location:** Berlin / Potsdam, Germany | Remote welcome

---

**Portfolio & case studies:** [TanaPhil.com](https://TanaPhil.com)
