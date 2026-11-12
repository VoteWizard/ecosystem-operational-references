# Ecosystem Operational References

Canonical operational reference materials for teams preparing, reviewing, and executing infrastructure changes and deployments within the Sky Ecosystem. These materials are used by Agents, Core Spell Teams, and other ecosystem participants as applicable.

This repository is intended to operationalize the relevant Atlas requirements and processes. Direct Atlas references will be added once the associated Atlas edits are finalized.

**Note:** The Agent Spell Reviewer Checklist currently remains maintained in its existing canonical location here: https://github.com/sky-ecosystem/pe-checklists/blob/master/spell/star-spell-reviewer-checklist.md. Agents and reviewers should continue using that version until further alignment on repository structure and migration decisions is completed.

## Contents

```
ecosystem-operational-references/
├── templates/
│   ├── technical-scope-template.md
│   └── morpho-vault-change-note-template.md
├── checklists/
│   └── deployment-checklist.md
├── examples/
│   └── technical-scope/
│       ├── star-spell-technical-scope-example.md
│       └── non-spell-technical-scope-example.md
├── guides/
│   └── morpho-deployment-verification-guide.md
├── .claude/skills/          ← placeholder for future Claude skills
└── .github/workflows/       ← placeholder for future workflows
```

## Guide

### Technical Scope Template (`templates/technical-scope-template.md`)

**What it is:** A standardized template for announcing any infrastructure changes (on- or offchain) with enough technical detail for an external team to review without additional context.

**Security-sensitive sections:** The template introduces sections for Technical risk self-assessment, Emergency actions, and Monitoring. These sections enforce a rigorous security mindset by requiring teams to consider risks, emergency responses, and monitoring for every infrastructure change. Because these sections may contain information that could be exploited if publicly disclosed, they are handled through a separate private submission process.

**Where to submit:** The filled-in template must be submitted through both public and private channels:

- **Public:** All sections except the security-sensitive sections defined above must be published as a Forum post on the Sky Forum.
- **Private:** The full template, including the security-sensitive sections (Technical Risk Self-Assessment, Emergency Actions, and Monitoring), must be submitted privately to Core GovOps.

**For Agents:** Agents must submit the full template, including the security-sensitive sections, as a Pull Request to the Agent's private fork of [technical-scope-submissions-template](https://github.com/Atlas-Axis/technical-scope-submissions-template). See the submission instructions in that repository for setup and workflow details. For Technical Scopes associated with a Prime Spell, both the Forum post and the private submission must be completed according to the following deadlines:

- **Sky Governance path** (Prime Agents whose Root Edit Primitive is not yet operational): by **Wednesday, 16:00 UTC of Week 1** of the Prime Spell Process.
- **Independent Governance path** (Prime Agents whose Root Edit Primitive is operational): by **end of Friday of Week 1** of the Prime Spell Process.

### Morpho Vault Change Note Template (`templates/morpho-vault-change-note-template.md`)

**What it is:** A standardized template for announcing a change to a Morpho vault already recorded in a Prime Agent Artifact and onboarded through a Technical Scope, where no new contract is deployed and no new market is created. A vault onboarded without a Technical Scope announces its first change with the Technical Scope Template, and later Morpho Vault Change Notes for that vault reference that Technical Scope. A change executed through an Executive Vote is announced in the Prime Spell's Forum post with its Technical Scope and recorded through the spell process, and does not use this template. Core GovOps may also require a Technical Scope instead of a Morpho Vault Change Note.

**Where to submit:** As a Forum post under the Prime Agent's Forum category, before the change is queued in the vault's timelock or, where no timelock applies, executed, and, for a change that requires governance approval, before the vote on it begins. Where the change alters a section of the referenced Technical Scope that the Technical Scope Template marks as security-sensitive, that section is updated and submitted again through the private channel described above. Each queueing (or execution, where no timelock applies) and each revocation is reported as a reply to the post within 24 hours, using the Execution Report section of the template; no further report is required when a queued change later executes. Revoking a queued change, removing an Allocator, decreasing a cap, and setting or changing the force deallocate penalty may be executed before they are announced. They are then reported within 24 hours in a new Forum post under the Prime Agent's Forum category, using the Execution Report section (A.2.2.10.1.1.1.3.6.2.1).

### Deployment Checklist (`checklists/deployment-checklist.md`)

**What it is:** A standardized checklist for contract deployments covering deployer hygiene, foundry setup, test deployments, and verification.

**When to use:** For every contract deployment within the Sky Ecosystem.

**Where to submit:** Where the deployment is included in a Technical Scope Forum post, the completed checklist must be publicly accessible and linked from the Pre-deployed Contracts section of that post for each deployed contract. If the deployment has not yet occurred at the time the Technical Scope post is published, the checklist link may be marked as pending and updated once deployment is completed. For deployments that do not have an accompanying Technical Scope Forum post, the completed checklist must be retained by the deploying team and made accessible on request.

### Guides (`guides/`)

Reusable verification methodologies and best practices for specific deployment types. Guides document a repeatable verification flow and may include worked examples.

## Getting started

Clone this repository:

```bash
git clone https://github.com/Atlas-Axis/ecosystem-operational-references.git
```

## Before you start

> [!IMPORTANT]
> Before using any reference material, you must pull the latest version to ensure your copy is aligned with the source repository:
> ```bash
> cd ecosystem-operational-references
> git pull origin main
> ```

Do not modify the template files directly. When filling out a template, copy it to a new file with a descriptive name (e.g., `technical-scope-may-2026-spell.md`) and work from the copy. This ensures `git pull` always updates the templates cleanly without merge conflicts.

Each template and checklist must be completed and submitted separately, in accordance with the submission instructions in this README and any guidance within the documents themselves regarding which sections need to be filled out.

## Maintenance

### Technical Scope Template

The Technical Scope Template is maintained by Core GovOps. All changes must be submitted as a Pull Request in this repository and require two (2) approvals, one (1) from each Core Spell Team, before they can be merged.

### Morpho Vault Change Note Template

The Morpho Vault Change Note Template is maintained by Core GovOps. All changes must be submitted as a Pull Request in this repository and require two (2) approvals, one (1) from each Core Spell Team, before they can be merged.

### Deployment Checklist

The Deployment Checklist is maintained by Core GovOps. All changes must be submitted as a Pull Request in this repository and require two (2) approvals, one (1) from each Core Spell Team, before they can be merged.
