---
title: Robin Duchesneau
subtitle: Regulated-domain AI transformation — assurance discipline, executive advisory, systems that ship
author: Robin
date: 2026-09-14
version: 5.4-ode
status: draft
source_files: Robin_Duchesneau_Resume_2026_v4.md, Robin_Duchesneau_Resume_2026_Leadership.docx, Ode Principal AI Transformation JD
---

# Contact

Pea Ridge, AR | (479) 866-5471 | rbndchsn@gmail.com
linkedin.com/in/robin-duchesneau | Fluent in English and French

# Profile

Twenty years turning environmental science and regulation into working systems, on every side of the field: writing the standards, certifying against them, advising the multinationals that must meet them, and now building the AI-enabled software that codifies them. Has stood up two practices from nothing and owned the quality bar for a third, led pursuit teams that won roughly $2M in engagements, and closed six-figure engagements from personal executive relationships.

Builds AI systems for regulated domains, anywhere the deliverable has to survive an auditor, a regulator, or a board. Sustainability and ESG disclosure is where the proof is live; the discipline transfers to any domain where the source of truth is a document with legal weight. Six systems shipped end to end under a repeatable method: brief, PRD with success and kill criteria, architecture, agentic build with quality control at every step, independent-model verification, and a human accountable for the final assessment. Model-agnostic by design: Claude Code, an agentic coding tool that reads the codebase, edits files, runs commands, and connects to external tools, drives the build from terminal and IDE, with a second instance overseeing the first; frontier LLMs handle extraction and judging, a different model always verifying the one that did the work; open-source models run locally (Llama via Ollama, Nomic, BERT/SBERT) where data sovereignty requires it. Builds multi-agent pipelines as products, not only as tooling: orchestrator, sub-agents, and verifier with resumable state.

# Executive, Commercial, and Delivery Record

- **Executive trust.** Advised ISEAL, Better Cotton, H&M, and Adidas on value-chain and chain-of-custody design; delivered Net Zero and disclosure strategy to Fortune 500 and mid-market leadership at Anthesis; recruited by Apex to build a practice from a standing start.
- **Revenue.** Led pursuit teams at Anthesis that won roughly $2M in engagements; separately closed two six-figure engagements sourced from own executive relationships; currently own go-to-market, pipeline, and client pitching for a new service line at Apex.
- **Mobilizing delivery.** Teams of 20+, direct reports developed, scope and budget owned, quality and knowledge-management systems built so delivery survives turnover.
- **Applied AI, not slideware.** Six shipped systems (below), built spec-first with Claude, governed so models classify and retrieve during construction and are removed from the answer path or fenced behind a trust boundary at runtime.
- **Learning agility.** Forest ecosystem simulation modeling to standards authorship to verification practice to full-stack AI systems, each ramp self-directed.

# Selected Builds

All AI-assisted up front; none rely on an LLM generating answers to users at runtime.

**Multi-tenant ESG compliance platform** (research prototype) — [compliance-saas.pages.dev/public/ghg-land](https://compliance-saas.pages.dev/public/ghg-land)
Built to test how far AI assistance takes one practitioner from published standard to working compliance interface. Requirement registers extracted from source PDFs through a vision-transformer layout and table pipeline: IFRS S2 (1,623 requirements), CSRD (6,016), GRI, SASB, EU Taxonomy, GHG Protocol Land Sector and Removals. Extractions verified by an independent-model grounding check (precision — found / not found / mismatch / interpretation, with counts) before human QA against a set acceptance threshold. SQLite schema, REST API on Cloudflare Workers, dual-token auth, evidence object storage, React front end.

**SBTi Corporate Net-Zero Standard V2.0 portal** — [rbndchsn.github.io/sbti-cnzs-portal](https://rbndchsn.github.io/sbti-cnzs-portal/)
Governed Answer Retrieval: every answer traces to the clause it came from and is served verbatim. Content human-graded and approved before serving (100% human eval as the release gate); clause-level grounding makes citation accuracy deterministic. No generation surface in front of the user.

**California SB 54 Compliance Navigator** — [rbndchsn.github.io/sb_portal](https://rbndchsn.github.io/sb_portal/)
Statute and regulations classified into a structured requirement register. Python content factory, generated JSON, deploy gated on deterministic validation checks (schema and content graders) so a failed check leaves the last good version serving.

**DocReview** — multi-agent document analysis pipeline (not public)
Orchestrator with resumable state, corpus manifest, and schema versioned in Git. Seven rubric modes including asymmetric critical review against authoritative references. Every finding carries a support level (dimensional scoring: explicit / inferred / uncertain / missing), never a collapsed numeric score; uncertain or conflicting findings are routed to a verifier pass (scoped LLM-as-judge). Rubric calibrated on two documents before any corpus run.

**Second Brain** — local-first agentic RAG for technical standards (not public)
Dual-path retrieval (semantic plus keyword/metadata) with transparency on completeness — the user always knows whether they saw 5 of 5 or 5 of 500 — and a keyword-only mode that gives recall by construction when exhaustiveness is required. Eval criteria set in the PRD before build: 100% recall on metadata-filter queries, top-5 semantic relevance ≥80% on a test query set, zero fabricated citations. Trust boundary between deterministic extraction metadata and LLM enrichment; dual-write storage with rollback; consent gate before any outbound call. Delivered from a BMAD PRD with SMART success criteria, kill/pivot triggers, and a traceability matrix.

**Star Trek Tri-Dimensional Chess** — live at [sustainable-iq.github.io/tri-d-chess](https://sustainable-iq.github.io/tri-d-chess/)
Outside the domain, to prove the method travels. Full FRS5 rules engine as pure TypeScript with engine/rendering separation; 3D WebGL board; in-browser alpha-beta/PVS opponent with transposition table and quiescence, running in a Web Worker. Evals built against a reference implementation adopted as oracle (gold-standard ground truth): replay of the annotated sample game (recall — every legal move accepted) plus per-position differential checks submitting every generated move to the validator (precision — no over-generation), run as a regression eval suite; deviations from the reference documented and cited.

# How I Build with AI

- **Spec first.** Brief → PRD with success criteria and kill triggers → architecture as the contract the PRD must satisfy → epics and stories → implementation. Method-literate (BMAD, spec-driven development, agentic workflows), not method-dependent.
- **Two-model build loop.** One Claude Code instance implements; a second oversees, issues prompts, and receives reports; I adjudicate.
- **Quality control at every step.** Predetermined checks run by an agent after each implementation step, so a failure localises to a stage.
- **Independent verification of extractions.** When AI extracts content that becomes source of truth, a different model checks every sentence against the source and returns found / not found / mismatch / interpretation with counts — a precision signal and a hallucination ceiling — before human review.
- **Threshold QA and human accountability.** End-of-pipeline acceptance against an explicit threshold set up front; a human makes the final assessment, with tooling routing that human to uncertain cases and a sample of the rest. Earlier R&D used SBERT similarity with a 0.75 threshold to flag likely non-compliance for human assessment, and established where similarity stops being truth.

# Experience

## Principal, Product Sustainability — Apex Companies
*Arkansas, February 2026 to present*

Recruited to stand up and lead a product sustainability practice from nothing, owning the service line end to end.

- Own service design, market positioning, go-to-market, and pipeline: build and manage the client pipeline in HubSpot, pitch alongside sales, coordinate outreach, prepare client materials, represent the firm at conferences.
- Lead product sustainability consulting and verification: Product Carbon Footprint, Extended Producer Responsibility, Environmental Product Declarations, life cycle assessment, supplier-specific emission factors, value chain interventions, supplier engagement.
- Build AI-enabled, full-stack tools that codify regulatory logic and institutional knowledge into repeatable delivery.
- Translate regulatory and market analysis into service innovation for clients in a compliance-driven market; partner with marketing to turn technical content into positioning.

## Director of Sustainability and Innovation — Sustainable IQ
*Arkansas, November 2024 to February 2026*

Founded and ran an independent practice delivering carbon accounting and decarbonization strategy, and built the systems behind it.

- Architected and built the multi-tenant ESG compliance platform, the document ingestion pipeline converting regulatory PDFs into structured requirement registers at scale, and the governed retrieval portals above.
- Applied LLMs, retrieval-augmented generation, and BERT-family models to codify regulatory logic into operational tools, governed so models classify and retrieve rather than generate answers.
- Delivered corporate carbon accounting and decarbonization strategy from GHG inventories and Scope 3 value chain analysis.
- Integrated quality and knowledge management systems to build institutional memory that survives turnover.

## Associate Director, Corporate Carbon Accounting — Anthesis
*Arkansas, October 2022 to November 2024*

Ran client and project delivery at a top-five global sustainability consultancy; owned QA and knowledge management for the Climate Resilience and Decarbonization business line.

- Led pursuit teams that won roughly $2M in engagements; closed two six-figure engagements sourced from own executive relationships.
- Led projects end to end from conception through delivery — client relationships, scope, budgets, CRM — for Fortune 500 and mid-market clients across retail, food and beverage, manufacturing, cloud services, healthcare, agriculture, and forestry.
- Designed Net Zero strategies integrating supplier engagement, product carbon footprinting, and life cycle assessment; built GHG inventories and Scope 3 mitigation assessments; implemented MRV systems aligned to ISO, Verra, Gold Standard, GHG Protocol, and SBTi.
- Delivered ESG reporting and disclosure support; facilitated executive stakeholder and supplier engagement.
- Managed and developed direct reports through mentorship, performance evaluation, and goal setting.

## Director, Value Chain Certification — SustainCERT (Gold Standard)
*Amsterdam, January 2020 to April 2022*

Directed program design and certification at the creation of a new assurance category, owning policies, procedures, and decisions for verification of corporate Scope 3 insetting under the Gold Standard Value Change Initiative.

- Designed the certification methodology for corporate Scope 3 insetting — a category with no prior accounting rules — and wrote the policies and verification procedures still used in that market.
- Certified more than twenty land use and forestry projects, contributing to issuance of hundreds of thousands of credits with more than forty SDG co-benefits.
- Conducted GHG audit assessments under GHG Protocol guidance and ISO 14064.
- Advised ISEAL, Better Cotton, H&M, and Adidas on value chain and chain-of-custody design.

## Earlier career, 1999–2020

Standards authorship (EcoLogo criteria for 300+ product categories, TerraChoice), nine years of ISO 14001, FSC, and USDA organic certification and audit practice, FSC audit leadership at Rainforest Alliance, and forest ecosystem simulation modeling as a research scientist at UBC and UQO, including climate scenario analysis for a million-dollar industry research collaboration. Details on request.

# Technical

**Languages and frameworks:** Python, SQL, SQLite, TypeScript, JavaScript, React, Hono
**Infrastructure:** Cloudflare Workers, Pages, R2, D1; GitHub Actions CI/CD
**AI and data:** Claude Code (agentic build, multi-instance implementer/overseer loops); frontier LLMs (Claude and others) for extraction and LLM-as-judge verification; open-source models run locally (Llama via Ollama, Nomic embeddings, BERT/SBERT); multi-agent orchestration with resumable state; RAG and governed retrieval; vision-transformer document ingestion; ChromaDB, DuckDB; schema design; ETL from unstructured regulatory text
**Standards:** GHG Protocol Corporate, Scope 3, and Land Sector and Removals; ISO 14064, 14065, 17029, 14001, 14025; SBTi; CSRD and ESRS; IFRS S2; EU Taxonomy; GRI; SASB; California SB 54 and EPR; Gold Standard; Verra; FSC; USDA NOP

# Education and Certification

M.Sc., Renewable Resources, University of Quebec in Chicoutimi, 1997
B.Sc., Biological Sciences, University of Quebec in Montreal, 1995

ISO 14001 Lead Auditor (RABQSA-EM, 2011) · FSC Auditor (Rainforest Alliance, 2010) · GHG Protocol Scope 3 Standard (2020) · TCFD Climate-Related Disclosures (2022)
