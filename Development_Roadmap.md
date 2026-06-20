# Big-Tech-Level Backend Software Engineer Roadmap (Python)
### System Design & Core CS Focus · 3 hrs/day, 6 days/week

**Schedule:** 3 hrs/day, **6 days/week = 18 hrs/week** (Sunday off).
**Total content:** ~840 hours.
**Total time: ~46.7 weeks (~10.7 months) of study.** No buffer — calendar time = study time.

**Built on what you already have, not from scratch.** You know full-stack MERN, you've shipped two projects, and you can code. So this roadmap deliberately **skips beginner programming, frontend, and DSA** (DSA lives in your ML roadmap). It spends its hours on the three things that actually gate big-tech backend offers and that MERN never forced you to reason about explicitly:

1. **Core CS fundamentals** — OS, networking, concurrency. You used these implicitly in Node; here you make them explicit and interview-ready.
2. **System design** — your stated gap. Roughly **a third of the entire roadmap** (Phases 5–8 + design mocks) is dedicated to it.
3. **The Python backend stack** — Flask / FastAPI / Django, mapped directly onto the Express patterns you already know so the framework switch is fast.

Everywhere possible, new material is anchored to something you've already done: Node's event loop → `asyncio`, Express middleware → Flask/FastAPI, MongoDB → relational + the tradeoffs Mongo hid from you, JWT auth → OAuth2/OIDC, Socket.IO → formal WebSockets and real-time system design.

---

## The Two Skill Buckets

| Bucket | What's In It | Total Hours | Share |
|---|---|---:|---:|
| **Knowledge & frameworks** (things you mostly *learn*) | Phases 0,1,2,3,4,9 | 400 hrs | 48% |
| **Design & application** (things you mostly *practice*) | Phases 5,6,7,8,10,11 | 440 hrs | 52% |

The roadmap is front-loaded with the CS and database depth you need *before* system design will make sense, then pivots hard into design and project work for the back half. Don't try to do system design case studies (Phase 8) before the foundations (Phases 1, 2, 6, 7) — you'll just memorize answers without understanding the tradeoffs, which interviewers detect instantly.

---

## Sample Weekly Template

| Day | 3-hr Block |
|---|---|
| Mon–Sat | Whichever phase you're currently on; once Phase 3 ends, split time so a backend project (Phase 10) runs alongside everything after it |
| Sunday | Rest / catch-up |

Sunday is your only slack — keep it genuinely off to make ~11 months sustainable. The single most common failure mode here is treating system design as something to "get to later" and spending all your time in comfortable framework/coding work. Protect the design phases.

---

## Quick Overview — All Phases

| # | Phase | Hours | Calendar Weeks (cumulative) |
|---|---|---:|---|
| 0 | Python for Backend Engineers (bridge from Node) | 35 | 0.0 – 1.9 |
| 1 | Core CS Foundations (OS · Networking · Concurrency) | 90 | 1.9 – 6.9 |
| 2 | Databases Deep Dive | 70 | 6.9 – 10.8 |
| 3 | Python Backend Frameworks (Flask · FastAPI · Django) | 90 | 10.8 – 15.8 |
| 4 | API Design & Backend Engineering | 55 | 15.8 – 18.9 |
| 5 | Object-Oriented Design & Design Patterns (LLD) | 45 | 18.9 – 21.4 |
| 6 | System Design Foundations | 80 | 21.4 – 25.8 |
| 7 | Distributed Systems | 70 | 25.8 – 29.7 |
| 8 | System Design Case Studies & Mocks | 75 | 29.7 – 33.9 |
| 9 | Infrastructure, DevOps & Observability | 60 | 33.9 – 37.2 |
| 10 | Backend Projects & Portfolio | 110 | 37.2 – 43.3 *(start in parallel right after Phase 3)* |
| 11 | Interview Preparation | 60 | 43.3 – 46.7 |
| | **TOTAL** | **840** | **0.0 – 46.7 weeks** |

> Phase 10's hours are listed sequentially for accounting, but you should **start building as soon as Phase 3 ends** — projects are where the design theory from Phases 5–8 actually sticks, and they're your strongest recruiter signal.

---

## Phase 0: Python for Backend Engineers *(Bridge from Node/JS)*
**Goal by end of phase:** Be fluent enough in idiomatic Python and its async model to build production backends without fighting the language — leaning on your JS/Node mental models instead of relearning programming.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **Python Idioms vs JS**<br>– comprehensions, generators, decorators<br>– context managers, dunder methods<br>– type hints & `typing` module | The idiomatic differences that trip up JS developers; writing Pythonic code, not "JavaScript in Python syntax." Type hints especially matter — FastAPI and Pydantic are built on them. | 12 |
| **Async Python**<br>– `asyncio`, `async`/`await`, event loop<br>– coroutines, tasks, `gather`<br>– sync vs async libraries | You already understand Node's single-threaded event loop — this maps that intuition onto Python's `asyncio`, including where Python differs (it's opt-in, not default). | 10 |
| **Testing & Tooling**<br>– pytest, fixtures, mocking<br>– poetry/uv, virtualenv<br>– ruff/black, mypy | Professional Python project hygiene; pytest is the industry standard and shows up in take-homes. | 8 |
| **Project Structure & Packaging**<br>– modules, packages, imports<br>– config & environment management | How real Python services are laid out — directly transferable from how you structure Node projects. | 5 |

**Phase total: 35 hours** *(go faster if comfortable — your coding background makes this the most compressible phase)*

---

## Phase 1: Core CS Foundations *(OS · Networking · Concurrency)*
**Goal by end of phase:** Build the operating-systems, networking, and concurrency mental models that big-tech backend interviews assume — the things you used implicitly in MERN but never had to explain.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **Operating Systems**<br>– processes vs threads<br>– memory management, virtual memory, paging<br>– CPU scheduling, context switching<br>– file I/O, system calls | The vocabulary behind "why is this slow / why did this crash." Process vs thread vs async is a recurring interview theme and underlies every backend performance decision. | 25 |
| **Networking (Deep)**<br>– TCP/IP model, TCP vs UDP<br>– HTTP/1.1 vs HTTP/2 vs HTTP/3<br>– TLS/HTTPS handshake, certificates<br>– DNS resolution<br>– WebSockets (formalizing your Socket.IO experience) | You've *used* HTTP and Socket.IO; now you understand what's happening on the wire — connection lifecycle, head-of-line blocking, why HTTP/2 multiplexes, how TLS actually secures a connection. Heavily tested. | 35 |
| **Concurrency & Parallelism**<br>– threads, locks, mutexes, semaphores<br>– race conditions, deadlocks, starvation<br>– the GIL (and what it means for Python)<br>– async I/O vs threads vs multiprocessing | The single most important backend-specific CS topic. When to reach for async vs threads vs processes — and the GIL's implications — is a defining Python-backend interview question. | 30 |

**Phase total: 90 hours**

---

## Phase 2: Databases Deep Dive
**Goal by end of phase:** Move from "I used MongoDB" to reasoning rigorously about storage — relational modeling, transactions, indexing, and the tradeoffs that drive nearly every system design decision.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **Relational & SQL (PostgreSQL)**<br>– schema design, normalization (1NF–3NF)<br>– joins, subqueries, CTEs, window functions<br>– constraints, foreign keys | The relational rigor Mongo let you skip. Postgres is the default big-tech relational store; deep SQL is assumed for backend roles. | 25 |
| **Indexing & Query Optimization**<br>– B-tree/hash indexes, composite indexes<br>– `EXPLAIN`/query plans<br>– when indexes hurt | Knowing *why* a query is slow and how an index fixes (or worsens) it — a classic differentiator and the foundation for "design a system that scales reads." | 15 |
| **Transactions & ACID**<br>– isolation levels (read committed → serializable)<br>– locking, MVCC<br>– deadlocks in DBs | The guarantees you didn't have to think about with single-document Mongo writes. Isolation levels and their anomalies (dirty/phantom reads) are common interview questions. | 15 |
| **NoSQL & Datastore Selection**<br>– document / key-value / wide-column / graph<br>– your Mongo experience, reframed with tradeoffs<br>– when to pick what | Turns your MongoDB familiarity into the ability to *justify* a datastore choice in a design interview — the part that actually scores points. | 15 |

**Phase total: 70 hours**

---

## Phase 3: Python Backend Frameworks *(Flask · FastAPI · Django)*
**Goal by end of phase:** Be productive across the Python backend stack, mapping each framework onto the Express patterns you already know so the switch is fast, not foundational.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **Flask**<br>– routing, blueprints<br>– request/response lifecycle<br>– extensions ecosystem | The "Express of Python" — minimal and explicit. The fastest framework for you to pick up because the mental model matches Express almost one-to-one. | 20 |
| **FastAPI**<br>– async-first, path/query/body params<br>– Pydantic models & validation<br>– dependency injection<br>– auto OpenAPI/Swagger docs | The modern default for new Python backends and the most interview-relevant. Type-driven, async, fast — leans directly on the typing and `asyncio` from Phase 0. | 35 |
| **Django & Django REST Framework**<br>– the ORM, migrations<br>– admin, auth, middleware<br>– DRF serializers & viewsets | "Batteries-included" — the opposite philosophy from Flask. The ORM and admin are huge productivity wins and Django shows up constantly in job listings. | 35 |

**Phase total: 90 hours**
*Build a small real API in each as you go — don't just read. Reimplementing one of your MERN backends here is ideal warm-up for Phase 10.*

---

## Phase 4: API Design & Backend Engineering
**Goal by end of phase:** Design APIs to big-tech standards — past "it returns JSON" into versioning, idempotency, rate limiting, and security.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **RESTful Design at Scale**<br>– resource modeling, status codes<br>– pagination (offset vs cursor)<br>– versioning, idempotency keys | The production concerns your MERN APIs probably didn't handle. Idempotency and cursor pagination in particular separate hobby APIs from big-tech ones. | 15 |
| **Auth & Authorization**<br>– sessions vs tokens (you've done JWT)<br>– OAuth2 flows, OpenID Connect<br>– RBAC vs ABAC | Formalizes the JWT auth you've built into the full landscape — when sessions beat tokens, how third-party login actually works, how to model permissions. | 15 |
| **API Security**<br>– OWASP Top 10<br>– input validation, injection, CSRF/CORS<br>– secrets management | The security baseline every backend engineer is expected to know; CORS especially you've hit in MERN — now understand *why*. | 10 |
| **Beyond REST**<br>– gRPC & protobufs<br>– GraphQL (tradeoffs vs REST)<br>– webhooks & event-driven APIs | Breadth for interviews and real systems — knowing when REST *isn't* the right tool. | 15 |

**Phase total: 55 hours**

---

## Phase 5: Object-Oriented Design & Design Patterns *(LLD)*
**Goal by end of phase:** Pass the low-level / object-oriented design interview round — turning a vague problem into a clean, extensible set of classes out loud.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **SOLID & Clean Code**<br>– the five SOLID principles<br>– composition vs inheritance<br>– cohesion & coupling | The principles interviewers listen for when you design classes; the difference between code that's "correct" and code that's "well-designed." | 10 |
| **Design Patterns**<br>– creational (factory, builder, singleton)<br>– structural (adapter, decorator, facade)<br>– behavioral (strategy, observer, state) | The shared vocabulary of OOD interviews. You don't memorize all 23 — you internalize the ~10 that recur and recognize when they apply. | 20 |
| **LLD Case Studies**<br>– parking lot, elevator system<br>– a rate limiter / cache as objects<br>– a vending machine, a deck of cards | The actual interview format: "design the classes for X." Practiced under time pressure, narrating your reasoning. | 15 |

**Phase total: 45 hours**

---

## Phase 6: System Design Foundations
**Goal by end of phase:** Learn the building blocks of scalable systems — this is the core of your stated gap, and every later case study assembles these pieces.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **Scalability Fundamentals**<br>– vertical vs horizontal scaling<br>– statelessness, load balancing (L4/L7)<br>– back-of-the-envelope estimation | The base layer of every design answer — and estimation (QPS, storage, bandwidth) is a step interviewers explicitly grade. | 15 |
| **Caching**<br>– Redis/Memcached<br>– cache strategies (cache-aside, write-through/back)<br>– invalidation, TTLs, CDN caching | Caching is the most common scaling lever and "how do you keep the cache consistent" is a favorite follow-up. | 20 |
| **Message Queues & Async Processing**<br>– Kafka, RabbitMQ, pub/sub<br>– work queues, Celery<br>– delivery guarantees (at-least/at-most/exactly-once) | How big systems decouple and absorb load. Celery ties back to your Python stack; delivery semantics are a deep-dive topic. | 20 |
| **Data at Scale**<br>– replication (leader/follower)<br>– sharding & partitioning strategies<br>– CAP theorem | Building directly on Phase 2 — how databases survive scale and failure, and the consistency/availability tradeoff that anchors most design discussions. | 25 |

**Phase total: 80 hours**

---

## Phase 7: Distributed Systems
**Goal by end of phase:** Understand the genuinely hard parts — consistency, consensus, and failure handling — that distinguish senior-level candidates from those who just memorized diagrams.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **Consistency Models**<br>– strong vs eventual consistency<br>– CAP revisited, PACELC<br>– read-your-writes, monotonic reads | The precise language for reasoning about what users see in a replicated system — where vague answers fall apart in interviews. | 15 |
| **Consensus & Coordination**<br>– leader election<br>– Raft / Paxos (conceptual)<br>– ZooKeeper / etcd | How distributed systems agree on anything despite failures. Conceptual depth is enough — you should be able to explain *why* consensus is hard. | 15 |
| **Distributed Transactions & Patterns**<br>– two-phase commit<br>– sagas, compensating transactions<br>– idempotency, the outbox pattern<br>– consistent hashing | The patterns that make microservices actually work. Idempotency and sagas recur constantly in both design and senior backend roles. | 20 |
| **Microservices Architecture**<br>– monolith vs microservices tradeoffs<br>– service discovery, API gateway<br>– inter-service communication | The architectural style most big-tech backends use — including *when not to* use it, which is the more impressive answer. | 20 |

**Phase total: 70 hours**

---

## Phase 8: System Design Case Studies & Mocks
**Goal by end of phase:** Apply every prior building block to the canonical big-tech system design problems, under realistic interview conditions.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **The Framework**<br>– requirements (functional + non-functional)<br>– estimation → high-level design → deep dive<br>– bottleneck analysis & tradeoffs | A repeatable structure so you never freeze on a blank whiteboard. This is as much about communication as correctness. | 10 |
| **Case Studies**<br>– URL shortener, rate limiter<br>– news feed / timeline<br>– chat & presence *(your Socket.IO experience is a real edge here)*<br>– notification system, file storage (Dropbox)<br>– typeahead / search, ride-sharing, payment system | Working the classic problems builds pattern recognition for novel ones. Lean into the real-time/chat designs where your Socket.IO background gives you concrete intuition most candidates lack. | 45 |
| **Timed Mock Interviews**<br>– 45-min sessions with feedback<br>– peers, Pramp/interviewing.io, or recorded self-review | Practicing under pressure is what converts knowledge into a passed interview. Record yourself and watch for hand-waving. | 20 |

**Phase total: 75 hours**

---

## Phase 9: Infrastructure, DevOps & Observability
**Goal by end of phase:** Ship and operate backend services reliably — the operational competence big tech expects from backend engineers (and the half your MERN projects probably skipped).

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **Linux & CLI**<br>– shell, processes, permissions<br>– logs, networking tools (curl, netstat, ss) | The environment every backend service runs in; fluency here makes debugging production issues possible. | 10 |
| **Docker & Kubernetes**<br>– images, containers, Compose<br>– K8s pods/services/deployments (basics) | The standard deployment substrate. Docker is assumed knowledge; K8s at a conceptual + basic-operational level is plenty for most backend roles. | 20 |
| **CI/CD**<br>– pipelines, automated testing/deploy<br>– GitHub Actions / GitLab CI | How code reaches production safely and repeatedly. | 10 |
| **Cloud Fundamentals (AWS)**<br>– EC2, S3, RDS, Lambda<br>– IAM, VPC basics | One major cloud at working depth is expected. AWS is the safest default; the concepts transfer to GCP/Azure. | 15 |
| **Observability**<br>– logging, metrics, distributed tracing<br>– SLI / SLO / SLA, alerting | How you know a live system is healthy — and the reliability vocabulary senior interviews probe. | 5 |

**Phase total: 60 hours**
*If you're also doing the ML roadmap, this overlaps its MLOps phase heavily — you can compress one against the other.*

---

## Phase 10: Backend Projects & Portfolio
**Goal by end of phase:** Have 2–3 substantial backend systems that demonstrate real design — your strongest signal past the resume screen and the anchor for most interview conversations.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **Flagship Distributed Backend**<br>– a system with real architecture: caching layer, message queue, multiple services, a proper DB schema<br>– deployed, documented, load-tested | One project that proves you can apply Phases 6–8, not just describe them. This is the project you'll walk an interviewer through. | 50 |
| **Rebuild/Extend a MERN Backend in Python**<br>– take one of your existing projects, re-architect its backend in FastAPI/Django<br>– add what it was missing: auth done right, caching, async jobs, tests | Highest-leverage use of your existing work — you already know the domain, so all the new effort goes into *good backend design*. | 35 |
| **Open Source / Technical Writeups**<br>– contribute to a Python OSS project, or<br>– write up a system design / architecture decision | Public, verifiable evidence of depth — recruiters and interviewers do look. A clear design writeup signals seniority. | 15 |
| **Resume, GitHub & Profile Polish**<br>– backend-focused framing<br>– clean repos with READMEs & architecture diagrams | Makes all the above visible and legible to recruiters scanning for backend signal. | 10 |

**Phase total: 110 hours**
*Start this the moment Phase 3 ends and run it in parallel with Phases 4–9 — building is how the design theory becomes real.*

---

## Phase 11: Interview Preparation *(Final Sprint)*
**Goal by end of phase:** Be interview-ready across the big-tech backend pillars — system design, low-level design, CS fundamentals, and behavioral. *(DSA/coding is covered in your ML roadmap, so it's intentionally excluded here.)*

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **System Design Mocks (continued)**<br>– timed sessions, novel problems | Keeps your design communication sharp right up to the real interviews — the highest-weighted round for backend roles. | 25 |
| **CS Fundamentals Rapid-Fire**<br>– OS, networking, DB, concurrency Q&A<br>– "explain X" / "why Y over Z" | The phone-screen and onsite conceptual questions that
