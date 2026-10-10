## ADDED Requirements

### Requirement: Transit project identity
The project SHALL use Transit as its public project and Python package identity
without changing its HTTP API or runtime behavior. Existing `INFERENCE_X_*`
environment variables SHALL remain accepted as compatibility aliases for their
corresponding `TRANSIT_*` variables.

#### Scenario: New project identity is used
- WHEN a user installs, imports, or configures the project using its documented
  identity
- THEN the distribution and importable package are named `transit`
- AND user-facing project branding identifies the application as Transit

#### Scenario: Existing environment configuration remains valid
- WHEN an existing deployment supplies an `INFERENCE_X_*` environment variable
  and no corresponding `TRANSIT_*` variable
- THEN the setting retains its existing value and behavior

#### Scenario: New environment configuration takes precedence
- WHEN both a `TRANSIT_*` variable and its `INFERENCE_X_*` alias are supplied
- THEN the `TRANSIT_*` variable determines the setting value

#### Scenario: Existing license notices are preserved
- WHEN the project identity is changed
- THEN existing license and copyright notices remain intact
