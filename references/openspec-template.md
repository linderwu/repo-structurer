# OpenSpec Template Reference

> OpenSpec lives in `spec/` (in the workspace, NOT in `wiki/`).
> OpenSpec is the **construction blueprint / contract** for each module.
> OpenSpec must cite the actual code path in `repos/<repo-name>/`.

## Per-Module Spec: `spec/[module]/SPEC.md`

```markdown
# [Module Name]

## Summary
One-paragraph description of what this module does and why it exists.

## Source of Truth
- **Repository**: `repos/<repo-name>/`
- **Primary path**: `path/to/module/`
- **Entry point**: `path/to/main/file.ts`

## Construction Blueprint

### Core Features
- **Feature 1**: ...
- **Feature 2**: ...

### Inputs
- `input_1`: description, type, source
- `input_2`: description, type, source

### Outputs
- `output_1`: description, type, destination
- `output_2`: description, type, destination

### Side Effects
- Any mutations, I/O, network calls, or state changes

### Cross-Repo Contracts
- Calls into: `repos/<other-repo>/path/to/endpoint` (link spec)
- Called by: `repos/<other-repo>/path/to/caller` (link spec)

## Interface

```[language]
// function signatures, API endpoints, class definitions
```

## Data Flow
How data moves through this module (input → transformation → output).

## Dependencies
- **Internal**: [other modules this depends on, link their specs]
- **External**: [libraries, services, infrastructure]

## Edge Cases
- Case 1: expected behavior
- Case 2: expected behavior

## Error Handling
How errors are detected, logged, and propagated.

## Testing Notes
Key test scenarios or testing approach (not actual tests — those go in code).

## Wiki Cross-References
- [[entity-name]] — wiki entity for this module
- [[concept-decision-name]] — design decision that shaped this contract
```

## System Overview Spec: `spec/SPEC.md`

```markdown
# [Project Name] — System Specification

## Overview
High-level description of the system, its purpose, and scope.

## Repositories
- `repos/<repo-a>/` — role, primary language
- `repos/<repo-b>/` — role, primary language
- `repos/<shared>/` — shared library / types

## Architecture
[Key components and how they interact, including cross-repo boundaries]

## Data Model
[Core entities and their relationships, with citations to repos/ source files]

## API Surface
[Public endpoints and their purpose; cite spec/<module>/SPEC.md entries]

## Configuration
[Environment variables, feature flags, key settings]

## Deployment
[How the system is deployed, infrastructure requirements, per-repo deployment notes]

## Security Considerations
[Auth, authorization, data classification, sensitive handling]
```
