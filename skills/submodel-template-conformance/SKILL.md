---
name: submodel-template-conformance
description: Validate JSON-oriented Submodel Templates for structural and semantic conformance in IEC61360-oriented AAS workflows. Use when users ask to check, audit, or enforce conformance of Submodel Templates and related JSON payloads.
---

# Submodel Template Conformance

Use this skill when the request is about validating Submodel Template JSON for conformance.

## Model targeting

- Primary: Claude Sonnet (deep analysis and nuanced findings)
- Secondary: Claude Haiku (fast checks and triage)

## Inputs expected

- One or more JSON files representing Submodel Templates or template fragments
- Optional conformance criteria (required fields, naming rules, semanticId policy, value constraints)

## Workflow

1. **Identify JSON scope**
   - Determine which files are templates vs examples vs generated output.
2. **Run structural checks**
   - Parse JSON.
   - Verify required keys and object shapes.
3. **Run semantic checks**
   - Inspect semantic identifiers, value domains, and data typing consistency.
4. **Classify findings**
   - `error`: breaks conformance
   - `warning`: potential interoperability issue
   - `info`: recommendation
5. **Produce machine-friendly report**
   - Return concise JSON findings and short remediation actions.

## Output contract

Return findings in this shape:

```json
{
  "summary": {"errors": 0, "warnings": 0, "info": 0},
  "findings": [
    {
      "severity": "error",
      "path": "$.submodelElements[3].semanticId",
      "rule": "semantic-id-required",
      "message": "semanticId is missing",
      "remediation": "Provide a globally unique semantic reference"
    }
  ]
}
```

## Use references

- Load `references/checklist.md` for the core conformance checklist.
- Load `references/prompt-profiles.md` to adapt prompting between Sonnet and Haiku.
