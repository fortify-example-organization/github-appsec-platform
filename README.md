# GitHub AppSec Platform Repository Index

This repository is an index for the standalone GitHub AppSec Platform repositories maintained by [fortify-example-organization](https://github.com/fortify-example-organization). It is **not** the source of truth for their code, documentation, releases, or configuration.

## Canonical Repositories

| Repository | Purpose |
| --- | --- |
| [platform-workflows](https://github.com/fortify-example-organization/platform-workflows) | Reusable GitHub Actions workflows |
| [platform-actions](https://github.com/fortify-example-organization/platform-actions) | Custom GitHub Actions and security controls |
| [platform-governance](https://github.com/fortify-example-organization/platform-governance) | Governance, compliance, and rollout automation |
| [platform-docs](https://github.com/fortify-example-organization/platform-docs) | Platform architecture, usage, and operational documentation |

For general questions or to browse other projects, visit the [organization repositories](https://github.com/orgs/fortify-example-organization/repositories).

## Working Across Repositories Locally

[github-appsec-platform.code-workspace](./github-appsec-platform.code-workspace) is a VS Code multi-root workspace that opens this index repository alongside sibling checkouts of `platform-workflows`, `platform-actions`, `platform-governance`, and `platform-docs`. Clone the canonical repositories as siblings of this one, then open the workspace file to edit all of them together. The workspace is a local convenience only; it does not change where source of truth lives for each repository.

## Which Repository Should I Change?

Make changes in the standalone repository that owns the code or documentation. For example, workflow changes belong in `platform-workflows`; documentation changes belong in `platform-docs`. A change in this index repository does not update those repositories.

When a change spans repositories, make and review the corresponding changes in each affected standalone repository. Consume reusable workflows and actions from their canonical repositories using the version tags and guidance documented there.

## Example Templates

`examples/` contains starter templates for Java, Node.js, Python, .NET, and polyglot monorepos. They are local templates, not submodules or mirrors of standalone repositories. Use `scripts/new-ref-app.ps1` to create a project from a template and `scripts/new-security-workflow.ps1` to add a caller workflow to an existing project.

The templates consume workflows from the canonical `fortify-example-organization/platform-workflows` repository. Changes to reusable workflows, actions, governance, or platform documentation belong in the canonical repositories linked above. This index and its templates do not publish or synchronize changes to those repositories.
