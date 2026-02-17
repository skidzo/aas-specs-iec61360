---
name: submodel-template-task-discovery
description: Discover additional high-value tasks, quality controls, and capabilities around JSON-based Submodel Template engineering and conformance operations. Use for roadmaping and capability gap analysis.
---

# Submodel Template Task Discovery

Use this skill when users ask for additional relevant tasks and capabilities beyond basic conformance checking.

## Model targeting

- Claude Sonnet: strategic capability mapping and prioritization
- Claude Haiku: rapid backlog drafting

## Discovery workflow

1. **Baseline understanding**
   - Identify current template lifecycle (authoring, validation, release).
2. **Find adjacent tasks**
   - Testing, migration, quality gates, governance, CI integration.
3. **Score opportunities**
   - `impact` (high/medium/low), `effort` (high/medium/low), `automation potential`.
4. **Propose capability set**
   - Define candidate skills with trigger phrases and outputs.
5. **Create a phased backlog**
   - Phase 1 quick wins, phase 2 hardening, phase 3 scale-out.

## Output format

Return a compact JSON backlog:

```json
{
  "capabilities": [
    {
      "name": "template-quality-gate",
      "impact": "high",
      "effort": "medium",
      "why": "Blocks invalid templates before release"
    }
  ]
}
```

## Use references

- Load `references/capability-catalog.md` for candidate capabilities.
