# AppFlowy Dart architecture analysis

Open `analysis.json` with **Load a file** at https://app.codeboarding.org to explore the component hierarchy. The JSON is about 6.1 MiB. [overview.md](overview.md) and the component Markdown files provide a text export.

## Run provenance

- Generated on 2026-11-15 from AppFlowy checkout `9a1363866ff49165c666a2dd95a117bba6bcf034`; application source is unchanged from `8fcee27d9`.
- Engine: CodeBoarding `feat/dart-flutter-support`, commit `9e3667caf26158ea95c70bc1d9ad60e3af03d0c9`.
- Managed Flutter 3.27.4 / Dart 3.6.2. No Dart/Flutter installation on PATH or SDK environment variables are required.
- Dart-only scope, configured in [.codeboardingignore](.codeboardingignore). Other engine-supported source languages are excluded; package manifests and documentation remain available as context.
- Model: `gemini-3.8-flash`; default affinity grouping and depth cap 3.
- Command, from the engine checkout with its virtual environment active:

```bash
python -m codeboarding_cli.main full --local /home/ivan/StartUp/repos/AppFlowy --render md --force --depth-cap 3
```

## Results and validation

- Dart static analysis processed 1,690 files (262,601 lines), producing 18,665 graph nodes and 36,518 dependency edges.
- The final architecture contains 175 components across three levels and 1,731 component relations, including nested and cross-scope relations.
- The compact v1 document indexes 18,114 methods in 1,587 Dart files and serializes 20,246 dependency edges. The output indexes members represented in components, not every scanned symbol or raw graph edge.
- The generated JSON passed the engine's `AnalysisDocument` schema validation. Component IDs are unique, all component relation endpoints and method/evidence IDs resolve, every key edge exists in the edge table, and all indexed files exist and are Dart files.
- There are 38 generated Markdown documents. `file_coverage.json` records analyzed and excluded files.
- The graph pipeline took 886.1 seconds, of which edge building took 808.6 seconds. Performance investigation: [CodeBoarding#696](https://github.com/CodeBoarding/CodeBoarding/issues/696).

## Limitations

This is a Dart-only analysis, not a complete native build. Dart produced diagnostics in 1,253 files (19,103 diagnostic items); successful graph extraction does not establish that the application compiles or that every reference resolved. Reference integrity checks do not prove that every generated relationship description is semantically correct.

Rust and other native implementations are intentionally excluded. Dart-side backend bridge components do not imply that Flutter-to-Rust FFI or Rust subsystem dependencies were analyzed. Component and relation totals are not directly comparable to the earlier mixed-language output, which used a different partition and document format.

Machine-local logs, lock files, and the static-analysis pickle/cache marker are excluded from Git. Application source files are unchanged.
