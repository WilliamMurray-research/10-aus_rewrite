# **AusRewrite‑T5 — Formal Hypothesis Document**

## **1. Title**  
**Hypothesis: Deterministic Hybrid Symbolic–Neural Rewriting for Australian Legal English**

---

## **2. Research Context**

AusRewrite‑T5 is a proposed rewriting subsystem designed to transform arbitrary English text into strict Australian English with a formal legal register. The subsystem integrates deterministic symbolic components (Prolog rule bases and regex pattern sets) with a constrained neural rewriting model. The research question is whether this hybrid architecture can achieve deterministic, rule‑faithful, semantically accurate rewriting suitable for legal and governmental contexts.

This document defines the formal hypothesis, sub‑hypotheses, falsification conditions, and evaluation criteria.

---

## **3. Primary Hypothesis**

**H0 — Hybrid Deterministic Rewriting Hypothesis**  
A rewriting system that integrates deterministic symbolic components (Prolog rule bases and regex transformations) with a constrained neural semantic rewriting model **will reliably transform arbitrary English text into strict Australian English with a formal legal register**, while maintaining **semantic fidelity**, **deterministic behaviour**, and **rule‑faithful compliance** with Australian linguistic and legal‑style conventions.

This hypothesis asserts that symbolic constraints can successfully bound neural behaviour, producing outputs that are both expressive and predictable.

---

## **4. Sub‑Hypotheses**

### **H1 — Determinism Through Symbolic Constraints**  
If rewriting operations are constrained by declarative Prolog rules and static regex patterns, then the system will exhibit **deterministic, reproducible outputs** across identical inputs and environments.

### **H2 — Semantic Fidelity Through Constrained Neural Decoding**  
If the neural rewriting model operates only on segments pre‑validated and pre‑structured by symbolic layers, then semantic fidelity will be preserved while stylistic transformations occur.

### **H3 — Register Compliance Through Rule Enforcement**  
If legal‑style register constraints (e.g., prohibition of contractions, preference for formal terminology, avoidance of colloquialisms) are encoded as symbolic rules, then the rewritten output will consistently conform to a formal Australian legal register.

### **H4 — Orthographic Accuracy Through Static Patterns**  
If Australian spelling and punctuation conventions are encoded as deterministic regex transformations, then the system will achieve consistent orthographic correctness independent of neural model variance.

### **H5 — Citation Integrity Through Pattern Validation**  
If citation structures (case law, legislation, pinpoints) are detected and validated through symbolic pattern matching, then the system will maintain citation integrity and avoid hallucinated or malformed legal references.

---

## **5. Falsification Conditions**

The hypothesis is falsified if any of the following occur:

- The system produces **non‑deterministic outputs** for identical inputs.  
- The system introduces **semantic drift** or alters meaning.  
- The system outputs text violating Australian spelling conventions.  
- The system outputs text violating legal‑style register constraints.  
- The system produces malformed or hallucinated citations.  
- Symbolic rules fail to constrain neural behaviour in predictable ways.  

These conditions provide measurable criteria for evaluation and audit.

---

## **6. Evaluation Criteria**

The hypothesis will be evaluated using the following metrics:

### **6.1 Determinism Tests**
- repeated‑input equivalence  
- environment‑independent reproducibility  
- version‑controlled artefact stability  

### **6.2 Semantic Fidelity Tests**
- semantic similarity scoring  
- clause‑level meaning preservation  
- contradiction and omission detection  

### **6.3 Rule‑Compliance Tests**
- Prolog‑based validation of register constraints  
- regex‑based orthographic correctness checks  
- punctuation conformity analysis  

### **6.4 Citation Integrity Tests**
- pattern‑based detection  
- Prolog‑based validation  
- malformed citation identification  

### **6.5 Human Expert Review**
- legal practitioners evaluate register conformity  
- editors evaluate clarity and correctness  

---

## **7. Research Objective**

To demonstrate that a hybrid symbolic–neural rewriting system can outperform purely neural or purely rule‑based approaches in:

- determinism  
- compliance  
- semantic fidelity  
- legal‑style consistency  
- auditability  

within the domain of Australian English legal rewriting.

---

## **8. Expected Contributions**

AusRewrite‑T5 is expected to contribute:

- a reproducible hybrid rewriting architecture  
- a deterministic legal‑style rewriting pipeline  
- a modular rule base for Australian English  
- a methodology for constraining neural models with symbolic logic  
- an evaluation framework for legal‑style rewriting systems  

These contributions support broader research into deterministic language systems and controlled rewriting.

---

## **9. Related Research Artefacts**

- **Subsystem specification**  
- **Prolog rule design**  
- **Regex pattern design**  
- **Pipeline architecture**  

---

## **10. Compliance Statement**

This hypothesis document conforms to the structural and governance requirements of the Universal Project Template Framework. It may be placed under:

```
docs/research/hypotheses/
```

without altering the canonical scaffold.

---

