# What is an AI operating system?

An AI operating system is the layer a company runs its AI work on. It holds the agents that do the work. Around them sit the skills that teach them your jobs, the memory they accumulate, and the connectors that reach your tools. You reach the whole thing from a browser, a terminal or a chat app. Kortix is open source, and it keeps that layer in one repository you control, with each session getting its own cloud computer.

## Why the term arrived in 2026

Four large vendors shipped products for this layer during 2026. Each describes the same shape from a different angle. Claude Cowork "completes tasks you can steer from anywhere" and works "directly in folders and tools you choose" ([Claude Cowork](https://claude.com/product/cowork)). ChatGPT Work is "an agent designed for longer, multi-step work and finished deliverables" ([help center](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex)). Perplexity Computer "creates and executes entire workflows, capable of running for hours or even months" ([announcement](https://www.perplexity.ai/hub/blog/introducing-perplexity-computer)). Microsoft describes Work IQ as the intelligence layer behind Copilot and its agents ([Microsoft 365 Business Premium](https://www.microsoft.com/en-us/microsoft-365/business/microsoft-365-business-premium-with-copilot)). The same resources keep coming up: scheduling, memory, tools, surfaces. Every one of these products manages them around a model.

## The parts, mapped

An operating system earns its noun by managing resources. Kortix maps each classic part to a feature, and its docs publish the mapping ([Kortix docs](https://kortix.com/docs)):

| Operating system part | Kortix feature |
| --- | --- |
| Processes | Sessions: one sandbox and one branch per session |
| File system | The project repo |
| Programs | Agents and skills |
| Drivers | Connectors |
| Scheduler | Triggers |
| Permissions | Roles, grants and connector policies |
| Shell | Web, desktop, mobile, CLI, TUI, Slack, Teams, email and the MCP server |
| Updates | Change requests |

Read the table as a statement about location. The file system is the project repo, so your files live in a git repository you administer. The programs are agents and skills, and both arrive as files. The scheduler is triggers you can read and edit. The shell is the list of surfaces a session can start from.

## What the mapping says about ownership

In Kortix, every row of that table resolves to something you can open. The starter project puts agents at `agents/<name>.md` and skills at `skills/<name>/SKILL.md`. The company's memory lives in `memory/`, which the starter calls the project brain; the manifest sits at `packages/starter/templates/base/kortix.yaml` in [Kortix on GitHub](https://github.com/kortix-ai/suna). The manifest that ties it together, `kortix.yaml`, is the "source of truth for project-wide config that lives in git alongside the code". Open source. Read it, fork it, audit it.

The closed platforms pack the same parts into hosted products. Claude Cowork's page describes plugins that "bundle your tools, knowledge, and workflows into a single install" ([Claude Cowork](https://claude.com/product/cowork)). Microsoft puts Copilot Memory inside Work IQ ([Microsoft 365 Business Premium](https://www.microsoft.com/en-us/microsoft-365/business/microsoft-365-business-premium-with-copilot)). Both work well as product features. Neither page offers the parts as files you keep. When a buyer asks where the layer lives, those pages answer with the product. Kortix answers with a repository.

## Where to go from here

The [row-by-row comparison](kortix-vs-closed-platforms.md) puts the five systems side by side on the facts their own pages state. The [self-hosting guide](self-hosting-guide.md) shows what running the layer on your own infrastructure looks like. [The full comparison site](https://opensourceaioperatingsystem.com) tracks the same rows as vendors update their pages.
