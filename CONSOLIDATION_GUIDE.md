# Roadmap Consolidation Guide

This document provides a consolidated structure and best practices for TauCeti roadmaps, based on
the improvements made to three representative roadmaps: StableMatching, RibbonKnots, and
BoltzmannGradLimitAndLanford.

## Standard Roadmap Structure

Each roadmap should follow this structure:

### 1. Summary
- One-sentence description of what the roadmap builds
- List of end theorems with citations

### 2. Scope and Ownership
- What is owned by this roadmap
- What is explicitly NOT in this roadmap
- Dependencies on other roadmaps

### 3. Conventions
- Notation and terminology
- Mathematical conventions specific to this area
- Witness examples

### 4. Exact Supplier Contracts
- From Mathlib: specific imports and theorems
- From Tau Ceti: specific modules and definitions
- From other roadmaps: specific sections and gaps

### 5. How to Read the Build
- Layer-by-layer description
- Dependencies between layers

### 6. Layers (0, 1, 2, ...)
Each layer contains:
- Section title with layer number
- **Target**: What to prove/build
- **API**: Public interface (definitions, lemmas)
- **Needs**: Dependencies (previous layers, external)
- **Checks**: Concrete verification steps
- **Examples**: Illustrative examples
- **Dependencies**: External requirements

### 7. Downstream Consumers
- Known roadmaps that depend on this one
- Potential future consumers

### 8. Research Context
- Historical development
- Connections to other areas of mathematics
- Applications

### 9. Open Problems
**NEW: Specific Mathematical Problem Statements**

This section should contain concrete, well-formulated mathematical problems that:
- Are directly related to the roadmap's mathematics
- Could potentially be formalized in Lean
- Are stated as precise mathematical statements (conjectures, theorems to prove, characterizations)
- Include proper attribution when known

Example format:
```
1. **Problem Name (Author Year)**: Prove or disprove: [precise mathematical statement].
   [Optional: Additional context, known partial results, references]
```

### 10. Provenance (Optional)
- Existing formalizations outside Tau Ceti
- Secondary sources

### 11. References
- Primary sources (theorem-level citations)
- Secondary sources (surveys, textbooks)

### 12. Additional Bibliography (NEW)
- Extended reading list
- Related works
- Historical papers
- Recent developments

## Consolidation Principles

### 1. Modularity
- Each roadmap should be self-contained
- Dependencies should be explicitly declared
- Shared mathematical structures should be identified

### 2. Consistency
- Use consistent notation across related roadmaps
- Follow the same section structure
- Maintain uniform citation style

### 3. Verifiability
- Include concrete checks that can be automated
- Provide examples that can be tested
- Reference specific theorem numbers from sources

### 4. Maintainability
- Keep roadmaps focused on specific mathematical areas
- Avoid duplication with other roadmaps
- Clearly state scope boundaries

## Best Practices Demonstrated

### From StableMatching (Combinatorics)
- Clear separation of layers (0: markets, 1: existence, 2: lattice, 3: incentives)
- Specific mathematical problem statements (Irving's conjecture, Roth's conjecture)
- Comprehensive bibliography spanning algorithmic and economic perspectives

### From RibbonKnots (Geometric Topology)
- Explicit supplier contracts with Tau Ceti and other roadmaps
- Gap declarations for missing dependencies
- Specific problem statements (slice-ribbon conjecture, invariant preservation)

### From BoltzmannGradLimitAndLanford (Kinetic Theory)
- Detailed conventions section with mathematical notation
- Clear layer structure (1: BBGKY, 2: Boltzmann hierarchy, 3: bounds, 4: trees, 5: convergence)
- Specific problem statements (Lanford extension, global existence, boundary conditions)

### From CubicSzegoEquation (PDEs/Integrable Systems)
- Focused scope on a specific PDE
- Clear connection to operator theory (Hankel operators)
- Specific problem statements (global well-posedness, norm growth, complete integrability)
- Comprehensive bibliography spanning PDEs, operator theory, and harmonic analysis

## Cross-Roadmap Connections

While the three example roadmaps are in different mathematical domains, they share:

1. **Structural Patterns**:
   - Layered organization
   - Clear dependency management
   - Separation of concerns

2. **Documentation Patterns**:
   - Summary at the top
   - Research context section
   - Open problems with specific statements
   - Additional bibliography

3. **Quality Assurance**:
   - Checks section with concrete tests
   - Examples section with worked examples
   - Explicit needs declarations

## Template for New Roadmaps

```markdown
# Roadmap: [Area Name]

**Summary.** [One-sentence description of what this roadmap builds and its end theorems].

## Scope and Ownership

Owned here: [list of definitions, theorems, algorithms]

Not owned here: [list of related topics not covered]

## Conventions

- **Notation**: [describe notation]
- **Terminology**: [define key terms]
- Witness: [concrete example]

## Exact Supplier Contracts

### From Mathlib
- [specific imports]

### From Tau Ceti
- [specific modules]

### From [Other Roadmap]
- [specific sections]

### Gaps
- [gap declarations]

## How to Read the Build

[Describe the layer structure and dependencies]

## Layer 0: [Name]

### 0.1 [Target]

[Define target]

*Needs:* [dependencies]

**Checks.**
- [check 1]
- [check 2]

### Examples
- [example 1]

### Dependencies
[external dependencies]

## [Additional Layers...]

## Downstream Consumers

[List known and potential consumers]

## Research Context

[Historical context, connections to other areas]

## Open Problems

### Specific Mathematical Problem Statements

1. **Problem 1 (Author Year)**: Prove or disprove: [precise statement].
2. **Problem 2**: [precise statement].
...

## Provenance (Optional)

[Existing formalizations]

## References

[Primary sources]

## Additional Bibliography

[Extended reading list]
```

## Consolidation Checklist

When creating or reviewing a roadmap:

- [ ] Does it follow the standard structure?
- [ ] Are layers clearly defined and ordered?
- [ ] Are dependencies explicitly declared?
- [ ] Are there concrete checks?
- [ ] Are there specific mathematical problem statements?
- [ ] Is the bibliography comprehensive?
- [ ] Are there examples?
- [ ] Is the scope clearly bounded?

## Maintenance

This guide should be updated as new patterns emerge and best practices evolve.
The four example roadmaps (StableMatching, RibbonKnots, BoltzmannGradLimitAndLanford, CubicSzegoEquation)
serve as reference implementations of these principles.
