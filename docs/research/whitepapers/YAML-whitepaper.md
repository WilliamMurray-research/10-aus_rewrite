# **Whitepaper: Deterministic Architecture Generation via Double‑Entry YAML Ledgers and Prolog Execution Loops**

## **Abstract**

This whitepaper defines a deterministic architecture‑generation mechanism based on a **double‑entry YAML ledger** embedded within a Markdown artefact. The ledger enumerates all required architectural files and tracks their completion state. A Prolog‑based execution engine consumes this ledger, identifies the next pending artefact, clears generation context, and produces the file deterministically. The ledger is then updated, ensuring full auditability and compliance with the Universal Project Template Framework (v2.1).

This system provides a reproducible, governance‑aligned method for constructing the `architecture/` domain of a project, ensuring structural invariants, eliminating drift, and enabling automated scaffolding.

---

# **1. Introduction**

The Universal Project Template Framework (v0.0.2) defines a canonical directory structure that all projects must preserve. The `architecture/` domain is mandatory and contains formal system specifications, C4 models, data schemas, interface definitions, and evolutionary roadmaps.

However, the template does not prescribe *how* these artefacts should be generated.

This whitepaper introduces a deterministic mechanism for generating the architecture domain using:

- a **double‑entry YAML ledger** stored on disk  
- a **Prolog execution loop** that consumes the ledger  
- a **context‑resetting generation pipeline**  
- a **governance‑aligned update mechanism**  

The result is a reproducible, auditable, and fully deterministic architecture generation system.

---

# **2. System Overview**

The system consists of three components:

### **2.1 Planning Ledger (Double‑Entry YAML)**  
A Markdown file containing a YAML block that enumerates:

- every required architectural artefact  
- its current completion state (`pending` or `complete`)  

This ledger is authoritative.

### **2.2 Prolog Execution Engine**  
A Prolog program that:

1. loads the ledger  
2. identifies the next `pending` artefact  
3. clears generation context  
4. generates the artefact deterministically  
5. updates the ledger  
6. repeats until all artefacts are complete  

### **2.3 Deterministic Generation Pipeline**  
A context‑resetting mechanism ensures each file is generated independently, preventing contamination between artefacts.

---

# **3. Ledger Specification**

The ledger is stored at:

```
architecture/roadmap/build_plan.md
```

It contains a YAML block:

```yaml
files:
  - path: architecture/system/context.md
    status: pending
  - path: architecture/system/containers.md
    status: pending
  - path: architecture/system/components.md
    status: pending
  - path: architecture/data/models.md
    status: pending
  - path: architecture/data/flows.md
    status: pending
  - path: architecture/data/storage.md
    status: pending
  - path: architecture/interfaces/api.md
    status: pending
  - path: architecture/interfaces/dsl.md
    status: pending
  - path: architecture/interfaces/rendering.md
    status: pending
  - path: architecture/roadmap/evolution.md
    status: pending
  - path: architecture/roadmap/versioning.md
    status: pending
```

### **3.1 Ledger Invariants**

- The ledger must enumerate *all* required architectural artefacts.  
- The ledger must be stored in version control.  
- The ledger must be updated only by the Prolog engine.  
- Manual edits are prohibited except during planning.  
- Status values must be one of:  
  - `pending`  
  - `complete`  

### **3.2 Double‑Entry Semantics**

The ledger is “double‑entry” because:

- **Column A**: required artefact path  
- **Column B**: completion state  

This mirrors accounting ledgers: every obligation has a corresponding fulfilment state.

---

# **4. Prolog Execution Engine**

The Prolog engine is responsible for deterministic generation.

### **4.1 Execution Loop**

The loop consists of:

1. **Load Ledger**  
   Parse YAML from the Markdown file.

2. **Find Next Pending Artefact**  
   Identify the first entry with `status: pending`.

3. **Clear Context**  
   Reset all generation state, ensuring independence.

4. **Generate Artefact**  
   Produce the file at the specified path.

5. **Update Ledger**  
   Set `status: complete` for the generated artefact.

6. **Repeat**  
   Continue until no pending entries remain.

### **4.2 Determinism Guarantees**

Determinism is achieved through:

- context clearing  
- canonical templates  
- strict ordering  
- ledger‑driven execution  
- immutability of completed artefacts  

---

# **5. Generation Pipeline**

### **5.1 Context Reset**

Before generating each artefact, the engine performs:

- memory flush  
- variable reset  
- template reload  
- environment sanitisation  

This ensures each artefact is generated without influence from previous ones.

### **5.2 Artefact Templates**

Each architectural file is generated from a canonical template, e.g.:

- C4 Level 1 context diagram  
- C4 Level 2 container diagram  
- DSL specification  
- rendering rules  
- data flow diagrams  
- storage invariants  

Templates may be parameterised but must be deterministic.

---

# **6. Governance Alignment**

The system aligns with the Universal Project Template Framework:

### **6.1 Structural Invariants**

The template states:

> “The structure itself is part of the project’s governance.”

The ledger enforces this by enumerating all required artefacts.

### **6.2 Extension Policy**

The template permits:

- adding new directories  
- adding new documents  

The ledger supports this by allowing new entries to be appended.

### **6.3 Auditability**

The ledger provides:

- a historical record of generation  
- a reproducible build plan  
- a compliance mechanism  

---

# **7. Failure Modes and Recovery**

### **7.1 Ledger Corruption**

If the ledger becomes invalid YAML:

- Prolog halts  
- human intervention required  
- ledger must be repaired manually  

### **7.2 Partial Generation**

If generation fails mid‑loop:

- the ledger remains unchanged  
- the artefact remains `pending`  
- the loop can be resumed safely  

### **7.3 Drift Detection**

If a file exists but ledger says `pending`:

- Prolog overwrites the file  
- ledger is updated  
- determinism preserved  

---

# **8. Security Considerations**

### **8.1 Integrity**

Ledger integrity is critical.  
It must be protected by:

- version control  
- append‑only commit policies  
- governance constraints  

### **8.2 Confidentiality**

The ledger itself is non‑proprietary.  
Generated artefacts may contain proprietary content depending on project domain.

### **8.3 Execution Safety**

Prolog must not execute arbitrary paths.  
Paths must be validated against the canonical template.

---

# **9. Conclusion**

This deterministic architecture‑generation system provides:

- reproducible architectural scaffolding  
- governance‑aligned structural compliance  
- auditability through double‑entry ledgers  
- deterministic generation via Prolog  
- independence of artefacts through context clearing  

It is suitable for:

- distributed plausibility pipelines  
- DSL‑driven architecture generation  
- automated project instantiation  
- compliance‑critical environments  

This mechanism transforms the architecture domain from a static directory into a **governed, deterministic, self‑generating system**.

---

