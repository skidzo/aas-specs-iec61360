---
name: submodel-template-json-transformation
description: Normalize and transform Submodel Template JSON into deterministic formats for review, diffing, and downstream conformance validation. Use for cleanup, canonicalization, and transformation pipelines.
---

# Submodel Template JSON Transformation

Use this skill when the request is about preparing or transforming template JSON before/after conformance checks.

## Model targeting

- Primary: Claude Sonnet for transformation design and migration logic
- Secondary: Claude Haiku for repetitive normalization tasks

## Workflow

1. **Detect source pattern**
   - Raw authoring JSON, generated JSON, or mixed payloads.
2. **Apply canonicalization**
   - Sort keys (stable policy), normalize whitespace, preserve value semantics.
3. **Normalize template conventions**
   - Harmonize key naming and repeated element structure.
4. **Generate diff-safe output**
   - Ensure deterministic ordering and stable line-level output.
5. **Hand over to conformance skill**
   - Run validation on transformed output.

## Guardrails

- Never change semantic meaning during normalization.
- Flag lossy conversions explicitly.
- Keep original and transformed artifacts traceable.

## Use references

- Load `references/transformation-patterns.md` for common transformation patterns.
- Load `references/agentic-handoff.md` for chaining with validation/reporting skills.
