# Changelog

## v5.8.1 — Packaging / Consistency Hotfix (2025-12-31)
- Fixed `CITATION.cff` DOI to: 10.5281/zenodo.18111574
- Normalized dataset filenames:
  - `quakeml (1).xml` → `quakeml_1.xml`
  - `quakeml (2).xml` → `quakeml_2.xml`
- Rewrote `INDEX.md` to match actual package contents and clarify evidence-only scope.
- Replaced `/bin/Dockerfile` with an evidence-only transport container (removes missing core references).
- Added `CHECKSUMS.sha256` for full-file integrity verification.

## v5.8.0 — Evidence Release (2025-12-31)
- Initial evidence + datasets + documentation bundle.
