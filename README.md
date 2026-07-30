# **AusRewrite‑T5: Australian English Legal Rewriting Engine**

AusRewrite‑T5 is a **hybrid symbolic–neural rewriting system** designed to convert *any English text* into **strict Australian English**, with a **formal legal register** aligned to Australian Government Style Manual conventions and AGLC‑adjacent tone.

The system combines:

- **Prolog** — rule‑based grammar, register constraints, citation validation  
- **Regex** — deterministic surface‑level transformations  
- **LLM** — semantic rewriting within symbolic constraints  

This architecture produces **high‑precision, deterministic rewrites** suitable for legal, academic, and government contexts.

---

## **1. Purpose**

AusRewrite‑T5 provides:

- Australian spelling normalisation  
- Legal‑style register enforcement  
- Deterministic grammar and punctuation rules  
- AGLC‑pattern detection and validation  
- Semantic rewriting without altering meaning  

It is designed for:

- legal drafting  
- legislative analysis  
- academic writing  
- government communication  
- controlled‑register rewriting pipelines  

---

## **2. System Architecture**





AusRewrite‑T5 uses a **three‑layer pipeline**:

### **Layer 1 — Regex Pre‑Processor**
Handles surface transformations:

- Australian spelling replacements  
- punctuation normalisation  
- contraction removal  
- citation pattern detection  
- whitespace and formatting cleanup  

### **Layer 2 — Prolog Rule Engine**
Applies structural and contextual constraints:

- grammar rules  
- legal register enforcement  
- citation validation  
- rule‑based transformations  
- constraint satisfaction  

### **Layer 3 — LLM Rewriter**
Performs semantic rewriting:

- preserves meaning  
- restructures sentences  
- applies formal tone  
- respects symbolic constraints  
- outputs deterministic legal‑style prose  

---

## **3. Features**

### **Australian Spelling**
- organisation, labour, defence  
- licence (noun) / license (verb)  
- centre, metre, colour  

### **Legal Register**
- no contractions  
- precise terminology (section, clause, subsection)  
- neutral, formal tone  
- no rhetorical or conversational phrasing  

### **Grammar & Punctuation**
- Australian quotation style  
- consistent comma/semicolon usage  
- list and section formatting  
- passive/active voice constraints  

### **Citation Awareness**
- case law pattern detection  
- legislation pattern detection  
- pinpoint references  
- AGLC‑style validation rules  

---

## **4. Workflow**

### **Input → Regex → Prolog → LLM → Prolog → Output**

1. **Regex Pre‑Processing**  
   - normalise spelling  
   - detect citations  
   - remove contractions  
   - tag legal structures  

2. **Prolog Rule Application**  
   - enforce grammar constraints  
   - validate citations  
   - apply legal register rules  
   - mark segments requiring semantic rewrite  

3. **LLM Rewrite**  
   - rewrite only marked segments  
   - preserve meaning  
   - apply formal Australian legal tone  

4. **Prolog Post‑Validation**  
   - ensure compliance with all rules  
   - check spelling, register, citations  

5. **Regex Final Cleanup**  
   - punctuation  
   - spacing  
   - formatting  

---

## **5. Example Usage**

### **Input**
```
The program will likely start next year, and the organization said they "can't confirm" the exact date.
```

### **Output**
```
The organisation stated that it cannot confirm the precise commencement date of the program, which is expected to begin next year.
```

---

## **6. Directory Structure**

```
ausrewrite-t5/
│
├── prolog/
│   ├── spelling_rules.pl
│   ├── grammar_rules.pl
│   ├── legal_register.pl
│   ├── citation_patterns.pl
│   └── validator.pl
│
├── regex/
│   ├── spelling_patterns.txt
│   ├── punctuation_patterns.txt
│   ├── citation_regex.txt
│   └── cleanup_regex.txt
│
├── model/
│   ├── tokenizer.json
│   ├── config.json
│   └── weights/
│
├── pipeline/
│   ├── preprocess.py
│   ├── prolog_interface.py
│   ├── rewrite.py
│   └── postprocess.py
│
└── README.md

```

---

## **7. Design Principles**

- **Deterministic first, probabilistic second**  
  Symbolic rules constrain the model, not the other way around.

- **Narrow domain, deep reasoning**  
  The system specialises in rewriting, not general chat.

- **Rule‑faithful outputs**  
  Every rewrite must pass Prolog validation.

- **Semantic fidelity**  
  Meaning is preserved; register and style change.

---

## **8. Roadmap**

- Add AGLC4 full citation normalisation  
- Add compression/expansion modes  
- Add plain‑language legal rewrite mode  
- Distil 7B → 500M → 100M specialist model  
- Integrate custom tokenizer for Australian legal vocabulary  

---

## **9. Related Components**

- **Prolog spelling rules**  
- **Regex pack for Australian spelling**  
- **Hybrid Prolog–LLM pipeline**  
- **100M specialist transformer blueprint**  

---


