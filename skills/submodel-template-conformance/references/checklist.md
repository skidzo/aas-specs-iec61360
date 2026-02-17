# Conformance Checklist (JSON-Oriented)

Use this checklist for Submodel Template conformance assessments.

## 1) Basic JSON integrity

- Valid UTF-8 JSON, no trailing commas, no duplicate keys.
- Deterministic key casing (prefer stable convention per project).

## 2) Template structure

- Top-level object exists and is not an array.
- Expected template anchors are present (e.g., identifiers, model type hints, element container).
- `submodelElements` (or equivalent container) is an array when present.

## 3) Identifier and semantic quality

- Every reusable element has a stable `idShort` (or equivalent local identifier).
- Semantic references are present where required.
- Semantic references follow one policy consistently (e.g., global key/reference format).

## 4) Data typing and value consistency

- Declared type matches actual value shape.
- Enumerations do not contain out-of-domain values.
- Unit-bearing properties use a consistent unit strategy.

## 5) Interoperability checks

- Language-dependent strings are represented consistently.
- No ambiguous element names where semantic references differ.
- Arrays use stable element schemas across entries.

## 6) Reporting

- Each finding includes: severity, JSON path, rule id, message, remediation.
- Group repeated findings under the same rule id when possible.
