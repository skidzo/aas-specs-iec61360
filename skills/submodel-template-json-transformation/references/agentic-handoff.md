# Agentic Handoff Sequence

Use this sequence in multi-agent workflows:

1. **Transform agent**
   - Normalizes JSON and emits transformed artifact.
2. **Conformance agent**
   - Validates transformed artifact with checklist-driven rules.
3. **Reporting agent**
   - Aggregates findings into release-readiness decision.

## Minimal handoff payload

```json
{
  "artifact": "path/to/template.normalized.json",
  "source": "path/to/template.raw.json",
  "transform_log": ["sorted keys", "normalized language strings"],
  "known_risks": []
}
```
