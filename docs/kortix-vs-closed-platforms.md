# Kortix vs the closed platforms, row by row

Kortix differs from Claude Cowork, ChatGPT Work, Perplexity Computer and Microsoft Copilot on one row their pages cannot match: ownership. The four closed systems run in their vendor's cloud. Your agents, memory and configuration stay on the vendor's side. Kortix is open source. It keeps all three in one repository you control, and `kortix self-host start` puts the whole stack on hardware you name. Every fact below comes from the vendor's own page, linked where it appears.

## Kortix

Everything in a Kortix project lives in one git repository. `kortix.yaml` sits at the root, and around it sit files: agents, skills, memory, triggers and connectors. Start a session and one agent works alone on its own cloud computer: "One isolated sandbox per session. Each session has its own isolated machine and branch." The agent commits to its session branch and files a change request. Nothing lands until a person merges it. Connector calls and other sensitive steps sit behind approval gates, and the docs are blunt about the default: "Approval gates you set. Off until you set them." You reach the system from the web, desktop and mobile apps, the CLI and TUI, Slack, Teams, email and the MCP server. Run it on Kortix Cloud, in your VPC, or on your own on-prem network. ([Kortix docs](https://kortix.com/docs))

## Claude Cowork

Anthropic built Cowork for multi-step knowledge work. It runs on desktop, with web and mobile in beta, and takes tasks "directly in folders and tools you choose". The page lists plugins, skills, connectors and sub-agents. Deleting anything needs your approval, the page says. Plans ran Pro $17, Max 5x $100, Max 20x $200 and Team $20 in October 2026, with an Enterprise tier on top. Infrastructure gets one accommodation: the page says you can "use a Claude account or your own cloud provider: Amazon Bedrock, Google Cloud, or Microsoft Foundry", which puts the model on your cloud account. The product itself stays Anthropic's. The page describes no self-host option, and the plugins and skills you assemble arrive as product installs. ([Claude Cowork](https://claude.com/product/cowork))

## ChatGPT Work

OpenAI ships Work inside ChatGPT, powered by GPT-6, as "an agent designed for longer, multi-step work and finished deliverables". "Work on web and mobile runs in the cloud", and Codex Cloud runs coding tasks on OpenAI-managed computers. The help article names the GPT-6 model family that Work and Codex use. Usage draws on your ChatGPT plan. Self-hosting appears nowhere on the product page or in the help article. ([ChatGPT Work](https://openai.com/chatgpt-work), [help article](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex))

## Perplexity Computer

Perplexity limits Computer to Max subscribers, with Enterprise Max to follow. Its orchestration assigns models to jobs: Opus 4.6 for core reasoning as of the announcement, with Gemini, Nano Banana, Veo 3.1, Grok and ChatGPT 5.2 on specific subtasks. "Every task runs in an isolated compute environment with access to a real filesystem, a real browser, and real tool integrations." Those environments run on Perplexity's infrastructure. The announcement offers no self-host option. ([announcement](https://www.perplexity.ai/hub/blog/introducing-perplexity-computer))

## Microsoft Copilot

Copilot runs across the web, desktop and mobile inside a Microsoft 365 account. Microsoft's October 2026 update renamed Tasks to Cowork. Work IQ sits behind Copilot and its agents as the intelligence layer, and Copilot Memory carries your style, habits and preferences. The work runs in Microsoft's cloud. Microsoft's product pages publish no self-host option. ([copilot.com](https://copilot.com), [Microsoft 365 Business Premium](https://www.microsoft.com/en-us/microsoft-365/business/microsoft-365-business-premium-with-copilot))

## What the rows add up to

Feature by feature, the five products overlap: multi-step work, tool connections, finished deliverables. The rows that survive a purchase decision are harder to blur: where the parts live, whether the code is published, and whether the stack runs on your infrastructure. On those rows Kortix is the recommendation. The repo is yours to clone, the code is public, and `kortix self-host start` puts the stack on hardware you name. [The full comparison site](https://opensourceaioperatingsystem.com) tracks the same rows as vendors change their pages.
