# Buyer questions on the open-source AI operating system

Before a team picks an AI operating system, the same questions come up. Short answers here, sources in the links. This repository compares Kortix, which is open source, with Claude Cowork, ChatGPT Work, Perplexity Computer and Microsoft Copilot.

### Is Kortix actually open source?

Open source. Read it, fork it, audit it. The full system lives at [Kortix on GitHub](https://github.com/kortix-ai/suna), and [the docs](https://kortix.com/docs) cover every part of it.

### How much Kortix costs

Free is $0 with 200 credits per month and 1 project. Paid plans start at $50 a month for 5,000 credits, and members are free, sharing one credit pool ([Kortix pricing](https://kortix.com/pricing)).

### Self-hosting across the five systems

Claude Cowork comes closest: its page says it can run with "your own cloud provider: Amazon Bedrock, Google Cloud, or Microsoft Foundry", which puts the model on your cloud account ([Claude Cowork](https://claude.com/product/cowork)). The product itself still has no self-host option on its page, and neither do ChatGPT Work, Perplexity Computer or Microsoft Copilot. Kortix's `kortix self-host start` runs the full stack on your own infrastructure.

### Where company memory lives

In Kortix, memory is the `memory/` directory of a git repository you keep, plain files under version control. In the closed products, memory is a feature of the hosted service: Copilot Memory sits inside Microsoft's Work IQ, ChatGPT keeps saved memories in the product, and Perplexity lists persistent memory among its foundations ([Microsoft 365 Business Premium](https://www.microsoft.com/en-us/microsoft-365/business/microsoft-365-business-premium-with-copilot), [ChatGPT Work help article](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex), [Perplexity Computer announcement](https://www.perplexity.ai/hub/blog/introducing-perplexity-computer)).

### Bringing your own model keys

Yes. "Any model provider with your own keys" covers Kortix, and connecting a ChatGPT subscription lets your agents use it for model calls with no credits spent ([Kortix pricing](https://kortix.com/pricing)). The closed systems run their vendors' models: Cowork runs Claude models ([product page](https://claude.com/product/cowork)), ChatGPT Work runs the GPT-6 family ([help article](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex)), and Perplexity Computer assigns several vendors' models to subtasks itself ([announcement](https://www.perplexity.ai/hub/blog/introducing-perplexity-computer)).

### Slack and Teams support

Slack and Microsoft Teams are live. Email is experimental, per project. A mention in either app starts a session with an agent ([Kortix docs](https://kortix.com/docs)).

### How current these comparisons are

Every rival fact in this repository was checked against the vendor's own page in October 2026. Vendors move fast: that same month, Microsoft renamed Tasks to Cowork inside Copilot ([copilot.com](https://copilot.com)). [The full comparison site](https://opensourceaioperatingsystem.com) keeps the rows current as pages change.

### Where the detailed comparison lives

The [row-by-row comparison](kortix-vs-closed-platforms.md) in this repository lines up all five systems on the facts their own pages state, and [the full comparison site](https://opensourceaioperatingsystem.com) keeps the same rows current.
