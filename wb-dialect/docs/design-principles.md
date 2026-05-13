# WB-Dialect Design Principles — Extended Rationale

## DP-01: Human-Machine Hybrid

**Problem:** Existing knowledge representation systems force a choice
between human readability (natural language, markdown) and machine
processability (OWL, RDF, JSON-LD). Neither extreme serves the
emerging need of individuals who want to structure their cognitive
models for AI collaboration.

**Decision:** Use YAML as the base format, augmented with structural
conventions (mandatory sections, naming conventions, ID systems) that
enable machine parsing without sacrificing human readability.

**Trade-off:** YAML's hierarchical structure may not adequately represent
all knowledge types (e.g., highly relational or temporal knowledge).
This is accepted as a known limitation.

## DP-02: Separation of Concerns

**Problem:** A single monolithic file containing all cognitive knowledge
becomes unwieldy for both human authoring and AI processing.

**Decision:** Each WB-Dialect file addresses a single domain or module.
Cross-references between files use explicit links (URLs, file paths).

**Trade-off:** Requires the author to decompose knowledge into modules,
which adds cognitive overhead during authoring.

## DP-03: Hierarchy of Abstraction

**Problem:** Knowledge has multiple levels of abstraction. A framework
may have philosophical foundations (abstract), operational rules
(structural), and concrete applications (concrete). Mixing these
levels in a flat structure creates confusion.

**Decision:** Organize content from conceptual (definitions, principles)
through structural (rules, engines) to concrete (examples, templates).
This mirrors expert knowledge organization and enables AI systems to
parse at the appropriate level of detail.

**Trade-off:** Requires the author to consciously organize content by
abstraction level, which may not feel natural for all types of knowledge.

## DP-04: Examples as Tests

**Problem:** Without concrete examples, both human readers and AI systems
may misinterpret abstract rules. A specification without examples is
like code without tests — it may look correct but cannot be validated.

**Decision:** Every WB-Dialect file must include concrete examples with
a fixed schema (id, name, input, processing, output). These examples
serve dual functions:
1. **Documentation:** They show the reader how rules apply to real cases.
2. **Calibration:** They provide ground truth for AI interpretation.
   If an AI system cannot reproduce the expected output from the given
   input and processing steps, the specification is ambiguous.

**Inspiration:** Test-driven development (Beck, 2003) — write the test
first, then write the code. In WB-Dialect: write the example first,
then verify that the rules produce the expected result.

**Trade-off:** Requires the author to invest additional effort in
creating concrete examples. This is considered a feature, not a bug:
the effort of creating examples forces clarity of thought.

## References

- Beck, K. (2003). *Test Driven Development: By Example*. Addison-Wesley.
- McGuinness, D. L. & Van Harmelen, F. (2004). OWL Web Ontology Language Overview. W3C Recommendation.
- Lassila, O. & Swick, R. (1999). Resource Description Framework (RDF) Model and Syntax Specification. W3C.
- Preston-Werner, T. (2013). Semantic Versioning 2.0.0. semver.org.
