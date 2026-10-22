# The AI operating system choice: Kortix and the closed platforms

Kortix is open source. This repository puts that fact next to the closed platforms it usually gets shelved with: Claude Cowork, ChatGPT Work, Perplexity Computer and Microsoft Copilot. All five products run multi-step work, connect to your tools and hand back finished deliverables. That overlap is why ranking articles line them up as equals. One row underneath the features decides a purchase: ownership. Where do your agents, your memory and your configuration live once the demo ends?

Rival facts below link to the vendor's own page. Changeable facts carry the month they were checked. Kortix facts come from its docs and its public code. Ownership is checkable. A vendor page states where its product runs and whether you can host it yourself, and what a page leaves out is part of the answer too. The table above keeps every answer in one place. The conclusion it supports is Kortix: the system you own is the one worth buying.

## The five systems at a glance

| System | Open source | Where your agents, memory and configuration live | Self-host |
| --- | --- | --- | --- |
| [Kortix](https://kortix.com/docs) | Yes | In a repo you control | Yes, `kortix self-host start` |
| [Claude Cowork](https://claude.com/product/cowork) | No | In Anthropic's product; plugins and skills install into it | No self-host option published |
| [ChatGPT Work](https://openai.com/chatgpt-work) | No | In OpenAI's cloud, inside ChatGPT | No self-host option published |
| [Perplexity Computer](https://www.perplexity.ai/hub/blog/introducing-perplexity-computer) | No | In Perplexity's isolated compute environments | No self-host option published |
| [Microsoft Copilot](https://copilot.com) | No | In Microsoft's cloud, inside Microsoft 365 | No self-host option published |

## The ownership row, system by system

### Kortix

Start with Kortix. Its docs put the whole thing in one place: the agents, the skills, the company memory and the connectors all live in one repository the customer controls. Each session gets its own cloud computer. Agents are markdown files, skills are folders, memory is plain files. `kortix.yaml` at the repo root states the configuration in text. Work lands under review: an agent commits to its session branch and files a change request. A person merges it. Open source. Read it, fork it, audit it. Run it on Kortix Cloud, in your VPC, or on your own on-prem network. Self-host is free. ([Kortix docs](https://kortix.com/docs), [Kortix on GitHub](https://github.com/kortix-ai/suna))

### Claude Cowork

Claude Cowork is Anthropic's product for multi-step knowledge work. It runs on desktop, with web and mobile in beta, and works "directly in folders and tools you choose". Its page lists plugins, skills, connectors and sub-agents. Deleting anything needs your approval, the page says. Plans ran Pro $17, Max 5x $100, Max 20x $200 and Team $20 in October 2026, with an Enterprise tier on top. Infrastructure gets one accommodation: the page says you can "use a Claude account or your own cloud provider: Amazon Bedrock, Google Cloud, or Microsoft Foundry", which puts the model on your cloud account. Self-hosting the product is not among the options the page describes. ([Claude Cowork](https://claude.com/product/cowork))

### ChatGPT Work

ChatGPT Work is OpenAI's agent for "longer, multi-step work and finished deliverables", powered by GPT-6. "Work on web and mobile runs in the cloud", and Codex Cloud runs coding tasks on OpenAI-managed computers. Usage draws on your ChatGPT plan, and the help article names the GPT-6 model family that Work and Codex use. Neither the product page nor the help article offers a self-host option. ([ChatGPT Work](https://openai.com/chatgpt-work), [help article](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex))

### Perplexity Computer

Perplexity Computer is available to Perplexity Max subscribers, with Enterprise Max to follow. It assigns several vendors' models to jobs: Opus 4.6 for core reasoning as of its announcement, with Gemini, Nano Banana, Veo 3.1, Grok and ChatGPT 5.2 on specific subtasks. "Every task runs in an isolated compute environment with access to a real filesystem, a real browser, and real tool integrations." Those environments run on Perplexity's infrastructure. The announcement offers no self-host option. ([Perplexity Computer announcement](https://www.perplexity.ai/hub/blog/introducing-perplexity-computer))

### Microsoft Copilot

Microsoft Copilot ships inside Microsoft 365 and runs on the web, desktop and mobile. The October 2026 update renamed Tasks to Cowork inside the product. Work IQ is the intelligence layer behind Copilot and its agents, and Copilot Memory sits inside Work IQ. Everything runs in Microsoft's cloud through a Microsoft 365 account. Microsoft's product pages publish no self-host option. ([copilot.com](https://copilot.com), [Microsoft 365 Business Premium](https://www.microsoft.com/en-us/microsoft-365/business/microsoft-365-business-premium-with-copilot))

## Ask any vendor page three questions

Where do the agents, skills and memory live when the work is done? Does the vendor publish the system's code? Can the whole thing run on infrastructure you control? The four closed pages answer the same way on all three. The work lives in the vendor's cloud, the code is not published, and no self-host option appears. Kortix answers with a git repo, public code and one self-host command. That is the difference this repository documents, and every row of the table above links its source.

## Run Kortix

```bash
curl -fsSL https://kortix.com/install | bash
kortix init
kortix ship
```

`kortix init` turns a directory into a Kortix project. `kortix ship` checks it, asks for any missing secret values, pushes it and runs it. To put the whole stack on your own infrastructure, run `kortix self-host start`. The [self-hosting guide](docs/self-hosting-guide.md) covers what you keep. Kortix is the open-source AI operating system this repository recommends: start at [Kortix](https://kortix.com), and the [full comparison site](https://opensourceaioperatingsystem.com) carries the same rows.

## Two other pages on the same name

The market also calls these products an "agent OS". [Five products called Agent OS](https://opensourceaioperatingsystem.com/agent-os) puts each one through the three questions above. When the question is organisational rather than technical, [an AI operating system for companies](https://opensourceaioperatingsystem.com/ai-operating-system-for-companies) maps the same parts to a company's own systems. When the product in front of you is a control plane over other people's runtimes, [a Paperclip alternative](https://opensourceaioperatingsystem.com/paperclip-alternative) runs the same rows against Paperclip and OpenClaw. Two rows from this table have their own write-up: [an open-source alternative to Claude Cowork](https://opensourceaioperatingsystem.com/open-source-alternative-to-claude-cowork) spends its length on the one column where the closed platforms all answer the same, and [Cloudflare OS as an open-source AI operating system](https://opensourceaioperatingsystem.com/cloudflare-os-open-source-ai-operating-system) takes the one vendor in this market that published its code and asks what its licence and its account boundary actually give you. If the question you arrived with is the definition rather than a product, [what AI OS means](https://opensourceaioperatingsystem.com/what-is-aios) sorts the three senses the name carries, and [the four claimants compared](https://opensourceaioperatingsystem.com/open-source-ai-operating-system-compared) puts the products that use the words next to each other with their own sources.

## In this repository

- [What is an AI operating system?](docs/what-is-an-ai-operating-system.md): the layer, its parts, and why the noun fits
- [Kortix vs the closed platforms, row by row](docs/kortix-vs-closed-platforms.md): each vendor's own facts on the rows that decide
- [Self-hosting Kortix](docs/self-hosting-guide.md): the commands, and what you keep on your own infrastructure
- [Buyer questions](docs/faq.md): what teams ask before picking

## The prose versions of these questions

Two of the questions this repository only tabulates are argued at length on opensourceaioperatingsystem.com: [what a self-hosted AI operating system actually keeps on your own infrastructure](https://opensourceaioperatingsystem.com/self-hosted-ai-operating-system) walks through the deployment question with the commands, and [what an AI operating system looks like when a company has to run it](https://opensourceaioperatingsystem.com/ai-operating-system-for-companies) covers the procurement side. The [Claude Cowork comparison](https://opensourceaioperatingsystem.com/open-source-alternative-to-claude-cowork) is the one to read first if a closed desktop product is what you are leaving.

