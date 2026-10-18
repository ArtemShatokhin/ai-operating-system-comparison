# Self-hosting Kortix: the commands and what you keep

Kortix self-hosts with one command. `kortix self-host start` installs and runs the full stack on your own infrastructure. Three parts accumulate as you use it: the memory your agents write, the credentials they spend, and the record of what they did. Self-hosting puts all three on hardware you control. The commands below get a project running first.

## Three commands to a running project

```bash
curl -fsSL https://kortix.com/install | bash
kortix init
kortix ship
```

The first line installs the `kortix` CLI. `kortix init` turns a directory into a Kortix project. It writes the starter files: `kortix.yaml` at the root, agents as `agents/<name>.md`, skills under `skills/`, and the project's memory under `memory/`. The starter manifest lives at `packages/starter/templates/base/kortix.yaml` in [Kortix on GitHub](https://github.com/kortix-ai/suna). Its header calls `kortix.yaml` the "source of truth for project-wide config that lives in git alongside the code". `kortix ship` checks the project, asks for any missing secret values, pushes it and runs it. The repo behaves the same on your laptop and in the cloud. Nothing about these three commands changes when you later self-host.

## What self-host start does

Run it after the three commands above. The first run asks six things and no model key. Models are BYOK in the app, so model usage goes to whichever provider owns the key you add. GitHub connects in the dashboard, under Settings and Git. ([Kortix docs](https://kortix.com/docs))

## The memory

The `memory/` directory in the repo is the project brain. It is plain files under version control, sitting next to the agents that read and write it. Self-hosted, those files live on the storage you point the stack at. You can back them up, diff them and move them like any other files. The contrast on this row comes from Microsoft, which puts Copilot Memory inside its hosted Work IQ layer ([Microsoft 365 Business Premium](https://www.microsoft.com/en-us/microsoft-365/business/microsoft-365-business-premium-with-copilot)).

## The credentials

Secrets live in the stack you run. "Secrets are encrypted at rest with a key per project." Connector credentials are brokered server-side and never enter the machine; self-hosted, the service that brokers them is part of your stack. A new secret defaults to the environment exposure. An egress-enforced secret keeps its real value out of the sandbox entirely. The sandbox holds a handle, and the real value is substituted outside it, only on approved HTTPS hosts. That exposure is still experimental. ([Kortix docs](https://kortix.com/docs))

## The audit trail

"Every action is recorded." Sessions start, connector calls fire, agents propose changes, and each one leaves a record in the stack you run. Work still moves through review. An agent commits to its session branch and files a change request, and a person reviews and merges it ([Kortix docs](https://kortix.com/docs)). On your own infrastructure, that record sits next to everything else the system keeps.

## What self-hosting does not change

The install pulls its components over the internet, like any software you install. Each session still gets its own cloud computer. Teams with stricter network requirements scope isolated topologies with the Kortix team directly.

## Where to go next

The [Kortix docs](https://kortix.com/docs) carry the full self-hosting reference. The [row-by-row comparison](kortix-vs-closed-platforms.md) shows what the closed platforms offer on this same row. [The full comparison site](https://opensourceaioperatingsystem.com) tracks both as vendor pages change.
