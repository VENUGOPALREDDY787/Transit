# Rename the project to Transit

## Why

The project is being rebranded as Transit. The branding and importable Python
package should use the new name while the repository's root directory remains
unchanged.

## What changes

- Rename public project branding and distribution metadata from InferenceX to
  Transit.
- Rename the Python package from `inference_x` to `transit` and update imports,
  package configuration, scripts, tests, and documentation.
- Adopt `TRANSIT_*` environment-variable names while continuing to accept
  existing `INFERENCE_X_*` names as compatibility aliases.
- Preserve existing behavior and HTTP API contracts.
- Keep the existing license and copyright notices intact.
- Keep the root directory name unchanged.

## Non-goals

- Changing API routes, request/response contracts, runtime behavior, or model
  licensing.
- Removing prior authorship or copyright notices.
- Renaming the repository's root folder.

## Impact

This affects package imports and installation metadata, environment-variable
configuration, CLI/setup instructions, tests, and user-facing project
documentation. Compatibility aliases are required to avoid breaking existing
deployments.
