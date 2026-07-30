# **AusRewrite‑T5 Technical Whitepaper**  
*A Hybrid Symbolic–Neural System for Deterministic Australian‑English Legal Rewriting*

---

## **Abstract**

AusRewrite‑T5 is a hybrid rewriting subsystem designed to transform arbitrary English text into strict Australian English with a formal legal register. The system integrates deterministic symbolic components (Prolog rule bases and regex pattern sets) with a constrained neural rewriting model. This architecture ensures semantic fidelity, rule‑faithful transformations, and deterministic behaviour suitable for legal, governmental, and compliance‑critical environments.

The subsystem is engineered to operate within the Universal Project Template Framework, respecting its structural invariants, governance constraints, and operational domains.

---

## **1. Introduction**

Legal and governmental writing requires:

- strict adherence to Australian spelling conventions  
- consistent formal register  
- precise grammatical structures  
- citation awareness  
- deterministic transformations  
- auditability and reproducibility  

General‑purpose language models cannot reliably satisfy these constraints. They exhibit non‑deterministic behaviour, inconsistent register control, and limited compliance with jurisdiction‑specific linguistic rules.

AusRewrite‑T5 addresses these limitations through a hybrid architecture combining:

- **symbolic rule enforcement**  
- **pattern‑based preprocessing**  
- **neural semantic rewriting**  
- **post‑validation and cleanup**  

This whitepaper describes the system’s architecture, rule design, execution pipeline, and operational guarantees.

---

## **2. System Overview**

AusRewrite‑T5 is composed of three cooperating layers:

1. **Regex Preprocessing Layer**  
   Deterministic surface‑level transformations.

2. **Prolog Rule Engine**  
   Grammar, register, and citation constraints.

3. **Neural Rewriting Model**  
   Semantic restructuring under symbolic constraints.

These layers form a pipeline that ensures both correctness and expressiveness.

---

## **3. Design Goals**

### **3.1 Determinism**
Outputs must be reproducible across runs, inputs, and environments.

### **3.2 Semantic Fidelity**
The system must preserve meaning while altering style, register, and spelling.

### **3.3 Rule Compliance**
All outputs must comply with:

- Australian spelling conventions  
- legal‑style register constraints  
- punctuation norms  
- citation patterns  

### **3.4 Auditability**
Symbolic components must be inspectable, testable, and version‑controlled.

### **3.5 Extensibility**
Rules must be modular and capable of incremental refinement.

---

## **4. Architectural Components**

### **4.1 Regex Layer (Static Patterns)**  
Located in:

- `assets/regex/`

This layer performs:

- spelling normalisation  
- punctuation correction  
- contraction removal  
- citation detection  
- whitespace cleanup  

Regex is chosen for:

- deterministic behaviour  
- high performance  
- ease of testing  
- suitability for surface transformations

### **4.2 Prolog Rule Engine (Symbolic Logic)**  
Located in:

- `assets/prolog/`

Prolog provides:

- declarative grammar rules  
- legal register constraints  
- citation validation  
- rule‑based transformations  
- constraint satisfaction  

Symbolic logic ensures:

- interpretability  
- deterministic rule application  
- strict compliance with linguistic constraints

### **4.3 Neural Rewriting Model (Semantic Layer)**  
Located in:

- `assets/model/`

The model performs:

- semantic restructuring  
- clause reordering  
- ambiguity resolution  
- tone enforcement  

The model is constrained by:

- Prolog rule outputs  
- regex preprocessing  
- post‑validation checks  

This prevents hallucination and ensures rule‑faithful rewriting.

---

## **5. Processing Pipeline**

Located in:

- `src/pipeline/`

The pipeline consists of four stages:

### **5.1 Preprocessing**
`preprocess.py`

- apply regex transformations  
- detect citations  
- tag legal structures  
- normalise spelling  
- remove contractions  

### **5.2 Symbolic Rule Application**
`prolog_interface.py`

- load Prolog rule bases  
- enforce grammar constraints  
- validate citations  
- apply register rules  
- mark segments requiring semantic rewrite  

### **5.3 Neural Rewrite**
`rewrite.py`

- rewrite marked segments  
- preserve meaning  
- enforce formal tone  
- maintain Australian spelling  
- avoid informal phrasing  

### **5.4 Postprocessing**
`postprocess.py`

- reapply regex cleanup  
- validate rule compliance  
- ensure deterministic punctuation  
- final formatting  

---

## **6. Rule Design**

### **6.1 Spelling Rules**
Examples:

- organisation ← organization  
- labour ← labor  
- defence ← defense  
- licence (noun) vs license (verb)  

### **6.2 Register Rules**
- no contractions  
- no colloquialisms  
- prefer “section”, “subsection”, “clause”  
- avoid rhetorical phrasing  

### **6.3 Grammar Rules**
- subject–verb agreement  
- punctuation normalisation  
- quotation mark rules  
- list formatting  

### **6.4 Citation Rules**
- case law patterns  
- legislation patterns  
- pinpoint references  
- validation logic  

---

## **7. Determinism Guarantees**

AusRewrite‑T5 ensures determinism through:

- static regex patterns  
- declarative Prolog rules  
- constrained neural decoding  
- post‑validation enforcement  
- version‑controlled artefacts  
- append‑only logs for pipeline behaviour  

This makes the subsystem suitable for:

- legal drafting  
- governmental communication  
- compliance workflows  
- archival rewriting tasks  

---

## **8. Security & Risk Considerations**

Although AusRewrite‑T5 is not part of the proprietary `risk/` or `security/` domains, it interacts with them indirectly:

- deterministic rewriting reduces risk of semantic drift  
- symbolic rules reduce attack surface for prompt‑based manipulation  
- auditability supports forensic analysis  
- versioning supports reproducibility  

All risk and security artefacts remain confined to:

- `risk/`  
- `security/`

as required by the Universal Project Template Framework.

---

## **9. Governance Alignment**

AusRewrite‑T5 respects all structural invariants:

- no modification of canonical directories  
- implementation confined to `src/`  
- static artefacts confined to `assets/`  
- subsystem specification can be added under `docs/` or root only by extension  
- no renaming or removal of existing branches  

This ensures full compliance with the project’s governance model.

---

## **10. Roadmap**

Planned enhancements:

- AGLC4 full citation normalisation  
- compression/expansion modes  
- plain‑language legal rewrite mode  
- multi‑variant register control  
- distillation to a 100M specialist model  
- Prolog rule expansion for legislative drafting  

---

## **11. Conclusion**

AusRewrite‑T5 provides a deterministic, rule‑faithful rewriting subsystem suitable for legal and governmental contexts. Its hybrid symbolic–neural architecture ensures semantic fidelity, compliance with Australian linguistic standards, and auditability. The system integrates cleanly into the Universal Project Template Framework without violating structural invariants.

---

