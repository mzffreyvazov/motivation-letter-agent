# Motivation Letter – Türkiye Scholarships 2026

> **Note:** Replace `[TARGET UNIVERSITY]` and `[TARGET PROGRAM]` with your actual Turkish university/program preferences before submission.

---

During my internship at [GOVERNMENT RESEARCH/INNOVATION CENTER], [HOME COUNTRY]'s Centre for the Fourth Industrial Revolution, I was building a RAG chatbot for [HOME COUNTRY]'s official legal platform, a system that had to retrieve and respond to legal queries in [NATIVE/LOCAL LANGUAGE]. The engineering was straightforward. The problem was not: reliable [NATIVE/LOCAL LANGUAGE] embedding models barely existed. A language spoken by millions of people, with a rich literary tradition, and the NLP infrastructure to support it was almost nonexistent. That discovery focused everything I had been working toward.

I am a final-year BSc Computer Science student at [HOME UNIVERSITY], graduating in July 2026. Beyond my degree, I completed intensive training through the [GOVERNMENT INNOVATION AGENCY]: the Advanced Computer Science Program with [INTERNATIONAL PARTNER UNIVERSITY], and the Data Science Program with [ORGANIZATION] and [TECH ACADEMY], where I finished among the top 11 performers and earned a [CLOUD PROVIDER] Data Science Professional certification. These programs transformed my understanding of applied AI at a professional level, and the chatbot I deployed at [GOVERNMENT RESEARCH/INNOVATION CENTER] was the direct product of that combined foundation.

My engagement with the field extends beyond code. I placed second in the university programming olympiad at [HOME UNIVERSITY], which sharpened my instinct for collaborative problem-solving under pressure. I also built [COMMUNITY PLATFORM], a community discovery platform, driven by a social challenge rather than a technical one: the difficulty of finding genuine intellectual community in a fragmented digital landscape. Through [GOVERNMENT INNOVATION AGENCY] cohorts, I mentored peers on their first machine learning projects, and found that teaching consistently deepened my own understanding.

Turkey is not an arbitrary choice. [NATIVE/LOCAL LANGUAGE] and Turkish are Turkic sister languages, and I can engage with Turkish academic life with a linguistic ease that would take years to build elsewhere. [TARGET UNIVERSITY]'s dedicated Artificial Intelligence Institute and MSc in Artificial Intelligence and Data Engineering offer precisely the research environment I need. The university's existing joint programmes with [HOME COUNTRY] institutions reflect a genuine bilateral academic commitment, and Turkey's broader AI ecosystem, supported by TÜBİTAK, makes it one of the strongest environments in the region for this field.

Upon graduating, I intend to return to [HOME COUNTRY] and contribute to the National AI Strategy [YEARS], which prioritises sovereign AI infrastructure and language technologies for [NATIVE/LOCAL LANGUAGE]. The gap I encountered at [GOVERNMENT RESEARCH/INNOVATION CENTER] is not a minor technical inconvenience; it is a structural deficit affecting information access for millions of people. Closing it requires deep expertise and strong institutional networks. Graduate study in Turkey, supported by the Türkiye Scholarship, builds both, and the ties between our two countries ensure that what I learn there will translate into direct impact at home.

**[APPLICANT NAME]**

---

## Research Proposal

### 1. Subject of Study

Training Open-Source [NATIVE/LOCAL LANGUAGE] Embedding Models for Retrieval-Augmented Generation in Low-Resource Turkic Languages

---

### 2. Research Question

Can a publicly released open-source [NATIVE/LOCAL LANGUAGE] embedding model achieve competitive retrieval performance in RAG systems?

---

### 3. Analysis of the Problem

[NATIVE/LOCAL LANGUAGE] is a low-resource language with no publicly available domain-specific embedding model suited for semantic retrieval. Retrieval-Augmented Generation (RAG) systems depend critically on embedding quality: the model that converts text into vector representations determines whether relevant documents are retrieved at all. Multilingual models such as mBERT and LaBSE include [NATIVE/LOCAL LANGUAGE] but are trained predominantly on high-resource languages, producing embeddings that perform poorly on language-specific retrieval tasks, particularly in legal and administrative domains.

This study examines whether training an open-source [NATIVE/LOCAL LANGUAGE] embedding model from a curated domain corpus can close this gap. The conceptual framework draws on the encoder architecture of transformer models, contrastive learning for sentence embedding, and the retrieval pipeline in RAG systems. A key design constraint is that the trained model and all associated resources — corpus, training code, evaluation benchmarks — are released publicly under open licences, making them reusable by any developer or researcher working on low-resource NLP. The expected output is a fully open-source [NATIVE/LOCAL LANGUAGE] embedding model evaluated against multilingual baselines on a purpose-built retrieval benchmark in the legal domain.

---

### 4. Research Method

The study proceeds in three phases.

**Phase 1 — Corpus construction:** Legal, administrative, and news texts in [NATIVE/LOCAL LANGUAGE] will be collected from government portals (including [LEGAL PLATFORM]), digital libraries, and news archives, targeting approximately 1–2 GB of cleaned text.

**Phase 2 — Open-source model training:** Starting from XLM-R as a publicly available multilingual base, domain-adaptive continued pre-training will be performed on the domain corpus using masked language modelling. This will be followed by contrastive fine-tuning on a labelled sentence-similarity dataset. Labelled pairs will be created via translation of existing English NLP benchmarks validated by native speakers, supplemented by semi-automatic generation from structured legal documents. All model weights, training scripts, and hyperparameter configurations will be versioned and released on Hugging Face.

**Phase 3 — Evaluation:** The adapted model will be benchmarked against mBERT, LaBSE, and multilingual embedding APIs on retrieval tasks using top-k passage retrieval accuracy, mean reciprocal rank (MRR), and NDCG. Ablation studies will isolate the contribution of domain-adaptive pre-training versus contrastive fine-tuning.

---

### 5. Preliminary Answer to the Research Question

The preliminary hypothesis is that an open-source [NATIVE/LOCAL LANGUAGE] embedding model trained via domain-adaptive continued pre-training will yield statistically significant improvements in retrieval accuracy over off-the-shelf multilingual models, particularly in legal and administrative doma