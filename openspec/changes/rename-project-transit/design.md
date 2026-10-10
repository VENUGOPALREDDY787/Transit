# Design: Rename the project to Transit

## Context

Transit is a rename of the existing application, not a behavior change. The
package distribution and import namespace will become `transit`; the root
directory, HTTP endpoints, and runtime behavior remain unchanged. Existing
users may already rely on `INFERENCE_X_*` environment variables.

## Decisions

- Use `transit` as both the Python import package and distribution name.
- Replace current environment-variable names with `TRANSIT_*` in public
  documentation and examples. At configuration lookup, prefer a new `TRANSIT_*`
  value and fall back to its `INFERENCE_X_*` alias when the new value is unset.
- Keep the existing MIT license file unchanged, including its copyright notice.
- Do not alter archived OpenSpec proposals or other explicitly historical
  records; the live project documentation and implementation should use Transit.
- Keep the root folder name `inference-x` unchanged.

## Risks and mitigations

- **Broken imports after package move:** update source imports, scripts, tests,
  package build configuration, and type-check settings together; run the unit
  suite and import/build checks.
- **Configuration regression:** use a single compatibility lookup path with
  explicit precedence and cover new-only, legacy-only, and both-set cases in
  tests.
- **Stale editable-install metadata:** update `pyproject.toml` and regenerate
  `uv.lock`, then verify the package build/import.
- **Attribution removal:** retain the existing license and copyright notice.
