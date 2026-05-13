# WB-Dialect v1.0.1

**A formal specification language for structuring human-AI cognitive collaboration.**

[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)
[![Version](https://img.shields.io/badge/version-1.0.1-blue.svg)]()
[![Status](https://img.shields.io/badge/status-stable-brightgreen.svg)]()

---

## What is WB-Dialect?

WB-Dialect is a YAML-based specification language designed to represent
human cognitive models in a format that is simultaneously **readable by
humans** and **processable by AI systems**.

It addresses a gap between:

| Approach | Strength | Limitation |
|---|---|---|
| **Prompt engineering** | Accessible, flexible | Non-reusable, unstructured, no schema |
| **Formal ontology languages** (OWL, RDF) | Rigorous, machine-readable | Human-inaccessible, requires expertise |
| **WB-Dialect** | **Human-authorable + machine-processable** | **Structured, reusable, with built-in validation** |

WB-Dialect occupies the space between informal human communication and
formal machine representation.

## Design Principles

| ID | Principle | Description |
|---|---|---|
| DP-01 | Human-Machine Hybrid | Legible by humans without technical training; processable by AI without prior context |
| DP-02 | Separation of Concerns | Each file addresses a single domain or module |
| DP-03 | Hierarchy of Abstraction | Conceptual → Structural → Concrete |
| DP-04 | Examples as Tests | Concrete cases validate AI interpretation (analogous to test-driven development) |

## File Structure

Every WB-Dialect file follows this mandatory structure:

```yaml
meta:
  formato: "wb_dialect"
  subformato: "wb_[module]"
  versao: "MAJOR.MINOR.PATCH"
  autor: "Author"
  descricao: "Description"

CONSTANTES:
  CONSTANT_NAME: value

definicoes:
  concept: "Formal definition"

[module_name]:
  # Primary module content

exemplos:
  - id: "PREFIX-NNN"
    nome: "Example name"
    entrada: {input}
    processamento: [steps]
    saida: output

templates:
  template_name: "Reusable structure"
```

## Naming Conventions

| Element | Convention | Example |
|---|---|---|
| Constants | SCREAMING_SNAKE_CASE | MAX_CONTEXT_SWITCH |
| Variables | snake_case | nivel_de_lastro |
| Rule IDs | PREFIX-NNN | DEC-001, R001, EX001 |
| Indentation | 2 spaces | YAML standard |
| Versioning | Semantic Versioning | MAJOR.MINOR.PATCH |

## Implementations

### Strata
An integrated existentialist and game-theoretic framework for autonomous
decision-making under constraint. Introduces the original concept of
**lastro (ballast)** — a multidimensional measure of autonomy capacity.

### The Manual
A cognitive operating system for neurodivergent self-management, derived
from neuropsychological assessment (ASD Level 1). Translates clinical
diagnosis into executable decision rules, execution protocols, and
failure recovery mechanisms.

## Scope

**Covers:**
- Structuring complex cognitive knowledge (philosophical, clinical, strategic)
- Enabling AI systems to interpret and reason about human frameworks
- Providing validation through embedded concrete examples

**Does not cover:**
- Replacement of formal ontology languages (OWL, RDF)
- Automatic knowledge generation (content is human-authored)
- Formal mathematical validation (validation is example-based)
- GUI or visualization tools

## Academic Paper

For the full academic treatment, see the preprint:

> Barros, W. (2026). WB-Dialect: A Formal Specification Language for
> Structuring Human-AI Cognitive Collaboration. SSRN.
> [DOI: pending]

## Quick Start

1. Clone this repository
2. Read `spec/wb-dialect-v1.0.1.yaml` — the full specification
3. Read `examples/wb-strata-v0.1.1.yaml` — a philosophical implementation
4. Read `examples/wb-manual-v2.1.1.yaml` — a clinical implementation
5. Create your own WB-Dialect file following the structure above

## Citation

```bibtex
@software{barros2026dialect,
  author    = {Barros, Wagner},
  title     = {WB-Dialect: A Formal Specification Language for
               Structuring Human-AI Cognitive Collaboration},
  year      = {2026},
  version   = {1.0.1},
  url       = {https://github.com/wb-framework/wb-dialect},
  license   = {CC BY-SA 4.0}
}
```

## License

CC BY-SA 4.0

— Copyright (c) 2024-2026 Wagner Barros

---

## Author

**Wagner Barros**  
Independent Researcher  
Brazil

---

*"I didn't create a language. I created a way for my brain and
machines to speak the same language."*
