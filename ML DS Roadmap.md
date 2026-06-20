# Big-Tech-Level ML Engineer / Data Scientist Roadmap
### (Restructured: 5 hrs/day ML + 3 hrs/day DSA, 6 days/week)

**New schedule:** 8 hrs/day, 6 days/week = **48 hrs/week** (up from the original 28 hrs/week)
**Total roadmap content:** 1,580 hours (unchanged)
**New total time: ~44.7 weeks (~10.3 months) of pure study** — faster than the original 13-month estimate, because total weekly hours went up ~71%.
**Realistic calendar time (exams, breaks, off-weeks @ ~15–20% buffer): ~52–54 weeks (~12–12.5 months)**

---

## Why This Isn't Just "1580 ÷ 48"

The content splits into two genuinely separate tracks that run **in parallel**, not sequentially — so the math isn't a single division. Each day you're running two unrelated curricula side by side: ML/DS knowledge in one block, interview coding in the other.

| Track | What's In It | Total Hours | Daily Rate | Weekly Rate | Track Duration |
|---|---|---:|---|---:|---:|
| **ML/DS Track** | Phases 0,1,2,4,5,6,7,8,9,10,11, and the non-DSA parts of Phase 12 | 1,340 hrs | 5 hrs/day | 30 hrs/wk | **44.7 weeks** |
| **DSA Track** | Phase 3 (core DSA) + the "DSA Mock Interviews" topic from Phase 12 | 240 hrs | 3 hrs/day | 18 hrs/wk | **13.3 weeks** |

**The ML track is the bottleneck.** DSA's total volume (240 hrs) only takes 13.3 weeks at 3 hrs/day — far less than the 44.7 weeks the ML track needs. That's actually good news: it means DSA doesn't need to occupy all 3 daily hours for the entire 10+ months. Here's the realistic way to use that:

1. **Weeks 1–11ish:** Run the full 200-hour core DSA curriculum (Data Structures → Patterns → Practice) at the full 3 hrs/day, in parallel with ML Phases 0→1→2 and the start of Phase 4. This is when DSA fluency gets built.
2. **Weeks ~11–42:** Core DSA is done. Drop to **light maintenance mode** — 3–5 problems a week (not 3 hrs/day) just to stay sharp — freeing up real bandwidth. You can either (a) keep it light and enjoy the breathing room, or (b) reallocate that freed time to accelerate the ML track (pushes total completion well under 44.7 weeks if you do this consistently).
3. **Final ~2–3 weeks (overlapping with ML Phase 12):** Ramp DSA back to full 3 hrs/day for the 40-hour "DSA Mock Interviews" block — timed, interview-condition practice right before you start applying, which is exactly when it matters most.

This mirrors the original roadmap's advice to avoid DSA as "one isolated 7-week block," just now formalized around your fixed daily split.

---

## Sample Weekly Template

| Day | ML Block (5 hrs) | DSA Block (3 hrs) |
|---|---|---|
| Mon–Sat | Whichever ML phase you're currently on | Core DSA (early months) → maintenance (mid) → mock interviews (final stretch) |
| Sunday | Rest / buffer / catch-up | Rest / buffer / catch-up |

Block order (morning vs evening) doesn't matter — what matters is treating them as two separate sessions so DSA doesn't get silently dropped once ML feels more "interesting," which is the most common way this kind of plan quietly falls apart.

---

## Quick Overview — All Phases (with Track & Calendar Position)

| # | Phase | Track | Hours | Calendar Weeks (cumulative) |
|---|---|---|---:|---|
| 0 | Python & Tooling Foundations | ML | 70 | 0.0 – 2.3 |
| 1 | Mathematical Foundations | ML | 140 | 2.3 – 7.0 |
| 2 | Data Analysis & SQL | ML | 85 | 7.0 – 9.8 |
| 3 | DSA for Big-Tech Interviews (core) | **DSA** | 200 | 0.0 – 11.1 *(parallel w/ Phases 0–2 + start of 4)* |
| 4 | Classical Machine Learning | ML | 160 | 9.8 – 15.2 |
| 5 | Deep Learning Foundations | ML | 140 | 15.2 – 19.8 |
| 6 | Modern DL / NLP / Generative AI | ML | 150 | 19.8 – 24.8 |
| 7 | MLOps & Production ML | ML | 105 | 24.8 – 28.3 |
| 8 | Big Data & Distributed Systems | ML | 85 | 28.3 – 31.2 |
| 9 | Statistics, A/B Testing & Causal Inference | ML | 70 | 31.2 – 33.5 |
| 10 | ML System Design | ML | 80 | 33.5 – 36.2 |
| 11 | Portfolio, Projects & Competitions | ML | 165 | 36.2 – 41.7 |
| 12 | Interview Prep — ML portion (breadth/depth, system design mocks, behavioral, take-homes) | ML | 90 | 41.7 – 44.7 |
| 12 | Interview Prep — DSA Mock Interviews | **DSA** | 40 | ~42.5 – 44.7 *(parallel w/ ML Phase 12)* |
| | **TOTAL** | | **1,580** | **0.0 – 44.7 weeks** |

> The DSA row for Phase 3 and the ML rows all share the same calendar weeks 0–11.1 — they're happening on the same days, just in different daily blocks. Total calendar length is set by the ML track (44.7 weeks), not by adding every row's duration together.

---

## Phase 0: Python & Tooling Foundations *(ML Track)*
**Goal by end of phase:** Write idiomatic Python fluently and manipulate numerical/tabular data without constantly looking things up — the baseline fluency every later phase assumes.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **Python Fundamentals**<br>– syntax, data structures, OOP<br>– comprehensions, generators, decorators<br>– error handling, typing | Core language fluency; Python's idioms (comprehensions, generators) differ a lot from JS, so this isn't optional even with your JS background. | 25 |
| **Tooling & Environment**<br>– venv/conda, pip<br>– Jupyter/Colab<br>– Git workflows for ML projects | Standard ML dev environment setup — notebooks for exploration, environments for reproducibility. | 10 |
| **NumPy**<br>– arrays, broadcasting<br>– vectorized operations, indexing | The numerical backbone of the entire Python ML stack; vectorization is the mental shift from loop-based JS thinking. | 15 |
| **Pandas**<br>– DataFrames, cleaning<br>– merging/joining, groupby, pivoting | The tool you'll use constantly for loading, cleaning, and reshaping data before any modeling happens. | 20 |

**Phase total: 70 hours**

---

## Phase 1: Mathematical Foundations *(ML Track)*
**Goal by end of phase:** Understand *why* ML algorithms work, not just how to call `.fit()` — this is what separates big-tech-level candidates from API-callers in interviews and on the job.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **Linear Algebra**<br>– vectors, matrices, matrix multiplication<br>– eigenvalues/eigenvectors<br>– SVD, matrix decomposition | The language ML is written in — embeddings, PCA, neural net weights, and recommendation systems are all matrix operations. | 35 |
| **Calculus**<br>– derivatives, partial derivatives<br>– chain rule, gradients<br>– Jacobians, Hessians | Needed to understand how models learn — backpropagation is just the chain rule applied repeatedly. | 25 |
| **Probability Theory**<br>– distributions (normal, binomial, Poisson)<br>– Bayes' theorem<br>– expectation, variance, joint/conditional probability | Underlies almost every ML model's assumptions, from Naive Bayes to uncertainty estimation. | 30 |
| **Statistics**<br>– hypothesis testing, confidence intervals<br>– p-values, MLE<br>– sampling theory | Lets you reason about whether results are real or noise — critical for both modeling and A/B testing later. | 30 |
| **Optimization**<br>– gradient descent variants<br>– convexity<br>– constrained optimization, Lagrange multipliers | Every model "learns" via an optimization process; understanding it demystifies training instability and convergence issues. | 20 |

**Phase total: 140 hours**

---

## Phase 2: Data Analysis & SQL *(ML Track)*
**Goal by end of phase:** Take a raw, messy dataset and turn it into clean, well-understood data with a clear story — the actual day-to-day job of a data scientist before any modeling starts.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **SQL Mastery**<br>– joins, window functions<br>– CTEs, subqueries<br>– query optimization, indexing basics | The single most-used tool in DS/analytics interviews and the actual job — most companies test SQL harder than ML theory. | 30 |
| **Exploratory Data Analysis & Visualization**<br>– Matplotlib, Seaborn, Plotly<br>– distribution analysis, outlier detection | Turns raw numbers into visual understanding; also how you communicate findings to non-technical stakeholders. | 25 |
| **Data Cleaning & Feature Engineering Basics**<br>– missing values, encoding categorical data<br>– scaling, outlier handling | Real-world data is dirty; this is the unglamorous 70% of actual DS work. | 20 |
| **Data Storytelling**<br>– structuring insights, dashboards basics | Translating analysis into decisions — a skill that's underrated but heavily weighted in DS performance reviews. | 10 |

**Phase total: 85 hours**

---

## Phase 3: Data Structures & Algorithms *(DSA Track — runs in parallel, weeks 0–11.1)*
**Goal by end of phase:** Pass the coding round at any FAANG-tier company — ML/DS roles at big tech still gate on general software engineering coding ability, not just ML knowledge.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **Core Data Structures**<br>– arrays, strings, linked lists<br>– trees, graphs, hashmaps, heaps | The vocabulary every coding interview problem is built from. | 60 |
| **Algorithmic Patterns**<br>– dynamic programming, two pointers<br>– sliding window, backtracking<br>– graph traversal (BFS/DFS), greedy | The reusable problem-solving patterns that let you recognize "I've seen this shape before" in a new problem. | 60 |
| **Deliberate Practice**<br>– 150–200 medium/hard problems<br>– timed mock practice | Volume + repetition under time pressure is what actually builds interview speed, not just understanding concepts. | 80 |

**Phase total: 200 hours** — done at 3 hrs/day, 6 days/week, this finishes in ~11.1 weeks. After this, switch to maintenance mode (a few problems a week) until Phase 12's mock-interview sprint.

---

## Phase 4: Classical Machine Learning *(ML Track)*
**Goal by end of phase:** Independently build, evaluate, and explain end-to-end ML pipelines on tabular data using scikit-learn — this is the actual baseline competency for any ML/DS interview.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **ML Workflow Fundamentals**<br>– bias-variance tradeoff<br>– train/val/test splits, cross-validation | The mental framework for "is my model actually good" that underlies everything else in this phase. | 15 |
| **Supervised Learning**<br>– linear/logistic regression<br>– decision trees, random forests<br>– gradient boosting (XGBoost/LightGBM)<br>– SVM, KNN | The core algorithm toolkit used in the vast majority of real-world tabular ML problems and interviews. | 50 |
| **Unsupervised Learning**<br>– k-means, hierarchical clustering<br>– PCA, DBSCAN<br>– anomaly detection | Used when there's no labeled target — clustering users, dimensionality reduction, fraud/outlier detection. | 25 |
| **Model Evaluation**<br>– precision/recall/F1, ROC-AUC<br>– regression metrics (RMSE, MAE, R²) | Knowing *which* metric matters for a given business problem is a classic interview differentiator. | 15 |
| **Feature Engineering & Selection**<br>– encoding, scaling<br>– feature importance, L1/L2 regularization | Often has more impact on model performance than algorithm choice — heavily emphasized at big tech. | 20 |
| **Hyperparameter Tuning**<br>– grid/random search<br>– Bayesian optimization (Optuna) | Systematic model improvement instead of manual guesswork. | 10 |
| **End-to-End scikit-learn Projects**<br>– pipelines, ColumnTransformer<br>– a complete tabular ML project | Cements everything above into one working, explainable project you can talk about in interviews. | 25 |

**Phase total: 160 hours**

---

## Phase 5: Deep Learning Foundations *(ML Track)*
**Goal by end of phase:** Understand and implement neural networks from first principles in PyTorch, including image and sequence models — the foundation for everything in Phase 6.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **Neural Network Fundamentals**<br>– perceptrons, activation functions<br>– forward pass, backpropagation | The actual mechanics of how a neural net learns — not just calling `.fit()`, but knowing what's happening underneath. | 25 |
| **Training Deep Networks**<br>– loss functions, optimizers (SGD, Adam)<br>– dropout, batch normalization, regularization | Why training sometimes fails (vanishing gradients, overfitting) and how to fix it. | 25 |
| **PyTorch**<br>– tensors, autograd<br>– `nn.Module`, custom training loops | The dominant framework at big tech research/ML teams; fluency here is assumed in interviews. | 35 |
| **Convolutional Neural Networks (CNNs)**<br>– convolutions, pooling<br>– architectures (ResNet), image classification | The standard architecture for any vision task, and a common interview/take-home topic. | 30 |
| **RNNs / LSTMs / GRUs**<br>– sequence modeling fundamentals<br>– vanishing gradient problem in sequences | The classical approach to sequential data — still useful conceptually even though transformers have largely replaced it. | 25 |

**Phase total: 140 hours**

---

## Phase 6: Modern Deep Learning, NLP & Generative AI *(ML Track)*
**Goal by end of phase:** Be conversant in the architecture and practical use of transformers and LLMs — non-negotiable for any 2026 big-tech ML role, regardless of specialization.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **Transformer Architecture**<br>– self-attention, multi-head attention<br>– positional encoding | The architecture behind essentially every modern state-of-the-art model — deeply tested in interviews now. | 30 |
| **NLP Pipeline**<br>– tokenization, embeddings<br>– word2vec/GloVe, transfer learning | The pre-transformer NLP toolkit, still useful for understanding why transformers were such a leap. | 25 |
| **Pretrained Models & Fine-Tuning**<br>– BERT, GPT-family architectures<br>– Hugging Face ecosystem (transformers, datasets) | The practical, job-relevant skill of adapting existing large models instead of training from scratch. | 35 |
| **LLMs & Generative AI**<br>– prompting strategies<br>– retrieval-augmented generation (RAG)<br>– fine-tuning & evaluating LLMs | The fastest-growing area of big tech ML hiring right now — directly relevant given your study-tool project experience with Gemini. | 35 |
| **Computer Vision (Advanced)**<br>– object detection, segmentation<br>– vision transformers (ViT) | Optional depth depending on whether you lean CV vs NLP, but useful breadth for general ML interviews. | 25 |

**Phase total: 150 hours**

---

## Phase 7: MLOps & Production ML Systems *(ML Track)*
**Goal by end of phase:** Take a trained model and actually ship it as a reliable production service — this is the "ML Engineer" half of the role, and where your full-stack background gives you a real head start.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **Model Deployment**<br>– FastAPI/Flask model serving<br>– REST API design for inference | Turning a trained model into something other services can actually call — directly maps to your Express/Node experience. | 20 |
| **Containerization & Orchestration**<br>– Docker<br>– Kubernetes basics | Standard deployment infrastructure at any big tech company; Docker especially is assumed knowledge. | 25 |
| **CI/CD for ML**<br>– automated testing for ML code<br>– model versioning (MLflow, DVC) | ML-specific version control — tracking not just code but data and model versions together. | 20 |
| **Monitoring & Observability**<br>– data drift, model drift<br>– logging and alerting for ML systems | Models silently degrade in production; this is how you catch it before it becomes a business problem. | 15 |
| **Cloud ML Platforms**<br>– pick one: AWS SageMaker / GCP Vertex AI / Azure ML | Big tech companies run ML at cloud scale; fluency in one major platform's ML tooling is expected. | 25 |

**Phase total: 105 hours**

---

## Phase 8: Big Data & Distributed Systems *(ML Track)*
**Goal by end of phase:** Process datasets that don't fit on a single machine — the scale at which big tech actually operates, distinct from the Kaggle-CSV scale most courses teach.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **Distributed Computing Concepts**<br>– MapReduce, partitioning, shuffling | The theoretical basis for why Spark/Hadoop-style systems work the way they do. | 15 |
| **Apache Spark (PySpark)**<br>– DataFrames, transformations<br>– Spark MLlib pipelines | The industry-standard tool for big-data processing and distributed feature engineering. | 30 |
| **Data Engineering Basics**<br>– ETL pipelines, Apache Airflow<br>– data warehousing concepts | The pipelines that feed data to ML systems — knowing this makes you far more self-sufficient on the job. | 25 |
| **Distributed Training (Overview)**<br>– data parallelism vs. model parallelism | Conceptual understanding of how huge models get trained across many GPUs — increasingly common interview topic. | 15 |

**Phase total: 85 hours**

---

## Phase 9: Statistics, A/B Testing & Causal Inference *(ML Track)*
**Goal by end of phase:** Design and correctly interpret an experiment — this is the single most heavily tested skill in Data Scientist interviews at big tech, often more than ML algorithms themselves.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **A/B Testing Fundamentals**<br>– hypothesis testing in practice<br>– sample size & power analysis | The standard framework big tech uses to validate any product change before shipping it broadly. | 25 |
| **Experimentation Pitfalls**<br>– novelty effects, network effects<br>– multiple testing correction (Bonferroni, FDR) | Knowing the ways experiments lie to you — a favorite interview topic because it separates real practitioners from textbook readers. | 15 |
| **Causal Inference Basics**<br>– confounders, propensity score matching<br>– difference-in-differences | For when you can't run a clean A/B test and need to infer cause from observational data. | 20 |
| **Metrics Design**<br>– north-star metrics, guardrail metrics | Choosing what to measure so you don't optimize the wrong thing — a core DS/PM collaboration skill. | 10 |

**Phase total: 70 hours**

---

## Phase 10: ML System Design *(ML Track)*
**Goal by end of phase:** Confidently design a full ML system end-to-end on a whiteboard — the signature senior-level interview format at every major tech company.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **System Design Framework**<br>– problem framing, data, model choice<br>– evaluation, deployment, monitoring loop | A repeatable structure to approach any "design X system" interview question without freezing up. | 20 |
| **Case Studies**<br>– recommendation systems<br>– search/feed ranking<br>– fraud detection, ad click prediction | Working through the canonical big-tech ML problems builds pattern recognition for novel ones in interviews. | 40 |
| **Mock Practice**<br>– timed whiteboard-style design sessions | Practicing under interview conditions, since this skill is as much about communication as technical correctness. | 20 |

**Phase total: 80 hours**

---

## Phase 11: Portfolio, Projects & Competitions *(ML Track)*
**Goal by end of phase:** Have 2–3 concrete, end-to-end, defensible projects — the proof points that actually get you past resume screens and anchor your interview conversations.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **End-to-End Capstone Project**<br>– real dataset → model → deployed service | One flagship project demonstrating the full pipeline, ideally tying into your existing strengths (e.g. an ML feature inside your BTP/MTP platform, or the study-tool's AI features taken further). | 60 |
| **Kaggle Competitions**<br>– 2–3 competitions, focus on process not just leaderboard rank | Forces you to handle messy, competitive, real-world-ish data under a fixed evaluation metric. | 60 |
| **Open-Source / Writeup / Blog**<br>– contribute to an ML repo, or write up a technical project | Builds public, verifiable evidence of depth — recruiters and interviewers do check this. | 30 |
| **Resume & Profile Polish**<br>– GitHub cleanup, resume, LinkedIn | Makes sure all the above work is actually visible and well-framed to recruiters. | 15 |

**Phase total: 165 hours**
*Start this phase's ML hours as soon as Phase 4 finishes — don't wait until everything else is "done."*

---

## Phase 12: Interview Preparation (Final Sprint) *(Mixed: ML + DSA, overlapping)*
**Goal by end of phase:** Be fully interview-ready across all four big-tech ML/DS interview pillars: coding, ML theory, system design, and behavioral.

| Topic & Sub-topics | What It Covers | Hours | Track |
|---|---|---:|---|
| **DSA Mock Interviews**<br>– continued timed practice | Keeps coding speed sharp right up to actual interviews. | 40 | DSA |
| **ML Breadth & Depth Prep**<br>– conceptual Q&A across classical ML, DL, stats | The "explain X concept" and "why would you choose Y over Z" style questions common in ML interviews. | 40 | ML |
| **ML System Design Mocks**<br>– live practice with feedback | Refining communication and structure under real interview pressure. | 20 | ML |
| **Behavioral Interview Prep**<br>– STAR method, leadership-principle-style stories | Big tech weighs this heavily — your project experience (PQC research, full-stack systems) gives you strong raw material to shape into stories. | 15 | ML |
| **Take-Home Assignment Practice**<br>– 1–2 simulated take-homes under time limits | Many big-tech and unicorn companies use take-homes instead of (or alongside) live coding for ML roles. | 15 | ML |

**Phase total: 130 hours** (90 ML + 40 DSA, running concurrently in the final ~3 weeks)

---

## Total Time Investment

| Metric | Value |
|---|---|
| Total content | 1,580 hours |
| Daily schedule | 5 hrs ML + 3 hrs DSA = 8 hrs/day |
| Days/week | 6 |
| Effective weekly hours | 48 hrs/week (30 ML + 18 DSA) |
| **Pure study time (set by the ML track bottleneck)** | **~44.7 weeks (~10.3 months)** |
| With realistic buffer (exams, breaks, off-weeks @ ~15–20%) | **~52–54 weeks (~12–12.5 months)** |

**Compared to the original plan:** the old 28 hrs/week version needed ~56.4 weeks (~13 months). This version needs ~44.7 weeks (~10.3 months) — about **12 weeks (~2.7 months) faster** — purely from the jump to 48 hrs/week. If you reallocate DSA's freed-up maintenance-mode hours back into the ML track once core DSA wraps around week 11, this could compress further toward ~38–40 weeks, but treat that as a stretch outcome, not the baseline plan.

---

## How to Sequence This Realistically

1. **Weeks 0–11ish — Dual intensive phase.** Full 5h ML + 3h DSA every scheduled day. ML moves through Phases 0 → 1 → 2 and starts Phase 4. DSA runs its full core curriculum (Phase 3) and finishes around week 11.
2. **Once core DSA is done — switch DSA to maintenance mode.** A few problems a week, not 3 hrs/day. Use the freed time to rest, go deeper on ML topics, or move slightly faster through the ML track — your call.
3. **Phases 4–6 (ML)** are sequential; each builds directly on the last.
4. **Phase 7 (MLOps)** should be your fastest ML phase relative to hours budgeted — your existing backend/deployment instincts (Socket.IO, auth, transactions, Drive integration) transfer almost directly.
5. **Phase 8 (Big Data)** can be deferred or trimmed if you're optimizing specifically for Data Scientist roles over ML Engineer roles.
6. **Phase 9 (Statistics/A-B Testing)** matters more if you're leaning Data Scientist; **Phases 7–8 (MLOps/Big Data)** matter more if you're leaning ML Engineer. Once you've got a feel for which you enjoy more, you can weight remaining hours accordingly.
7. **Phase 11 (Portfolio)** should start as soon as Phase 4 ends.
8. **Final ~2–3 weeks (Phase 12).** DSA ramps back up to full 3 hrs/day for mock interviews, in parallel with the ML-side interview prep (breadth/depth, system design mocks, behavioral, take-homes). This is the only other stretch besides weeks 0–11 where DSA gets full daily time.

---

*This is a living plan — log actual hours per topic as you go. The DSA maintenance-mode gap (roughly weeks 11–42) is the part most likely to get neglected in practice — protect at least a token weekly DSA slot there, even if it's just 2–3 problems, so Phase 12's mock-interview ramp-up isn't starting from zero.*
