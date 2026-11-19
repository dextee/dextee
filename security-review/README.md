# Security finding · An invoice agent had approval rights

**Hold the release.** Finance asked for an agent that prepares invoice drafts for a person to approve. The candidate configuration also assigned approval to the agent. Remove that grant and verify the approval boundary before enabling the integration.

This is a synthetic assessment sample. The three CSV files are small enough to inspect on GitHub. They illustrate the evidence and retest a buyer can ask for in an access review.

| Evidence | What it shows |
| --- | --- |
| [Agreed access](agreed-access.csv) | The agent may read and draft invoices. A finance approver may read and approve. A reviewer may read. |
| [Before the fix, row 4](access-before.csv#L4) | The candidate export grants `invoice.approve` to `invoice-agent`. That is the only extra role-permission pair. |
| [After the fix](access-after.csv) | All five agreed grants remain. The agent can still prepare drafts. Approval belongs to the finance role alone. |

**Business impact.** If the application honours the candidate configuration, a draft prepared under the agent identity could also be approved under that identity. Finance would lose its independent sign-off. This sample contains no transaction history.

**Remediation and ownership.** The application owner removes approval from the agent role. The finance owner confirms who should hold the approver role. Both need to agree on the decision before the integration goes live.

**Retest.** Comparing the corrected export with the agreed access list produced zero differences. That closes the configuration finding in this sample. To sign off a deployment, the owner would still need runtime evidence that an agent-prepared draft waits for a separate approver and that the audit log identifies both actors.

## Reproduce the comparison

From this repository's root, run the two commands separately. The files use the same columns and row order.

```sh
git diff --no-index -- security-review/agreed-access.csv security-review/access-before.csv
git diff --no-index -- security-review/agreed-access.csv security-review/access-after.csv
```

The first command shows one extra grant and exits with status 1. The second has no output and exits with status 0. You can also inspect all three files in the table above.

## Discuss a security assessment

You can start with a message like this.

> I found your access review on GitHub. We're preparing to launch [application or integration] by [date]. We want to confirm who can [business action] and agree which fixes need a retest.

[Discuss the scope with Dexter on LinkedIn](https://www.linkedin.com/in/dexterng/)
