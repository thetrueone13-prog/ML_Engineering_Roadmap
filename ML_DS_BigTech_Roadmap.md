# Big-Tech-Level ML Engineer / Data Scientist Roadmap

**Weekly commitment:** 28 hrs/week
**Total roadmap effort:** 1,580 hours → **~56.5 weeks (~13 months)** of pure study time
**Realistic calendar time (with exams, breaks, slow weeks):** ~15–16 months

This roadmap assumes your starting point: strong full-stack (MERN) engineering skills, comfort with complex backend logic and system design instincts, and some research-paper experience (PQC project). That means you can move fast through general programming/CS fundamentals and spend your time where it actually matters — math, ML theory, and the parts of the stack you haven't touched yet (Python's data/ML ecosystem, statistics, deep learning, MLOps).

---

## Quick Overview — All Phases

| # | Phase | Hours | Weeks @28h/wk |
|---|-------|------:|---------------:|
| 0 | Python & Tooling Foundations | 70 | 2.5 |
| 1 | Mathematical Foundations | 140 | 5.0 |
| 2 | Data Analysis & SQL | 85 | 3.0 |
| 3 | DSA for Big-Tech Interviews | 200 | 7.1 |
| 4 | Classical Machine Learning | 160 | 5.7 |
| 5 | Deep Learning Foundations | 140 | 5.0 |
| 6 | Modern DL / NLP / Generative AI | 150 | 5.4 |
| 7 | MLOps & Production ML | 105 | 3.75 |
| 8 | Big Data & Distributed Systems | 85 | 3.0 |
| 9 | Statistics, A/B Testing & Causal Inference | 70 | 2.5 |
| 10 | ML System Design | 80 | 2.9 |
| 11 | Portfolio, Projects & Competitions | 165 | 5.9 |
| 12 | Interview Preparation (Final Sprint) | 130 | 4.6 |
| | **TOTAL** | **1,580** | **~56.4 weeks (~13 months)** |

> Phases 0–2 build the base. Phases 3–10 are the technical core (can be reordered slightly, e.g. doing DSA in parallel with Phase 1–2 in small daily doses instead of as one block). Phases 11–12 are best treated as overlapping with everything before them — start a project as soon as Phase 4 ends, and start light interview prep once Phase 6 ends.

---

## Phase 0: Python & Tooling Foundations
**Goal by end of phase:** Write idiomatic Python fluently and manipulate numerical/tabular data without constantly looking things up — the baseline fluency every later phase assumes.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **Python Fundamentals**<br>– syntax, data structures, OOP<br>– comprehensions, generators, decorators<br>– error handling, typing | Core language fluency; Python's idioms (comprehensions, generators) differ a lot from JS, so this isn't optional even with your JS background. | 25 |
| **Tooling & Environment**<br>– venv/conda, pip<br>– Jupyter/Colab<br>– Git workflows for ML projects | Standard ML dev environment setup — notebooks for exploration, environments for reproducibility. | 10 |
| **NumPy**<br>– arrays, broadcasting<br>– vectorized operations, indexing | The numerical backbone of the entire Python ML stack; vectorization is the mental shift from loop-based JS thinking. | 15 |
| **Pandas**<br>– DataFrames, cleaning<br>– merging/joining, groupby, pivoting | The tool you'll use constantly for loading, cleaning, and reshaping data before any modeling happens. | 20 |

**Phase total: 70 hours (~2.5 weeks)**

---

## Phase 1: Mathematical Foundations
**Goal by end of phase:** Understand *why* ML algorithms work, not just how to call `.fit()` — this is what separates big-tech-level candidates from API-callers in interviews and on the job.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **Linear Algebra**<br>– vectors, matrices, matrix multiplication<br>– eigenvalues/eigenvectors<br>– SVD, matrix decomposition | The language ML is written in — embeddings, PCA, neural net weights, and recommendation systems are all matrix operations. | 35 |
| **Calculus**<br>– derivatives, partial derivatives<br>– chain rule, gradients<br>– Jacobians, Hessians | Needed to understand how models learn — backpropagation is just the chain rule applied repeatedly. | 25 |
| **Probability Theory**<br>– distributions (normal, binomial, Poisson)<br>– Bayes' theorem<br>– expectation, variance, joint/conditional probability | Underlies almost every ML model's assumptions, from Naive Bayes to uncertainty estimation. | 30 |
| **Statistics**<br>– hypothesis testing, confidence intervals<br>– p-values, MLE<br>– sampling theory | Lets you reason about whether results are real or noise — critical for both modeling and A/B testing later. | 30 |
| **Optimization**<br>– gradient descent variants<br>– convexity<br>– constrained optimization, Lagrange multipliers | Every model "learns" via an optimization process; understanding it demystifies training instability and convergence issues. | 20 |

**Phase total: 140 hours (~5 weeks)**

---

## Phase 2: Data Analysis & SQL
**Goal by end of phase:** Take a raw, messy dataset and turn it into clean, well-understood data with a clear story — the actual day-to-day job of a data scientist before any modeling starts.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **SQL Mastery**<br>– joins, window functions<br>– CTEs, subqueries<br>– query optimization, indexing basics | The single most-used tool in DS/analytics interviews and the actual job — most companies test SQL harder than ML theory. | 30 |
| **Exploratory Data Analysis & Visualization**<br>– Matplotlib, Seaborn, Plotly<br>– distribution analysis, outlier detection | Turns raw numbers into visual understanding; also how you communicate findings to non-technical stakeholders. | 25 |
| **Data Cleaning & Feature Engineering Basics**<br>– missing values, encoding categorical data<br>– scaling, outlier handling | Real-world data is dirty; this is the unglamorous 70% of actual DS work. | 20 |
| **Data Storytelling**<br>– structuring insights, dashboards basics | Translating analysis into decisions — a skill that's underrated but heavily weighted in DS performance reviews. | 10 |

**Phase total: 85 hours (~3 weeks)**

---

## Phase 3: Data Structures & Algorithms (Big-Tech Interview Requirement)
**Goal by end of phase:** Pass the coding round at any FAANG-tier company — ML/DS roles at big tech still gate on general software engineering coding ability, not just ML knowledge.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **Core Data Structures**<br>– arrays, strings, linked lists<br>– trees, graphs, hashmaps, heaps | The vocabulary every coding interview problem is built from. | 60 |
| **Algorithmic Patterns**<br>– dynamic programming, two pointers<br>– sliding window, backtracking<br>– graph traversal (BFS/DFS), greedy | The reusable problem-solving patterns that let you recognize "I've seen this shape before" in a new problem. | 60 |
| **Deliberate Practice**<br>– 150–200 medium/hard problems<br>– timed mock practice | Volume + repetition under time pressure is what actually builds interview speed, not just understanding concepts. | 80 |

**Phase total: 200 hours (~7 weeks)**
*Tip: this phase doesn't have to be a single block — running 3–4 problems a day in parallel with Phases 1–2 works well and prevents this from feeling like a slog.*

---

## Phase 4: Classical Machine Learning
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

**Phase total: 160 hours (~5.7 weeks)**

---

## Phase 5: Deep Learning Foundations
**Goal by end of phase:** Understand and implement neural networks from first principles in PyTorch, including image and sequence models — the foundation for everything in Phase 6.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **Neural Network Fundamentals**<br>– perceptrons, activation functions<br>– forward pass, backpropagation | The actual mechanics of how a neural net learns — not just calling `.fit()`, but knowing what's happening underneath. | 25 |
| **Training Deep Networks**<br>– loss functions, optimizers (SGD, Adam)<br>– dropout, batch normalization, regularization | Why training sometimes fails (vanishing gradients, overfitting) and how to fix it. | 25 |
| **PyTorch**<br>– tensors, autograd<br>– `nn.Module`, custom training loops | The dominant framework at big tech research/ML teams; fluency here is assumed in interviews. | 35 |
| **Convolutional Neural Networks (CNNs)**<br>– convolutions, pooling<br>– architectures (ResNet), image classification | The standard architecture for any vision task, and a common interview/take-home topic. | 30 |
| **RNNs / LSTMs / GRUs**<br>– sequence modeling fundamentals<br>– vanishing gradient problem in sequences | The classical approach to sequential data — still useful conceptually even though transformers have largely replaced it. | 25 |

**Phase total: 140 hours (~5 weeks)**

---

## Phase 6: Modern Deep Learning, NLP & Generative AI
**Goal by end of phase:** Be conversant in the architecture and practical use of transformers and LLMs — non-negotiable for any 2026 big-tech ML role, regardless of specialization.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **Transformer Architecture**<br>– self-attention, multi-head attention<br>– positional encoding | The architecture behind essentially every modern state-of-the-art model — deeply tested in interviews now. | 30 |
| **NLP Pipeline**<br>– tokenization, embeddings<br>– word2vec/GloVe, transfer learning | The pre-transformer NLP toolkit, still useful for understanding why transformers were such a leap. | 25 |
| **Pretrained Models & Fine-Tuning**<br>– BERT, GPT-family architectures<br>– Hugging Face ecosystem (transformers, datasets) | The practical, job-relevant skill of adapting existing large models instead of training from scratch. | 35 |
| **LLMs & Generative AI**<br>– prompting strategies<br>– retrieval-augmented generation (RAG)<br>– fine-tuning & evaluating LLMs | The fastest-growing area of big tech ML hiring right now — directly relevant given your study-tool project experience with Gemini. | 35 |
| **Computer Vision (Advanced)**<br>– object detection, segmentation<br>– vision transformers (ViT) | Optional depth depending on whether you lean CV vs NLP, but useful breadth for general ML interviews. | 25 |

**Phase total: 150 hours (~5.4 weeks)**

---

## Phase 7: MLOps & Production ML Systems
**Goal by end of phase:** Take a trained model and actually ship it as a reliable production service — this is the "ML Engineer" half of the role, and where your full-stack background gives you a real head start.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **Model Deployment**<br>– FastAPI/Flask model serving<br>– REST API design for inference | Turning a trained model into something other services can actually call — directly maps to your Express/Node experience. | 20 |
| **Containerization & Orchestration**<br>– Docker<br>– Kubernetes basics | Standard deployment infrastructure at any big tech company; Docker especially is assumed knowledge. | 25 |
| **CI/CD for ML**<br>– automated testing for ML code<br>– model versioning (MLflow, DVC) | ML-specific version control — tracking not just code but data and model versions together. | 20 |
| **Monitoring & Observability**<br>– data drift, model drift<br>– logging and alerting for ML systems | Models silently degrade in production; this is how you catch it before it becomes a business problem. | 15 |
| **Cloud ML Platforms**<br>– pick one: AWS SageMaker / GCP Vertex AI / Azure ML | Big tech companies run ML at cloud scale; fluency in one major platform's ML tooling is expected. | 25 |

**Phase total: 105 hours (~3.75 weeks)**

---

## Phase 8: Big Data & Distributed Systems
**Goal by end of phase:** Process datasets that don't fit on a single machine — the scale at which big tech actually operates, distinct from the Kaggle-CSV scale most courses teach.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **Distributed Computing Concepts**<br>– MapReduce, partitioning, shuffling | The theoretical basis for why Spark/Hadoop-style systems work the way they do. | 15 |
| **Apache Spark (PySpark)**<br>– DataFrames, transformations<br>– Spark MLlib pipelines | The industry-standard tool for big-data processing and distributed feature engineering. | 30 |
| **Data Engineering Basics**<br>– ETL pipelines, Apache Airflow<br>– data warehousing concepts | The pipelines that feed data to ML systems — knowing this makes you far more self-sufficient on the job. | 25 |
| **Distributed Training (Overview)**<br>– data parallelism vs. model parallelism | Conceptual understanding of how huge models get trained across many GPUs — increasingly common interview topic. | 15 |

**Phase total: 85 hours (~3 weeks)**

---

## Phase 9: Statistics, A/B Testing & Causal Inference
**Goal by end of phase:** Design and correctly interpret an experiment — this is the single most heavily tested skill in Data Scientist interviews at big tech, often more than ML algorithms themselves.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **A/B Testing Fundamentals**<br>– hypothesis testing in practice<br>– sample size & power analysis | The standard framework big tech uses to validate any product change before shipping it broadly. | 25 |
| **Experimentation Pitfalls**<br>– novelty effects, network effects<br>– multiple testing correction (Bonferroni, FDR) | Knowing the ways experiments lie to you — a favorite interview topic because it separates real practitioners from textbook readers. | 15 |
| **Causal Inference Basics**<br>– confounders, propensity score matching<br>– difference-in-differences | For when you can't run a clean A/B test and need to infer cause from observational data. | 20 |
| **Metrics Design**<br>– north-star metrics, guardrail metrics | Choosing what to measure so you don't optimize the wrong thing — a core DS/PM collaboration skill. | 10 |

**Phase total: 70 hours (~2.5 weeks)**

---

## Phase 10: ML System Design
**Goal by end of phase:** Confidently design a full ML system end-to-end on a whiteboard — the signature senior-level interview format at every major tech company.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **System Design Framework**<br>– problem framing, data, model choice<br>– evaluation, deployment, monitoring loop | A repeatable structure to approach any "design X system" interview question without freezing up. | 20 |
| **Case Studies**<br>– recommendation systems<br>– search/feed ranking<br>– fraud detection, ad click prediction | Working through the canonical big-tech ML problems builds pattern recognition for novel ones in interviews. | 40 |
| **Mock Practice**<br>– timed whiteboard-style design sessions | Practicing under interview conditions, since this skill is as much about communication as technical correctness. | 20 |

**Phase total: 80 hours (~2.9 weeks)**

---

## Phase 11: Portfolio, Projects & Competitions
**Goal by end of phase:** Have 2–3 concrete, end-to-end, defensible projects — the proof points that actually get you past resume screens and anchor your interview conversations.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **End-to-End Capstone Project**<br>– real dataset → model → deployed service | One flagship project demonstrating the full pipeline, ideally tying into your existing strengths (e.g. an ML feature inside your BTP/MTP platform, or the study-tool's AI features taken further). | 60 |
| **Kaggle Competitions**<br>– 2–3 competitions, focus on process not just leaderboard rank | Forces you to handle messy, competitive, real-world-ish data under a fixed evaluation metric. | 60 |
| **Open-Source / Writeup / Blog**<br>– contribute to an ML repo, or write up a technical project | Builds public, verifiable evidence of depth — recruiters and interviewers do check this. | 30 |
| **Resume & Profile Polish**<br>– GitHub cleanup, resume, LinkedIn | Makes sure all the above work is actually visible and well-framed to recruiters. | 15 |

**Phase total: 165 hours (~5.9 weeks)**
*Start this phase as soon as Phase 4 finishes — don't wait until everything else is "done."*

---

## Phase 12: Interview Preparation (Final Sprint)
**Goal by end of phase:** Be fully interview-ready across all four big-tech ML/DS interview pillars: coding, ML theory, system design, and behavioral.

| Topic & Sub-topics | What It Covers | Hours |
|---|---|---:|
| **DSA Mock Interviews**<br>– continued timed practice | Keeps coding speed sharp right up to actual interviews. | 40 |
| **ML Breadth & Depth Prep**<br>– conceptual Q&A across classical ML, DL, stats | The "explain X concept" and "why would you choose Y over Z" style questions common in ML interviews. | 40 |
| **ML System Design Mocks**<br>– live practice with feedback | Refining communication and structure under real interview pressure. | 20 |
| **Behavioral Interview Prep**<br>– STAR method, leadership-principle-style stories | Big tech weighs this heavily — your project experience (PQC research, full-stack systems) gives you strong raw material to shape into stories. | 15 |
| **Take-Home Assignment Practice**<br>– 1–2 simulated take-homes under time limits | Many big-tech and unicorn companies use take-homes instead of (or alongside) live coding for ML roles. | 15 |

**Phase total: 130 hours (~4.6 weeks)**

---

## Total Time Investment

| Metric | Value |
|---|---|
| Total hours | **1,580 hours** |
| Weekly commitment | 28 hours/week |
| Pure study time | **~56.4 weeks (~13 months)** |
| With realistic buffer (exams, breaks, off-weeks @ ~15-20%) | **~64–68 weeks (~15–16 months)** |

---

## How to Sequence This Realistically

1. **Phases 0–2** are sequential and foundational — do them in order.
2. **Phase 3 (DSA)** runs best in parallel, in daily small doses (e.g., 1 hr/day) alongside Phases 1–2 and 4, rather than as one isolated 7-week block — it prevents burnout and keeps the skill fresh closer to interview time.
3. **Phases 4–6** (Classical ML → Deep Learning → Modern DL/NLP) are sequential; each builds directly on the last.
4. **Phase 7 (MLOps)** is where your existing backend/deployment instincts (Socket.IO, auth, transactions, Drive integration) transfer almost directly — likely your fastest phase relative to hours budgeted.
5. **Phase 8 (Big Data)** can be deferred or trimmed if you're optimizing specifically for Data Scientist roles over ML Engineer roles — it matters more for the engineering-heavy track.
6. **Phase 9 (Statistics/A&B Testing)** matters more if you're leaning Data Scientist; **Phase 7–8 (MLOps/Big Data)** matter more if you're leaning ML Engineer. Both are included since you asked for both — but once you're a few phases in and have a sense of which you enjoy more, you can weight remaining hours accordingly.
7. **Phase 11 (Portfolio)** should start as soon as Phase 4 ends — don't wait for "complete knowledge" before building.
8. **Phase 12 (Interview Prep)** is the final 4–5 weeks before you start actually applying, but light review of Phase 3 and 10 material should continue throughout.

---

*This is a living plan — track actual hours per topic as you go and adjust the remaining estimates. Topics you move through faster (likely Phase 0, parts of Phase 7) free up time to go deeper on the topics that turn out to be harder for you (commonly Phase 1 math and Phase 10 system design).*
