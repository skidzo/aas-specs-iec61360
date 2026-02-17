# Prompt Profiles for Claude Sonnet and Haiku

## Sonnet profile (deep conformance)

Use when precision matters:

- Ask for strict rule-by-rule validation.
- Request explicit JSONPath evidence for each finding.
- Ask for minimal remediation patches.

Suggested instruction snippet:

> Validate this Submodel Template JSON against the provided checklist. Return strict findings with JSONPath evidence and a remediation suggestion for each error.

## Haiku profile (fast triage)

Use when speed matters:

- Ask for highest-impact issues first.
- Limit output to top findings per severity.
- Prefer short remediation bullets.

Suggested instruction snippet:

> Perform a quick conformance triage on this Submodel Template JSON. Return top errors/warnings with JSONPath and one-line fixes.
