# Morpho Vault Change Note Template

> [!NOTE]
> ### When this template can be used
> - Only for a change to a Morpho vault, its adapters, or its markets, where the vault is recorded in a Prime Agent Artifact as an Instance of the Allocation System Primitive and was onboarded through a Technical Scope. A vault onboarded without a Technical Scope announces its first change with the General Technical Scope Template, and later notes for that vault reference that Technical Scope (A.1.10.2.5.2.4).
> - Only where no new contract is deployed and no new market is created, and the change falls within A.2.2.10.1.1.1.3.6.1.1 (Morpho Vault Changes Requiring Governance Approval) or A.2.2.10.1.1.1.3.6.1.2 (Morpho Vault Changes Requiring Disclosure Only). Otherwise, use the General Technical Scope Template.
> - Core GovOps can require a Technical Scope instead of a Morpho Vault Change Note.
> - Urgent and Emergency actions are not announced with this template (see A.2.2.10.1.1.1.3.6.1.3).
> - Not for a change executed through an Executive Vote, which is announced in the Prime Spell's Forum post with its Technical Scope and recorded through the spell process (A.2.2.10.1.1.1.3.6.2.1, A.2.2.10.1.1.1.3.6.2.2).
> - Revoking a queued change, removing an Allocator, decreasing a cap, and setting or changing the force deallocate penalty may be executed before they are announced. They are then reported within 24 hours in a new Forum post, using the Execution Report section (A.2.2.10.1.1.1.3.6.2.1, A.2.2.10.1.1.1.3.6.2.2).

> [!NOTE]
> ### General rules on **filling out** the template
> - No sections can be skipped or removed. If a section is non-applicable, provide a one-line explanation why it's not relevant.
> - All notes and warnings should be removed from the filled-in template before posting or submitting.
> - All addresses have to be in a checksummed format.
> - All times have to be in UTC. All on-chain values have to state the block at which they were read.
> - One Morpho Vault Change Note covers one vault and its adapters. Each on-chain call is listed as a separate action, in execution order.
> - The title of the Forum post is `[Chain] <Prime Agent> Liquidity Layer: <summary of the change>`.

## Reference

> [!NOTE]
> Links to the vault's record. The Technical Scope this note references already contains the deployment, audit, role and address context; don't repeat it here.

- Prime Agent:
- Vault name and token symbol:
- Vault address (linked to the explorer) and chain:
- Vault version (Morpho Vaults V1.1 or V2):
- Onboarding Technical Scope (Forum URL), or the Technical Scope used for the first change where the vault was onboarded without one:
- Instance Configuration Document (Atlas document number and URL):

## Change category

> [!NOTE]
> Classify every action under A.2.2.10.1.1.1.3.6.1. If an action can fall into more than one category, the stricter one applies. If the Prime Agent Artifact is stricter than the Core category (e.g., requires a poll for a disclosure-only change), state it.

1. **[Action number and name]**
    - Core category (governance approval or disclosure only):
    - Core provision and bullet:
    - Prime Agent Artifact requirement, if stricter:

- Governance vote, if the change requires one (link, or expected opening and closing times):
- Queueing before approval, if the Prime Agent Artifact allows it: the conditions, and how each early queueing meets them:
- Entity that announces and reports, and why it is that entity under A.2.2.10.1.1.1.3.6.2.1. Where the Operational Facilitator designated it, link the Forum post:
- Addresses that may revoke each queued action, including any additional revokers the Prime Agent Artifact designates:

## The reason(s) behind this update

## Proposed actions

> [!NOTE]
> List every action planned to be performed, in execution order, with exact input values and their sources, as well as the exact address that will perform those actions. Current values are read at a stated block. List every operation pending in the timelock of the vault or of any of its adapters at that block under "Pending timelock operations" below, including those on other functions. List any revocation as an action (A.2.2.10.1.1.1.3.6.1.2). In case the actions are planned to be performed by a multisig, this section should link already staged transactions.

1. **[What is proposed]**
    - Contract being called:
    - Function being called:
    - Who will perform this action:
    - Important arguments:
        1. [Argument name]
            - Current value (and the block at which it was read):
            - Proposed value:
            - External source of the value or an explanation of how this value can be verified, and who has to confirm it:
    - Calldata:
    - Effect on the Morpho Verification Report. Name any check this action makes outdated and link the updated report (A.1.10.2.5.2.3.2), or write "none":
    - Applicable timelock delay and its source. State the current delay on the contract being called, the minimum required by A.2.2.10.1.1.1.3.3 where one applies, and any longer delay required by the Prime Agent Artifact:
    - Planned queueing time:
    - Earliest executable time:
    - Planned execution time and executor:

### Pending timelock operations

> [!NOTE]
> Every operation pending in the timelock of the vault or of any of its adapters at the stated block, or "none".

1. **[Function and arguments as submitted]**
    - Contract (vault or adapter address):
    - Executable from (UTC):
    - Conflicts with an action in this note:
    - Revoked by this note (action number) or left to execute:

### Markets or adapters added to the vault for the first time

> [!NOTE]
> Required for every market or adapter added that the referenced Technical Scope does not cover. Provide the references below, the applicable checks from the Morpho Deployment Verification Guide (A.1.10.2.5.2.3), and the updated Morpho Verification Report entry (A.1.10.2.5.2.3.2).

1. **[Action number: market or adapter being added]**
    - Market (id, loan and collateral assets, oracle, IRM, LLTV) or adapter (address, type, underlying market or vault):
    - Deployment provenance:
    - Compliance with the Market Eligibility Requirements in A.2.2.10.1.1.1.3.2 for the loan asset, the collateral and its LLTV, the oracle methodology and the interest rate model:
    - Oracle configuration check (guide section 5):
    - Audit coverage, where applicable:
    - Morpho Verification Report entry and verifier:

## Artifact update

> [!NOTE]
> List every value recorded in the Prime Agent Artifact that the actions change. For a change requiring governance approval, the Artifact Edit Proposal is what the vote approves, through the Prime Agent's Root Edit process (A.2.2.10.1.1.1.3.6). For a disclosure-only change, the Operational Facilitator opens the pull request on the basis of this note and merges it once the change is executed and reported (A.2.2.10.1.1.1.3.6.1.2).

- Artifact documents and values affected:
- Pull request or proposal:

## Security-sensitive sections

> [!NOTE]
> State whether the sections of the Technical Scope this note references that the Technical Scope Template marks as security-sensitive (currently Technical risk self-assessment, Emergency actions and Monitoring) still apply unchanged. If not, don't describe the new content here: update the affected sections and submit them again, together with this note, through the private submission channel (A.1.10.2.5.2.1.1). The original Technical Scope post is not modified.

- Unchanged from the referenced Technical Scope:
- If not, private submission reference:

---

# Execution Report

> [!WARNING]
> **NOT PART OF THE ANNOUNCEMENT — remove this section before posting.** Each report is posted as a reply to the announcement (or, where the change was executed before it was announced, in a new Forum post under the Prime Agent's Forum category) within 24 hours of each queueing (or execution, where no timelock applies) and of any revocation, by the holder of the role that performed the action (A.2.2.10.1.1.1.3.6.2.2). No further report is required when a queued change later executes. Where a role is held jointly, the Operational Executor Agent reports if it is one of the holders. Where a role is held by a contract, or where no joint holder is the Operational Executor Agent, the entity designated for that role in the Prime Agent Artifact reports; where the Artifact designates none, the Prime Agent's Operational Facilitator designates the reporting entity in a Forum post under the Prime Agent's Forum category.

## Queued or executed actions

1. **[Action number and name, as announced]**
    - Transaction hash:
    - Change as queued or executed (confirm that it matches the announced values, or state the difference):
    - UTC time at which the change becomes executable, or at which it was executed where no timelock applies:
    - Value read back after execution (where executed; otherwise "not yet executed"):
    - Governance vote (link and result), if applicable:
    - If queued before approval: statement that approval had not been obtained at queueing, and the expected poll closing time used:

## Revoked actions

1. **[Revoked action number and name, as announced]**
    - Transaction hash of the revocation:
    - UTC time of the revocation:
    - Change revoked (as queued, with its announced values):
    - Governance vote (link and result), if applicable:
    - Reason:
    - Next step (resubmission, new Morpho Vault Change Note, or none):
