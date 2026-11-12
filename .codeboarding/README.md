# AppFlowy architecture analysis

Open `analysis.json` with **Load a file** at https://app.codeboarding.org to explore the component hierarchy. The JSON is about 50 MiB; GitHub may not display it inline. [overview.md](overview.md) and the component Markdown files provide a text export.

## Run provenance

- Generated on 2026-11-12 from AppFlowy commit `8fcee27d9`.
- Engine: CodeBoarding `feat/dart-flutter-support`, commit `088b52da03ed2362caa2411e9f1548a8caff01e7`.
- Flutter 3.27.4 / Dart 3.6.2, matching this repository's pinned Flutter version.
- Model: `gemini-3.8-flash`; default affinity grouping and depth cap 3.
- Command, from the engine checkout with its virtual environment active and Flutter on PATH:

```bash
python -m codeboarding_cli.main full --local /home/ivan/StartUp/repos/AppFlowy --render md
```

## Results and validation

- Dart static analysis processed 1,690 files, producing 18,715 graph nodes and 36,446 dependency edges.
- The final architecture contains 115 components across three levels and 576 component relations, including nested and cross-scope relations.
- The final method index contains 23,724 entries across all languages, including 18,114 Dart entries. Its file index contains 2,102 files, including 1,587 Dart files; the index includes files represented in components, not every scanned file.
- The generated JSON passed the engine's `UnifiedAnalysisJson` schema validation. Component IDs are unique, all component relation endpoints and file method keys resolve, and all indexed source files exist.
- There are 27 generated Markdown documents. `file_coverage.json` records analyzed and excluded files.

## Limitations

This is a Dart-enabled whole-repository run, not a complete native build. Dart produced diagnostics in 1,253 files (19,103 diagnostic items); successful graph extraction does not establish that the application compiles or that every reference resolved.

Rust discovered 5,470 nodes but no call edges, and the engine explicitly reported degraded Rust results. Do not interpret missing Rust relationships as absence of dependencies. C++ analysis lacked a compilation database and platform headers, reporting 604 errors; its relationships are incomplete. Kotlin used a source-only workspace after its build import was blocked.

Machine-local logs, lock files, and the static-analysis pickle/cache marker are excluded from Git. Application source files are unchanged.
