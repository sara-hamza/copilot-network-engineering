# copilot-network-engineering

## What it does

Network Engineer: config review, change validation, routing analysis and troubleshooting from pasted configs and logs.

Part of the **department-copilots** suite: local-only copilots where the employee provides the input, Claude analyses it on the machine, and the employee decides what to do. No CRM, NMS, email or system integrations.

## Install

```bash
claude plugin marketplace add sara-hamza/department-copilots
```

```bash
claude plugin install network-engineering@department-copilots
```

Paste a config snippet, a proposed change, a log extract or a routing table and get back a structured review, a layered troubleshooting plan, a plain explanation or an offline lab to test it.

| Command | Use when |
|---|---|
| `/network-engineering:troubleshoot <paste>` | Routing, MPLS, aggregation or NNI fault. Layered evidence table and next checks |
| `/network-engineering:review-config <paste>` | Review an existing or proposed config for hygiene, policy gaps and risk |
| `/network-engineering:review-change <paste>` | Review a change request: intent, risks, pre-checks, order, verification, rollback |
| `/network-engineering:explain <paste or question>` | Explain a config or protocol behaviour with a worked packet or route path |
| `/network-engineering:build-lab <paste or description>` | Produce a minimal containerlab / EVE-NG style lab to test a change offline |

Requires `copilot-common`. Works with `sticky-notes` for carrying context between sessions.

Reference knowledge lives in `skills/network-engineer/references/`. Platform names, maintenance-window rules and the risk matrix thresholds there are sensible defaults marked `CUSTOMISE`; tune them to the company's standards.
