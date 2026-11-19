# Dexter Ng · AI agents and cybersecurity

I'm the CTO & Cybersecurity Lead at VYR in Singapore. I build custom AI agents for operations teams and help businesses find and fix security weaknesses in their applications.

**Custom AI agents.** If your team rekeys orders, checks invoices or routes the same enquiries every day, bring me one workflow, the systems it touches and its monthly volume. We'll identify what the agent can handle, what needs a person and how to test the result. [Scope an AI agent with VYR](https://vyrwork.com/contact?utm_source=github&utm_medium=referral&utm_campaign=github_profile&utm_content=ai_agent_enquiry)

**Cybersecurity assessments.** If you're launching a web application, connecting an agent to business data or deciding which security fixes to prioritise, tell me the system and your deadline. You'll get findings your engineers can trace, remediation priorities and agreed retest criteria. [Discuss a security assessment with me](https://www.linkedin.com/in/dexterng/) · [See a sample finding](https://github.com/dextee/dextee/tree/main/security-review)

## AI agents in practice

**Live client work.** For food distributor MM Trading, VYR's live workflow takes in purchase orders, validates them and routes them for human approval before preparing a draft in Xero. [VYR's published client work](https://vyrwork.com/) · [Explore the workflow catalog](https://github.com/dextee/vyr-agent-os-workflows/blob/main/docs/workflows/README.md)

**Try a finance decision yourself.** In my public workbench, a supplier bills S$222 for 12 desk trays. Two receipts account for six and four. The report shows the two missing trays and why the invoice stays out of the draft. The sample uses synthetic records and runs offline. [Open the workbench](https://github.com/dextee/invoice-match-workbench) · [Download the finished report](https://github.com/dextee/invoice-match-workbench/releases/download/v0.1.1/report.html)

[![Invoice report showing the 12 trays billed, 10 received and S$215 eligible for drafting](https://raw.githubusercontent.com/dextee/invoice-match-workbench/v0.1.1/docs/invoice-review.png)](https://github.com/dextee/invoice-match-workbench/releases/tag/v0.1.1)

## What a cybersecurity finding looks like

**Could an invoice agent approve its own work?** In this sample access review, finance authorised the agent to draft invoices. One extra permission also let its role approve them. The finding identifies the exact row, explains the business impact and shows the corrected export beside the agreed permissions. It also records the runtime check a release owner would still need. [Read the sample finding and retest](https://github.com/dextee/dextee/tree/main/security-review)

For teams that release sensitive documents, my PDF checker can find a reviewer's note that survives in an annotation or compressed object. Its sample reports distinguish a match from a file it could only partially inspect. [Inspect the PDF release checker](https://github.com/dextee/pdf-release-preflight)

## More engineering work

- **Choosing a model.** Two routing strategies each scored 20/20 on the same synthetic billing cases in two trials. The second model added about 19 seconds per batch. The records and offline grader are public. [Replay the routing evaluation](https://github.com/dextee/agent-routing-evals/releases/tag/v0.1.1)
- **Governing a release.** Inspect an attempted override, the evidence behind a held invoice and the corrected receipt that changed the decision. [Read the worked governance review](https://github.com/dextee/singapore-ai-governance-checklist/blob/main/docs/invoice-workbench-release-review.md)
- **Building agent teams.** Start with a duplicate-charge support ticket, then inspect the roles and handoffs in the guide for your environment. [Support example](https://github.com/dextee/chatgpt-agent-team-guide/tree/v2026.11.20/examples/support-triage) · [ChatGPT and Codex](https://github.com/dextee/chatgpt-agent-team-guide/releases/tag/v2026.11.20) · [Claude Code](https://github.com/dextee/claude-agent-team-guide/releases/tag/v3.0.0) · [Kimi Code](https://github.com/dextee/kimi-agent-team-guide)

I spoke at HITBSecConf2023 in Phuket while CTO at Privacy Ninja. The organiser's speaker record covers my background in vulnerability assessment and penetration testing. [HITB speaker record](https://conference.hitb.org/hitbsecconf2023hkt/speaker/dexter-ng/) · [Meet the VYR team](https://vyrwork.com/about)
