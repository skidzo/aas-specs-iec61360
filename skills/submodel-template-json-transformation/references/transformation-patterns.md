# Transformation Patterns (JSON)

## Pattern A: Canonical formatting

- Parse and re-emit JSON with consistent indentation.
- Sort keys with a stable strategy.
- Keep arrays in original semantic order unless policy says otherwise.

## Pattern B: Key harmonization

- Map deprecated keys to current keys (non-destructive first).
- Emit deprecation notes for changed keys.

## Pattern C: Structural normalization

- Convert singleton/object dual-forms into one canonical form.
- Normalize language-string arrays into one preferred representation.

## Pattern D: Validation-ready snapshot

- Add no derived data unless explicitly requested.
- Produce a clean, deterministic file for linting and conformance checks.
