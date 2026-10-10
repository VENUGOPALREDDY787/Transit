## 1. Project identity
- [ ] 1.1 Update user-facing branding, package metadata, and active documentation
      to Transit while preserving the repository root folder and license.
- [ ] 1.2 Rename the Python package and update imports, build/type-check
      configuration, scripts, tests, and lockfile metadata.

## 2. Configuration compatibility
- [ ] 2.1 Add `TRANSIT_*` environment-variable names with `INFERENCE_X_*`
      fallback aliases and new-name precedence.
- [ ] 2.2 Update examples and documentation; test new, legacy, and conflicting
      values.

## 3. Validation
- [ ] 3.1 Confirm no unintended old branding or package references remain outside
      compatibility aliases, preserved license notices, and historical records.
- [ ] 3.2 Run relevant unit tests, lint, type check, and package/import smoke
      checks; validate the OpenSpec change.
