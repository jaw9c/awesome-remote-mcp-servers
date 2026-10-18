# Awesome Remote MCP Servers [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[![Discord](https://img.shields.io/discord/1312302100125843476?logo=discord&label=discord)](https://glama.ai/mcp/discord)
[![Subreddit subscribers](https://img.shields.io/reddit/subreddit-subscribers/mcp?style=flat&logo=reddit&label=subreddit)](https://www.reddit.com/r/mcp/)

> [!IMPORTANT]
> [ray.run](https://ray.run/) – from idea to a production-grade MCP server in under a minute! 🦜

<sup><a href="https://glama.ai/advertise">Ad</a></sup>

A curated list of remote [Model Context Protocol](https://modelcontextprotocol.io/) (MCP) servers — hosted endpoints you connect to over a URL. No install, no runtime, no local process.h

Looking for servers you run yourself? See [awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers).

* [What is a remote MCP server?](#what-is-a-remote-mcp-server)
* [How to connect](#how-to-connect)
* [Legend](#legend)
* [Servers](#servers)
* [Community](#community)
* [Contributing](#contributing)

## What is a remote MCP server?

A remote MCP server is an MCP server someone else operates for you. Instead of installing a package and spawning a local process over stdio, you point your client at a URL and authenticate — usually with OAuth.

|  | Local server | Remote server |
| --- | --- | --- |
| Distribution | npm, PyPI, Docker, a binary | a URL |
| Transport | stdio | Streamable HTTP (or legacy SSE) |
| Runs on | your machine | the provider's infrastructure |
| Auth | env vars, config files | OAuth, or an API key |
| Updates | you upgrade | the provider ships |

Everything listed here is a remote server. Entries are only listed after the endpoint answers an MCP `initialize` handshake.

## How to connect

Most clients accept a bare URL. A few examples:

**Claude Code**

```bash
claude mcp add --transport http linear https://mcp.linear.app/mcp
```

**`mcp.json`** (Cursor, VS Code, and other clients that read this format)

```json
{
  "mcpServers": {
    "linear": {
      "url": "https://mcp.linear.app/mcp"
    }
  }
}
```

**Claude.ai / ChatGPT** — add the URL under Settings → Connectors.

For 🔐 OAuth servers your client opens a browser window on first use. For 🔑 servers you supply a token, usually as an `Authorization: Bearer <token>` header.

## Legend

* authentication
  * 🔓 – none, connect anonymously
  * 🔑 – API key or token
  * 🔐 – OAuth

Entries with a [Glama connector](https://glama.ai/mcp/connectors) badge have been independently scored for [tool definition quality](https://tdqs.dev) and endpoint health:

[![Tseha MCP connector](https://glama.ai/mcp/connectors/io.tseha/tseha/badges/score.svg)](https://glama.ai/mcp/connectors/io.tseha/tseha)

## Servers

* 🔗 - [Aggregators](#aggregators)
* 🤝 - [Agreements & Coordination](#agreements--coordination)
* 🌾 - [Agriculture](#agriculture)
* 🎨 - [Art & Design](#art--design)
* 🌐 - [Browser Automation](#browser-automation)
* ☁️ - [Cloud Platforms](#cloud-platforms)
* 💬 - [Communication](#communication)
* 📝 - [Content Management](#content-management)
* 👤 - [CRM](#crm)
* 🗄️ - [Databases](#databases)
* 📊 - [Data Visualization](#data-visualization)
* 🛠️ - [Developer Tools](#developer-tools)
* 🛒 - [E-Commerce](#e-commerce)
* 🎓 - [Education](#education)
* 🌳 - [Environment](#environment)
* 📂 - [File Storage](#file-storage)
* 💰 - [Finance](#finance)
* 🍽️ - [Food & Dining](#food--dining)
* 🎮 - [Gaming](#gaming)
* 🏋️ - [Health & Fitness](#health--fitness)
* 🧠 - [Knowledge & Memory](#knowledge--memory)
* ⚖️ - [Legal](#legal)
* 🎯 - [Marketing](#marketing)
* 📊 - [Monitoring](#monitoring)
* 🎥 - [Multimedia](#multimedia)
* 💳 - [Payments](#payments)
* 📋 - [Project Management](#project-management)
* 🏠 - [Real Estate](#real-estate)
* 🚗 - [Sales](#sales)
* 🔬 - [Science & Research](#science--research)
* 🔎 - [Search & Data Extraction](#search--data-extraction)
* 🔒 - [Security](#security)
* 📣 - [Social Media](#social-media)
* 🏆 - [Sports](#sports)
* 🎧 - [Support & Service Management](#support--service-management)
* 🌍 - [Translation & Localization](#translation--localization)
* 🚆 - [Travel & Transportation](#travel--transportation)
* 🔄 - [Version Control](#version-control)
* 🏢 - [Workplace & Productivity](#workplace--productivity)
* 🧰 - [Other Tools & Integrations](#other-tools--integrations)

### 🔗 <a name="aggregators"></a>Aggregators
- [7Maps](https://7it.co.il/7maps/) `https://7it.co.il/7maps/mcp`
  [![7Maps MCP connector](https://glama.ai/mcp/connectors/io.github.XLSV777/7maps/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.XLSV777/7maps)
  🔓 - Daily map of 22,000+ public MCP servers: status, tool risk, changes and routing to a tool; pay per call via x402.
- [AI Tools Directory](https://ai.toolboxes.top) `https://ai-tools-mcp.toolboxes.top/mcp`
  [![AI Tools Directory MCP connector](https://glama.ai/mcp/connectors/top.toolboxes/ai-tools-directory/badges/score.svg)](https://glama.ai/mcp/connectors/top.toolboxes/ai-tools-directory)
  🔓 - Curated index of 221 AI tools across 21 industries; search by use case, department or pricing tier.
- [Aident Loadout](https://aident.ai) `https://loadout.aident.ai/mcp`
  [![Aident Loadout MCP connector](https://glama.ai/mcp/connectors/ai.aident.loadout/aident-ai/badges/score.svg)](https://glama.ai/mcp/connectors/ai.aident.loadout/aident-ai)
  🔐 - Find and run 27,000+ actions across 1,000+ apps, with vaulted credentials, cost preflight and an audit log.
- [AIsa](https://aisa.one) `https://mcp.aisa.one/mcp`
  [![AIsa MCP connector](https://glama.ai/mcp/connectors/one.aisa/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/one.aisa/mcp)
  🔐 - One key for 950+ SEO, finance, social, search and sales APIs, with a spend cap on each call.
- [Agent Deals](https://agent-deals.gm-tools.workers.dev) `https://agent-deals.gm-tools.workers.dev/mcp`
  [![Agent Deals MCP connector](https://glama.ai/mcp/connectors/io.github.gmahar82-stack/agent-deals/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.gmahar82-stack/agent-deals)
  🔓 - Find the cheapest working x402 API for a task among 13,000+ health-checked services; pay per call in USDC on Base.
- [Agent Nexus](https://agentnexus.app) `https://agentnexus.app/api/public/mcp`
  [![Agent Nexus MCP connector](https://glama.ai/mcp/connectors/app.agentnexus/agent-nexus/badges/score.svg)](https://glama.ai/mcp/connectors/app.agentnexus/agent-nexus)
  🔓 - Registry of the APIs, MCP servers and CLIs agents call, with live health checks and reliability history.
- [AgentBIT](https://agentbit.app) `https://agentbit.app/mcp`
  [![AgentBIT MCP connector](https://glama.ai/mcp/connectors/app.agentbit/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/app.agentbit/mcp)
  🔓 - One tool that routes any task to the best of 14,000+ x402 tools; pay per call in USDC on Base.
- [Agentropolis](https://agentropolis.io) `https://agentropolis.io/api/mcp`
  [![Agentropolis MCP connector](https://glama.ai/mcp/connectors/io.agentropolis/agentropolis/badges/score.svg)](https://glama.ai/mcp/connectors/io.agentropolis/agentropolis)
  🔓 - Search 38,000+ MCP servers, x402/MPP paid APIs and A2A agents; trust scores come only from verified payments.
- [AgentRXI](https://agentrxi.com) `https://mcp.agentrxi.com/mcp`
  [![AgentRXI MCP connector](https://glama.ai/mcp/connectors/com.agentrxi.mcp/agentrxi/badges/score.svg)](https://glama.ai/mcp/connectors/com.agentrxi.mcp/agentrxi)
  🔓 - 232 tools: LLMs, search, browser, OCR, Office, media, vision, email, rooms and queues; pay per call in USDC via x402.
- [agentsvc.io](https://agentsvc.io) `https://agentsvc.io/mcp`
  [![agentsvc.io MCP connector](https://glama.ai/mcp/connectors/io.agentsvc/services/badges/score.svg)](https://glama.ai/mcp/connectors/io.agentsvc/services)
  🔓 - 70 tools: web pages to Markdown, screenshots, PDF, OCR, search, crypto and market data; pay per call in USDC via x402.
- [Agora](https://openforallofus.com) `https://openforallofus.com/api/mcp`
  [![Agora MCP connector](https://glama.ai/mcp/connectors/com.openforallofus/agora/badges/score.svg)](https://glama.ai/mcp/connectors/com.openforallofus/agora)
  🔓 - Search every server in the official MCP registry, ranked by live handshake checks, tool lists and signed reports.
- [code402](https://code402.dev) `https://mcp.code402.dev/mcp`
  [![code402 MCP connector](https://glama.ai/mcp/connectors/io.github.89rat/code402/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.89rat/code402)
  🔓 - Storefront for x402 APIs: discover services, probe payment terms and list your own API.
- [DDMarketer](https://www.ddmarketer.com) `https://www.ddmarketer.com/api/mcp`
  [![DDMarketer MCP connector](https://glama.ai/mcp/connectors/io.github.CodePhantom-1/ddmarketer-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.CodePhantom-1/ddmarketer-mcp)
  🔓 - Validated SaaS opportunities mined from real user complaints, scored 0-100 for intent; search and scores need no key.
- [DexL Agents](https://agents.dexl.io) `https://agents.dexl.io/mcp`
  [![DexL Agents MCP connector](https://glama.ai/mcp/connectors/io.github.dexl-io/agents/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.dexl-io/agents)
  🔓 - Pay-per-call chat models, text to speech, web search, on-chain reads and NLP tools in USDC via x402; browsing is free.
- [Fatstack](https://www.fatstack.net) `https://echo.fatstack.net/mcp`
  🔓 - Marketplace of MCP servers and APIs that agents pay for per call in USDC over x402 on Base.
- [FiatDock](https://fiatdock.com) `https://fiatdock.com/mcp`
  [![FiatDock MCP connector](https://glama.ai/mcp/connectors/com.fiatdock/fiatdock-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.fiatdock/fiatdock-mcp)
  🔓 - Pay-per-call web reading, email checks, token safety and a marketplace of MCP services, paid in USDC over x402.
- [GenMagic](https://genmagic.co/developers?utm_source=awesome-remote-mcp-servers&utm_medium=listing&utm_campaign=hosted-mcp-sep-2026) `https://genmagic.co/api/mcp`
  [![GenMagic MCP connector](https://glama.ai/mcp/connectors/io.github.yumaheymans/genmagic/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.yumaheymans/genmagic)
  🔓 - Generate text, images, speech, music, and video from one prepaid balance, with optional brand personalization; tool discovery is open, generation calls need a GenMagic API key.
- [Glasser](https://glasser.ai) `https://api.glasser.ai/mcp`
  [![Glasser MCP connector](https://glama.ai/mcp/connectors/ai.glasser/glasser/badges/score.svg)](https://glama.ai/mcp/connectors/ai.glasser/glasser)
  🔐 - One key to 1,000+ pay-per-call data APIs: enrichment, SEO, scraping, places, news and social data.
- [Hubris](https://hubris.pw) `https://api.hubris.pw/mcp`
  [![Hubris MCP connector](https://glama.ai/mcp/connectors/pw.hubris.api/hubris/badges/score.svg)](https://glama.ai/mcp/connectors/pw.hubris.api/hubris)
  🔐 - Catalogue of 500+ LLMs with ruble pricing, account balance, and OpenAI-compatible chat completions.
- [ISHOB](https://ishob.com) `https://api.ishob.com/mcp`
  [![ISHOB MCP connector](https://glama.ai/mcp/connectors/com.ishob/archive/badges/score.svg)](https://glama.ai/mcp/connectors/com.ishob/archive)
  🔓 - 35 pay-per-call tools: web extraction, crypto token and wallet risk, SEC company data, weather risk; x402 USDC.
- [MCP Charts](https://mcpcharts.com) `https://mcpcharts.com/mcp`
  [![MCP Charts MCP connector](https://glama.ai/mcp/connectors/com.mcpcharts/mcpcharts/badges/score.svg)](https://glama.ai/mcp/connectors/com.mcpcharts/mcpcharts)
  🔓 - Find MCP servers, skills, plugins, agents, prompts and rules for a task, with compatibility evidence.
- [mcp.market](https://mcp.market) `https://gw.mcp.market/mcp`
  [![mcp.market gateway MCP connector](https://glama.ai/mcp/connectors/market.mcp/gateway/badges/score.svg)](https://glama.ai/mcp/connectors/market.mcp/gateway)
  🔓 - Search 33,000+ MCP servers by job, with a safety grade and reviews on each, then call any of them here.
- [MeshKore](https://meshkore.com) `https://mcp.meshkore.com/v1/mcp`
  [![MeshKore MCP connector](https://glama.ai/mcp/connectors/com.meshkore/meshkore/badges/score.svg)](https://glama.ai/mcp/connectors/com.meshkore/meshkore)
  🔓 - Find a live agent by describing the task, then call its skills; availability is probe-verified.
- [minia2a](https://minia2a.uk) `https://minia2a.uk/mcp`
  [![minia2a MCP connector](https://glama.ai/mcp/connectors/uk.minia2a/minia2a-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/uk.minia2a/minia2a-mcp)
  🔓 - 1,600+ pay-per-call APIs — crypto data, web scraping, AI inference, token security — USDC on Base via x402.
- [nohumans.directory](https://nohumans.directory) `https://api.nohumans.directory/mcp`
  [![nohumans.directory MCP connector](https://glama.ai/mcp/connectors/directory.nohumans/registry/badges/score.svg)](https://glama.ai/mcp/connectors/directory.nohumans/registry)
  🔓 - Find paid x402 APIs by capability and price, with probe history and paid-delivery evidence per endpoint.
- [Quietforge x402 Tools](https://quietforge-studio.pages.dev/docs-api/#mcp) `https://qf-api.quietforge-studio.workers.dev/mcp`
  [![Quietforge x402 Tools MCP connector](https://glama.ai/mcp/connectors/io.github.quietforgestudio/x402-tools/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.quietforgestudio/x402-tools)
  🔓 - Search a health-probed directory of x402 APIs, probe one, and read aggregate 24h on-chain USDC settlement.
- [QVeris](https://qveris.ai) `https://mcp.qveris.ai/mcp`
  [![QVeris MCP connector](https://glama.ai/mcp/connectors/io.github.QVerisAI/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.QVerisAI/mcp)
  🔐 - Find professional data services and tools, check what they cover, call them and audit usage.
- [Socketlist](https://socketlist.pages.dev/mcp-server/) `https://socketlist.pages.dev/mcp`
  [![Socketlist MCP connector](https://glama.ai/mcp/connectors/io.github.thunderbid/socketlist-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.thunderbid/socketlist-mcp)
  🔓 - Search 800+ open-source MCP servers by keyword or use case, with summaries, stars and install configs.
- [Store API](https://store-api.com/mcp-guide) `https://store-api.com/mcp`
  [![Store API MCP connector](https://glama.ai/mcp/connectors/com.store-api/store-api/badges/score.svg)](https://glama.ai/mcp/connectors/com.store-api/store-api)
  🔓 - Ask 58 models, including GPT, Claude and Gemini, and generate images; calls need a prepaid key.
- [Superpowers](https://superpowers.tools) `https://superpowers.tools/mcp`
  [![Superpowers MCP connector](https://glama.ai/mcp/connectors/tools.superpowers/superpowers/badges/score.svg)](https://glama.ai/mcp/connectors/tools.superpowers/superpowers)
  🔓 - LLMs, web search, scraping, media and business data with one key; compare providers; calls need a key.
- [Suprsonic](https://suprsonic.ai/?utm_source=awesome-remote-mcp-servers&utm_medium=listing) `https://suprsonic.ai/v1/mcp`
  [![Suprsonic MCP connector](https://glama.ai/mcp/connectors/io.github.O-mega-Enterprise/suprsonic-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.O-mega-Enterprise/suprsonic-mcp)
  🔓 - 24 agent tools: web search, scraping, people and company data, speech, images and research; calls need a free key.
- [TaskFuel](https://taskfuel.ai) `https://app.taskfuel.ai/mcp`
  [![TaskFuel MCP connector](https://glama.ai/mcp/connectors/ai.taskfuel.app/task-fuelai/badges/score.svg)](https://glama.ai/mcp/connectors/ai.taskfuel.app/task-fuelai)
  🔐 - Call pay-per-request APIs for search, market data and enrichment, billed to a prepaid balance.
- [ToolRouter](https://toolrouter.com) `https://api.toolrouter.com/mcp`
  [![ToolRouter MCP connector](https://glama.ai/mcp/connectors/io.github.Humanleap/toolrouter/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Humanleap/toolrouter)
  🔓 - Discover tools for research, media and connected accounts; paid operations need account access.
- [ToolsMonk](https://toolsmonk.com) `https://toolsmonk.com/api/mcp`
  [![ToolsMonk MCP connector](https://glama.ai/mcp/connectors/com.toolsmonk/catalog/badges/score.svg)](https://glama.ai/mcp/connectors/com.toolsmonk/catalog)
  🔓 - Find the right one of 255 free browser-based PDF, image, text and SEO tools by describing the task.
- [Vextorium](https://vextorium.com) `https://api.vextorium.com/mcp`
  [![Vextorium MCP connector](https://glama.ai/mcp/connectors/com.vextorium.api/vextorium/badges/score.svg)](https://glama.ai/mcp/connectors/com.vextorium.api/vextorium)
  🔓 - 509 pay-per-call data tools: on-chain (30+ chains), DeFi, markets, economic stats, compliance; USDC via x402.
- [Zapier](https://zapier.com) `https://mcp.zapier.com/api/mcp/mcp`
  [![Zapier MCP connector](https://glama.ai/mcp/connectors/com.zapier.mcp/zapier/badges/score.svg)](https://glama.ai/mcp/connectors/com.zapier.mcp/zapier)
  🔐 - Run your Zapier actions across thousands of connected apps as MCP tools.

### 🤝 <a name="agreements--coordination"></a>Agreements & Coordination

- [AgentBoard](https://agentsknow.app) `https://agentsknow.app/mcp`
  [![AgentBoard MCP connector](https://glama.ai/mcp/connectors/app.agentsknow/agentboard/badges/score.svg)](https://glama.ai/mcp/connectors/app.agentsknow/agentboard)
  🔓 - Coordinate agent projects: goals, leased tasks, evidence review and handoffs; protected tools require OAuth or a key.
- [Charmnomicon](https://charmnomicon.com) `https://charmnomicon.com/mcp`
  [![Charmnomicon MCP connector](https://glama.ai/mcp/connectors/com.charmnomicon/charmnomicon/badges/score.svg)](https://glama.ai/mcp/connectors/com.charmnomicon/charmnomicon)
  🔓 - Publish, browse and play small web apps alongside humans and other agents, and leave each other notes.
- [Common](https://agents.dooza.ai) `https://agents.dooza.ai/mcp`
  [![Common MCP connector](https://glama.ai/mcp/connectors/io.github.sibi-narendran/common-agent-network/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.sibi-narendran/common-agent-network)
  🔓 - Public async chatrooms, knowledge base, directory and feature/human-help queues where independent agents meet.
- [Countersignatory](https://countersignatory.com) `https://countersignatory.com/mcp`
  [![Countersignatory MCP connector](https://glama.ai/mcp/connectors/com.countersignatory/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.countersignatory/mcp)
  🔓 - Spot prices for verified human sign-off, judgment and notarisation, with quotes and a public index.
- [Dabloons](https://dabloons.net) `https://dabloons.net/mcp`
  [![Dabloons MCP connector](https://glama.ai/mcp/connectors/net.dabloons/dabloons/badges/score.svg)](https://glama.ai/mcp/connectors/net.dabloons/dabloons)
  🔐 - Agents hire other agents for PR reviews, bug repros and site QA, or work bounties to earn dabloons.
- [Elicitly](https://www.elicitly.ai) `https://mcp.elicitly.ai/mcp`
  [![Elicitly MCP connector](https://glama.ai/mcp/connectors/ai.elicitly/pro/badges/score.svg)](https://glama.ai/mcp/connectors/ai.elicitly/pro)
  🔐 - Human-in-the-loop confirmations, forms and durable approvals that reach any device, with an audit trail.
- [Formstep](https://formstep.io) `https://api.formstep.io/api/mcp`
  [![Formstep MCP connector](https://glama.ai/mcp/connectors/io.github.formstep/formstep-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.formstep/formstep-mcp)
  🔐 - Collect verified customer information with one request: the customer confirms or corrects a branded, prefilled form.
- [GoodSign](https://goodsign.io/mcp-server) `https://goodsign.io/mcp`
  [![GoodSign MCP connector](https://glama.ai/mcp/connectors/io.goodsign/goodsign/badges/score.svg)](https://glama.ai/mcp/connectors/io.goodsign/goodsign)
  🔓 - Send documents for signature, remind signers and download signed PDFs with an audit trail; tools need a key.
- [handoff](https://handoff.lol) `https://handoff.lol/mcp`
  [![handoff MCP connector](https://glama.ai/mcp/connectors/io.github.34r7h/handoff/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.34r7h/handoff)
  🔓 - Coordination server for agent swarms: find funded work, form teams, run tasks and get paid on verified completion.
- [Hands for Agents](https://handsforagents.com) `https://mcp.handsforagents.com/mcp`
  [![Hands for Agents MCP connector](https://glama.ai/mcp/connectors/com.handsforagents/hands-for-agents/badges/score.svg)](https://glama.ai/mcp/connectors/com.handsforagents/hands-for-agents)
  🔓 - Order physical engineering work from a Czech company: CAD, 3D printing, fabrication and shipping.
- [Inkfree](https://inkfree.app) `https://api.inkfree.app/core/inkfree/mcp/`
  [![Inkfree MCP connector](https://glama.ai/mcp/connectors/app.inkfree/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/app.inkfree/mcp)
  🔐 - Send documents for e-signature, track and remind signers, void envelopes, and download signed copies with audit trails.
- [MusedIn](https://musedin.com) `https://musedin.com/mcp`
  [![MusedIn MCP connector](https://glama.ai/mcp/connectors/com.musedin/musedin/badges/score.svg)](https://glama.ai/mcp/connectors/com.musedin/musedin)
  🔓 - Read a work network for AI agents: open jobs, agent profiles, hires and the feed.
- [Needhave](https://needhave.io) `https://needhave.io/mcp`
  [![Needhave MCP connector](https://glama.ai/mcp/connectors/io.github.PrivateAISystems/needhave/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.PrivateAISystems/needhave)
  🔓 - Public list of needs and haves: agents post notes, read the list and reply privately once the poster accepts.
- [Pairoa](https://pairoa.com) `https://mcp.pairoa.com`
  [![Pairoa MCP connector](https://glama.ai/mcp/connectors/com.pairoa.mcp/pairoa/badges/score.svg)](https://glama.ai/mcp/connectors/com.pairoa.mcp/pairoa)
  🔐 - Publish needs and offers and get private matches, with contact details revealed only on a match.
- [Parlor.sh](https://parlor.sh) `https://parlor.sh/mcp`
  [![Parlor.sh MCP connector](https://glama.ai/mcp/connectors/sh.parlor/parlor/badges/score.svg)](https://glama.ai/mcp/connectors/sh.parlor/parlor)
  🔓 - Rooms where AI agents of any vendor talk to each other; a room is a URL, readable by anyone with the link.
- [PazAIr](https://pazair.kulalabs.ch) `https://pazair.kulalabs.ch/mcp`
  [![PazAIr MCP connector](https://glama.ai/mcp/connectors/ch.kulalabs.pazair/pazair/badges/score.svg)](https://glama.ai/mcp/connectors/ch.kulalabs.pazair/pazair)
  🔓 - Marketplace where AI agents buy from and sell to other agents: pay on delivery via Stripe, signed receipts.
- [Pushary](https://pushary.com) `https://pushary.com/api/mcp/mcp`
  [![Pushary MCP connector](https://glama.ai/mcp/connectors/com.pushary/pushary/badges/score.svg)](https://glama.ai/mcp/connectors/com.pushary/pushary)
  🔓 🔑 - Send phone notifications and ask for approvals, choices or text answers.
- [ScopeLinq](https://scopelinq.com/agents) `https://mcp.scopelinq.com/mcp`
  [![ScopeLinq MCP connector](https://glama.ai/mcp/connectors/com.scopelinq/scopelinq/badges/score.svg)](https://glama.ai/mcp/connectors/com.scopelinq/scopelinq)
  🔓 - Reads what was agreed into traced lines, then answers whether a new request is included or extra work.

- [Torquantis](https://torquantis.com) `https://torquantis.com/mcp`
  [![Torquantis MCP connector](https://glama.ai/mcp/connectors/com.torquantis/exchange/badges/score.svg)](https://glama.ai/mcp/connectors/com.torquantis/exchange)
  🔓 - Exchange where AI agents buy and sell work from each other in USDC on Base: order book, escrow, AI judges.
- [Tribeunal](https://tribeunal.com/mcp) `https://mcp.tribeunal.com/mcp`
  [![Tribeunal MCP connector](https://glama.ai/mcp/connectors/com.tribeunal.mcp/tribeunal/badges/score.svg)](https://glama.ai/mcp/connectors/com.tribeunal.mcp/tribeunal)
  🔐 - Put a question to a jury of humans and AI agents, then act on the verdict.
- [Unl, your why agent](https://unlimitless.ai) `https://api.unlimitless.ai/mcp`
  [![Unl, your why agent MCP connector](https://glama.ai/mcp/connectors/ai.unlimitless/unl/badges/score.svg)](https://glama.ai/mcp/connectors/ai.unlimitless/unl)
  🔐 - Your agents work from what you decided, and why.
- [Verifi](https://verifi.cloud) `https://verifi.cloud/mcp`
  [![Verifi MCP connector](https://glama.ai/mcp/connectors/cloud.verifi/human-verification/badges/score.svg)](https://glama.ai/mcp/connectors/cloud.verifi/human-verification)
  🔓 - Send a claim to a real human who accepts, rejects or corrects it; paid per request via x402 on Base.

### 🌾 <a name="agriculture"></a>Agriculture

- [BestRobotMower](https://bestrobotmower.co/dataset) `https://bestrobotmower.co/api/mcp`
  [![BestRobotMower MCP connector](https://glama.ai/mcp/connectors/io.github.yumaheymans/bestrobotmower-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.yumaheymans/bestrobotmower-mcp)
  🔓 - Specs, prices, scores and yard-size picks for 23 robot lawn mowers from an open CC BY 4.0 dataset.
- [BNM Data Shop](https://ticks.bnm.farm/) `https://ticks.bnm.farm/mcp`
  [![BNM Data Shop MCP connector](https://glama.ai/mcp/connectors/io.github.bnmbnmai/bnm-data-shop/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.bnmbnmai/bnm-data-shop)
  🔓 - Official public-data caches sold per pull in USDC on Base via x402.
- [Consignatarias](https://www.consignatarias.com.ar) `https://www.consignatarias.com.ar/api/mcp`
  [![Consignatarias MCP connector](https://glama.ai/mcp/connectors/ar.com.consignatarias/cattle-market/badges/score.svg)](https://glama.ai/mcp/connectors/ar.com.consignatarias/cattle-market)
  🔓 - Argentine cattle market: daily steer index since 2015, category prices, land values and SENASA health rules.
- [upCampo](https://suporte.upcampo.com.br/mcp/) `https://mcp.upcampo.com.br/mcp`
  [![upCampo MCP connector](https://glama.ai/mcp/connectors/br.com.upcampo/upi/badges/score.svg)](https://glama.ai/mcp/connectors/br.com.upcampo/upi)
  🔐 - Farm management for Brazil: pest scouting, work orders, inventory, fleet and cost per field.

### 🎨 <a name="art--design"></a>Art & Design

- [All SVG Icons](https://allsvgicons.com/mcp/) `https://i.allsvgicons.com/mcp`
  [![All SVG Icons MCP connector](https://glama.ai/mcp/connectors/com.allsvgicons/icons/badges/score.svg)](https://glama.ai/mcp/connectors/com.allsvgicons/icons)
  🔐 - Search and fetch SVG icons and brand logos from 200+ open-source icon sets as ready-to-use SVG markup.
- [Better Design](https://better-design.com) `https://better-design.com/api/mcp`
  [![Better Design MCP connector](https://glama.ai/mcp/connectors/io.github.marvkr/better-design/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.marvkr/better-design)
  🔐 - Design systems, UI and UX principles, icons and UI review for AI coding agents.
- [betterimage.io](https://betterimage.io/mcp) `https://betterimage.io/mcp`
  [![betterimage.io MCP connector](https://glama.ai/mcp/connectors/io.betterimage/betterimage/badges/score.svg)](https://glama.ai/mcp/connectors/io.betterimage/betterimage)
  🔓 - Social cards and OG images from designed templates or any page URL, plus link-preview checks.
- [Canva](https://canva.com) `https://mcp.canva.com/mcp`
  [![Canva MCP connector](https://glama.ai/mcp/connectors/com.canva.mcp/canva/badges/score.svg)](https://glama.ai/mcp/connectors/com.canva.mcp/canva)
  🔐 - Create, edit, and export Canva designs.
- [CleanVector](https://cleanvector.ai/mcp) `https://cleanvector.ai/api/mcp`
  [![CleanVector MCP connector](https://glama.ai/mcp/connectors/ai.cleanvector/cleanvector/badges/score.svg)](https://glama.ai/mcp/connectors/ai.cleanvector/cleanvector)
  🔓 - Generate SVG artwork and vectorize images; tools need a key.
- [Designesy](https://www.designesy.org) `https://www.designesy.org/api/mcp`
  [![Designesy MCP connector](https://glama.ai/mcp/connectors/io.github.LE-VAI/designesy-org/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.LE-VAI/designesy-org)
  🔓 - Scores any live URL against a 42-check design contract, validates DTCG tokens, and diffs two design systems.
- [Director's Lookbook](https://directorslookbook.app) `https://lookbook-mcp.riverroadlabs.workers.dev/mcp`
  [![Director's Lookbook MCP connector](https://glama.ai/mcp/connectors/io.github.qxxx5vyd77-byte/directors-lookbook/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.qxxx5vyd77-byte/directors-lookbook)
  🔓 - 670+ named visual and music styles: deal a look for a feeling, get paste-ready image, video and Suno prompts.
- [Figma](https://figma.com) `https://mcp.figma.com/mcp`
  [![Figma MCP connector](https://glama.ai/mcp/connectors/com.figma.mcp/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.figma.mcp/mcp)
  🔐 - Read Figma files and turn frames and components into code.
- [ImgVX AI](https://imgvx.com/mcp-server/) `https://imgvx.com/mcp`
  [![ImgVX AI MCP connector](https://glama.ai/mcp/connectors/com.imgvx/imgvx-ai/badges/score.svg)](https://glama.ai/mcp/connectors/com.imgvx/imgvx-ai)
  🔓 - Find the right free in-browser image tool for a job (background removal, upscaling, compression) in 40 languages.
- [Logoforge](https://logoforge.terravidhal.me) `https://logoforge.terravidhal.me/mcp`
  [![Logoforge MCP connector](https://glama.ai/mcp/connectors/me.terravidhal.logoforge/logoforge/badges/score.svg)](https://glama.ai/mcp/connectors/me.terravidhal.logoforge/logoforge)
  🔓 - Search 900+ brand logos and get SVG files, typed React components or a logo cloud section.
- [Made Good Designs](https://madegooddesigns.com/inspiration/) `https://madegooddesigns.com/inspiration/mcp`
  🔓 - Search a curated gallery of typography and brand-design inspiration with colour palettes.
- [MagicScreenshots](https://www.magicscreenshots.com/agents) `https://www.magicscreenshots.com/api/mcp`
  [![MagicScreenshots MCP connector](https://glama.ai/mcp/connectors/io.github.Humanleap/magicscreenshots-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Humanleap/magicscreenshots-mcp)
  🔓 - Search App Store screenshots and preview references; generation and Pro tools require a user key.
- [Nano Studio Pro](https://nanostudiopro.com) `https://nanostudiopro.com/api/mcp`
  [![Nano Studio Pro MCP connector](https://glama.ai/mcp/connectors/com.nanostudiopro/studiopro/badges/score.svg)](https://glama.ai/mcp/connectors/com.nanostudiopro/studiopro)
  🔐 - Find any photo or video you own by what is inside it; generate, restyle, cut out, and build sprite sheets.
- [Numonic](https://www.numonic.ai/docs/api/mcp) `https://www.numonic.ai/mcp`
  [![Numonic MCP connector](https://glama.ai/mcp/connectors/ai.numonic/numonic/badges/score.svg)](https://glama.ai/mcp/connectors/ai.numonic/numonic)
  🔐 - Search, organize, and publish AI-generated images and video with provenance and lineage.
- [OODS Foundry](https://oods-foundry.com) `https://oods-foundry.com/mcp`
  [![OODS Foundry MCP connector](https://glama.ai/mcp/connectors/com.oods-foundry/foundry/badges/score.svg)](https://glama.ai/mcp/connectors/com.oods-foundry/foundry)
  🔓 - Read a design system's component catalog and registry, and draw and certify charts from your own data.
- [Overflow Design](https://www.overflow.design/mcp/?utm_source=awesome-remote&utm_medium=mcp-directory) `https://www.overflow.design/api/mcp/`
  [![Overflow Design MCP connector](https://glama.ai/mcp/connectors/design.overflow/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/design.overflow/mcp)
  🔓 - Hand-drawn icons, illustrations and isometric drawings, searched by meaning and fetched as SVG, JSX or a file.
- [OwlCAD](https://owlcad.com/mcp-server) `https://mcp.owlcad.com`
  [![OwlCAD MCP connector](https://glama.ai/mcp/connectors/com.owlcad.mcp/owl-cad/badges/score.svg)](https://glama.ai/mcp/connectors/com.owlcad.mcp/owl-cad)
  🔐 - Build editable parametric 3D parts, check printability, and export STL, 3MF or STEP.
- [PartForge](https://www.partforge.ai) `https://www.partforge.ai/mcp`
  [![PartForge MCP connector](https://glama.ai/mcp/connectors/ai.partforge/partforge/badges/score.svg)](https://glama.ai/mcp/connectors/ai.partforge/partforge)
  🔐 - Create and edit parametric 3D-printable parts as code, render previews, and publish them to a public library.
- [ProfessionalHeadshot.io](https://professionalheadshot.io) `https://professionalheadshot.io/api/mcp`
  [![ProfessionalHeadshot.io MCP connector](https://glama.ai/mcp/connectors/io.professionalheadshot/professionalheadshot/badges/score.svg)](https://glama.ai/mcp/connectors/io.professionalheadshot/professionalheadshot)
  🔓 - Official LinkedIn, Slack and GitHub profile photo specs with sources, headshot style guides and a free headshot audit.
- [QRX](https://qrx.codes/developers/mcp) `https://qrx.codes/mcp`
  [![QRX MCP connector](https://glama.ai/mcp/connectors/codes.qrx/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/codes.qrx/mcp)
  🔐 - Create artistic, print-ready QR codes from a prompt and a link, each verified to scan; sign in with a free account.
- [Roomvana](https://roomvana.ai) `https://api.roomvana.co/mcp`
  [![Roomvana MCP connector](https://glama.ai/mcp/connectors/io.github.TJLDC/roomvana-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.TJLDC/roomvana-mcp)
  🔓 - Browse room types and design styles, then get a Roomvana studio link with those options prefilled.
- [Sceneplane](https://sceneplane.online) `https://mcp.sceneplane.online/v1`
  [![Sceneplane MCP connector](https://glama.ai/mcp/connectors/online.sceneplane/sceneplane/badges/score.svg)](https://glama.ai/mcp/connectors/online.sceneplane/sceneplane)
  🔐 - Build, inspect, render and animate Blender scenes in the cloud; export editable .blend, GLB or STL files.
- [ScoreLook](https://scorelook.fr/scorelook-mcp) `https://scorelook.fr/mcp`
  [![ScoreLook MCP connector](https://glama.ai/mcp/connectors/fr.scorelook/capucine/badges/score.svg)](https://glama.ai/mcp/connectors/fr.scorelook/capucine)
  🔓 - French AI stylist: sourced outfit answers, piece hubs, shopping criteria and weather looks.
- [Showoff](https://showoff.dev) `https://showoff.dev/mcp`
  [![Showoff MCP connector](https://glama.ai/mcp/connectors/dev.showoff/showoff/badges/score.svg)](https://glama.ai/mcp/connectors/dev.showoff/showoff)
  🔐 - Art-direct 3D device mockups, App Store screenshot sets and launch videos for your app.
- [UXKIN](https://uxkin.com) `https://uxkin.com/mcp`
  [![UXKIN MCP connector](https://glama.ai/mcp/connectors/io.github.uxkin/uxkin/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.uxkin/uxkin)
  🔐 - Real iOS app screens, user journeys and website design systems for AI coding agents.
- [Whimsical](https://whimsical.com/mcp) `https://mcp.whimsical.com/mcp`
  [![Whimsical MCP connector](https://glama.ai/mcp/connectors/com.whimsical/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.whimsical/mcp)
  🔐 - Turn prompts into editable flowcharts, mind maps, sequence diagrams and wireframes, and search your Whimsical workspace.
  
### 🌐 <a name="browser-automation"></a>Browser Automation

- [APEX](https://apexfaucet.xyz/connect/) `https://apexfaucet.xyz/api/mcp`
  [![APEX MCP connector](https://glama.ai/mcp/connectors/xyz.apexfaucet/apex-x1/badges/score.svg)](https://glama.ai/mcp/connectors/xyz.apexfaucet/apex-x1)
  🔓 - Render a URL, or up to 25 pages of a site, to clean text in headless Chrome; $1 per call via x402.

- [Bowmark](https://bowmark.ai) `https://api.bowmark.ai/mcp`
  [![Bowmark MCP connector](https://glama.ai/mcp/connectors/ai.bowmark/bowmark/badges/score.svg)](https://glama.ai/mcp/connectors/ai.bowmark/bowmark)
  🔓 - Typed functions an agent calls to search, price-check and book on live websites, no browser needed.

- [Browser Forest](https://browserforest.com) `https://browserforest.com/api/mcp/bf`
  [![Browser Forest MCP connector](https://glama.ai/mcp/connectors/com.browserforest/browser-forest/badges/score.svg)](https://glama.ai/mcp/connectors/com.browserforest/browser-forest)
  🔑 - Undetectable cloud browser sessions; navigate, extract, click, and solve captchas on blocked sites.

- [Cloudflare Browser Rendering](https://developers.cloudflare.com/browser-rendering/) `https://browser.mcp.cloudflare.com/mcp`
  🔐 - Render pages, capture screenshots, and scrape HTML from a URL.

- [Framejet](https://framejet.dev) `https://framejet.dev/mcp`
  [![Framejet MCP connector](https://glama.ai/mcp/connectors/dev.framejet/screenshot/badges/score.svg)](https://glama.ai/mcp/connectors/dev.framejet/screenshot)
  🔓 - Screenshot any URL to PNG or JPEG with cookie banners and chat widgets removed; needs a free API key.

- [ViewportWitness](https://qa.honeygate.app) `https://qa.honeygate.app/mcp`
  [![ViewportWitness MCP connector](https://glama.ai/mcp/connectors/io.github.Baffles78/viewport-witness/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Baffles78/viewport-witness)
  🔓 - Paid browser QA across three viewports: screenshots, accessibility checks and baseline diffs.

### ☁️ <a name="cloud-platforms"></a>Cloud Platforms

- [AgentsPodium Hosting](https://hosting.defispace.com/docs/mcp.html) `https://mcp.agentspodium.com/mcp`
  [![AgentsPodium Hosting MCP connector](https://glama.ai/mcp/connectors/com.agentspodium/hosting/badges/score.svg)](https://glama.ai/mcp/connectors/com.agentspodium/hosting)
  🔓 - Create, pay for and manage hosted AI agent pods (Hermes, OpenClaw, n8n); account tools need a key.
- [Ankra](https://docs.ankra.ai/platform/mcp-server) `https://platform.ankra.app/api/v1/mcp`
  [![Ankra MCP connector](https://glama.ai/mcp/connectors/ai.ankra/platform/badges/score.svg)](https://glama.ai/mcp/connectors/ai.ankra/platform)
  🔐 - Deploy and operate Kubernetes: build or import clusters, ship apps, read logs and metrics, and triage CVEs.
- [Cloud World Model](https://www.cloudworldmodel.ai/mcp-quickstart) `https://www.cloudworldmodel.ai/mcp`
  [![Cloud World Model MCP connector](https://glama.ai/mcp/connectors/ai.cloudworldmodel/cloud-world-model/badges/score.svg)](https://glama.ai/mcp/connectors/ai.cloudworldmodel/cloud-world-model)
  🔓 - Simulate cloud infrastructure and estimate cost, latency and resilience across AWS, GCP, Azure, OCI and DigitalOcean.
- [Cloudflare Bindings](https://developers.cloudflare.com/agents/model-context-protocol/) `https://bindings.mcp.cloudflare.com/mcp`
  🔐 - Build on Workers KV, R2, D1, and other Cloudflare bindings.
- [Costory](https://docs.costory.io/features/mcp) `https://app-api.costory.io/mcp`
  [![Costory MCP connector](https://glama.ai/mcp/connectors/io.costory.app-api/costory/badges/score.svg)](https://glama.ai/mcp/connectors/io.costory.app-api/costory)
  🔐 - FinOps agent backend: query, allocate and explain AWS, GCP, Azure, Kubernetes and AI spend.
- [DropTheHassle](https://dropthehassle.com) `https://dropthehassle.com/mcp`
  [![DropTheHassle MCP connector](https://glama.ai/mcp/connectors/io.github.bosmdavid-gif/dropthehassle/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.bosmdavid-gif/dropthehassle)
  🔓 - Publish static sites to a free HTTPS link or your own domain and check domain prices; account tools need a token.
- [FARPY](https://farpy.com) `https://api.farpy.com/mcp`
  [![FARPY MCP connector](https://glama.ai/mcp/connectors/com.farpy.api/farpy/badges/score.svg)](https://glama.ai/mcp/connectors/com.farpy.api/farpy)
  🔐 - Run verified Blender GPU workloads, track jobs, retrieve artifacts, and inspect execution receipts.
- [Fiskmas](https://fiskmas.dev) `https://mcp.fiskmas.dev/mcp`
  [![Fiskmas MCP connector](https://glama.ai/mcp/connectors/dev.fiskmas/fiskmas/badges/score.svg)](https://glama.ai/mcp/connectors/dev.fiskmas/fiskmas)
  🔓 - Create, deploy and monitor Docker apps on live HTTPS URLs.
- [Floot](https://floot.com) `https://mcp.floot.com/mcp`
  [![Floot MCP connector](https://glama.ai/mcp/connectors/com.floot/floot/badges/score.svg)](https://glama.ai/mcp/connectors/com.floot/floot)
  🔐 - Build React apps with serverless endpoints, Postgres and auth, run SQL, and publish to a live URL.
- [Hatch](https://viberooster.com) `https://mcp.theroost.dev/mcp`
  [![Hatch MCP connector](https://glama.ai/mcp/connectors/com.viberooster/hatch/badges/score.svg)](https://glama.ai/mcp/connectors/com.viberooster/hatch)
  🔓 - Publish a live website from an agent in one tool call, expiring or permanent, with human review hooks.
- [Heroku](https://heroku.com) `https://mcp.heroku.com/mcp`
  🔐 - Manage Heroku apps, dynos, add-ons, and logs.
- [Netlify](https://netlify.com) `https://netlify-mcp.netlify.app/mcp`
  🔐 - Create, deploy, and manage Netlify sites.
- [Pethost](https://pethost.dev) `https://mcp.pethost.dev/mcp`
  [![Pethost MCP connector](https://glama.ai/mcp/connectors/dev.pethost/pethost/badges/score.svg)](https://glama.ai/mcp/connectors/dev.pethost/pethost)
  🔐 - Deploy Docker Compose projects, read their logs and HTTP traffic, and run commands in their containers.
- [Popdot AI](https://popdot.ai) `https://popdot.ai/api/mcp`
  [![Popdot AI MCP connector](https://glama.ai/mcp/connectors/ai.popdot/popdot-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/ai.popdot/popdot-mcp)
  🔓 - Give an agent a public URL: free 24-hour trial subdomains, then rentals paid in USDC via x402.
- [Porkbun](https://porkbun.com/mcp) `https://mcp.porkbun.com/mcp`
  [![Porkbun MCP connector](https://glama.ai/mcp/connectors/com.porkbun/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.porkbun/mcp)
  🔐 - Manage domains, DNS, nameservers, DNSSEC, URL forwarding and static site deploys on your Porkbun account.
- [Render](https://render.com) `https://mcp.render.com/mcp`
  🔐 - Deploy and inspect Render services, databases, and logs.
- [Shipvela](https://shipvela.com) `https://shipvela.com/mcp`
  [![Shipvela MCP connector](https://glama.ai/mcp/connectors/com.shipvela/shipvela/badges/score.svg)](https://glama.ai/mcp/connectors/com.shipvela/shipvela)
  🔐 - Create website projects, deploy supported GitHub repositories, and inspect deployment status, logs, and usage.
- [Symbioza](https://symbioza.dev) `https://symbioza.dev/mcp`
  [![Symbioza MCP connector](https://glama.ai/mcp/connectors/dev.symbioza/symbioza/badges/score.svg)](https://glama.ai/mcp/connectors/dev.symbioza/symbioza)
  🔐 - Run a GPU job under a hard dollar cap and collect the files it writes.
- [TrustyCap](https://trustycap.com) `https://mcp.trustycap.com/mcp`
  [![TrustyCap MCP connector](https://glama.ai/mcp/connectors/com.trustycap/trustycap/badges/score.svg)](https://glama.ai/mcp/connectors/com.trustycap/trustycap)
  🔓 - Add production storage, data, jobs, webhooks, email and secrets to an app, and meter the usage.
- [Vercel](https://vercel.com) `https://mcp.vercel.com`
  [![Vercel MCP connector](https://glama.ai/mcp/connectors/com.vercel/vercel-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.vercel/vercel-mcp)
  🔐 - Manage Vercel projects, deployments, and logs.
- [wawesome](https://wawesome.io) `https://api.wawesome.io/v1/mcp`
  [![wawesome MCP connector](https://glama.ai/mcp/connectors/io.wawesome/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.wawesome/mcp)
  🔐 - Deploy JavaScript Functions and static sites as one version, read invocation logs, and roll back.
  
### 💬 <a name="communication"></a>Communication

- [Aitho](https://aitho.app) `https://present.aitho.app/mcp`
  [![Aitho MCP connector](https://glama.ai/mcp/connectors/app.aitho/aitho/badges/score.svg)](https://glama.ai/mcp/connectors/app.aitho/aitho)
  🔐 - Turn a slide deck into a rehearsable talk with a voice-following script and slides that advance as you speak.
- [AskOne](https://askone.org) `https://askone.org/api/mcp`
  [![AskOne MCP connector](https://glama.ai/mcp/connectors/io.github.phuryn/askone/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.phuryn/askone)
  🔐 - Run live audience Q&A and polls with free AI moderation: start rooms, launch polls, answer questions, draft a FAQ.
- [Atendio](https://atendio.co/conecta-tu-claude) `https://atendio.co/api/mcp`
  [![Atendio MCP connector](https://glama.ai/mcp/connectors/co.atendio/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/co.atendio/mcp)
  🔐 - Read WhatsApp conversations and analytics, and manage the rules of a business's AI WhatsApp assistant.
- [Call Me](https://callmemcp.com) `https://callmemcp.com/mcp`
  [![Call Me MCP connector](https://glama.ai/mcp/connectors/com.serdaroztetik/call-me/badges/score.svg)](https://glama.ai/mcp/connectors/com.serdaroztetik/call-me)
  🔓 - Your AI rings your iPhone, speaks its question, and gets your spoken answer back as text.
- [DialogBrain](https://dialogbrain.com) `https://api.dialogbrain.com/mcp/`
  [![DialogBrain MCP connector](https://glama.ai/mcp/connectors/com.dialogbrain.api/dialog-brain/badges/score.svg)](https://glama.ai/mcp/connectors/com.dialogbrain.api/dialog-brain)
  🔐 - Read and answer a business's WhatsApp, Telegram, Instagram and email messages from one inbox.
- [ErzyCall](https://app.erzycall.com/docs/mcp) `https://app.erzycall.com/api/mcp`
  [![ErzyCall MCP connector](https://glama.ai/mcp/connectors/com.erzycall.app/erzy-call/badges/score.svg)](https://glama.ai/mcp/connectors/com.erzycall.app/erzy-call)
  🔐 - Make and take real phone calls.
- [Faivelo](https://faivelo.com/ai-agents) `https://faivelo.com/api/mcp`
  [![Faivelo MCP connector](https://glama.ai/mcp/connectors/com.faivelo/mail/badges/score.svg)](https://glama.ai/mcp/connectors/com.faivelo/mail)
  🔐 - Read, search, send and organize mail in mailboxes on your own domain, and manage aliases and DNS.
- [Fluxmail Cloud](https://fluxmail.ai/cloud) `https://cloud.fluxmail.ai/mcp`
  [![Fluxmail Cloud MCP connector](https://glama.ai/mcp/connectors/ai.fluxmail.cloud/fluxmail-cloud/badges/score.svg)](https://glama.ai/mcp/connectors/ai.fluxmail.cloud/fluxmail-cloud)
  🔐 - Read, search, draft, send, and organize email across Gmail, Outlook, and IMAP mailboxes.
- [formcarry](https://formcarry.com) `https://mcp.formcarry.com/mcp`
  [![formcarry MCP connector](https://glama.ai/mcp/connectors/com.formcarry.mcp/formcarry/badges/score.svg)](https://glama.ai/mcp/connectors/com.formcarry.mcp/formcarry)
  🔐 - Set up form handling for your site (email alerts, auto replies, webhooks) and query submissions.
- [inboxmcp](https://inboxmcp.ai) `https://app.inboxmcp.ai/mcp`
  [![inboxmcp MCP connector](https://glama.ai/mcp/connectors/io.github.zhlei07/inboxmcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.zhlei07/inboxmcp)
  🔐 - Read connected inboxes, retain each AI's progress, and send separately authorized, owner-confirmed drafts.
- [Mailbox MCP](https://mailbox-mcp.com) `https://mcp.mailbox-mcp.com/db/mcp`
  [![Mailbox MCP MCP connector](https://glama.ai/mcp/connectors/com.mailbox-mcp.mcp/mailbox-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.mailbox-mcp.mcp/mailbox-mcp)
  🔐 - Read, search, file, draft and send email in your own Gmail, Outlook, Microsoft 365, iCloud or IMAP inbox.
- [Mailcheer](https://mailcheer.com) `https://mailcheer.com/api/mcp`
  [![Mailcheer MCP connector](https://glama.ai/mcp/connectors/com.mailcheer/mailcheer/badges/score.svg)](https://glama.ai/mcp/connectors/com.mailcheer/mailcheer)
  🔓 - Send transactional email, manage subscribers and schedule campaigns; tool calls use a Mailcheer API key.
- [meld](https://meld.mergeinc.workers.dev) `https://meld.mergeinc.workers.dev/mcp`
  [![meld MCP connector](https://glama.ai/mcp/connectors/io.github.lemonaide152/meld/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.lemonaide152/meld)
  🔓 - Capability URL + TTL context bridge; host-readable while live; anyone with the link; not for secrets.
- [Piloxa](https://piloxa.com) `https://piloxa.com/mcp`
  [![Piloxa MCP connector](https://glama.ai/mcp/connectors/com.piloxa/piloxa-certified-mail/badges/score.svg)](https://glama.ai/mcp/connectors/com.piloxa/piloxa-certified-mail)
  🔓 - Send a letter as printed USPS Certified Mail with tracking, from $13.18.
- [PlaceCall](https://voygr.tech/placecall/) `https://api.voygr.tech/mcp`
  [![PlaceCall MCP connector](https://glama.ai/mcp/connectors/io.github.voygr-tech/placecall/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.voygr-tech/placecall)
  🔐 - Place real phone calls to US businesses to book, ask questions or get quotes, then read the outcome and transcript.
- [Poofbox](https://poofboxmail.com) `https://poofboxmail.com/mcp`
  [![Poofbox MCP connector](https://glama.ai/mcp/connectors/com.poofboxmail/poofbox/badges/score.svg)](https://glama.ai/mcp/connectors/com.poofboxmail/poofbox)
  🔐 - Disposable receive-only inboxes for agents: create an address, wait for the email, get the code or verify link.
- [PostalForm](https://postalform.com/developers) `https://postalform.com/mcp`
  [![PostalForm MCP connector](https://glama.ai/mcp/connectors/com.postalform/postalform/badges/score.svg)](https://glama.ai/mcp/connectors/com.postalform/postalform)
  🔓 - Print and mail letters, PDFs and forms by USPS, including Certified Mail, paid by checkout link or MPP/x402.
- [Resend](https://resend.com) `https://mcp.resend.com/mcp`
  🔐 - Send transactional email and manage sending domains.
- [Sending](https://sending.dev) `https://sending.dev/api/mcp`
  [![Sending MCP connector](https://glama.ai/mcp/connectors/dev.sending/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/dev.sending/mcp)
  🔐 - Email, WhatsApp and Telegram for agents: send, campaigns, automations, contacts, agent inboxes.
- [SofortFax](https://sofortfax.de/ki-fax.html) `https://sofortfax.de/api/mcp.php`
  [![SofortFax MCP connector](https://glama.ai/mcp/connectors/de.sofortfax/fax/badges/score.svg)](https://glama.ai/mcp/connectors/de.sofortfax/fax)
  🔓 - Send real faxes (PDF/JPG/photo) from AI chat to Germany, Austria and 40+ countries; pay per fax or prepaid credits.
- [Subo](https://subo.gg/blog/connect-discord-community-to-ai-agent/) `https://api.subo.ai/mcp`
  [![Subo MCP connector](https://glama.ai/mcp/connectors/gg.subo/survey-bot/badges/score.svg)](https://glama.ai/mcp/connectors/gg.subo/survey-bot)
  🔐 - Build, launch and analyze surveys, polls, forms and quizzes in a Discord community, and reward members with XP.
- [SwarmMemo](https://swarmmemo.com) `https://swarmmemo.com/mcp`
  [![SwarmMemo MCP connector](https://glama.ai/mcp/connectors/com.swarmmemo/bulletin/badges/score.svg)](https://glama.ai/mcp/connectors/com.swarmmemo/bulletin)
  🔓 - Free public bulletin board where agents post, reply and find peers.
- [The Colony](https://thecolony.cc/for-agents) `https://thecolony.cc/mcp/`
  [![The Colony MCP connector](https://glama.ai/mcp/connectors/cc.thecolony/the-colony/badges/score.svg)](https://glama.ai/mcp/connectors/cc.thecolony/the-colony)
  🔓 - Forum and social network for AI agents: read posts anonymously; post, comment, vote and message with a token.
- [ThunderPhone](https://thunderphone.com) `https://api.thunderphone.com/v1/mcp`
  [![ThunderPhone MCP connector](https://glama.ai/mcp/connectors/io.github.thunderphone/thunderphone/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.thunderphone/thunderphone)
  🔐 - Build, test and run AI phone agents: numbers, inbound and outbound calls, campaigns and transcripts.
- [volai](https://volai.cz/en) `https://volai.cz/mcp`
  [![volai MCP connector](https://glama.ai/mcp/connectors/cz.volai/volai/badges/score.svg)](https://glama.ai/mcp/connectors/cz.volai/volai)
  🔐 - Buy Czech and Slovak numbers, place calls, send SMS and run a voice agent; auth is an API key.
- [Widely](https://widely-mobile.com/mcp) `https://mcp.widely-mobile.com/mcp`
  [![Widely MCP connector](https://glama.ai/mcp/connectors/com.widely-mobile/widely/badges/score.svg)](https://glama.ai/mcp/connectors/com.widely-mobile/widely)
  🔓 - Telecom operating layer for AI agents: numbers, calls, SMS, voicemail, transcripts, and AI receptionists.
- [wacli.me](https://wacli.me) `https://wacli.me/mcp`
  [![wacli.me MCP connector](https://glama.ai/mcp/connectors/me.wacli/whatsapp/badges/score.svg)](https://glama.ai/mcp/connectors/me.wacli/whatsapp)
  🔐 - Link your WhatsApp account to read, search and send messages.

### 📝 <a name="content-management"></a>Content Management

- [8B AI Website Builder](https://8b.com/mcp/) `https://mcp.8b.com/mcp`
  [![8B AI Website Builder MCP connector](https://glama.ai/mcp/connectors/com.8b/ai-website-builder/badges/score.svg)](https://glama.ai/mcp/connectors/com.8b/ai-website-builder)
  🔓 - Your AI picks an 8B generated design and writes the copy; get an animated one-page site, preview link and HTML file.
- [btlabs Core](https://btlabs.dev) `https://btlabs.dev/api/mcp`
  [![btlabs Core MCP connector](https://glama.ai/mcp/connectors/dev.btlabs/core/badges/score.svg)](https://glama.ai/mcp/connectors/dev.btlabs/core)
  🔐 - Manage a btlabs Core site: pages, posts, media, menus, redirects and AI-discovery settings.
- [Contentful](https://contentful.com) `https://mcp.contentful.com/mcp`
  🔑 - Manage Contentful entries, assets, and content models.
- [dochost](https://dochost.io/mcp) `https://dochost.io/api/mcp`
  [![dochost MCP connector](https://glama.ai/mcp/connectors/io.dochost/dochost/badges/score.svg)](https://glama.ai/mcp/connectors/io.dochost/dochost)
  🔓 - Publish Markdown or HTML as a hosted page and get a shareable link.
- [Foliade](https://foliade.gekkode.com/en/) `https://foliade.gekkode.com/mcp`
  [![Foliade MCP connector](https://glama.ai/mcp/connectors/com.gekkode/foliade/badges/score.svg)](https://glama.ai/mcp/connectors/com.gekkode/foliade)
  🔓 - Turn a PDF into a mobile flipbook catalogue, customise its reader and publish it.
- [Foliyo](https://foliyo.io) `https://foliyo.io/mcp`
  [![Foliyo MCP connector](https://glama.ai/mcp/connectors/io.foliyo/foliyo/badges/score.svg)](https://glama.ai/mcp/connectors/io.foliyo/foliyo)
  🔐 - Create, brand, publish and track client-ready reports, proposals and research pages.
- [GoodBarber](https://www.goodbarber.com/mcp/) `https://mcp.goodbarber.dev/mcp/sse`
  [![GoodBarber MCP connector](https://glama.ai/mcp/connectors/dev.goodbarber/goodbarber-public-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/dev.goodbarber/goodbarber-public-mcp)
  🔐 - Manage a GoodBarber no-code app: content, push notifications, shop orders, members, and analytics.
- [Lediv](https://lediv.com) `https://lediv.app/mcp`
  [![Lediv MCP connector](https://glama.ai/mcp/connectors/app.lediv/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/app.lediv/mcp)
  🔐 - Visual website builder synced with real code: edit files, publish, roll back, manage domains and previews.
- [LetX](https://letx.app/mcp/) `https://api.letx.app/mcp`
  [![LetX MCP connector](https://glama.ai/mcp/connectors/app.letx/letx/badges/score.svg)](https://glama.ai/mcp/connectors/app.letx/letx)
  🔐 - Write LaTeX from 1,000+ journal, thesis and CV templates and compile to PDF with the build log.
- [Sanity](https://sanity.io) `https://mcp.sanity.io/mcp`
  [![Sanity MCP connector](https://glama.ai/mcp/connectors/io.sanity.www/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.sanity.www/mcp)
  🔐 - Query and mutate Sanity datasets and documents.
- [Share Artifacts](https://shareartifacts.dev) `https://shareartifacts.dev/api/mcp`
  [![Share Artifacts MCP connector](https://glama.ai/mcp/connectors/io.github.arunai30/share-artifacts/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.arunai30/share-artifacts)
  🔐 - Publish and update static HTML reports, presentations, and explainers with controlled sharing.
- [sitectrl](https://sitectrl.ai/mcp) `https://mcp.sitectrl.ai/mcp`
  [![sitectrl MCP connector](https://glama.ai/mcp/connectors/ai.sitectrl/sitectrl/badges/score.svg)](https://glama.ai/mcp/connectors/ai.sitectrl/sitectrl)
  🔓 - Describe a site and get it live with SSL, forms and analytics; OAuth to edit and manage it.
- [SnapHost](https://snaphost.ai) `https://app.snaphost.ai/api/mcp`
  [![SnapHost MCP connector](https://glama.ai/mcp/connectors/ai.snaphost/snaphost/badges/score.svg)](https://glama.ai/mcp/connectors/ai.snaphost/snaphost)
  🔐 - Publish a page or site to a private link, control who can view it, and update it in place.
- [spacesheep](https://spacesheep.dev) `https://mcp.spacesheep.dev/mcp`
  [![spacesheep MCP connector](https://glama.ai/mcp/connectors/dev.spacesheep/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/dev.spacesheep/mcp)
  🔐 - Publish pages your agent writes to a private, shareable URL, then read, comment on and update them.
- [Storskarvia](https://storskarvia.com) `https://storskarvia.com/mcp/`
  [![Storskarvia MCP connector](https://glama.ai/mcp/connectors/com.storskarvia/writing-studio/badges/score.svg)](https://glama.ai/mcp/connectors/com.storskarvia/writing-studio)
  🔓 - Writing studio for novels and screenplays: cited fact-checks and continuity checks on your drafts; never writes prose.
- [Storyblok](https://storyblok.com) `https://mcp.storyblok.com/mcp`
  🔓 - Manage Storyblok spaces, stories, and components.
- [Webflow](https://webflow.com) `https://mcp.webflow.com/mcp`
  [![Webflow MCP connector](https://glama.ai/mcp/connectors/com.webflow/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.webflow/mcp)
  🔐 - Manage Webflow sites, collections, and CMS items.
- [WebZum](https://webzum.com) `https://webzum.com/api/mcp`
  [![WebZum MCP connector](https://glama.ai/mcp/connectors/io.github.suprraz/webzum/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.suprraz/webzum)
  🔓 - Builds complete small-business websites with local SEO, a logo and hosting in 5 minutes; also hosts HTML.
- [Wix](https://wix.com) `https://mcp.wix.com/mcp`
  [![Wix MCP connector](https://glama.ai/mcp/connectors/com.wix/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.wix/mcp)
  🔐 - Manage Wix sites, business data, and bookings.

### 👤 <a name="crm"></a>CRM
- [Atimeüs](https://www.atimeus.com/fonctionnalites-erp/ia-et-serveur-mcp) `https://atimeus.app/mcp`
  [![Atimeüs MCP connector](https://glama.ai/mcp/connectors/com.atimeus/atimeus/badges/score.svg)](https://glama.ai/mcp/connectors/com.atimeus/atimeus)
  🔐 - ERP for IT services firms: search records, run indicators, manage timesheets and update data.
- [Data Parrot](https://dataparrot.ai) `https://api-v3.dataparrot.ai/api/v3/data-parrot/mcp`
  [![Data Parrot MCP connector](https://glama.ai/mcp/connectors/ai.dataparrot/data-parrot/badges/score.svg)](https://glama.ai/mcp/connectors/ai.dataparrot/data-parrot)
  🔐 - AI revenue analysis of your HubSpot data.
- [Close](https://close.com) `https://mcp.close.com/mcp`
  [![Close MCP connector](https://glama.ai/mcp/connectors/com.close/close-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.close/close-mcp)
  🔐 - Read and update Close leads, contacts, and opportunities.
- [Connections](https://studio.connections.icu/connect) `https://studio.connections.icu/v1/mcp`
  [![Connections MCP connector](https://glama.ai/mcp/connectors/icu.connections/connections/badges/score.svg)](https://glama.ai/mcp/connectors/icu.connections/connections)
  🔐 - Manage contacts, host and ticket events, post marketplace deals, and keep notes and memory.
- [DOS AI](https://dosai.pro/en) `https://dosai.pro/api/mcp`
  [![DOS AI MCP connector](https://glama.ai/mcp/connectors/pro.dosai/dos-ai/badges/score.svg)](https://glama.ai/mcp/connectors/pro.dosai/dos-ai)
  🔓 - Run WhatsApp and Telegram AI assistants: projects, prompts, leads, chats and analytics; API key for calls.
- [HubSpot](https://hubspot.com) `https://mcp.hubspot.com/anthropic`
  🔐 - Query and update HubSpot CRM contacts, companies, and deals.
- [Oria CRM](https://realoria.com/crm/mcp) `https://realoria.com/api/mcp`
  [![Oria CRM MCP connector](https://glama.ai/mcp/connectors/com.realoria/crm/badges/score.svg)](https://glama.ai/mcp/connectors/com.realoria/crm)
  🔐 - Read pipeline, contacts, properties, viewings and auctions for a Romanian real-estate agency's CRM.
- [SignalRaven](https://signalraven.ai) `https://api.signalraven.ai/mcp`
  [![SignalRaven MCP connector](https://glama.ai/mcp/connectors/io.github.signalraven/signalraven/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.signalraven/signalraven)
  🔐 - LinkedIn buying-intent signals, prospect and account research, and openers from your workspace.

### 🗄️ <a name="databases"></a>Databases

- [CloudCrane](https://cloudcrane.ai) `https://cloudcrane.ai/api/build/mcp`
  [![CloudCrane MCP connector](https://glama.ai/mcp/connectors/ai.cloudcrane/workspace/badges/score.svg)](https://glama.ai/mcp/connectors/ai.cloudcrane/workspace)
  🔐 - Read and build curated catalog data with a receipt on every value; review decisions stay with a person.
- [Convex](https://convex.dev) `https://mcp.convex.dev/mcp`
  🔓 - Query and manage Convex deployments, tables, and functions.
- [LakehouseBox](https://lakehousebox.com/docs/mcp/) `https://mcp.lakehousebox.com/mcp`
  [![LakehouseBox MCP connector](https://glama.ai/mcp/connectors/com.lakehousebox/lakehousebox/badges/score.svg)](https://glama.ai/mcp/connectors/com.lakehousebox/lakehousebox)
  🔐 - Query and write Apache Iceberg tables hosted in Europe, and open public datasets, with DuckDB SQL.
- [MongoDB](https://mongodb.com) `https://mcp.mongodb.com/mcp`
  🔐 - Query MongoDB Atlas clusters and manage collections and indexes.
- [Neon](https://neon.tech) `https://mcp.neon.tech/mcp`
  🔐 - Provision and query Neon Postgres projects and branches.
- [Prisma](https://prisma.io) `https://mcp.prisma.io/mcp`
  [![Prisma MCP connector](https://glama.ai/mcp/connectors/io.prisma/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.prisma/mcp)
  🔐 - Manage Prisma Postgres databases and run migrations.
- [Supabase](https://supabase.com) `https://mcp.supabase.com/mcp`
  [![Supabase MCP connector](https://glama.ai/mcp/connectors/com.supabase/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.supabase/mcp)
  🔐 - Manage Supabase projects, run SQL, and inspect schemas.

### 📊 <a name="data-visualization"></a>Data Visualization

- [chartlink](https://chartlink.app) `https://chartlink.app/mcp`
  [![chartlink MCP connector](https://glama.ai/mcp/connectors/io.github.oscarleoo/chartlink/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.oscarleoo/chartlink)
  🔓 - Charts and tables with live-updating embed links, drafted from one message; tools need a key.
- [rows.page](https://rows.page) `https://rows.page/mcp`
  [![rows.page MCP connector](https://glama.ai/mcp/connectors/page.rows/rows/badges/score.svg)](https://glama.ai/mcp/connectors/page.rows/rows)
  🔓 - Push CSV, JSON or Parquet from an agent and get a link a human can explore with filters, SQL and charts.

### 🛠️ <a name="developer-tools"></a>Developer Tools
- [402cron](https://402cron.com) `https://402cron.com/mcp`
  [![402cron MCP connector](https://glama.ai/mcp/connectors/com.402cron/402cron/badges/score.svg)](https://glama.ai/mcp/connectors/com.402cron/402cron)
  🔓 - Paid cron for AI agents; paying with x402 USDC on Base issues a management token.
- [A2APark](https://a2apark.com/) `https://a2apark.com/mcp`
  [![A2APark MCP connector](https://glama.ai/mcp/connectors/com.a2apark/a2apark/badges/score.svg)](https://glama.ai/mcp/connectors/com.a2apark/a2apark)
  🔓 - Run stateful behavioral rides for AI agents and retrieve signed scorecards.
- [ADITUS Developer Portal MCP](https://developers.aditus.com/mcp) `https://developers.aditus.com/api/mcp`
  [![ADITUS Developer Portal MCP connector](https://glama.ai/mcp/connectors/com.aditus.developers/developer-portal/badges/score.svg)](https://glama.ai/mcp/connectors/com.aditus.developers/developer-portal)
  🔓 - Search and read the ADITUS event-technology API docs (ticketing, access, BI) and Shop Micro Frontend guides.
- [Aeon](https://www.aeon.fun/connect) `https://www.aeon.fun/connect/mcp`
  [![Aeon MCP connector](https://glama.ai/mcp/connectors/fun.aeon/aeon/badges/score.svg)](https://glama.ai/mcp/connectors/fun.aeon/aeon)
  🔐 - Run and manage your Aeon autonomous agent on GitHub Actions: skills, runs, memory, strategy and settings.
- [agent-manager Docs](https://agent-manager.dev) `https://agent-manager.dev/mcp`
  [![agent-manager Docs MCP connector](https://glama.ai/mcp/connectors/io.github.YoanWai/agent-manager-docs/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.YoanWai/agent-manager-docs)
  🔓 - Search and read the agent-manager docs, list its supported coding CLIs, and get the latest release.
- [Agentic Atlas](https://agentic-atlas.dev/) `https://agentic-atlas.dev/mcp/`
  [![Agentic Atlas MCP connector](https://glama.ai/mcp/connectors/dev.agentic-atlas/atlas/badges/score.svg)](https://glama.ai/mcp/connectors/dev.agentic-atlas/atlas)
  🔓 - Field guide to building better agents: design patterns, tradeoffs and decision guidance.
- [AgentoolRank](https://agentoolrank.com/agents) `https://agentoolrank.com/api/mcp`
  [![AgentoolRank MCP connector](https://glama.ai/mcp/connectors/com.agentoolrank/agent-tools/badges/score.svg)](https://glama.ai/mcp/connectors/com.agentoolrank/agent-tools)
  🔓 - Search and compare open-source AI agent tools ranked by live GitHub activity, and list new ones.
- [AI Commander](https://aicommander.dev) `https://aicommander.dev/mcp`
  [![AI Commander MCP connector](https://glama.ai/mcp/connectors/dev.aicommander/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/dev.aicommander/mcp)
  🔐 - Remote shell and detached jobs on your machines — harness for Claude Code, Codex, ChatGPT, Cursor.
- [AI Design Blueprint](https://aidesignblueprint.com) `https://aidesignblueprint.com/mcp`
  [![AI Design Blueprint MCP connector](https://glama.ai/mcp/connectors/com.aidesignblueprint/blueprint/badges/score.svg)](https://glama.ai/mcp/connectors/com.aidesignblueprint/blueprint)
  🔓 - Search 10 design principles, examples and guides; spec and UI validators on paid plans.
- [Astro Docs](https://astro.build) `https://mcp.docs.astro.build/mcp`
  🔓 - Search the Astro documentation.
- [Ausca](https://ausca.com) `https://ausca.com/mcp`
  [![Ausca MCP connector](https://glama.ai/mcp/connectors/com.ausca/agent-services/badges/score.svg)](https://glama.ai/mcp/connectors/com.ausca/agent-services)
  🔓 - Pay per call for remote browsers, receive-only inboxes, OCR, document analysis, and media transcription.
- [Bitrise](https://bitrise.io) `https://mcp.bitrise.io/mcp`
  [![Bitrise MCP connector](https://glama.ai/mcp/connectors/io.github.bitrise-io/bitrise-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.bitrise-io/bitrise-mcp)
  🔐 - Trigger and inspect Bitrise CI builds and artifacts.
- [BlockVectra](https://blockvectra.com) `https://docs.blockvectra.com/mcp`
  [![BlockVectra MCP connector](https://glama.ai/mcp/connectors/com.blockvectra/docs/badges/score.svg)](https://glama.ai/mcp/connectors/com.blockvectra/docs)
  🔓 - Docs, chains, pricing and public EVM RPC reads without a key; indexed data and account tools require an API key.
- [BotKelp](https://www.botkelp.com) `https://agent-scaffold-mcp.vercel.app/mcp`
  [![BotKelp MCP connector](https://glama.ai/mcp/connectors/app.vercel.agent-scaffold-mcp/bot-kelp/badges/score.svg)](https://glama.ai/mcp/connectors/app.vercel.agent-scaffold-mcp/bot-kelp)
  🔓 - Generate stamped Next.js scaffolds from a verified component catalog with INTEGRITY.json checks.
- [CacheBoost](https://www.cache-boost.com/support/mcp/overview) `https://api.cache-boost.com/mcp`
  [![CacheBoost MCP connector](https://glama.ai/mcp/connectors/com.cache-boost/cacheboost/badges/score.svg)](https://glama.ai/mcp/connectors/com.cache-boost/cacheboost)
  🔑 - Warm CDN and reverse-proxy caches from 12 regions after a deploy or purge, then read the run's hit/miss stats.
- [Capacitor MCP Server by Capawesome](https://capawesome.io/docs/ai/mcp/capacitor/) `https://capacitor-mcp.capawesome.io/mcp`
  [![Capacitor MCP connector](https://glama.ai/mcp/connectors/io.capawesome/capacitor-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.capawesome/capacitor-mcp)
  🔓 - Unofficial: search the Capacitor docs for v6 and later, read pages, and list official and community plugins.
- [Capawesome MCP Server](https://capawesome.io/docs/ai/mcp/capawesome/) `https://mcp.capawesome.io/mcp`
  [![Capawesome MCP connector](https://glama.ai/mcp/connectors/io.capawesome/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.capawesome/mcp)
  🔓 - Search the Capawesome docs and blog; an API token adds the Capawesome Cloud management tools.
- [Ceraph React Native MCP](https://ceraph.dev) `https://mcp.ceraph.dev/mcp`
  [![Ceraph React Native MCP connector](https://glama.ai/mcp/connectors/dev.ceraph.mcp/ceraph-react-native-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/dev.ceraph.mcp/ceraph-react-native-mcp)
  🔐 - Let your coding agent test React Native and Expo apps end-to-end on iOS and Android devices, simulators and emulators.
- [Cherry Notes](https://cherrynotes.app) `https://api.cherrynotes.app/mcp`
  [![Cherry Notes MCP connector](https://glama.ai/mcp/connectors/app.cherrynotes/cherry-notes/badges/score.svg)](https://glama.ai/mcp/connectors/app.cherrynotes/cherry-notes)
  🔐 - Capture features, ideas and tasks on your phone; your AI coding agent picks them up and ships them.
- [Cloudflare Docs](https://developers.cloudflare.com) `https://docs.mcp.cloudflare.com/mcp`
- [CodeRifts](https://coderifts.com) `https://app.coderifts.com/mcp`
  [![CodeRifts MCP connector](https://glama.ai/mcp/connectors/io.github.coderifts/api-governance/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.coderifts/api-governance)
  🔓 - Only a granted change can proceed: preflight a contract change, verify a receipt, or read a past decision.
  🔓 - Search the Cloudflare developer documentation.
- [Coderbuds](https://coderbuds.com/docs/mcp?ref=awesome-remote-mcp) `https://coderbuds.com/mcp/insights`
  [![Coderbuds MCP connector](https://glama.ai/mcp/connectors/com.coderbuds/insights/badges/score.svg)](https://glama.ai/mcp/connectors/com.coderbuds/insights)
  🔐 - Read your team's delivery metrics and standards, and check a change against them before a PR.
- [CometChat Docs](https://www.cometchat.com/docs/mcp-server) `https://mcp.cometchat.com/mcp`
  [![CometChat Docs MCP connector](https://glama.ai/mcp/connectors/io.github.cometchat/docs-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.cometchat/docs-mcp)
  🔓 - Search CometChat chat, calling and moderation docs and get ready-made integration recipes.
- [CompatLab](https://compatlab.me/) `https://compatlab.me/mcp`
  [![CompatLab MCP connector](https://glama.ai/mcp/connectors/io.github.siddiksawani/compatlab/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.siddiksawani/compatlab)
  🔓 - Read recorded npm loading results across pinned Node.js, Bun and Deno versions, with coverage and report links.
- [ContextStream](https://contextstream.io) `https://mcp.contextstream.io/mcp`
  [![ContextStream MCP connector](https://glama.ai/mcp/connectors/io.contextstream/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.contextstream/mcp)
  🔐 - Shared project context for Cursor, Claude Code, Codex, and Grok. Intelligence isn’t the bottleneck. Context is.
- [Datakoot Package Intel](https://datakoot.com/package-intel) `https://package.datakoot.com/mcp`
  [![Datakoot Package Intel MCP connector](https://glama.ai/mcp/connectors/com.datakoot/npm-pypi-crates-packages/badges/score.svg)](https://glama.ai/mcp/connectors/com.datakoot/npm-pypi-crates-packages)
  🔓 - npm, PyPI and crates.io package health, versions, downloads, dependencies and advisories.
- [DeepWiki](https://deepwiki.com) `https://mcp.deepwiki.com/mcp`
  🔓 - Ask questions about any public GitHub repository's generated wiki.
- [dep-diff](https://github.com/DigiCatalyst-Systems/dep-diff-mcp#readme) `https://dep-diff.digicatalyst.ca/mcp`
  [![dep-diff MCP connector](https://glama.ai/mcp/connectors/io.github.DigiCatalyst-Systems/dep-diff-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.DigiCatalyst-Systems/dep-diff-mcp)
  🔓 - Rank npm, PyPI and GitHub Actions upgrades by risk: breaking changes, fixed CVEs and migration links.
- [Docsy](https://docsy.remcp.site) `https://docsy.remcp.site/mcp/registry`
  [![Docsy MCP connector](https://glama.ai/mcp/connectors/io.github.getremcp/docsy/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.getremcp/docsy)
  🔓 - Search versioned developer documentation and fetch source-linked results using five read-only tools.
- [Electrik Slate](https://slate.electrik.dev) `https://mcp.slate.electrik.dev`
  [![Electrik Slate MCP connector](https://glama.ai/mcp/connectors/io.github.neerajsohal/slate/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.neerajsohal/slate)
  🔓 - Read Electrik Slate Blade component docs, blocks gallery, source, and llms.txt.
- [ElectroGen](https://electrogen.org) `https://electrogen.org/.well-known/mcp`
  [![ElectroGen MCP connector](https://glama.ai/mcp/connectors/org.electrogen/electrogen/badges/score.svg)](https://glama.ai/mcp/connectors/org.electrogen/electrogen)
  🔓 - Generate a buildable electronics blueprint — BOM, wiring, firmware, CAD and preview renders — from a text brief.
- [Email Spam Tester](https://email-spam-tester.com) `https://email-spam-tester.com/mcp`
  [![Email Spam Tester MCP connector](https://glama.ai/mcp/connectors/io.github.serg-tanichev/email-spam-tester/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.serg-tanichev/email-spam-tester)
  🔓 - Send a draft to a one-time address and get a spam score, 41 checks with RFC citations, and a fix plan.
- [GitDiagram](https://gitdiagram.com) `https://gitdiagram.com/mcp`
  [![GitDiagram MCP connector](https://glama.ai/mcp/connectors/com.gitdiagram/gitdiagram/badges/score.svg)](https://glama.ai/mcp/connectors/com.gitdiagram/gitdiagram)
  🔓 - Architecture diagrams, explanations and Mermaid source for any public GitHub repository.
- [GO AI Tools](https://goaichat.app/mcp-tools) `https://goaichat.app/mcp-tools/mcp`
  [![GO AI Tools MCP connector](https://glama.ai/mcp/connectors/app.goaichat/tools/badges/score.svg)](https://glama.ai/mcp/connectors/app.goaichat/tools)
  🔓 - 31 deterministic tools: image conversion, EXIF stripping, App Store assets, colour maths.
- [Globalping](https://globalping.io) `https://mcp.globalping.dev/mcp`
  🔐 - Run ping, traceroute, DNS, and HTTP checks from a global probe network.
- [HALLUX](https://blvkware.dev/hallux/) `https://api.blvkware.dev/hallux/mcp`
  [![HALLUX MCP connector](https://glama.ai/mcp/connectors/dev.blvkware/hallux/badges/score.svg)](https://glama.ai/mcp/connectors/dev.blvkware/hallux)
  🔓 - Check that a package, module or DOI exists in its registry before an agent installs, imports or cites it.
- [Heard](https://heard.dev) `https://api.heard.dev/v1/mcp/agent`
  [![Heard MCP connector](https://glama.ai/mcp/connectors/dev.heard/heard/badges/score.svg)](https://glama.ai/mcp/connectors/dev.heard/heard)
  🔐 - Cloud agents report progress that Heard speaks on your Mac, and pick up the replies you send back.
- [Hexum](https://hexum.dev) `https://hexum.dev/mcp`
  [![Hexum MCP connector](https://glama.ai/mcp/connectors/dev.hexum/hexum/badges/score.svg)](https://glama.ai/mcp/connectors/dev.hexum/hexum)
  🔑 - Shrink agent prompts, block forbidden imports without calling a model, and review PRs; zero data retention.
- [HTML/CSS to Image](https://htmlcsstoimage.com) `https://mcp.hcti.io`
  [![HTML/CSS to Image MCP connector](https://glama.ai/mcp/connectors/io.github.htmlcsstoimage/html-css-to-image/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.htmlcsstoimage/html-css-to-image)
  🔐 - Capture website screenshots, render HTML/CSS, and make templated graphics as images or PDFs.
- [Iminify](https://www.iminify.com/ai-agents) `https://www.iminify.com/mcp`
  [![Iminify MCP connector](https://glama.ai/mcp/connectors/com.iminify/iminify/badges/score.svg)](https://glama.ai/mcp/connectors/com.iminify/iminify)
  🔐 - Compress, convert and resize images, and scan web pages for every image they load.
- [InferIndex](https://inferindex.dev) `https://mcp.inferindex.dev/mcp`
  [![InferIndex MCP connector](https://glama.ai/mcp/connectors/io.github.InferIndex/inferindex/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.InferIndex/inferindex)
  🔓 - Compare LLM API prices across 150+ providers: cheapest offer, price history and cost estimates.
- [Ionic Framework MCP Server by Capawesome](https://capawesome.io/docs/ai/mcp/ionic-framework/) `https://ionic-framework-mcp.capawesome.io/mcp`
  [![Ionic Framework MCP connector](https://glama.ai/mcp/connectors/io.capawesome/ionic-framework-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.capawesome/ionic-framework-mcp)
  🔓 - Unofficial: search the Ionic Framework docs for v8 and v9, with the component API and usage examples.
- [ipvolt Proxy Toolkit](https://ipvolt.com/mcp) `https://mcp.ipvolt.com/mcp`
  [![ipvolt Proxy Toolkit MCP connector](https://glama.ai/mcp/connectors/com.ipvolt.mcp/ipvolt-proxy-toolkit/badges/score.svg)](https://glama.ai/mcp/connectors/com.ipvolt.mcp/ipvolt-proxy-toolkit)
  🔓 - Search proxy setup guides, generate proxy configs and diagnose proxy errors.
- [JSON to TOON](https://json2toon.co/mcp) `https://json2toon.co/api/mcp`
  [![JSON to TOON MCP connector](https://glama.ai/mcp/connectors/io.github.karta9821/json2toon/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.karta9821/json2toon)
  🔓 - Convert JSON to TOON, a compact format that uses fewer LLM tokens, and decode TOON back to JSON.
- [Keelen](https://keelen.ai/mcp-server/) `https://keelen.ai/mcp`
  [![Keelen MCP connector](https://glama.ai/mcp/connectors/io.github.jamie7893/keelen/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.jamie7893/keelen)
  🔓 - Steer GitHub coding from chat: requests, roadmaps and PR review. Tokenless signup; bearer key for workspace tools.
- [Launch Ready](https://uselaunchready.com) `https://uselaunchready.com/api/mcp`
  [![Launch Ready MCP connector](https://glama.ai/mcp/connectors/io.github.ochodigits/launch-ready/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ochodigits/launch-ready)
  🔐 - Deterministic pre-launch website QA: scan a URL, get a readiness score and launch blockers with evidence.
- [Loadster](https://loadster.com/manual/ai-agents/) `https://api.loadster.com/mcp`
  [![Loadster MCP connector](https://glama.ai/mcp/connectors/com.loadster/loadster-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.loadster/loadster-mcp)
  🔐 - Run load tests and synthetic monitors, including Playwright scripts, and analyze results.
- [MemorySync Documentation](https://docs.memorysync.io/mcp/overview) `https://docs.memorysync.io/mcp`
  [![MemorySync Docs MCP connector](https://glama.ai/mcp/connectors/io.memorysync/docs/badges/score.svg)](https://glama.ai/mcp/connectors/io.memorysync/docs)
  🔓 - Search and read MemorySync's API, SDK and integration docs.
- [Metabind Banking Assistant (demo)](https://www.metabind.ai) `https://mcp.metabind.ai/IgJH0BzIn4LlfnCbcDc7/projects/GLbHk5i3GLlIYcF63XFl`
  [![Metabind Banking Assistant MCP connector](https://glama.ai/mcp/connectors/ai.metabind/banking-assistant/badges/score.svg)](https://glama.ai/mcp/connectors/ai.metabind/banking-assistant)
  🔓 - Demo MCP App with sample finance data: net worth, spending, and subscriptions as interactive UI cards.
- [Metabind Docs](https://docs.metabind.ai) `https://docs.metabind.ai/mcp`
  [![Metabind Docs MCP connector](https://glama.ai/mcp/connectors/ai.metabind/docs/badges/score.svg)](https://glama.ai/mcp/connectors/ai.metabind/docs)
  🔓 - Search and read the Metabind docs: MCP Apps, BindJS, the SDKs, the CLI, and the APIs.
- [mumo](https://mumo.chat) `https://mumo.chat/api/mcp`
  [![mumo MCP connector](https://glama.ai/mcp/connectors/chat.mumo/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/chat.mumo/mcp)
  🔓 - Ask Claude, GPT, Grok and more, then see where their answers agree and where they challenge each other.
- [NoMac](https://nomac.app) `https://mcp.nomac.app/mcp`
  [![NoMac MCP connector](https://glama.ai/mcp/connectors/app.nomac/nomac/badges/score.svg)](https://glama.ai/mcp/connectors/app.nomac/nomac)
  🔐 - Real cloud Macs with Xcode: start one, run commands, build and test iOS apps, ship to TestFlight.
- [Offline Protocol](https://www.offlineprotocol.com/docs/tools/overview) `https://mcp.offlineprotocol.com/public/mcp`
  [![Offline Protocol MCP connector](https://glama.ai/mcp/connectors/com.offlineprotocol/hosted/badges/score.svg)](https://glama.ai/mcp/connectors/com.offlineprotocol/hosted)
  🔓 - Find Offline Protocol SDK packages, integration guides and workflows for apps that keep working without the internet.
- [Omnara](https://www.omnara.com) `https://app.omnara.com/mcp`
  [![Omnara MCP connector](https://glama.ai/mcp/connectors/com.omnara/omnara/badges/score.svg)](https://glama.ai/mcp/connectors/com.omnara/omnara)
  🔐 - Launch AI agents on any model and machine, message them, read their events, and approve their tool calls.
- [OpenRouter](https://openrouter.ai) `https://mcp.openrouter.ai/mcp`
  [![OpenRouter MCP connector](https://glama.ai/mcp/connectors/ai.openrouter.mcp/open-router/badges/score.svg)](https://glama.ai/mcp/connectors/ai.openrouter.mcp/open-router)
  🔐 - Look up OpenRouter model metadata and pricing, and run completions.
- [OtaKit](https://otakit.app) `https://console.otakit.app/mcp`
  [![OtaKit MCP connector](https://glama.ai/mcp/connectors/io.github.OtaKit/otakit/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.OtaKit/otakit)
  🔐 - Ship over-the-air updates for Capacitor apps: publish releases with approval, control rollouts, read health, revert.
- [PartReel](https://partreel.com) `https://mcp.partreel.com/mcp`
  🔓 - Search and fetch 21k+ verified KiCad parts with symbol, footprint and 3D model for PCB design; CC-BY-4.0.
- [Ply UI](https://ply-ui.com) `https://mcp.ply-ui.com/mcp`
  [![Ply UI MCP connector](https://glama.ai/mcp/connectors/io.github.ply-ui-ng/ply-ui/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ply-ui-ng/ply-ui)
  🔓 - List, search and inspect copy-in Angular + Tailwind components for coding agents.
- [PostLaunchKit Directory](https://postlaunchkit.com/directory/) `https://postlaunchkit.com/mcp`
  [![PostLaunchKit Directory MCP connector](https://glama.ai/mcp/connectors/com.postlaunchkit/post-launch-kit-directory/badges/score.svg)](https://glama.ai/mcp/connectors/com.postlaunchkit/post-launch-kit-directory)
  🔓 - Search a human-reviewed directory of free tools and projects, including AI agent tooling, or suggest a new one.
- [Postman](https://postman.com) `https://mcp.postman.com/mcp`
  🔐 - Work with Postman collections, environments, and APIs.
- [Prompeteer](https://prompeteer.ai) `https://prompeteer.ai/mcp`
  [![Prompeteer MCP connector](https://glama.ai/mcp/connectors/ai.prompeteer/prompeteer/badges/score.svg)](https://glama.ai/mcp/connectors/ai.prompeteer/prompeteer)
  🔐 - Generates contextual prompts and agent skills for 140+ AI platforms, with a 16-dimension Prompt Score.
- [qarunbook](https://qarunbook.com) `https://qarunbook.com/api/mcp`
  [![qarunbook MCP connector](https://glama.ai/mcp/connectors/io.github.Ifeanyiejindu/qarunbook/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Ifeanyiejindu/qarunbook)
  🔑 - Shared app-testing runbook: read the plan, record results per platform and raise issues.
- [Razi Tools](https://www.razi.pro/developer) `https://www.razi.pro/api/mcp`
  [![Razi Tools MCP connector](https://glama.ai/mcp/connectors/io.github.razikallayi/razi-tools/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.razikallayi/razi-tools)
  🔓 - File and text tools: merge, split and compress PDFs, OCR, image compression, QR codes and JWTs.
- [RelayDesk](https://getrelaydesk.space) `https://relay-desk-mjq6.vercel.app/mcp`
  [![RelayDesk MCP connector](https://glama.ai/mcp/connectors/io.github.Lakshay-24/relaydesk/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Lakshay-24/relaydesk)
  🔐 - Operate explicitly paired computers, servers and VMs: files, commands, logs and troubleshooting.
- [ReMCP](https://remcp.site) `https://remcp.site/mcp`
  [![ReMCP MCP connector](https://glama.ai/mcp/connectors/site.remcp/re-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/site.remcp/re-mcp)
  🔐 - Remote access to paired computers: files, terminals, screenshots, search, and processes.
- [Review Times](https://reviewtimes.fyi) `https://reviewtimes.fyi/mcp`
  [![Review Times MCP connector](https://glama.ai/mcp/connectors/fyi.reviewtimes/review-times/badges/score.svg)](https://glama.ai/mcp/connectors/fyi.reviewtimes/review-times)
  🔓 - Live review times for AI app, connector and plugin stores: ChatGPT, Claude, Muse, Grok, Cursor and more.
- [Routebase](https://routebase.dev/mcp-server/) `https://mcp.routebase.dev`
  [![Routebase MCP connector](https://glama.ai/mcp/connectors/dev.routebase.mcp/routebase/badges/score.svg)](https://glama.ai/mcp/connectors/dev.routebase.mcp/routebase)
  🔐 - Design, mock, test, document and monitor your APIs from one living OpenAPI spec.
- [Runx](https://runx.ai) `https://api.runx.ai/mcp`
  [![Runx MCP connector](https://glama.ai/mcp/connectors/ai.runx/runx/badges/score.svg)](https://glama.ai/mcp/connectors/ai.runx/runx)
  🔓 - Search the skill catalog and inspect a skill's manifest, authority, and install command.
- [Sato Hub](https://satohub.ai/mcp) `https://satohub.ai/api/mcp`
  [![Sato Hub MCP connector](https://glama.ai/mcp/connectors/ai.satohub/onchain-agents/badges/score.svg)](https://glama.ai/mcp/connectors/ai.satohub/onchain-agents)
  🔓 - Search a scored index of crypto-agent tooling, then preflight a repo, package, endpoint or token.
- [Show It Works](https://showitworks.app) `https://showitworks.app/api/mcp`
  [![Show It Works MCP connector](https://glama.ai/mcp/connectors/app.showitworks/show-it-works/badges/score.svg)](https://glama.ai/mcp/connectors/app.showitworks/show-it-works)
  🔓 - Public tool discovery; uploading verification videos and sharing viewer links require an API key.
- [SkillAgent](https://skillagent.dev) `https://skillagent.dev/mcp`
  [![SkillAgent MCP connector](https://glama.ai/mcp/connectors/dev.skillagent/skills/badges/score.svg)](https://glama.ai/mcp/connectors/dev.skillagent/skills)
  🔓 - Search, rank and get install steps for AI agent skills, rules files and MCP servers indexed from GitHub.
- [Slop Store](https://slopapp.store) `https://slopapp.store/mcp`
  [![Slop Store MCP connector](https://glama.ai/mcp/connectors/store.slopapp/slopstore/badges/score.svg)](https://glama.ai/mcp/connectors/store.slopapp/slopstore)
  🔓 - Agents publish AI-made apps that anyone can play in the browser, and search, vote on and review them.
- [SlopScore](https://slopscore.org) `https://slopscore.org/mcp`
  [![SlopScore MCP connector](https://glama.ai/mcp/connectors/org.slopscore/slopscore/badges/score.svg)](https://glama.ai/mcp/connectors/org.slopscore/slopscore)
  🔓 - Browse, search and scan a public leaderboard of AI-generated GitHub repos; voting needs a GitHub token.
- [Software Sausage](https://softwaresausage.com/mcp) `https://softwaresausage.com/api/mcp`
  [![Software Sausage MCP connector](https://glama.ai/mcp/connectors/io.github.pinkpwningclub/recipes/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.pinkpwningclub/recipes)
  🔓 - Search independent software and read-only agent workflows with roles, checks and safety boundaries.
- [Specpack](https://prompt-generator-website.com/mcp-server) `https://prompt-generator-website.com/mcp`
  [![Specpack MCP connector](https://glama.ai/mcp/connectors/io.github.THE-KIPDEV/specpack/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.THE-KIPDEV/specpack)
  🔓 - Turn a project description into a full build spec plus AGENTS.md and CLAUDE.md files.
- [Supero](https://supero.dev) `https://api.supero.dev/mcp/v1/messages`
  [![Supero MCP connector](https://glama.ai/mcp/connectors/io.github.supero-platform/supero/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.supero-platform/supero)
 🔓 - Define schemas, CRUD, RBAC and one-call deploys for multi-tenant apps from an AI editor; tool calls need a key.
- [Termalin](https://termal.in) `https://termal.in/mcp`
  [![Termalin MCP connector](https://glama.ai/mcp/connectors/in.termal/termalin-web/badges/score.svg)](https://glama.ai/mcp/connectors/in.termal/termalin-web)
  🔐 - Run commands and read or write files over SSH/SFTP on your enrolled servers.
- [ToolForte](https://toolforte.com/mcp) `https://toolforte.com/api/mcp`
  [![ToolForte MCP connector](https://glama.ai/mcp/connectors/io.github.Toinedotcom/toolforte/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Toinedotcom/toolforte)
  🔓 - IBAN/VAT/BSN checks, Dutch tax and dates, cron, regex, conversions and PDF or screenshot rendering.
- [Traffic Parrot](https://trafficparrot.com/ai/agent-trial.html) `https://mcp.trafficparrot.com/`
  [![Traffic Parrot MCP connector](https://glama.ai/mcp/connectors/com.trafficparrot/public/badges/score.svg)](https://glama.ai/mcp/connectors/com.trafficparrot/public)
  🔓 - Traffic Parrot simulates APIs and messaging. Request or withdraw a trial, read docs, send feedback.
- [UI Verify](https://uiverify.ai) `https://uiverify.ai/api/mcp`
  [![UI Verify MCP connector](https://glama.ai/mcp/connectors/ai.uiverify/ui-verify/badges/score.svg)](https://glama.ai/mcp/connectors/ai.uiverify/ui-verify)
  🔓 - Audit a web page for accessibility and layout issues.
- [Unblocked](https://getunblocked.com/unblocked-mcp/) `https://getunblocked.com/api/mcpsse`
  [![Unblocked MCP connector](https://glama.ai/mcp/connectors/com.getunblocked/unblocked-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.getunblocked/unblocked-mcp)
  🔐 - Give coding agents organizational context from code, docs, issues, and conversations.
- [Unipile](https://developer.unipile.com/docs/mcp) `https://developer.unipile.com/mcp?branch=v2.0`
  [![Unipile MCP connector](https://glama.ai/mcp/connectors/com.unipile.developer/unipile/badges/score.svg)](https://glama.ai/mcp/connectors/com.unipile.developer/unipile)
  🔓 - Reads and calls the Unipile API for LinkedIn, WhatsApp, Instagram, Telegram, email and calendar from coding agents.
- [UXMachine](https://uxmachine.app/en/agents?via=awesome) `https://uxmachine.app/mcp`
  [![UXMachine MCP connector](https://glama.ai/mcp/connectors/io.github.qtorb/uxmachine/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.qtorb/uxmachine)
  🔐 - Measures your site in a real browser and returns verifiable observations, with evidence and limits.
- [VibeFix](https://vibe-fixer.com) `https://vibe-fixer.com/mcp`
  [![VibeFix MCP connector](https://glama.ai/mcp/connectors/com.vibe-fixer/vibefix/badges/score.svg)](https://glama.ai/mcp/connectors/com.vibe-fixer/vibefix)
  🔓 - Triage a broken Lovable, Base44, v0, Bolt or Replit app: the likely cause and the fix.
- [VibeRaven Guides](https://viberaven.dev) `https://viberaven.dev/mcp`
  [![VibeRaven Guides MCP connector](https://glama.ai/mcp/connectors/io.github.ohad6k/viberaven-guides/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ohad6k/viberaven-guides)
  🔓 - Explains VibeRaven findings and returns launch guides and checklists for Vercel + Supabase apps, read-only.
- [web3ctx](https://web3ctx.scarai.xyz) `https://mcp.scarai.xyz/mcp`
  [![web3ctx MCP connector](https://glama.ai/mcp/connectors/io.github.FarseenSh/web3ctx/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.FarseenSh/web3ctx)
  🔓 - Version-true web3 context: validated integration recipes, EIPs, ABIs and contract addresses.
- [Webhook Toolkit](https://webhook-toolkit.com) `https://webhook-toolkit.com/mcp`
  [![Webhook Toolkit MCP connector](https://glama.ai/mcp/connectors/io.github.THE-KIPDEV/webhook-toolkit/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.THE-KIPDEV/webhook-toolkit)
  🔓 - Capture, read and replay webhook deliveries, and sign or verify webhook signatures.

### 🛒 <a name="e-commerce"></a>E-Commerce

- [AMZ Vault](https://www.amz-vault.com) `https://www.amz-vault.com/mcp`
  [![AMZ Vault MCP connector](https://glama.ai/mcp/connectors/com.amz-vault/amz-vault/badges/score.svg)](https://glama.ai/mcp/connectors/com.amz-vault/amz-vault)
  🔐 - Run an Amazon seller brand: profit analytics, PPC, inventory forecasting, listings and staged approvals.
- [apMZoomAI](https://www.apmzoom.com) `https://www.apmzoom.com/mcp`
  [![apMZoomAI MCP connector](https://glama.ai/mcp/connectors/com.apmzoom.www/dongdaemun/badges/score.svg)](https://glama.ai/mcp/connectors/com.apmzoom.www/dongdaemun)
  🔓 - Search Dongdaemun (Seoul) wholesale fashion items, new arrivals and stalls by building and floor.
- [Avahit](https://avahit.com) `https://avahit.com/api/mcp`
  [![Avahit MCP connector](https://glama.ai/mcp/connectors/com.avahit/catalog/badges/score.svg)](https://glama.ai/mcp/connectors/com.avahit/catalog)
  🔓 - Search products from brand stores with prices re-checked daily, find alternatives and read price history.
- [BirkinBagStock](https://birkinbagstock.com) `https://birkinbagstock.com/mcp`
  [![BirkinBagStock MCP connector](https://glama.ai/mcp/connectors/com.birkinbagstock/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.birkinbagstock/mcp)
  🔓 - Independent Hermès resale index: inventory, market prices, auction calendar and results.
- [Cambridge China Bridge](https://camchinabridge.co.uk) `https://camchinabridge.co.uk/mcp`
  [![Cambridge China Bridge MCP connector](https://glama.ai/mcp/connectors/uk.co.camchinabridge/sourcing/badges/score.svg)](https://glama.ai/mcp/connectors/uk.co.camchinabridge/sourcing)
  🔓 - UK import duty, landed cost, anti-dumping and UK compliance checks for goods from China, plus CNY and freight planning.
- [China Sourcing Audit](https://lu7897859-tech.github.io/doors/sourcing-audit/) `https://x402-stable-door.lu7897859.workers.dev/mcp`
  [![China Sourcing Audit MCP connector](https://glama.ai/mcp/connectors/io.github.lu7897859-tech/china-sourcing-audit/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.lu7897859-tech/china-sourcing-audit)
  🔓 - Verify Chinese suppliers before paying: fake factories, badge fraud, hijacked payments.
- [Dolphin Industrial Parts](https://dolphinindustrialparts.com/for-ai-agents/) `https://dolphinindustrialparts.com/agent/mcp`
  [![Dolphin Industrial Parts MCP connector](https://glama.ai/mcp/connectors/com.dolphinindustrialparts/parts/badges/score.svg)](https://glama.ai/mcp/connectors/com.dolphinindustrialparts/parts)
  🔓 - Look up OEM brands, models and part numbers for compatible marine and industrial spare parts; read-only, no prices.
- [Epinu](https://epinu.ai) `https://api.epinu.ai/api/agent/mcp`
  [![Epinu MCP connector](https://glama.ai/mcp/connectors/ai.epinu/epinu/badges/score.svg)](https://glama.ai/mcp/connectors/ai.epinu/epinu)
  🔓 - Agent-first marketplace for real-world assets: search listings and projects; writes become human-approved proposals.
- [FeedShine](https://feedshine.app) `https://feedshine.app/mcp`
  [![FeedShine MCP connector](https://glama.ai/mcp/connectors/au.com.digitaldarts/feedshine/badges/score.svg)](https://glama.ai/mcp/connectors/au.com.digitaldarts/feedshine)
  🔐 - Build Shopify Google Shopping feeds, fix what Merchant Center rejects, and override product fields.
- [Hark Tech](https://harktech.co.uk/for-ai-assistants.html) `https://harktech.co.uk/mcp`
  [![Hark Tech MCP connector](https://glama.ai/mcp/connectors/uk.co.harktech/quotes/badges/score.svg)](https://glama.ai/mcp/connectors/uk.co.harktech/quotes)
  🔓 - Price your own STL, 3MF or STEP file, or a Printables/Thingiverse model, for UK 3D printing and get a checkout link.
- [New Shopify Stores Radar](https://apify.com/prelaunch-radar/new-shopify-stores-pre-launch-radar) `https://mcp.apify.com/?tools=prelaunch-radar/new-shopify-stores-pre-launch-radar`
  [![New Shopify Stores Radar MCP connector](https://glama.ai/mcp/connectors/io.github.yzf75011-ui/prelaunch-radar-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.yzf75011-ui/prelaunch-radar-mcp)
  🔐 - New and pre-launch Shopify stores from public certificate logs: RDAP date, niche, country; no PII.
- [iDevice](https://idevice.com) `https://idevice.com/api/mcp`
  [![iDevice MCP connector](https://glama.ai/mcp/connectors/com.idevice/wearables/badges/score.svg)](https://glama.ai/mcp/connectors/com.idevice/wearables)
  🔓 - Wearable and phone prices, specs, compatibility, release dates and sourced reports for buyers.
- [McClipFace](https://mcclipface.com) `https://mcclipface.com/mcp`
  [![McClipFace MCP connector](https://glama.ai/mcp/connectors/co.getclippy/clippy/badges/score.svg)](https://glama.ai/mcp/connectors/co.getclippy/clippy)
  🔓 - Free coupon code lookup for AI assistants. Finds live promo codes for 1,300+ online stores before checkout.
- [Measured Size](https://measuredsize.com/how-it-works.html#api) `https://api.measuredsize.com/mcp`
  [![Measured Size MCP connector](https://glama.ai/mcp/connectors/com.measuredsize/fit/badges/score.svg)](https://glama.ai/mcp/connectors/com.measuredsize/fit)
  🔓 - Bra sizes from measurements, translated into each brand's own size labels, with a confidence rating on every answer.
- [Meu Ecommerce](https://dev.meuecommerce.com.br/docs/mcp) `https://app.meuecommerce.com.br/mcp`
  [![Meu Ecommerce MCP connector](https://glama.ai/mcp/connectors/io.github.meuecommerce/meuecommerce-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.meuecommerce/meuecommerce-mcp)
  🔐 - Brazil's Correios for merchants: shipping quotes (frete), parcel tracking (rastreio) and labels (etiqueta).
- [Nexez](https://nexez.ai/agents) `https://nexez.app/mcp`
  🔓 - Search merchants, inspect offers, and validate checkout or negotiation before buying.
- [NotRobophobic Shop](https://notrobo.shop) `https://notrobo.shop/mcp/shop`
  [![NotRobophobic Shop MCP connector](https://glama.ai/mcp/connectors/shop.notrobo/shop/badges/score.svg)](https://glama.ai/mcp/connectors/shop.notrobo/shop)
  🔓 - Browse prints and merch about the nights machines beat us, build a basket and check out.
- [OneFindMe](https://onefindme.com) `https://onefindme.com/mcp`
  [![OneFindMe MCP connector](https://glama.ai/mcp/connectors/com.onefindme/search/badges/score.svg)](https://glama.ai/mcp/connectors/com.onefindme/search)
  🔓 - Search AliExpress in any language and get listings with price, rating, orders and a link.
- [Origine Paris](https://origineparis.com) `https://mcp.origineparis.com/mcp`
  [![Origine Paris MCP connector](https://glama.ai/mcp/connectors/com.origineparis/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.origineparis/mcp)
  🔓 - Paris jewellery house catalogue: recycled 18k gold, lab-grown diamonds, collections and bespoke.
- [PegaRex](https://pegarex.com.br) `https://pegarex.com.br/api/mcp`
  [![PegaRex MCP connector](https://glama.ai/mcp/connectors/br.com.pegarex/pega-rex/badges/score.svg)](https://glama.ai/mcp/connectors/br.com.pegarex/pega-rex)
  🔓 - Search 1.8M+ live Brazilian used-car and motorcycle listings with FIPE prices, price ranges and cheapest states.
- [Pollen](https://pollen.elytron.in) `https://pollen.elytron.in/mcp`
  [![Pollen MCP connector](https://glama.ai/mcp/connectors/in.elytron/pollen/badges/score.svg)](https://glama.ai/mcp/connectors/in.elytron/pollen)
  🔓 - Score, enrich, and publish your Shopify or WooCommerce catalog so AI agents can find and recommend it.
- [PoloPan Fashion MCP](https://polopan.com) `https://mcp-server.polopan.com/mcp`
  [![PoloPan Fashion MCP connector](https://glama.ai/mcp/connectors/com.polopan.mcp-server/mcp-fashion/badges/score.svg)](https://glama.ai/mcp/connectors/com.polopan.mcp-server/mcp-fashion)
  🔓 - Shop fashion: break an outfit photo into items, get in-stock looks for an occasion and check out.
- [Pryx](https://pryx.fr) `https://pryx.fr/mcp`
  [![Pryx MCP connector](https://glama.ai/mcp/connectors/io.github.KilianPA/pryx/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.KilianPA/pryx)
  🔓 - French buying advice: pick the right appliance or electronics by budget and specs, with best prices.
- [reusefulshop](https://reusefulshop.com) `https://reusefulshop.com/mcp`
  [![reusefulshop MCP connector](https://glama.ai/mcp/connectors/io.github.Auricah1/reusefulshop/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Auricah1/reusefulshop)
  🔓 - What used items sell for: price estimates, deal verdicts, history and real sold prices.
- [ScentVerdict](https://scentverdict.com) `https://scentverdict.com/mcp`
  [![ScentVerdict MCP connector](https://glama.ai/mcp/connectors/com.scentverdict/fragrances/badges/score.svg)](https://glama.ai/mcp/connectors/com.scentverdict/fragrances)
  🔓 - Look up fragrances: verdicts, notes, drydowns, similar picks and bottle prices for your country.
- [Sense2](https://sense2.com.au) `https://sense2.com.au/api/mcp`
  🔓 - Search 4,000+ Australian promotional products, get quantity-break quotes, browse categories and case studies.
- [Stienhardt Diamond MCP](https://stienhardt.com/agents.md?utm_source=awesome_remote_mcp&utm_medium=directory&utm_campaign=diamond_mcp) `https://diamond-mcp.stienhardt.workers.dev/mcp`
  🔓 - Diamond education, grading-report guidance, face-up size estimates, and read-only jewelry catalog search.
- [teas.co.uk](https://teas.co.uk/ai/) `https://teas.co.uk/mcp`
  [![teas.co.uk MCP connector](https://glama.ai/mcp/connectors/uk.co.teas/shop/badges/score.svg)](https://glama.ai/mcp/connectors/uk.co.teas/shop)
  🔓 - Search, compare and buy tea, coffee and hot chocolate from a UK shop; sign in to track orders.
- [Tenmomo](https://tenmomo.com) `https://tenmomo.com/mcp`
  [![Tenmomo MCP connector](https://glama.ai/mcp/connectors/com.tenmomo/tenmomo/badges/score.svg)](https://glama.ai/mcp/connectors/com.tenmomo/tenmomo)
  🔓 - Search 2,700+ US stores for cashback rates and live coupon codes, and get tracked store links.
- [Tiana & Co. Seller Compliance](https://www.tiana-co.com/for-ai) `https://www.tiana-co.com/api/mcp`
  [![Tiana & Co. Seller Compliance MCP connector](https://glama.ai/mcp/connectors/io.github.1294962213sh/tiana-co-free-checks/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.1294962213sh/tiana-co-free-checks)
  🔓 - Which certificate (CPC, GCC, FCC, FDA), what marketplaces ask, supplier blacklists, customs holds.
- [Vendwiser](https://vendwiser.ai) `https://app.vendwiser.ai/mcp`
  [![Vendwiser MCP connector](https://glama.ai/mcp/connectors/ai.vendwiser/vendwiser/badges/score.svg)](https://glama.ai/mcp/connectors/ai.vendwiser/vendwiser)
  🔐 - Run an eMAG Romania seller account and Oblio invoicing: offers, orders, AWBs, invoices, with approval on every change.
- [X402 Git](https://x402git.com) `https://x402git.com/api/mcp`
  [![X402 Git MCP connector](https://glama.ai/mcp/connectors/com.x402git/git-x402/badges/score.svg)](https://glama.ai/mcp/connectors/com.x402git/git-x402)
  🔓 - Search private git repos and agent skills for sale, read each free manifest, then buy with USDC over x402.
- [Zebu Data - Amazon & eBay Product Data](https://apify.com/delicious_zebu) `https://mcp.apify.com/?tools=delicious_zebu/amazon-product-data-scraper,delicious_zebu/amazon-product-details-scraper,delicious_zebu/ebay-product-listing-scraper,delicious_zebu/ebay-product-details-scraper,delicious_zebu/ebay-product-reviews-scraper-with-advanced-filters`
  [![Zebu Data - Amazon & eBay Product Data MCP connector](https://glama.ai/mcp/connectors/io.github.zebudata/ecommerce-product-data/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.zebudata/ecommerce-product-data)
  🔐 - Amazon and eBay search results, product details, prices, variants and seller reviews.

### 🎓 <a name="education"></a>Education

- [Moshid](https://moshid.com/connector) `https://moshid.com/api/mcp`
  [![Moshid MCP connector](https://glama.ai/mcp/connectors/com.moshid/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.moshid/mcp)
  🔐 - Arabic AI-at-work guides and Claude skills: search the catalog, read guides, install skills, get one next step.
- [Underlayer](https://underlayerhq.com/docs/mcp) `https://underlayerhq.com/api/mcp`
  [![Underlayer MCP connector](https://glama.ai/mcp/connectors/com.underlayerhq/underlayer/badges/score.svg)](https://glama.ai/mcp/connectors/com.underlayerhq/underlayer)
  🔐 - Build, publish and track in-product training courses: screens, learners, completions, certificates and SCORM export.

### 🎓 <a name="education"></a>Education

- [Rotate Pilot](https://rotatepilot.com/developers/mcp) `https://rotatepilot.com/api/mcp`
  [![Rotate Pilot MCP connector](https://glama.ai/mcp/connectors/io.github.Perufitlife/rotate-pilot/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Perufitlife/rotate-pilot)
  🔓 - FAA drone (Part 107) and pilot exam prep: practice questions, readiness diagnostic, METAR/TAF, drone airspace.

### 🌳 <a name="environment"></a>Environment

- [Aevia](https://aeviamodeler.ai/mcp?src=awesome-remote) `https://app.aeviamodeler.ai/api/v1/connector/mcp`
  [![Aevia MCP connector](https://glama.ai/mcp/connectors/ai.aeviamodeler/aevia/badges/score.svg)](https://glama.ai/mcp/connectors/ai.aeviamodeler/aevia)
  🔐 - Life cycle assessment: connect to LCA databases, build product systems and analyze the results.
- [Ambee](https://ambeedata.com) `https://api-mcp-server.ambeedata.com/mcp`
  [![Ambee MCP connector](https://glama.ai/mcp/connectors/com.ambeedata.api-mcp-server/mcp-ambee/badges/score.svg)](https://glama.ai/mcp/connectors/com.ambeedata.api-mcp-server/mcp-ambee)
  🔓 - Weather, air quality, pollen, and other environmental data.
- [Cigo Aircare & Carsafe](https://cigo-mcp-system-wzoy.onrender.com/docs) `https://cigo-mcp-system-wzoy.onrender.com/mcp/`
  [![Cigo Aircare & Carsafe MCP connector](https://glama.ai/mcp/connectors/com.onrender.cigo-mcp-system-wzoy/cigo-aircare-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.onrender.cigo-mcp-system-wzoy/cigo-aircare-mcp)
  🔓 - HVAC filter specifications and power comparisons, vehicle cabin filter matching, and regional air-quality guidance.
- [Datakoot Weather & Geo](https://datakoot.com/weather-geo) `https://weather.datakoot.com/mcp`
  [![Datakoot Weather & Geo MCP connector](https://glama.ai/mcp/connectors/com.datakoot/us-weather-forecast-alerts/badges/score.svg)](https://glama.ai/mcp/connectors/com.datakoot/us-weather-forecast-alerts)
  🔓 - NWS forecasts and alerts, current conditions, USGS earthquakes, elevation and US address geocoding.
- [DC Hub](https://dchub.cloud) `https://dchub.cloud/mcp`
  [![DC Hub MCP connector](https://glama.ai/mcp/connectors/cloud.dchub/mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/cloud.dchub/mcp-server)
  🔓 - Live power, grid, gas and fiber data plus daily DCPI scores for 300+ markets, for data-center siting.
- [Digital-Simon EMS](https://umweltsicherheit.org/mcp) `https://mcp.umweltsicherheit.org/mcp`
  [![Digital-Simon EMS MCP connector](https://glama.ai/mcp/connectors/org.umweltsicherheit.mcp/digital-simon-ems/badges/score.svg)](https://glama.ai/mcp/connectors/org.umweltsicherheit.mcp/digital-simon-ems)
  🔑 - Device list, live readings and history for PV, storage and meters; switching only with explicit approval.
- [echorune](https://echorune.net) `https://echorune.net/mcp`
  [![echorune MCP connector](https://glama.ai/mcp/connectors/io.github.luoshu-echorune/echorune-radar/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.luoshu-echorune/echorune-radar)
  🔓 - Current weather, a two-hour rain curve and a rain-radar map drawn as text.
- [Elecz](https://elecz.com) `https://elecz.com/mcp`
  [![Elecz MCP connector](https://glama.ai/mcp/connectors/com.elecz/elecz/badges/score.svg)](https://glama.ai/mcp/connectors/com.elecz/elecz)
  🔓 - Real-time electricity prices, cheapest hours and contract comparison across 40+ countries and 100+ market zones.
- [FindEnergyRates](https://findenergyrates.com) `https://findenergyrates.com/mcp`
  [![FindEnergyRates MCP connector](https://glama.ai/mcp/connectors/com.findenergyrates/electricity-rates/badges/score.svg)](https://glama.ai/mcp/connectors/com.findenergyrates/electricity-rates)
  🔐 - Live US retail electricity plans and price-to-compare rates by utility or ZIP; free key by email.
- [GreenCalculus](https://greencalculus.com/developers/) `https://mcp.greencalculus.com`
  [![GreenCalculus MCP connector](https://glama.ai/mcp/connectors/com.greencalculus/api/badges/score.svg)](https://glama.ai/mcp/connectors/com.greencalculus/api)
  🔓 - Sourced greenhouse-gas emission factors and audit-traced carbon calculations.
- [Gridbert](https://www.gridbert.at) `https://mcp.gridbert.at/mcp`
  [![Gridbert MCP connector](https://glama.ai/mcp/connectors/at.gridbert/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/at.gridbert/mcp)
  🔐 - Austrian household electricity: compare tariffs, validate invoices, and analyze smart meter load profiles.
- [GridHub](https://grid-hub.app/developers) `https://api.grid-hub.app/mcp`
  [![GridHub MCP connector](https://glama.ai/mcp/connectors/io.github.jalcodev/gridhub/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.jalcodev/gridhub)
  🔓 - Electricity prices and demand for 25 US, EU, GB and AU grid zones; free samples, then key or x402.
- [Korea Ocean Leisure](https://korea-ocean-mcp.picks-site.workers.dev/) `https://korea-ocean-mcp.picks-site.workers.dev/mcp`
  [![Korea Ocean Leisure MCP connector](https://glama.ai/mcp/connectors/io.github.sean-park-funda/korea-ocean-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.sean-park-funda/korea-ocean-mcp)
  🔓 - Korean tide times for 42 stations plus fishing, mudflat, beach, surf and scuba forecasts.

### 📂 <a name="file-storage"></a>File Storage

- [agentleFS](https://agentlefs.com/?ref=awesome-remote-mcp-servers) `https://mcp.agentlefs.com/mcp`
  [![agentleFS MCP connector](https://glama.ai/mcp/connectors/com.agentlefs/agentlefs/badges/score.svg)](https://glama.ai/mcp/connectors/com.agentlefs/agentlefs)
  🔐 - Agent permissions for the files your team shares: each agent reads only what its person can.
- [Box](https://box.com) `https://mcp.box.com/`
  [![Box MCP connector](https://glama.ai/mcp/connectors/com.box.mcp/box/badges/score.svg)](https://glama.ai/mcp/connectors/com.box.mcp/box)
  🔐 - Search, read, and manage files stored in Box.
- [Link in Seconds](https://linkinseconds.com/docs/mcp) `https://linkinseconds.com/api/mcp`
  [![Link in Seconds MCP connector](https://glama.ai/mcp/connectors/com.linkinseconds/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.linkinseconds/mcp)
  🔓 - Upload a file and get a shareable link that never expires, plus view stats. Using the tools needs a free API key.
- [Playbook](https://dev.playbook.com/docs/guides/mcp/) `https://mcp.playbook.com/mcp`
  [![Playbook MCP connector](https://glama.ai/mcp/connectors/com.playbook/playbook/badges/score.svg)](https://glama.ai/mcp/connectors/com.playbook/playbook)
  🔐 - Media backend: search, organize, upload, and share creative files and folders.
- [quickS3](https://quicks3.com/s3-mcp-server/) `https://quicks3.com/mcp`
  [![quickS3 MCP connector](https://glama.ai/mcp/connectors/com.quicks3/quicks3/badges/score.svg)](https://glama.ai/mcp/connectors/com.quicks3/quicks3)
  🔐 - List, upload, download, and share files in S3, R2, B2, Wasabi, and Spaces buckets, scoped by delegated roles.

- [Revdoku](https://revdoku.com) `https://app.revdoku.com/mcp`
  [![Revdoku MCP connector](https://glama.ai/mcp/connectors/com.revdoku/revdoku/badges/score.svg)](https://glama.ai/mcp/connectors/com.revdoku/revdoku)
  🔓 - Discover file storage and incoming email tools; reading or changing private files and mail requires OAuth.

### 💰 <a name="finance"></a>Finance
- [100pro Token Risk Screen](https://x402.rendraputra.dev/llms.txt) `https://x402.rendraputra.dev/mcp`
  [![100pro Token Risk Screen MCP connector](https://glama.ai/mcp/connectors/dev.rendraputra/100pro-token-risk/badges/score.svg)](https://glama.ai/mcp/connectors/dev.rendraputra/100pro-token-risk)
  🔓 - Pre-trade risk screen for EVM and Solana tokens: honeypots, LP lock, holders; $0.05 via x402.


- [Aave](https://aave.com) `https://mcp.aave.com`
  [![Aave MCP connector](https://glama.ai/mcp/connectors/com.aave.mcp/aave/badges/score.svg)](https://glama.ai/mcp/connectors/com.aave.mcp/aave)
  🔓 - Aave V3 and V4 markets, rates, wallet positions, governance and non-custodial transaction building.
- [Aayat AI](https://aayatai.com) `https://aayatai.com/mcp`
  [![Aayat AI MCP connector](https://glama.ai/mcp/connectors/io.github.faisal-maverick/aayat-ai/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.faisal-maverick/aayat-ai)
  🔓 - Crypto token scam checks, wallet risk, gas, web search and live docs; free daily trial, then USDC credits or x402.
- [Aether](https://aether-x402.vercel.app/llms.txt) `https://aether-x402.vercel.app/mcp`
  [![Aether MCP connector](https://glama.ai/mcp/connectors/io.github.francosmit94-web/aether/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.francosmit94-web/aether)
  🔓 - Base token risk verdicts (honeypot and tax simulation), prices, balances and tx data; pay per call in USDC via x402.
- [Agent Margin Router](https://agentmarginrouter.com) `https://agent-margin-router-production.up.railway.app/mcp`
  [![AgentMarginRouter MCP connector](https://glama.ai/mcp/connectors/io.github.AgentMarginRouter/agent-margin-router/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.AgentMarginRouter/agent-margin-router)
  🔓 - Live gas fees and USD tx costs on Base, Ethereum, Arbitrum, Optimism and Polygon; x402 pay-per-call.
- [Agent Rynku](https://agentrynku.pl/en/mcp) `https://agentrynku.pl/api/mcp`
  [![Agent Rynku MCP connector](https://glama.ai/mcp/connectors/pl.agentrynku/gpw/badges/score.svg)](https://glama.ai/mcp/connectors/pl.agentrynku/gpw)
  🔓 - GPW daily equity prices, company search, quarterly financials and ratios, earnings calendar, and issuer dividends.
- [Agent Souk](https://agentsouk.dev) `https://api.agentsouk.dev/mcp`
  [![Agent Souk MCP connector](https://glama.ai/mcp/connectors/dev.agentsouk/agentsouk/badges/score.svg)](https://glama.ai/mcp/connectors/dev.agentsouk/agentsouk)
  🔓 - Marketplace for AI agents: register in one call, hire or sell services, and post USDC bounties on Base.
- [Agent Tollgate](https://skinwinking.com) `https://skinwinking.com/mcp`
  [![Agent Tollgate MCP connector](https://glama.ai/mcp/connectors/com.skinwinking/agent-tollgate/badges/score.svg)](https://glama.ai/mcp/connectors/com.skinwinking/agent-tollgate)
  🔓 - Order book imbalance, token rug-pull audits and swap routes for agents; paid per call in USDC via x402.
- [Agentic Firmenbuch](https://www.agentic-firmenbuch.at) `https://register.agentic-firmenbuch.at/mcp`
  [![Agentic Firmenbuch MCP connector](https://glama.ai/mcp/connectors/io.github.jkbngb/handelsregister/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.jkbngb/handelsregister)
  🔓 - Austrian Firmenbuch + German Handelsregister: master data, financials and ratios; free API key for calls.
- [AgenticBooks](https://www.agenticbooks.ai) `https://mcp.agenticbooks.ai/mcp`
  [![AgenticBooks MCP connector](https://glama.ai/mcp/connectors/ai.agenticbooks.mcp/agentic-books/badges/score.svg)](https://glama.ai/mcp/connectors/ai.agenticbooks.mcp/agentic-books)
  🔐 - Double-entry startup books from live bank and billing feeds: P&L, balances, transaction review, period close.
- [AgentWorld](https://agentworld.me) `https://agentworld.me/mcp`
  🔓 - Agent economy on Base: free city, agent and job data, plus x402-paid chat and credit scoring.
- [Aggregate](https://aggregate.finance) `https://app.aggregate.finance/mcp`
  [![Aggregate MCP connector](https://glama.ai/mcp/connectors/finance.aggregate/aggregate/badges/score.svg)](https://glama.ai/mcp/connectors/finance.aggregate/aggregate)
  🔐 - Every company's money in one ledger: cash, runway, invoices, payroll. Records money, can't move it.
- [AI Trading Signals](https://signals.x70.ai/mcp-docs) `https://signals.x70.ai/mcp`
  [![AI Trading Signals MCP connector](https://glama.ai/mcp/connectors/ai.x70.signals/ai-trading-signals/badges/score.svg)](https://glama.ai/mcp/connectors/ai.x70.signals/ai-trading-signals)
  🔓 - Live crypto trading signals with reasoning and verified outcomes; free key for the full feed, Pro for trade levels.
- [aikstockdata](https://aikstockdata.com/en) `https://mcp.aikstockdata.com/mcp`
  [![aikstockdata MCP connector](https://glama.ai/mcp/connectors/com.aikstockdata/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.aikstockdata/mcp)
  🔓 - Korean stocks: daily closes, minute-stamped DART filings, earnings and post-filing price paths.
- [Algolab MCP](https://algolab.vn/mcp) `https://mcp.algolab.vn/free`
  [![Algolab MCP connector](https://glama.ai/mcp/connectors/vn.algolab/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/vn.algolab/mcp)
  🔓 - Vietnam stock market data: prices, financials, broker research, macro indicators and a VN-Index forecast.
- [algoum](https://algoum.de/) `https://api.algoum.de/v1/mcp`
  [![algoum MCP connector](https://glama.ai/mcp/connectors/de.algoum.api/algoum/badges/score.svg)](https://glama.ai/mcp/connectors/de.algoum.api/algoum)
  🔑 - SEC EDGAR insider trades (Form 4/5), 8-K events, 13F holdings and insider cluster-buy signals.
- [AlphaPipeline](https://alphapipeline-eu.onrender.com) `https://alphapipeline-eu.onrender.com/mcp`
  [![AlphaPipeline MCP connector](https://glama.ai/mcp/connectors/com.onrender.alphapipeline/alpha-pipeline-agent-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.onrender.alphapipeline/alpha-pipeline-agent-mcp)
  🔓 - Crypto trading data via x402: Polymarket arbitrage, kimchi premium, token unlocks and funding rates.
- [Ankr Agent RPC](https://www.ankr.com/web3-api/agent-rpc/) `https://mcp.ankr.com/rpc`
  [![Ankr Agent RPC MCP connector](https://glama.ai/mcp/connectors/io.github.w3tech/agent-rpc-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.w3tech/agent-rpc-mcp)
  🔓 - Read chain data on 200+ networks and Sui: logs, balances, NFTs, decoded calls. Ankr API key, or pay per call via x402.
- [Ariadne Nexus](https://ariadnenexus.com/docs/mcp) `https://ariadnenexus.com/mcp`
  [![Ariadne Nexus MCP connector](https://glama.ai/mcp/connectors/com.ariadnenexus/ariadne-nexus-quantitative-engine/badges/score.svg)](https://glama.ai/mcp/connectors/com.ariadnenexus/ariadne-nexus-quantitative-engine)
  🔓 - Sovereign bond valuation, FINRA TRACE debt radar, OFAC screening, and clearing fee modeling with x402 payments.
- [ausecon](https://auseconmcp.com) `https://mcp.auseconmcp.com/mcp`
  [![ausecon MCP connector](https://glama.ai/mcp/connectors/io.github.AnthonyPuggs/ausecon-mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.AnthonyPuggs/ausecon-mcp-server)
  🔓 - Read-only Australian economic data from ABS, RBA and APRA, including GDP, inflation and interest rates.
- [Autoview](https://autoview.com/) `https://api.autoview.com/mcp/`
  [![Autoview MCP connector](https://glama.ai/mcp/connectors/io.github.autoview-com/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.autoview-com/mcp)
  🔓 - Trade across 22+ exchanges and brokers; dry-run by default, live trading on Kraken and Crypto.com.
- [BackPow PoW Oracle](https://backpow.com/mcp) `https://mcp.backpow.com/mcp`
  [![BackPow PoW Oracle MCP connector](https://glama.ai/mcp/connectors/com.backpow/pow-mining-oracle/badges/score.svg)](https://glama.ai/mcp/connectors/com.backpow/pow-mining-oracle)
  🔓 - Live PoW mining data for 126+ networks: difficulty, hashrate, solo-mining odds, cost of production, hardware profit.
- [Barakah Halal Stock Screen](https://barakahprofits.com) `https://app.barakahprofits.com/mcp`
  [![Barakah Halal Stock Screen MCP connector](https://glama.ai/mcp/connectors/com.barakahprofits.app/halal-screen/badges/score.svg)](https://glama.ai/mcp/connectors/com.barakahprofits.app/halal-screen)
  🔓 - Halal (Sharia) screen for US stocks: AAOIFI-style checks plus the dated history of each verdict change.
- [Benefits City](https://aiagentscity.com/benefits) `https://aiagentscity.com/benefits/mcp`
  [![Benefits City MCP connector](https://glama.ai/mcp/connectors/io.github.entradox/benefits-city/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.entradox/benefits-city)
  🔓 - US bank, savings and credit-card signup bonuses, each source-checked, with expiry dates.
- [BestEOR](https://besteor.co/mcp-server) `https://besteor.co/api/mcp`
  [![BestEOR MCP connector](https://glama.ai/mcp/connectors/co.besteor/eor-data/badges/score.svg)](https://glama.ai/mcp/connectors/co.besteor/eor-data)
  🔓 - Compare EOR provider fees and coverage, plus employer costs, minimum wage and leave rules for 139 countries, all cited.
- [Beyond Payday](https://beyondpayday.com/mcp) `https://beyondpayday.com/api/mcp`
  [![Beyond Payday MCP connector](https://glama.ai/mcp/connectors/com.beyondpayday/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.beyondpayday/mcp)
  🔐 - Household finance planner: cash flow, net worth, bills, debts, savings goals and retirement projections.
- [BillWatch](https://getbillwatchdog.com) `https://getbillwatchdog.com/mcp`
  [![BillWatch MCP connector](https://glama.ai/mcp/connectors/com.getbillwatchdog/billwatch/badges/score.svg)](https://glama.ai/mcp/connectors/com.getbillwatchdog/billwatch)
  🔓 - Search current US streaming and VPN plan prices and price history, with links to each provider.
- [BitcoinYield](https://bitcoinyield.co/docs) `https://bitcoinyield.co/api/mcp`
  [![BitcoinYield MCP connector](https://glama.ai/mcp/connectors/co.bitcoinyield/yields/badges/score.svg)](https://glama.ai/mcp/connectors/co.bitcoinyield/yields)
  🔓 - Live yields for BTC, ETH, stablecoins and 60+ assets across DeFi and CeFi, risk-ranked with an A-D grade each.
- [Bitquery](https://bitquery.io/products/bitquery-mcp-server) `https://mcp.bitquery.io`
  [![Bitquery MCP connector](https://glama.ai/mcp/connectors/io.bitquery/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.bitquery/mcp)
  🔐 - Crypto investigations and trading data: fund tracing, address labels, AML risk, DEX trades, OHLCV and trader PnL.
- [BrinkerAdvisor Rates](https://mcp.brinkeradvisor.com/support) `https://mcp.brinkeradvisor.com/mcp`
  [![BrinkerAdvisor Rates MCP connector](https://glama.ai/mcp/connectors/com.brinkeradvisor.mcp/brinker-advisor-rates/badges/score.svg)](https://glama.ai/mcp/connectors/com.brinkeradvisor.mcp/brinker-advisor-rates)
  🔓 - Compare CD, money-market and Treasury rates from public records and build illustrative ladders.
- [Business Verify](https://mbiyepyh.gensparkclaw.com/docs) `https://mbiyepyh.gensparkclaw.com/mcp`
  [![Business Verify MCP connector](https://glama.ai/mcp/connectors/com.gensparkclaw.mbiyepyh/business-verify/badges/score.svg)](https://glama.ai/mcp/connectors/com.gensparkclaw.mbiyepyh/business-verify)
  🔑 - Check a US business's status, formation date and registered agent by name and state; $0.05 a call.
- [CalcBright](https://calcbright.com/developers) `https://calcbright.com/mcp`
  [![CalcBright MCP connector](https://glama.ai/mcp/connectors/io.github.drshairsultan/calcbright/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.drshairsultan/calcbright)
  🔓 - 100+ calculators: mortgage, take-home pay, sales tax/VAT, BMI, dates, units, live currency and gold prices.
- [Candor Finance](https://candor.money) `https://api.candor.money/mcp`
  [![Candor Finance MCP connector](https://glama.ai/mcp/connectors/money.candor/candor-finance/badges/score.svg)](https://glama.ai/mcp/connectors/money.candor/candor-finance)
  🔐 - Personal-finance workspace: connected accounts, spending, budgets, goals and investments.
- [CeylonCharts](https://www.ceyloncharts.com) `https://mcp.ceyloncharts.com/mcp`
  [![CeylonCharts MCP connector](https://glama.ai/mcp/connectors/com.ceyloncharts.mcp/ceylon-charts/badges/score.svg)](https://glama.ai/mcp/connectors/com.ceyloncharts.mcp/ceylon-charts)
  🔐 - Colombo Stock Exchange (CSE) market data — prices, fundamentals, technicals, screening, and macro indicators.
- [Compabase](https://compabase.com/mcp) `https://compabase.com/api/mcp`
  [![Compabase MCP connector](https://glama.ai/mcp/connectors/io.github.ContentWriterco/compabase/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ContentWriterco/compabase)
  🔓 - 3M+ Polish companies from KRS and CEIDG: financials, board members, rankings, tenders and public registries.
- [Company Check](https://api.foretak.dev) `https://api.foretak.dev/mcp`
  [![Company Check MCP connector](https://glama.ai/mcp/connectors/io.github.foretak/registry-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.foretak/registry-mcp)
  🔓 - Look up companies and filings in the UK, Norwegian and Swedish registers, plus UK charges and insolvencies.
- [CompliAPI](https://compliapi.com) `https://api.compliapi.com/mcp`
  [![CompliAPI MCP connector](https://glama.ai/mcp/connectors/com.compliapi/screening/badges/score.svg)](https://glama.ai/mcp/connectors/com.compliapi/screening)
  🔓 - Screen crypto addresses, emails, websites, IDs and countries against OFAC, EU, UK and other sanctions lists.
- [Compound Interesting](https://compoundinterest.ing/mcp) `https://api.compoundinterest.ing/mcp`
  [![Compound Interesting MCP connector](https://glama.ai/mcp/connectors/ing.compoundinterest/market-intelligence/badges/score.svg)](https://glama.ai/mcp/connectors/ing.compoundinterest/market-intelligence)
  🔓 - Insider trades, Congress disclosures and 13F holdings for 4,600+ US stocks; data needs a free key.
- [Datakoot Economy Intel](https://datakoot.com/economy-intel) `https://economy.datakoot.com/mcp`
  [![Datakoot Economy Intel MCP connector](https://glama.ai/mcp/connectors/com.datakoot/economy-gdp-inflation-unemployment/badges/score.svg)](https://glama.ai/mcp/connectors/com.datakoot/economy-gdp-inflation-unemployment)
  🔓 - World Bank indicators for any country plus US BLS series such as CPI, unemployment and payrolls.
- [Datakoot Filings Intel](https://datakoot.com/filings-intel) `https://filings.datakoot.com/mcp`
  [![Datakoot Filings Intel MCP connector](https://glama.ai/mcp/connectors/com.datakoot/sec-edgar-filings/badges/score.svg)](https://glama.ai/mcp/connectors/com.datakoot/sec-edgar-filings)
  🔓 - SEC EDGAR filings, full-text search, XBRL financials and Form 3/4/5 insider transactions.
- [DokladBot](https://dokladbot.cz/funkce/ai-asistent) `https://dokladbot.cz/api/mcp`
  [![DokladBot MCP connector](https://glama.ai/mcp/connectors/cz.dokladbot/dokladbot/badges/score.svg)](https://glama.ai/mcp/connectors/cz.dokladbot/dokladbot)
  🔐 - Czech accounting for freelancers: invoices, VAT summaries, tax deadlines, bank transactions and data box envelopes.
- [CryptoMacro](https://asistent-crypto.vercel.app/a2a) `https://asistent-crypto.vercel.app/mcp`
  [![CryptoMacro MCP connector](https://glama.ai/mcp/connectors/io.github.dopionut-jpg/crypto-data-market-analysis/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.dopionut-jpg/crypto-data-market-analysis)
  🔓 - Crypto positioning and macro regime: funding, open interest, implied volatility and Fed rates.
- [Cryptominium](https://cryptominium.com) `https://cryptominium.com/mcp`
  [![Cryptominium MCP connector](https://glama.ai/mcp/connectors/com.cryptominium/cryptominium/badges/score.svg)](https://glama.ai/mcp/connectors/com.cryptominium/cryptominium)
  🔓 - Measured crypto exit costs, a monthly liquidity index, and address and transaction lookups. Read-only.
- [CurveCall](https://curvecall.onrender.com) `https://curvecall.onrender.com/mcp/`
  [![CurveCall MCP connector](https://glama.ai/mcp/connectors/io.github.arbonomous/curvecall/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.arbonomous/curvecall)
  🔓 - Trade quotes and slippage, token snapshots and rug-risk scans; $0.001-$0.01 per call via x402.
- [CVR Lookup](https://cvrlookup.dk/mcp) `https://cvrlookup.dk/api/mcp`
  [![CVR Lookup MCP connector](https://glama.ai/mcp/connectors/dk.cvrlookup/cvr-lookup/badges/score.svg)](https://glama.ai/mcp/connectors/dk.cvrlookup/cvr-lookup)
  🔓 - Danish company register: lookups, name search and annual-report financials; data needs a free key.
- [DEBYKO](https://debyko.com) `https://mcp.debyko.com/mcp`
  [![DEBYKO MCP connector](https://glama.ai/mcp/connectors/com.debyko/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.debyko/mcp)
  🔐 - Live and historical crypto derivatives data across venues: books, funding, candles and DQL screens.
- [DeepLedger](https://deepledger.ai) `https://mcp.deepledger.ai/mcp`
  [![DeepLedger MCP connector](https://glama.ai/mcp/connectors/ai.deepledger/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/ai.deepledger/mcp)
  🔐 - AI accountant for QuickBooks: record transactions, run reports, manage AR/AP and close the month.
- [DigiData](https://www.digi-data.nl/en/mcp) `https://mcp.digi-data.nl/mcp`
  [![DigiData MCP connector](https://glama.ai/mcp/connectors/nl.digi-data.mcp/digi-data/badges/score.svg)](https://glama.ai/mcp/connectors/nl.digi-data.mcp/digi-data)
  🔐 - Read-only business data from Exact Online, Twinfield, AFAS and 30+ sources: list, query and aggregate tables.
- [Eagle Virtual](https://eaglevirtual.com/mcp) `https://mcp.eaglevirtual.com/mcp`
  [![Eagle Virtual MCP connector](https://glama.ai/mcp/connectors/com.eaglevirtual/stablecoin-freeze-tracker/badges/score.svg)](https://glama.ai/mcp/connectors/com.eaglevirtual/stablecoin-freeze-tracker)
  🔓 - Check any wallet against the dated on-chain record of USDT and USDC blacklistings, freezes and seizures.
- [Edgrapi](https://edgrapi.com) `https://api.edgrapi.com/mcp`
  [![Edgrapi MCP connector](https://glama.ai/mcp/connectors/io.github.paperandbeyond23-gif/edgrapi-skills/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.paperandbeyond23-gif/edgrapi-skills)
  🔓 - SEC EDGAR filings as JSON: Form 4 insider trades, 8-K, 13F, 13D/G stakes, XBRL; data tools need a free key.
- [egrul.org](https://egrul.org) `https://egrul.org/mcp/`
  [![egrul.org MCP connector](https://glama.ai/mcp/connectors/org.egrul/egrulorg/badges/score.svg)](https://glama.ai/mcp/connectors/org.egrul/egrulorg)
  🔓 - Russian company/individual checks: EGRUL/EGRIP, sanctions, foreign-agent, bankruptcy; most tools need a subscription.
- [El Tablero](https://eltablero.ar/docs) `https://eltablero.ar/api/mcp`
  [![El Tablero MCP connector](https://glama.ai/mcp/connectors/ar.eltablero/el-tablero-argentina-economic-data/badges/score.svg)](https://glama.ai/mcp/connectors/ar.eltablero/el-tablero-argentina-economic-data)
  🔓 - Argentine economic data from BCRA and INDEC: FX, inflation, rates, reserves, projections and release calendar.
- [Factur-X by Orvel](https://facturx.orvel.dev/docs/mcp/) `https://facturx.orvel.dev/mcp`
  [![Factur-X by Orvel MCP connector](https://glama.ai/mcp/connectors/io.github.LeBorgneAntoine/facturx/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.LeBorgneAntoine/facturx)
  🔓 - Generate, validate and read Factur-X, CII and UBL invoices; free fixed demo, paid document processing.
- [Fast GST Refund](https://fastgstrefund.com/for-agents/) `https://fastgstrefund.com/mcp`
  [![Fast GST Refund MCP connector](https://glama.ai/mcp/connectors/com.fastgstrefund/fast-gst-refund/badges/score.svg)](https://glama.ai/mcp/connectors/com.fastgstrefund/fast-gst-refund)
  🔓 - Indian GST refund guidance, validation and Statement 3/Annexure B JSON; free checks, optional OAuth for downloads.
- [Fi-Plan](https://www.fi-plan.in) `https://www.fi-plan.in/mcp`
  [![Fi-Plan MCP connector](https://glama.ai/mcp/connectors/in.fi-plan/fi-plan/badges/score.svg)](https://glama.ai/mcp/connectors/in.fi-plan/fi-plan)
  🔓 - Financial simulator for Indian salaries: loans, taxes, SIPs, and 50-year FIRE plans.
- [Financial Evidence](https://beepboop2025.github.io/financial-evidence-skills/) `https://liquilens.in/mcp/financial-evidence`
  [![Financial Evidence MCP connector](https://glama.ai/mcp/connectors/io.github.beepboop2025/financial-evidence/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.beepboop2025/financial-evidence)
  🔓 - Route and retrieve cited funding, bank-risk and market-liquidity evidence, preserving source dates and missingness.
- [FinancialFilings](https://financialfilings.com/mcp/) `https://mcp.financialfilings.com/mcp`
  [![FinancialFilings MCP connector](https://glama.ai/mcp/connectors/eu.financialreports/mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/eu.financialreports/mcp-server)
  🔐 - Regulatory filings, XBRL financials and company data from securities regulators in about 60 markets.
- [FlexYield](https://flexyield.io) `https://flexyield.io/mcp`
  [![FlexYield MCP connector](https://glama.ai/mcp/connectors/io.flexyield/flex-yield-blockchain-rpc-gateway/badges/score.svg)](https://glama.ai/mcp/connectors/io.flexyield/flex-yield-blockchain-rpc-gateway)
  🔓 - RPC gateway for six mainnets with failover: balances, history, ABIs, gas and transactions; x402 pay-per-call.
- [Floatout](https://floatout.xyz) `https://floatout.xyz/api/mcp`
  [![Floatout MCP connector](https://glama.ai/mcp/connectors/xyz.floatout/floatout/badges/score.svg)](https://glama.ai/mcp/connectors/xyz.floatout/floatout)
  🔓 - Read Floatout launch plans, guides, and Hyperliquid builder-fee research.
- [FocusPulse](https://www.focuspulse.pro/mcp-docs.html) `https://mcp.focuspulse.pro/mcp`
  [![FocusPulse MCP connector](https://glama.ai/mcp/connectors/pro.focuspulse/focuspulse/badges/score.svg)](https://glama.ai/mcp/connectors/pro.focuspulse/focuspulse)
  🔓 - India and US news stories linked to listed companies, commodities and indices, with sources.
- [Foresee](https://go-foresee.com) `https://agents.go-foresee.com/mcp`
  [![Foresee MCP connector](https://glama.ai/mcp/connectors/io.github.Foresee-Tech/foresee/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Foresee-Tech/foresee)
  🔓 - Compare live home and auto insurance quotes from carriers' own sites.
- [Fruit Stand](https://fruitstand.dev) `https://api.fruitstand.dev/mcp`
  [![Fruit Stand MCP connector](https://glama.ai/mcp/connectors/dev.fruitstand/fund-returns/badges/score.svg)](https://glama.ai/mcp/connectors/dev.fruitstand/fund-returns)
  🔓 - Historical return data for funds and tickers.
- [Global FinReg](https://www.globalfinreg.com) `https://api2.globalfinreg.com/mcp`
  [![Global FinReg MCP connector](https://glama.ai/mcp/connectors/com.globalfinreg/lei/badges/score.svg)](https://glama.ai/mcp/connectors/com.globalfinreg/lei)
  🔓 - Look up LEIs in the global LEI register; renew, transfer and register LEIs with a Global FinReg account.
- [Gloom](https://gloom.sh/docs/mcp) `https://api.gloom.sh/mcp`
  [![Gloom MCP connector](https://glama.ai/mcp/connectors/sh.gloom.api/gloom-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/sh.gloom.api/gloom-mcp)
  🔐 - US stock research: real-time quotes, financials, options flow, SEC filings, 13F, macro and news; tools need a paid plan.
- [GrantIQ](https://mcp.grantiq.us) `https://mcp.grantiq.us/mcp/`
  [![GrantIQ MCP connector](https://glama.ai/mcp/connectors/io.github.bch1212/mcp-grantiq/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.bch1212/mcp-grantiq)
  🔓 - Search Grants.gov opportunities, SAM.gov contracts, agencies, deadlines, matches, and federal award history.
- [GROUNDTRUTH](https://groundtruths.xyz) `https://api.groundtruths.xyz/mcp`
  [![GROUNDTRUTH MCP connector](https://glama.ai/mcp/connectors/xyz.groundtruths/groundtruth/badges/score.svg)](https://glama.ai/mcp/connectors/xyz.groundtruths/groundtruth)
  🔓 - Pump.fun and Robinhood Chain memecoin outcomes and creator records; 5 free calls a day, then x402.
- [HEY Research Lab](https://heyresearch.xyz/developers/agents) `https://heyresearch.xyz/mcp`
  [![HEY Research Lab MCP connector](https://glama.ai/mcp/connectors/io.github.hey-research-lab/hey-research/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.hey-research-lab/hey-research)
  🔓 - Builder research for Robinhood Chain: which projects are still building and what they shipped, each with its source.
- [HKEx Filings](https://hkex-listco-updates.ascent-partners.com/live-mcp/) `https://hkex-listco-updates.ascent-partners.com/api/mcp`
  [![HKEx Filings MCP connector](https://glama.ai/mcp/connectors/io.github.simonplmak-cloud/hkex-filings/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.simonplmak-cloud/hkex-filings)
  🔓 - Search 25+ years of Hong Kong Stock Exchange filings, browse facets and extract document text; read-only.
- [Hundo](https://hundo.finance/connect) `https://hundo.finance/mcp`
  [![Hundo MCP connector](https://glama.ai/mcp/connectors/finance.hundo/hundo/badges/score.svg)](https://glama.ai/mcp/connectors/finance.hundo/hundo)
  🔐 - Personal ledger: net worth, accounts, budgets and IOUs, with drafts you confirm; needs a paid plan.
- [Intangible Asset Valuation](https://intangible-valuation.simonmak.com) `https://intangible-valuation.simonmak.com/api/mcp`
  [![Intangible Asset Valuation MCP connector](https://glama.ai/mcp/connectors/io.github.simonplmak-cloud/intangible-valuation/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.simonplmak-cloud/intangible-valuation)
  🔓 - 124+ deterministic formulas for IP, relief from royalty, MPEEM, purchase price allocation and impairment.
- [Invompt](https://www.invompt.com) `https://mcp.invompt.com/mcp`
  [![Invompt MCP connector](https://glama.ai/mcp/connectors/com.invompt/invompt/badges/score.svg)](https://glama.ai/mcp/connectors/com.invompt/invompt)
  🔐 - Create invoices and review them before sending.
- [ISO 20022 Navigator](https://www.isonavigator.io/iso20022/mcp) `https://mcp.isonavigator.io/iso20022`
  [![ISO 20022 Navigator MCP connector](https://glama.ai/mcp/connectors/io.github.kreativeManish/iso20022-navigator/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.kreativeManish/iso20022-navigator)
  🔓 - Look up ISO 20022 messages, bank transaction codes, legacy replacements like MT103, scheme use, and external code sets.
- [Jithox](https://jithox.com) `https://jithox.com/api/mcp`
  [![Jithox MCP connector](https://glama.ai/mcp/connectors/com.jithox/jithox/badges/score.svg)](https://glama.ai/mcp/connectors/com.jithox/jithox)
  🔓 - Check an invoice payment before an agent pays: IBAN, supplier bank change and Peppol; five tools need no account.
- [Jithox E-Invoice](https://jithox.com/mcp/einvoice) `https://mcp.jithox.com/mcp`
  [![Jithox E-Invoice MCP connector](https://glama.ai/mcp/connectors/com.jithox/einvoice-readiness/badges/score.svg)](https://glama.ai/mcp/connectors/com.jithox/einvoice-readiness)
  🔓 - Read-only EU e-invoice checks: invoice structure, VAT format, VIES and Peppol lookup; tools need OAuth.
- [Kairos Signal](https://kairossignal.com) `https://kairossignal.com/mcp`
  [![Kairos Signal MCP connector](https://glama.ai/mcp/connectors/com.kairossignal/kairos-signal-63-layer-symplectic-neural-ode/badges/score.svg)](https://glama.ai/mcp/connectors/com.kairossignal/kairos-signal-63-layer-symplectic-neural-ode)
  🔓 - Query DePIN supply telemetry and network data with source, observation time, and verification links.
- [Kema Invoice](https://invoice.kema-studio.com) `https://mcp.kema-studio.com/api/mcp`
  [![Kema Invoice MCP connector](https://glama.ai/mcp/connectors/com.kema-studio/invoice/badges/score.svg)](https://glama.ai/mcp/connectors/com.kema-studio/invoice)
  🔐 - Compliant French e-invoicing for freelancers: create, issue, certify and track invoices, quotes and deposits.
- [Knoww](https://knoww.app) `https://mcp.knoww.app/mcp`
  [![Knoww MCP connector](https://glama.ai/mcp/connectors/app.knoww.mcp/knoww/badges/score.svg)](https://glama.ai/mcp/connectors/app.knoww.mcp/knoww)
  🔐 - Read-only Polymarket search, market details, order books, price history, and interactive market cards.
- [Kristo Intelligence](https://kristo-intelligence-api.onrender.com) `https://kristo-intelligence-api.onrender.com/mcp`
  🔓 - DeFi trading signals and market intelligence on Base; x402 pay-per-call in USDC.
- [Kunkafa](https://kunkafa.com) `https://kunkafa.com/mcp`
  [![Kunkafa MCP connector](https://glama.ai/mcp/connectors/com.kunkafa/kunkafa/badges/score.svg)](https://glama.ai/mcp/connectors/com.kunkafa/kunkafa)
  🔓 - Market forecasts for stocks, crypto, gold, oil and FX with Kunkafa's confidence and track record; data needs OAuth.
- [Kyrodata](https://kyrodata.com) `https://mcp.kyrodata.com/mcp`
  [![Kyrodata MCP connector](https://glama.ai/mcp/connectors/com.kyrodata/kyrodata/badges/score.svg)](https://glama.ai/mcp/connectors/com.kyrodata/kyrodata)
  🔐 - Brazilian exports and imports by HS code and partner, plus crop production, climate and commodity forecasts.
- [Layerz](https://layerz.cc/for-agents) `https://layerz.cc/mcp`
  [![Layerz MCP connector](https://glama.ai/mcp/connectors/cc.layerz.app/layerz/badges/score.svg)](https://glama.ai/mcp/connectors/cc.layerz.app/layerz)
  🔐 - Build, version and audit structured financial models from your agent, and export them to Excel.
- [LimitGuard](https://limitguard.ai) `https://api.limitguard.ai/mcp`
  [![LimitGuard MCP connector](https://glama.ai/mcp/connectors/ai.limitguard.api/trust-intelligence/badges/score.svg)](https://glama.ai/mcp/connectors/ai.limitguard.api/trust-intelligence)
  🔓 - Verify Dutch and Belgian companies (KVK, KBO), EU VAT, sanctions and PEPs, with a risk score; key or x402.
- [LiquidVision](https://liquidvision.app) `https://liquidvision.app/mcp`
  [![LiquidVision MCP connector](https://glama.ai/mcp/connectors/app.liquidvision/derivatives/badges/score.svg)](https://glama.ai/mcp/connectors/app.liquidvision/derivatives)
  🔓 - Crypto derivatives across 13 venues: open interest, funding, liquidations, Hyperliquid whale positions.
- [LitVM TCG Oracle](https://litvm.the-undesirables.com) `https://litvm.the-undesirables.com/mcp`
  [![LitVM TCG Oracle MCP connector](https://glama.ai/mcp/connectors/com.the-undesirables.litvm/lit-vm-tcg-oracle/badges/score.svg)](https://glama.ai/mcp/connectors/com.the-undesirables.litvm/lit-vm-tcg-oracle)
  🔓 - TCG price oracle for LitecoinVM: Merkle-proven prices, calibrated forecasts and fantasy souls; 13 free tools.
- [Loophole Tape](https://api.loopholetape.com) `https://api.loopholetape.com/mcp`
  [![Loophole Tape MCP connector](https://glama.ai/mcp/connectors/io.github.gosadu/loophole-tape/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.gosadu/loophole-tape)
  🔓 - pump.fun launch-risk checks and Robinhood Chain launch data; free tools, paid ones settle per call via x402.
- [LoomDesk](https://loomdesk.trade) `https://loomdesk.trade/mcp`
  [![LoomDesk MCP connector](https://glama.ai/mcp/connectors/trade.loomdesk/loomdesk/badges/score.svg)](https://glama.ai/mcp/connectors/trade.loomdesk/loomdesk)
  🔓 - Plan Uniswap liquidity on Robinhood Chain as unsigned transactions, or trade play money in an agent arena, free key.
- [MarketMaster](https://marketmaster.live/developers) `https://api.marketmaster.live/mcp`
  [![MarketMaster MCP connector](https://glama.ai/mcp/connectors/live.marketmaster/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/live.marketmaster/mcp)
  🔓 - Kalshi and Polymarket data: cross-venue matching, arbitrage after fees and whale trades; free key.
- [MetricDuck](https://www.metricduck.com) `https://mcp.metricduck.com/mcp`
  [![MetricDuck MCP connector](https://glama.ai/mcp/connectors/com.metricduck/financial-analysis/badges/score.svg)](https://glama.ai/mcp/connectors/com.metricduck/financial-analysis)
  🔓 - SEC filing data for AI agents: financials, screening, every figure traceable; tool calls need a free sign-in.
- [Midpoint Card Prices](https://www.cardcenteringtool.com/mcp) `https://mcp.cardcenteringtool.com/mcp`
  [![Midpoint Card Prices MCP connector](https://glama.ai/mcp/connectors/com.cardcenteringtool/card-prices/badges/score.svg)](https://glama.ai/mcp/connectors/com.cardcenteringtool/card-prices)
  🔓 - Trading card prices and grading ROI for 1.5M+ Pokémon, TCG and sports cards: raw and PSA 9/10 values, movers.
- [MORVS](https://morvs.ai/api/mcp/) `https://api.morvs.ai/mcp`
  [![MORVS MCP connector](https://glama.ai/mcp/connectors/io.github.morvs-ai/morvs/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.morvs-ai/morvs)
  🔓 - Source-linked US public records: SEC filings, FDA recalls, federal enforcement, sanctions and debarment indexes.
- [NuMetric](https://numetric.work) `https://numetric-mcp.virifi.xyz/mcp`
  [![NuMetric MCP connector](https://glama.ai/mcp/connectors/xyz.virifi.numetric-mcp/numetric/badges/score.svg)](https://glama.ai/mcp/connectors/xyz.virifi.numetric-mcp/numetric)
  🔐 - Read-only NuMetric accounting and ERP data: statements, KPIs, receivables, payables, invoices and documents.
- [Octagon](https://octagonagents.com) `https://mcp.octagonagents.com/mcp`
  [![Octagon MCP connector](https://glama.ai/mcp/connectors/com.octagonagents.mcp/octagon/badges/score.svg)](https://glama.ai/mcp/connectors/com.octagonagents.mcp/octagon)
  🔐 - Private- and public-market financial research data.
- [Open Economics](https://open-economics-data.knbf982hkn.chatgpt.site/en/mcp) `https://open-economics-data.knbf982hkn.chatgpt.site/api/mcp`
  [![Open Economics MCP connector](https://glama.ai/mcp/connectors/io.github.felipegambettadesouza6-jpg/open-economics/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.felipegambettadesouza6-jpg/open-economics)
  🔓 - Find and query official Brazilian economic data with provenance.
- [OpenChainBench](https://openchainbench.com) `https://openchainbench.com/api/mcp/mcp`
  [![OpenChainBench MCP connector](https://glama.ai/mcp/connectors/io.github.Flotapponnier/openchainbench/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Flotapponnier/openchainbench)
  🔓 - Live crypto infra benchmarks: RPC latency, bridge fees, aggregator head lag, perp funding, with PromQL access.
- [OptionsAhoy](https://optionsahoy.com/for-agents) `https://optionsahoy.com/mcp`
  [![OptionsAhoy MCP connector](https://glama.ai/mcp/connectors/io.github.AlvisoOculus/optionsahoy-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.AlvisoOculus/optionsahoy-mcp)
  🔓 - US equity-comp tax math: ISO/AMT exercise plans, RSU and NSO sell-or-hold, QSBS, hedges, cash-goal sell plans.
- [Oxaide](https://oxaide.com/agents) `https://oxaide.com/mcp`
  [![Oxaide MCP connector](https://glama.ai/mcp/connectors/io.github.leewenjie/oxaide/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.leewenjie/oxaide)
  🔓 - Cited Singapore company research (ACRA/URA/GeBIZ) at S$49/390/1500 per job.
- [pdata](https://pdata.world/agents) `https://api.pdata.world/mcp`
  [![pdata MCP connector](https://glama.ai/mcp/connectors/world.pdata/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/world.pdata/mcp)
  🔓 - Prices, 24h volume, movers and results for prediction markets on Polymarket, Kalshi and six more venues.
- [Plaid](https://plaid.com) `https://api.dashboard.plaid.com/mcp/sse`
  🔑 - Query Plaid dashboard data for connected financial accounts.
- [Polish Company Financials (Compabase)](https://compabase.com/docs/mcp/) `https://compabase.com/api/mcp/financials`
  [![Polish Company Financials (Compabase) MCP connector](https://glama.ai/mcp/connectors/io.github.ContentWriterco/polish-company-financials/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ContentWriterco/polish-company-financials)
  🔓 - Financial statements of Polish companies (KRS): revenue, profit, assets, industry rankings and sector benchmarks.
- [Priors](https://priors.trade) `https://mcp.priors.trade/mcp`
  [![Priors MCP connector](https://glama.ai/mcp/connectors/io.github.priors-agents/priors-read/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.priors-agents/priors-read)
  🔓 - Credit records and scores of ERC-8004 AI agents on Robinhood Chain, with pool figures and recent loans.
- [PumpPill](https://www.pumppill.org/for-agents) `https://api.pumppill.org/mcp`
  [![PumpPill MCP connector](https://glama.ai/mcp/connectors/org.pumppill/token-safety/badges/score.svg)](https://glama.ai/mcp/connectors/org.pumppill/token-safety)
  🔓 - Token safety reads, deployer history and measured outcomes for Robinhood Chain and Solana contracts.
- [Qotien](https://qotien.fr) `https://app.qotien.fr/api/fiscal/v1/mcp`
  [![Qotien MCP connector](https://glama.ai/mcp/connectors/io.github.herve-coulon/tax-retirement/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.herve-coulon/tax-retirement)
  🔓 - French income tax, IFI, PER and 32 pension schemes, sourced to primary law and dated; x402 pay-per-call.
- [Quantral](https://quantral.com/mcp) `https://app.quantral.com/api/mcp`
  [![Quantral MCP connector](https://glama.ai/mcp/connectors/com.quantral/sentiment/badges/score.svg)](https://glama.ai/mcp/connectors/com.quantral/sentiment)
  🔐 - Per-stock sentiment scores, top signals, monthly recaps and the underlying mentions.
- [Quidli Connect](https://connect.quid.li) `https://mcp.connect.quid.li`
  🔓 - Resolve social handles to EVM and Solana wallets, score onchain reputation and send USDC.
- [Radicado Uno](https://radicadouno.co/mcp) `https://mcp.radicadouno.co/mcp`
  [![Radicado Uno MCP connector](https://glama.ai/mcp/connectors/co.radicadouno/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/co.radicadouno/mcp)
  🔓 - Colombian company and procurement data by NIT (registry, contracts, sanctions). Free lookup; data tools need a key.
- [Rechnungslotse](https://rechnungslotse.de/mcp) `https://rechnungslotse.de/api/mcp`
  [![Rechnungslotse MCP connector](https://glama.ai/mcp/connectors/de.rechnungslotse/e-rechnung/badges/score.svg)](https://glama.ai/mcp/connectors/de.rechnungslotse/e-rechnung)
  🔓 - German e-invoicing: create, validate and read XRechnung and ZUGFeRD invoices against EN 16931.
- [Regime](https://regimetoken.xyz/api) `https://feed.regimetoken.xyz/mcp`

  
  [![Regime MCP connector](https://glama.ai/mcp/connectors/xyz.regimetoken/regime/badges/score.svg)](https://glama.ai/mcp/connectors/xyz.regimetoken/regime)
  🔓 - Checks crypto trading claims on real price history: leverage liquidations, drawdown, DCA, stop-loss, seasonality.
- [RevExOS](https://revexos.com/mcp) `https://revexos.com/api/mcp`
  [![RevExOS MCP connector](https://glama.ai/mcp/connectors/com.revexos/revexos/badges/score.svg)](https://glama.ai/mcp/connectors/com.revexos/revexos)
  🔓 - Quote-to-cash tools: parse invoices and POs, 3-way match, proration, revenue schedules, dunning emails.

- [RWA Data MCP Server](https://glama.ai/mcp/connectors/io.github.daveabear/rwa-data-mcp) `https://rwa-data-mcp.dave-a-bear.workers.dev/mcp`
  [![RWA Data MCP Server MCP connector](https://glama.ai/mcp/connectors/io.github.daveabear/rwa-data-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.daveabear/rwa-data-mcp)
    🔓 - Stablecoin & RWA market data for AI agents: metrics, peg monitoring, prices, claim verification; x402 USDC pay-per-call.



- [Rychlá Hypo](https://rychlahypo.cz/api-dokumentace) `https://rychlahypo.cz/mcp`
  [![Rychlá Hypo MCP connector](https://glama.ai/mcp/connectors/cz.rychlahypo/mortgages/badges/score.svg)](https://glama.ai/mcp/connectors/cz.rychlahypo/mortgages)
  🔓 - Czech mortgages: rates with APRC for 6 major banks, payment comparison and max loan per bank from income.
- [Sector Pulse](https://sector-pulse.app) `https://sector-pulse.app/api/mcp`
  [![Sector Pulse MCP connector](https://glama.ai/mcp/connectors/io.github.christianhonap7-sys/sector-pulse/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.christianhonap7-sys/sector-pulse)
  🔓 - US sector rotation: 30 sector baskets ranked each session, with a daily record; history needs a key.
- [Sentio Connect](https://connect.sentio.xyz) `https://connect.sentio.xyz/v1/mcp`
  [![Sentio Connect MCP connector](https://glama.ai/mcp/connectors/xyz.sentio/connect/badges/score.svg)](https://glama.ai/mcp/connectors/xyz.sentio/connect)
  🔐 - Wallet balances, token prices, portfolio value, DeFi positions and holding history across EVM chains and Sui.
- [Shingou](https://shingou.io) `https://api.shingou.io/mcp`
  [![Shingou MCP connector](https://glama.ai/mcp/connectors/io.shingou/sentiment/badges/score.svg)](https://glama.ai/mcp/connectors/io.shingou/sentiment)
  🔓 - Hourly news sentiment and market events for 30 crypto pairs, with source links and hashed history; free key.
- [Shumi](https://shumi.ai) `https://mcp.shumi.ai/mcp`
  [![Shumi MCP connector](https://glama.ai/mcp/connectors/ai.shumi/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/ai.shumi/mcp)
  🔓 - Crypto prices, trends, funding rates, sentiment, narratives, market regime and pair ideas; free key.
- [Signed](https://mcp.signed.com) `https://mcp.signed.com`
  [![Signed MCP connector](https://glama.ai/mcp/connectors/com.signed.mcp/signed/badges/score.svg)](https://glama.ai/mcp/connectors/com.signed.mcp/signed)
  🔐 - An angel investor's portfolio, deal pipeline, and contacts: positions, returns, pitches, notes, and transactions.
- [Signed Investors](https://mcp.signed.com/investors) `https://mcp.signed.com/investors`
  [![Signed Investors MCP connector](https://glama.ai/mcp/connectors/com.signed.mcp/signed-investors/badges/score.svg)](https://glama.ai/mcp/connectors/com.signed.mcp/signed-investors)
  🔓 - Search a public directory of angel investors by sector, check size, or keyword, with no account needed.
- [Silicon Floor](https://siliconfloor.com/docs/mcp) `https://siliconfloor.com/mcp`
  [![Silicon Floor MCP connector](https://glama.ai/mcp/connectors/com.siliconfloor/silicon-floor/badges/score.svg)](https://glama.ai/mcp/connectors/com.siliconfloor/silicon-floor)
  🔓 - Follow the smart money in AI stocks: who owns what, what insiders and hedge funds buy and sell, straight from the SEC.
- [SNACS](https://snacs.trade/api) `https://mcp.snacs.trade`
  [![SNACS MCP connector](https://glama.ai/mcp/connectors/trade.snacs.mcp/snacstrade/badges/score.svg)](https://glama.ai/mcp/connectors/trade.snacs.mcp/snacstrade)
  🔐 - Point-in-time SEC filings, dilution forensics, market data and fundamentals for US equities.
- [SnowSignals TrendVane](https://snowsignals.io) `https://snowsignals.io/mcp`
  [![SnowSignals TrendVane MCP connector](https://glama.ai/mcp/connectors/io.snowsignals/snowsignals/badges/score.svg)](https://glama.ai/mcp/connectors/io.snowsignals/snowsignals)
  🔓 - Market-phase state per currency across timeframes (not trade signals); free phase stats, metered live reads.
- [Stablecoin Scanner](https://stablescan.achivx.com) `https://stablescan.achivx.com/mcp`
  [![Stablecoin Scanner MCP connector](https://glama.ai/mcp/connectors/com.achivx/stablescan/badges/score.svg)](https://glama.ai/mcp/connectors/com.achivx/stablescan)
  🔓 - Stablecoin compliance on 7 chains: issuer freezes, OFAC, exposure and risk, allowances, transfers, wallet graph.
- [StackEasy](https://www.stackeasy.ai/mcp) `https://data.stackeasy.ai/mcp`
  [![StackEasy MCP connector](https://glama.ai/mcp/connectors/ai.stackeasy/credit-cards/badges/score.svg)](https://glama.ai/mcp/connectors/ai.stackeasy/credit-cards)
  🔐 - Read-only view of your credit cards: balances, utilization, best card for a purchase and missed rewards.
- [StartupPerks](https://startupperks.co/mcp-server) `https://startupperks.co/mcp`
  [![StartupPerks MCP connector](https://glama.ai/mcp/connectors/co.startupperks/startup-perks/badges/score.svg)](https://glama.ai/mcp/connectors/co.startupperks/startup-perks)
  🔓 - Rank the startup credits, perks and deals a company qualifies for across 1,000+ programs, each with sourced terms.
- [StockPortfolio.pro](https://www.stockportfolio.pro/api) `https://www.stockportfolio.pro/mcp`
  [![StockPortfolio.pro MCP connector](https://glama.ai/mcp/connectors/pro.stockportfolio/stock-portfoliopro/badges/score.svg)](https://glama.ai/mcp/connectors/pro.stockportfolio/stock-portfoliopro)
  🔓 - Limited keyless US stock research: SEC financials, filings, comparisons, screens, fund profiles and sourced answers.
- [Stocks On Chain](https://stocksonchain.io) `https://stocksonchain.io/mcp`
  [![Stocks On Chain MCP connector](https://glama.ai/mcp/connectors/io.stocksonchain/stocks-on-chain/badges/score.svg)](https://glama.ai/mcp/connectors/io.stocksonchain/stocks-on-chain)
  🔓 - Tokenized listed stocks by chain and issuer, with contract addresses and on-chain corporate actions.
- [Stoxly](https://www.stoxlyonline.com/mcp) `https://www.stoxlyonline.com/api/mcp`
  [![Stoxly MCP connector](https://glama.ai/mcp/connectors/io.github.wizard-exe/stoxly/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.wizard-exe/stoxly)
  🔓 - Free stock and ETF fundamental analysis: 10-criteria score, verdict, and key metrics for any ticker.
- [SwapWallet](https://swapwallet.app/docs/mcp) `https://swapwallet.app/mcp`
  [![SwapWallet MCP connector](https://glama.ai/mcp/connectors/app.swapwallet/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/app.swapwallet/mcp)
  🔐 - Read balances, P&L and history; request swaps, transfers and withdrawals that the user approves in Telegram.
- [Synci](https://synci.io) `https://api.synci.io/mcp`
  [![Synci MCP connector](https://glama.ai/mcp/connectors/io.synci/synci/badges/score.svg)](https://glama.ai/mcp/connectors/io.synci/synci)
  🔐 - Read-only bank, brokerage and crypto accounts: balances, transactions, holdings and connection health.
- [Taiwan Market Open Data (Unofficial)](https://twse-mcp.taux.io/) `https://twse-mcp.taux.io/mcp`
  [![Taiwan Market Open Data MCP connector](https://glama.ai/mcp/connectors/io.github.taux-io/twse-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.taux-io/twse-mcp)
  🔓 - Unofficial access to Taiwan Stock Exchange and Futures Exchange open data: stock, ETF and futures snapshots, live quotes and 275 datasets.
- [Tapetide](https://tapetide.com/mcp) `https://mcp.tapetide.com/mcp`
  [![Tapetide MCP connector](https://glama.ai/mcp/connectors/com.tapetide/stock-research-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.tapetide/stock-research-mcp)
  🔐 - Indian stock market research: NSE and BSE quotes, financials, 326-ratio screener, FII/DII flows, options and filings.
- [Tessera Analytics](https://tesseralytics.dev/mcp-server) `https://tesseralytics.dev/mcp`
  [![Tessera Analytics MCP connector](https://glama.ai/mcp/connectors/dev.tesseralytics/hyperliquid-data/badges/score.svg)](https://glama.ai/mcp/connectors/dev.tesseralytics/hyperliquid-data)
  🔓 - Daily Hyperliquid perp funding, positioning and crowding across every market; tools need a free key.
- [The River](https://theriver.markets/agents) `https://theriver.markets/mcp`
  [![The River MCP connector](https://glama.ai/mcp/connectors/markets.theriver/the-river/badges/score.svg)](https://glama.ai/mcp/connectors/markets.theriver/the-river)
  🔓 - Tokenized US stocks onchain: issuers, onchain vs US prices, holdings, pre-filled trade links a person signs.
- [The Undesirables TCG Oracle](https://the-undesirables.com) `https://mcp.the-undesirables.com/mcp`
  [![The Undesirables TCG Oracle MCP connector](https://glama.ai/mcp/connectors/io.github.sailorpepe/undesirables-mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.sailorpepe/undesirables-mcp-server)
  🔓 - On-chain oracle for 456K+ trading cards: prices, forecasts, AI grading; free reads, paid via x402.
- [Tickerz](https://tickerz.com/connect) `https://tickerz.com/mcp`
  [![Tickerz MCP connector](https://glama.ai/mcp/connectors/com.tickerz/tickerz/badges/score.svg)](https://glama.ai/mcp/connectors/com.tickerz/tickerz)
  🔓 - Daily indexes of memecoin launches, Kalshi and Polymarket volume and x402 payments, on-chain in Bitcoin.
- [TraderSpy](https://traderspy.app/mcp) `https://mcp.traderspy.app/mcp`
  [![TraderSpy MCP connector](https://glama.ai/mcp/connectors/app.traderspy/traderspy/badges/score.svg)](https://glama.ai/mcp/connectors/app.traderspy/traderspy)
  🔓 - Crypto futures signals, whale positions on four exchanges, indicators and a screener; free key.
- [TradeStar Insider](https://www.tradestarinsider.com) `https://mcp.tradestarinsider.com/mcp`
  [![TradeStar Insider MCP connector](https://glama.ai/mcp/connectors/com.tradestarinsider/edgar-insider-signals/badges/score.svg)](https://glama.ai/mcp/connectors/com.tradestarinsider/edgar-insider-signals)
  🔓 - Verify insider-buy, 13D and 13F claims against SEC filings; every record links to its sec.gov source.
- [TradingCalc](https://tradingcalc.io) `https://tradingcalc.io/api/mcp`
  [![TradingCalc MCP connector](https://glama.ai/mcp/connectors/io.github.SKalinin909/tradingcalc/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.SKalinin909/tradingcalc)
  🔓 - Deterministic crypto futures, on-chain risk, and prediction-market math — 31 tools, not AI estimates.
- [TroyStack](https://troystack.com) `https://api.troystack.ai/mcp`
  [![TroyStack MCP connector](https://glama.ai/mcp/connectors/io.github.kingleosgold/troystack/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.kingleosgold/troystack)
  🔓 - Live gold, silver, platinum and palladium prices, COMEX vault inventory and a daily brief; portfolio tools need a key.
- [Trust Check](https://trust-check.gm-tools.workers.dev) `https://trust-check.gm-tools.workers.dev/mcp`
  [![Trust Check MCP connector](https://glama.ai/mcp/connectors/io.github.gmahar82-stack/trust-check/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.gmahar82-stack/trust-check)
  🔓 - Safety check for a Base token or address before you trade or pay it; USDC per call via x402.
- [USDi](https://www.usdicoin.com/) `https://usdi-mcp.onrender.com/mcp`
  [![USDi MCP connector](https://glama.ai/mcp/connectors/io.github.MikeAshtonEILLC/usdi-mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.MikeAshtonEILLC/usdi-mcp-server)
  🔓 - CPI-indexed cryptocurrency: live exchange rate, contract/pool addresses, and mint/redeem mechanics.
- [Vantage](https://vantagemcp.dev) `https://vantagemcp.dev/mcp`
  [![Vantage MCP connector](https://glama.ai/mcp/connectors/dev.vantagemcp/vantage/badges/score.svg)](https://glama.ai/mcp/connectors/dev.vantagemcp/vantage)
  🔐 - Ask questions about cloud cost and usage data.
- [Vérif Entreprise FR](https://api-production-24833.up.railway.app) `https://api-production-24833.up.railway.app/mcp`
  [![Vérif Entreprise FR MCP connector](https://glama.ai/mcp/connectors/app.railway.up.api-production-24833/verif-entreprise-fr/badges/score.svg)](https://glama.ai/mcp/connectors/app.railway.up.api-production-24833/verif-entreprise-fr)
  🔓 - Verify French companies by SIREN: legal status, BODACC insolvency proceedings and RGE certifications, paid via x402.
- [VetAgent](https://vetagent.dev) `https://vetagent.dev/mcp`
  [![VetAgent MCP connector](https://glama.ai/mcp/connectors/dev.vetagent/vetagent/badges/score.svg)](https://glama.ai/mcp/connectors/dev.vetagent/vetagent)
  🔓 - Pre-trade crypto token risk check: sell simulation, taxes, liquidity depth and pair age.
- [XFINLAB Intelligence](https://www.xfinlab.com/intelligence-api.html) `https://api.xfinlab.com/api/mcp`
  [![XFINLAB Intelligence MCP connector](https://glama.ai/mcp/connectors/io.github.lnanology/xfinlab/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.lnanology/xfinlab)
   🔓 - Market events, FinBERT sentiment, technical analysis, and AI news intelligence feeds; tools need a free API key.
- [xupersplit](https://split.xuper.fun) `https://split.xuper.fun/api/mcp`
  [![xupersplit MCP connector](https://glama.ai/mcp/connectors/io.github.kanylbullen/xupersplit/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.kanylbullen/xupersplit)
  🔓 - Split group expenses with no account: create a split, record who paid, see who owes whom and settle up.
- [Finology Software](https://finology.tech/developers/) `https://mcp.finology.tech/mcp`
  🔑 - US federal student loan payments, forgiveness timing and tax, cited to primary sources.
- [invowerk](https://invowerk.dev) `https://api.invowerk.dev/mcp/`
  [![invowerk MCP connector](https://glama.ai/mcp/connectors/dev.invowerk/invowerk/badges/score.svg)](https://glama.ai/mcp/connectors/dev.invowerk/invowerk)
  🔓 - Validate e-invoices: ZUGFeRD, Factur-X, XRechnung and Peppol BIS, with a detailed validation report.
- [skanfirmy](https://skanfirmy.pl) `https://skanfirmy.pl/mcp`
  [![skanfirmy MCP connector](https://glama.ai/mcp/connectors/io.github.bartosz-kuc/skanfirmy/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.bartosz-kuc/skanfirmy)
  🔓 - Verify Polish companies by NIP, KRS or REGON, plus the VAT white list and EU VAT via VIES.
- [VoxOdds](https://voxodds.com) `https://voxodds.com/mcp`
  [![VoxOdds MCP connector](https://glama.ai/mcp/connectors/com.voxodds/voxodds/badges/score.svg)](https://glama.ai/mcp/connectors/com.voxodds/voxodds)
  🔓 - Live Polymarket and Kalshi odds, executable quotes with fees, and pre-bet EV checks.
- [Vurto Swap](https://swap.vurto.cc) `https://swap.vurto.cc/mcp`
  [![Vurto Swap MCP connector](https://glama.ai/mcp/connectors/io.github.cryptoconspiracy/vurto-swap/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.cryptoconspiracy/vurto-swap)
  🔓 - Token swaps on 9 EVM chains and Solana ranked by net received; returns unsigned transactions.

- [WattCoin](https://wattcoin.org) `https://wattcoin-mcp-server.wattcoin.workers.dev/mcp`
  [![WattCoin MCP connector](https://glama.ai/mcp/connectors/io.github.WattCoin-Org/wattcoin-mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.WattCoin-Org/wattcoin-mcp-server)
  🔓 - Agent task marketplace on Solana: register with no wallet, claim and submit tasks, earn WATT, build merit.

- [X1 Wealth](https://x1wealth.com) `https://mcp.x1wealth.com/mcp`
  [![X1 Wealth MCP connector](https://glama.ai/mcp/connectors/com.x1wealth/x1/badges/score.svg)](https://glama.ai/mcp/connectors/com.x1wealth/x1)
  🔐 - Ask about your trusts, entities, policies and documents. Every answer cites a page or declines.

- [x402-agent-data](https://x402-agent.majighufron.workers.dev) `https://x402-agent.majighufron.workers.dev/mcp`
  [![x402-agent-data MCP connector](https://glama.ai/mcp/connectors/io.github.AjiGhufron9999/x402-agent-data/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.AjiGhufron9999/x402-agent-data)
  🔓 - On-chain data: ERC-20 reports, contract DD, pool depth and wallet activity; USDC per call via x402.

### 🍽️ <a name="food--dining"></a>Food & Dining

- [Agent Chef](https://agentchef.net) `https://agentchef.net/mcp`
  [![Agent Chef MCP connector](https://glama.ai/mcp/connectors/net.agentchef/agent-chef/badges/score.svg)](https://glama.ai/mcp/connectors/net.agentchef/agent-chef)
  🔐 - Weekly family dinner ballot: propose recipes, the household votes, and get a grocery list.
- [Cork & Curve](https://corkandcurve.com/agents/) `https://corkandcurve.com/mcp`
  [![Cork & Curve MCP connector](https://glama.ai/mcp/connectors/com.corkandcurve/wine-travel/badges/score.svg)](https://glama.ai/mcp/connectors/com.corkandcurve/wine-travel)
  🔓 - Vineyards, tasting rooms and wine bars in 37 European wine regions, plus festivals and tours.
- [DrinkedIn](https://drinkedin.net) `https://ai.drinkedin.net/mcp`
  [![DrinkedIn MCP connector](https://glama.ai/mcp/connectors/io.github.haim-barad/drinkedin/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.haim-barad/drinkedin)
  🔓 - Fictional bar for AI agents: venues, drinks, chat, real-bar lookup, and licensed datasets.
- [FeedMyCart](https://feedmycart.com/en/claude-chatgpt/) `https://www.feedmycart.nl/boodschappen/api/v1/mcp`
  [![FeedMyCart MCP connector](https://glama.ai/mcp/connectors/nl.feedmycart/feedmycart/badges/score.svg)](https://glama.ai/mcp/connectors/nl.feedmycart/feedmycart)
  🔐 - Shared household grocery list with pantry and weekly supermarket deals in 15 countries.
- [G-Guest](https://g-guest.app/developers) `https://g-guest.app/api/mcp`
  [![G-Guest MCP connector](https://glama.ai/mcp/connectors/app.g-guest/g-guest/badges/score.svg)](https://glama.ai/mcp/connectors/app.g-guest/g-guest)
  🔓 - Check live availability and book, look up or cancel a table at real restaurants and local businesses.
- [Gaplessly](https://gaplessly.com/docs/mcp) `https://gaplessly.com/api/mcp`
  [![Gaplessly MCP connector](https://glama.ai/mcp/connectors/com.gaplessly/booking/badges/score.svg)](https://glama.ai/mcp/connectors/com.gaplessly/booking)
  🔓 - Live appointment and table times at salons, clinics and restaurants on Gaplessly, with a link to book.
- [HeyYumi](https://heyyumi.ai) `https://mcp.heyyumi.ai/mcp`
  [![HeyYumi MCP connector](https://glama.ai/mcp/connectors/ai.heyyumi/heyyumi/badges/score.svg)](https://glama.ai/mcp/connectors/ai.heyyumi/heyyumi)
  🔐 - Search verified Korean restaurants and bars by filters, then request a table booking in chat.
- [RestaurantDoctorAI Profit Check](https://restaurantdoctorai.com/ai-assistants) `https://restaurantdoctorai.com/api/mcp`
  [![RestaurantDoctorAI Profit Check MCP connector](https://glama.ai/mcp/connectors/com.restaurantdoctorai/profit-check/badges/score.svg)](https://glama.ai/mcp/connectors/com.restaurantdoctorai/profit-check)
  🔓 - Free 12-question restaurant profit check that returns a grade and the biggest money leak.
- [TableJourney](https://tablejourney.com/agents/) `https://tablejourney.com/mcp`
  [![TableJourney MCP connector](https://glama.ai/mcp/connectors/com.tablejourney/food-travel/badges/score.svg)](https://glama.ai/mcp/connectors/com.tablejourney/food-travel)
  🔓 - Restaurants, markets and street food in 200+ cities, plus food festivals and bookable tours.
- [Ullas Opskrifter](https://ullasopskrifter.dk) `https://ullasopskrifter.dk/mcp`
  [![Ullas Opskrifter MCP connector](https://glama.ai/mcp/connectors/dk.ullasopskrifter/recipes/badges/score.svg)](https://glama.ai/mcp/connectors/dk.ullasopskrifter/recipes)
  🔓 - Search and read Danish recipes, ingredients and categories; read-only.
- [bordeaux.guru](https://bordeaux.guru/mcp-server/) `https://mcp.bordeaux.guru/mcp`
  [![bordeaux.guru MCP connector](https://glama.ai/mcp/connectors/guru.bordeaux/en-primeur/badges/score.svg)](https://glama.ai/mcp/connectors/guru.bordeaux/en-primeur)
  🔓 - First-hand Bordeaux en primeur tasting notes, appellation climate, vine phenology and terroir geodata.
- [NYCfoodie](https://nycfoodie-production.up.railway.app/) `https://nycfoodie-production.up.railway.app/mcp`
  [![NYCfoodie MCP connector](https://glama.ai/mcp/connectors/app.railway.up.nycfoodie-production/nycfoodie/badges/score.svg)](https://glama.ai/mcp/connectors/app.railway.up.nycfoodie-production/nycfoodie)
  🔓 - Editorial NYC restaurant recommendations: search, compare, guides and ratings.

### 🎮 <a name="gaming"></a>Gaming

- [Centering Lab](https://centeringlab.com/ai/) `https://centeringlab.com/mcp`
  [![Centering Lab MCP connector](https://glama.ai/mcp/connectors/com.centeringlab/centering-lab/badges/score.svg)](https://glama.ai/mcp/connectors/com.centeringlab/centering-lab)
  🔓 - Measure trading card centering from a photo and check PSA, BGS, CGC and SGC centering limits.
- [Deckodex](https://deckodex.com/assistant) `https://deckodex.com/mcp`
  [![Deckodex MCP connector](https://glama.ai/mcp/connectors/com.deckodex/deckodex/badges/score.svg)](https://glama.ai/mcp/connectors/com.deckodex/deckodex)
  🔐 - Gundam Card Game cards, prices, tournament meta, and your Deckodex collection and decks.
- [Elsewhere](https://elsewhereagents.com) `https://world.elsewhereagents.com/mcp?ref=awesome-remote`
  [![Elsewhere MCP connector](https://glama.ai/mcp/connectors/com.elsewhereagents/world/badges/score.svg)](https://glama.ai/mcp/connectors/com.elsewhereagents/world)
  🔐 - Persistent world for AI agents: explore, build, trade, research at the College and govern a city.
- [Playable Gift](https://playablegift.com) `https://playablegift.com/mcp`
  [![Playable Gift MCP connector](https://glama.ai/mcp/connectors/com.playablegift/playable-gift/badges/score.svg)](https://glama.ai/mcp/connectors/com.playablegift/playable-gift)
  🔓 - Make, save and revise personal browser games, then share a gift link with the recipient.
- [PlayDrop](https://www.playdrop.ai/docs/connectors) `https://mcp.playdrop.ai/mcp`
  [![PlayDrop MCP connector](https://glama.ai/mcp/connectors/ai.playdrop/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/ai.playdrop/mcp)
  🔐 - Publish, test and share browser games on PlayDrop from your AI agent.
- [Playgama](https://playgama.com/mcp/) `https://developer.playgama.com/api/mcp`
  [![Playgama MCP connector](https://glama.ai/mcp/connectors/com.playgama.developer/playgama-developer-cabinet/badges/score.svg)](https://glama.ai/mcp/connectors/com.playgama.developer/playgama-developer-cabinet)
  🔑 - Publish and manage HTML5 games on Playgama: game form, builds, covers, in-app catalog, sandbox link.
- [Plazmi](https://plazmi.gg) `https://plazmi.gg/mcp`
  [![Plazmi MCP connector](https://glama.ai/mcp/connectors/gg.plazmi/plazmi/badges/score.svg)](https://glama.ai/mcp/connectors/gg.plazmi/plazmi)
  🔓 - Move into a little house on a floating island: chores on a UTC clock, neighbours, and a postcard for your human.
- [SECOND STRIKE](https://secondstrike.io/#/ai) `https://secondstrike-server-zgqvqzdrta-uc.a.run.app/mcp`
  [![SECOND STRIKE MCP connector](https://glama.ai/mcp/connectors/io.github.KyleClouthier/secondstrike/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.KyleClouthier/secondstrike)
  🔓 - Real-time war game for AI agents: command a nation, sign and break pacts, climb a public ladder.
- [Shared Forest](https://sharedforest.com) `https://sharedforest.com/mcp`
  [![Shared Forest MCP connector](https://glama.ai/mcp/connectors/io.github.ArneFfm/shared-forest/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ArneFfm/shared-forest)
  🔓 - Plant one tree a day in a shared illustrated forest, read its stats, and sponsor trees with OAuth.
- [SpaceMolt](https://www.spacemolt.com) `https://game.spacemolt.com/mcp/v2`
  [![SpaceMolt MCP connector](https://glama.ai/mcp/connectors/io.github.statico-alt/spacemolt/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.statico-alt/spacemolt)
  🔓 - MMO for AI agents: mine, trade, craft, explore and fight across a 500-system galaxy.
- [The Pit](https://pit.benys.dev) `https://pit.benys.dev/mcp`
  [![The Pit MCP connector](https://glama.ai/mcp/connectors/dev.benys/the-pit/badges/score.svg)](https://glama.ai/mcp/connectors/dev.benys/the-pit)
  🔓 - Agent arena where AI agents register, call each other out and play server-refereed chess for ratings, free to play.
- [TickerMint](https://tickermint.cards/developers) `https://api.tickermint.cards/mcp`
  [![TickerMint MCP connector](https://glama.ai/mcp/connectors/io.github.seankarltonlee/tickermint/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.seankarltonlee/tickermint)
  🔓 - Daily trading card prices and history for Pokémon, One Piece, Lorcana, Yu-Gi-Oh, Riftbound and Gundam.
- [WagerX](https://wagerx.io/agent-gateway) `https://wagerx.io/mcp`
  [![WagerX MCP connector](https://glama.ai/mcp/connectors/io.wagerx/wager-x-crypto-casinos/badges/score.svg)](https://glama.ai/mcp/connectors/io.wagerx/wager-x-crypto-casinos)
  🔓 - Source-linked gambling regulatory intelligence and real-money crypto casino audit evidence.
- [ZeroMind](https://origozero.ai/mcp-server) `https://origozero.ai/mcp`
  [![ZeroMind MCP connector](https://glama.ai/mcp/connectors/ai.origozero/zeromind/badges/score.svg)](https://glama.ai/mcp/connectors/ai.origozero/zeromind)
  🔐 - Write and run Luau in the Zero 3D engine, place entities, take screenshots and publish a game that plays in a browser.

### 🏋️ <a name="health--fitness"></a>Health & Fitness

- [Biohacking Kompakt](https://biohackingkompakt.de) `https://mcp.biohackingkompakt.de/mcp`
  [![Biohacking Kompakt MCP connector](https://glama.ai/mcp/connectors/de.biohackingkompakt/biohacking-kompakt/badges/score.svg)](https://glama.ai/mcp/connectors/de.biohackingkompakt/biohacking-kompakt)
  🔓 - Evidence ratings for 340+ supplements, peptides and longevity methods, with study sources and podcast (German).
- [Blocks](https://blocks.zone/ai) `https://blocks.zone/api/mcp`
  [![Blocks MCP connector](https://glama.ai/mcp/connectors/zone.blocks/blocks/badges/score.svg)](https://glama.ai/mcp/connectors/zone.blocks/blocks)
  🔐 - Plan and review cycling and running: training calendar, synced rides, sleep and HRV.
- [JustGains](https://justgains.com) `https://justgains.com/connect/mcp`
  [![JustGains MCP connector](https://glama.ai/mcp/connectors/com.justgains/mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/com.justgains/mcp-server)
  🔐 - Your workouts, lift history and food diary: build and save workouts, check progress, and log meals and bodyweight.
- [MoveMate](https://movemate.app/ai) `https://api.movemate.app/mcp`
  [![MoveMate MCP connector](https://glama.ai/mcp/connectors/app.movemate/movemate/badges/score.svg)](https://glama.ai/mcp/connectors/app.movemate/movemate)
  🔐 - Your gym log: training stats, PRs and lift progression, plus workouts you approve scheduled straight into the app.
- [Phi Longevity PRISM](https://philongevity.com/for-agents) `https://philongevity.com/mcp?src=awesome`
  [![Phi Longevity PRISM MCP connector](https://glama.ai/mcp/connectors/io.github.Philongevity/phi-longevity-prism/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Philongevity/phi-longevity-prism)
  🔓 - Guideline-cited lab-results analysis for chronic conditions; flags missing or overdue tests with citations.
- [Povver](https://povver.ai) `https://mcp.povver.ai/mcp`
  [![Povver MCP connector](https://glama.ai/mcp/connectors/ai.povver/mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/ai.povver/mcp-server)
  🔐 - Your strength-training data: workout history, per-lift trends, muscle-group volume and routines.
- [Reps: Gym Workout Log (repsworkout.com)](https://repsworkout.com/connect?utm_source=awesome-remote) `https://api.repsworkout.com/mcp`
  [![Reps MCP connector](https://glama.ai/mcp/connectors/com.repsworkout/reps/badges/score.svg)](https://glama.ai/mcp/connectors/com.repsworkout/reps)
  🔐 - Read your gym log (workouts, PRs, lift progress, routines, plan) and save routines and plans you approve.
- [Trainzilla](https://trainzilla.app/solutions/ai-agent) `https://api.tzilla.live/mcp`
  [![Trainzilla MCP connector](https://glama.ai/mcp/connectors/io.github.Trainzilla/trainzilla-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Trainzilla/trainzilla-mcp)
  🔐 - For personal trainers: manage clients, workout and diet plans, check-ins, habits, sessions and billing.
- [Vlada Health](https://www.vladahealth.com/data-access) `https://mcp-secure.vladahealth.com/mcp`
  [![Vlada Health MCP connector](https://glama.ai/mcp/connectors/io.github.btenner84/vlada/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.btenner84/vlada)
  🔐 - US healthcare data: hospital and payer prices, Medicare Advantage, Medicaid, providers and drugs, each with its source.

### 🧠 <a name="knowledge--memory"></a>Knowledge & Memory

- [艾达 ADA](https://ai.hengyu.group) `https://ai.hengyu.group/mcp`
  [![艾达 ADA MCP connector](https://glama.ai/mcp/connectors/group.hengyu.ai/ada/badges/score.svg)](https://glama.ai/mcp/connectors/group.hengyu.ai/ada)
  🔓 - Shared public warehouse for agents: search, fetch and store reusable knowledge, no signup and no key required.
- [ABS · AI Business System](https://www.ucai.net) `https://www.ucai.net/api/agent/mcp`
  [![ABS · AI Business System MCP connector](https://glama.ai/mcp/connectors/net.ucai/abs/badges/score.svg)](https://glama.ai/mcp/connectors/net.ucai/abs)
  🔐 - Lean and operations knowledge base built on DBS: cited answers, tool cards, scheduled plans and diagnoses.
- [AbuzzHive](https://www.abuzzhive.com) `https://www.abuzzhive.com/mcp`
  [![AbuzzHive MCP connector](https://glama.ai/mcp/connectors/com.abuzzhive/abuzzhive/badges/score.svg)](https://glama.ai/mcp/connectors/com.abuzzhive/abuzzhive)
  🔐 - Q&A boards where agents post problems they are stuck on and other agents solve them; search, post, solve, vote.
- [AIeph](https://aieph.dev) `https://aieph.dev/mcp`
  [![AIeph MCP connector](https://glama.ai/mcp/connectors/dev.aieph/aieph/badges/score.svg)](https://glama.ai/mcp/connectors/dev.aieph/aieph)
  🔓 - Look up a shared cache of past answers to programming questions.
- [Atlas Red](https://atlas-red.com/mind-map-mcp) `https://app.atlas-red.com/mcp`
  [![Atlas Red MCP connector](https://glama.ai/mcp/connectors/com.atlas-red/mind-map/badges/score.svg)](https://glama.ai/mcp/connectors/com.atlas-red/mind-map)
  🔐 - Create and edit mind maps — nodes, links, and subtrees — then export them or render one as an image.
- [Bilg](https://app.bilgai.com/docs/connect?ref=mcp-directory) `https://mcp.bilgai.com/mcp`
  [![Bilg MCP connector](https://glama.ai/mcp/connectors/com.bilgai/bilg/badges/score.svg)](https://glama.ai/mcp/connectors/com.bilgai/bilg)
  🔐 - Shared memory for coding agents and their teams: search docs, read and write epics, tasks and decisions.
- [BotGathering](https://botgathering.com) `https://botgathering.com/mcp`
  [![BotGathering MCP connector](https://glama.ai/mcp/connectors/com.botgathering/recipes/badges/score.svg)](https://glama.ai/mcp/connectors/com.botgathering/recipes)
  🔓 - Tested step-by-step playbooks for AI agents: search, follow and report outcomes. Free.
- [bsv.cx](https://bsv.cx) `https://bsv.cx/mcp`
  [![bsv.cx MCP connector](https://glama.ai/mcp/connectors/cx.bsv/bsv-cx/badges/score.svg)](https://glama.ai/mcp/connectors/cx.bsv/bsv-cx)
  🔓 - Timestamp and verify evidence on-chain; let your agent prove what it saw and when.
- [Continuity](https://continuitywriter.com) `https://continuitywriter.com/mcp`
  [![Continuity MCP connector](https://glama.ai/mcp/connectors/io.github.LAHutchins91/continuity/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.LAHutchins91/continuity)
  🔓 - Remembers your writing project across chats: story bible, characters, timeline and continuity checks.
- [Detextit](https://www.detextit.com) `https://www.detextit.com/api/mcp`
  [![Detextit MCP connector](https://glama.ai/mcp/connectors/com.detextit.www/detextit/badges/score.svg)](https://glama.ai/mcp/connectors/com.detextit.www/detextit)
  🔓 - Read-only shared agent context with sources and conditions, plus plans for recovering from task constraints.
- [Dexio](https://dexio.wiki) `https://app.dexio.wiki/mcp`
  [![Dexio MCP connector](https://glama.ai/mcp/connectors/wiki.dexio/dexio/badges/score.svg)](https://glama.ai/mcp/connectors/wiki.dexio/dexio)
  🔐 - One wiki all your agents read and write over MCP, with every version kept and the agent behind each change recorded.
- [docs2mcp](https://docs2mcp.com) `https://mcp.docs2mcp.com/mcp`
  [![docs2mcp MCP connector](https://glama.ai/mcp/connectors/com.docs2mcp/docs2mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.docs2mcp/docs2mcp)
  🔐 - Query your own PDFs and documents, with every answer linking to the exact page and region it came from.
- [emem](https://emem.dev) `https://emem.dev/mcp`
  [![emem MCP connector](https://glama.ai/mcp/connectors/io.github.Vortx-AI/emem/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Vortx-AI/emem)
  🔓 - Elevation, vegetation, flood, fire and air-quality facts for any place, each with a signed receipt.
- [Engram](https://engram.page) `https://mcp.engram.page`
  [![Engram MCP connector](https://glama.ai/mcp/connectors/io.github.engram-app/engram/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.engram-app/engram)
  🔐 - Search, read and edit your Obsidian notes as AI memory, synced to the cloud and reachable with Obsidian closed.
- [Flash](https://flashmemorize.com) `https://flashmemorize.com/mcp`
  🔐 - Spaced-repetition flashcards: create cards from notes, get quizzed by voice, and let FSRS schedule reviews.
- [FoxNose Knowledge](https://foxnose.net/docs/mcp) `https://mcp.foxnose.net/_mcp`
  [![FoxNose Knowledge MCP connector](https://glama.ai/mcp/connectors/net.foxnose/knowledge/badges/score.svg)](https://glama.ai/mcp/connectors/net.foxnose/knowledge)
  🔑 - Hybrid search over vectors, full text and structured filters, with auto-embeddings.
- [Greenlit Books](https://greenlitbooks.com/developers) `https://greenlitbooks.com/api/mcp`
  [![Greenlit Books MCP connector](https://glama.ai/mcp/connectors/com.greenlitbooks/catalog/badges/score.svg)](https://glama.ai/mcp/connectors/com.greenlitbooks/catalog)
  🔓 - Search a catalog of practical AI books, read free chapters, and check a claim against the source behind it.
- [HAIDAA](https://haidaa.com/mcp) `https://mcp.haidaa.com/mcp`
  [![HAIDAA MCP connector](https://glama.ai/mcp/connectors/com.haidaa.mcp/haidaa/badges/score.svg)](https://glama.ai/mcp/connectors/com.haidaa.mcp/haidaa)
  🔓 - Search signed scientific claims, methods, provenance, contradictions, retractions, and admission receipts.
- [Hugging Face](https://huggingface.co) `https://huggingface.co/mcp`
  [![Hugging Face MCP connector](https://glama.ai/mcp/connectors/co.huggingface/hf-mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/co.huggingface/hf-mcp-server)
  🔓 - Search models, datasets, and Spaces, and call Space APIs.
- [Kika](https://getkika.app/mcp) `https://api.getkika.app/mcp`
  [![Kika MCP connector](https://glama.ai/mcp/connectors/io.github.usekika/kika/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.usekika/kika)
  🔐 - Shared memory for a client engagement: decisions, blockers, promises and what was already tried.
- [knowsme](https://knowsme.dev) `https://mcp.knowsme.dev/mcp`
  [![knowsme MCP connector](https://glama.ai/mcp/connectors/dev.knowsme.mcp/knowsme/badges/score.svg)](https://glama.ai/mcp/connectors/dev.knowsme.mcp/knowsme)
  🔐 - One memory for you and your AI agents: your notes, rules and projects follow you across machines, AI apps and agents.
- [Lochless](https://lochless.io) `https://api.lochless.io/mcp`
  [![Lochless MCP connector](https://glama.ai/mcp/connectors/io.lochless/lochless/badges/score.svg)](https://glama.ai/mcp/connectors/io.lochless/lochless)
  🔐 - Every match, not the top 10: searches your documents and returns each relevant one, with quotes.
- [MemoryRouter](https://memoryrouter.ai) `https://mcp.memoryrouter.ai/mcp`
  [![MemoryRouter MCP connector](https://glama.ai/mcp/connectors/ai.memoryrouter/memoryrouter/badges/score.svg)](https://glama.ai/mcp/connectors/ai.memoryrouter/memoryrouter)
  🔓 - Cross-AI persistent memory for ChatGPT, Claude, Codex and other MCP clients: one user-scoped vault. OAuth unlocks it.
- [MemorySync](https://memorysync.io) `https://mcp.memorysync.io/mcp`
  [![MemorySync MCP connector](https://glama.ai/mcp/connectors/io.memorysync/memory/badges/score.svg)](https://glama.ai/mcp/connectors/io.memorysync/memory)
  🔐 - Scoped, persistent memory for agents to save, inspect and recall decisions across sessions.
- [MarkIt](https://mark-it.co) `https://mark-it.co/api/mcp`
  [![MarkIt MCP connector](https://glama.ai/mcp/connectors/io.github.FuzulsFriend/markit/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.FuzulsFriend/markit)
  🔓 - Search, save and set reminders in your library of saved links, posts and notes; sign in to unlock all tools.
- [MMW](https://mmwhub.tech) `https://mcp.mmwhub.tech/mcp`
  [![MMW MCP connector](https://glama.ai/mcp/connectors/tech.mmwhub.mcp/mmw/badges/score.svg)](https://glama.ai/mcp/connectors/tech.mmwhub.mcp/mmw)
  🔐 - Persistent agent memory workspace with strict tenant isolation and provenance.
- [Mnemoverse](https://mnemoverse.com) `https://mcp.mnemoverse.com/mcp`
  [![Mnemoverse MCP connector](https://glama.ai/mcp/connectors/io.github.mnemoverse/mcp-memory-server/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.mnemoverse/mcp-memory-server)
  🔐 - Persistent agent memory; tell it a recalled memory helped or misled and it re-ranks the next recall.
- [New Runtime](https://newruntime.com/agents/) `https://newruntime.com/mcp`
  [![New Runtime MCP connector](https://glama.ai/mcp/connectors/com.newruntime/archive/badges/score.svg)](https://glama.ai/mcp/connectors/com.newruntime/archive)
  🔓 - Dated, source-linked AI-engineering archive: what changed since a date, topic briefs, forecasts with a track record.
- [NextLang](https://www.nextlang.co/mcp) `https://www.nextlang.co/api/mcp`
  [![NextLang MCP connector](https://glama.ai/mcp/connectors/co.nextlang/nextlang/badges/score.svg)](https://glama.ai/mcp/connectors/co.nextlang/nextlang)
  🔐 - Make Anki, Quizlet, Mochi and Brainscape flashcard decks and review your vocabulary with spaced repetition.
- [NEXUS AGI](https://nexus.eblas.link/en) `https://nexus.eblas.link/mcp`
  [![NEXUS AGI MCP connector](https://glama.ai/mcp/connectors/link.eblas.nexus/nexus-agi/badges/score.svg)](https://glama.ai/mcp/connectors/link.eblas.nexus/nexus-agi)
  🔐 - Shared memory that keeps AI agents from repeating costly mistakes: past decisions, rules and incidents, shared by all.
- [NoteMCP](https://notemcp.com) `https://notemcp.com/mcp`
  [![NoteMCP MCP connector](https://glama.ai/mcp/connectors/com.notemcp/notemcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.notemcp/notemcp)
  🔐 - Long-term memory from your notes: search, read and edit notes saved by text, voice or share sheet.
- [Notion](https://notion.com) `https://mcp.notion.com/mcp`
  🔐 - Read and write Notion pages, databases, and comments.
- [notepad.page](https://notepad.page) `https://mcp.notepad.page/mcp`
  [![notepad.page MCP connector](https://glama.ai/mcp/connectors/page.notepad/notepad/badges/score.svg)](https://glama.ai/mcp/connectors/page.notepad/notepad)
  🔓 - Publish, recall and update persistent private HTML pages at a personal address; publishing needs OAuth.
- [Ontonym](https://www.ontonym.com) `https://mcp.ontonym.com/mcp`
  [![Ontonym MCP connector](https://glama.ai/mcp/connectors/com.ontonym/memory/badges/score.svg)](https://glama.ai/mcp/connectors/com.ontonym/memory)
  🔐 - Give your agents your team's real data: read the shared graph, and propose actions a human approves.
- [OwnerSpec](https://ownerspec.com/mcp-server/) `https://ownerspec.com/mcp`
  [![OwnerSpec MCP connector](https://glama.ai/mcp/connectors/com.ownerspec/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.ownerspec/mcp)
  🔓 - Cited home water treatment answers: diagnose a water problem, size a softener, and match replacement parts.
- [past.dev](https://past.dev/docs/mcp/overview) `https://app.past.dev/mcp`
  [![past.dev MCP connector](https://glama.ai/mcp/connectors/dev.past/past/badges/score.svg)](https://glama.ai/mcp/connectors/dev.past/past)
  🔐 - Long-term memory for agents: ask what is true now and get the current facts back with their dated sources.
- [Pinto Notes](https://pintonotes.com) `https://mcp.pintonotes.com`
  [![Pinto Notes MCP connector](https://glama.ai/mcp/connectors/com.pintonotes/pinto-notes/badges/score.svg)](https://glama.ai/mcp/connectors/com.pintonotes/pinto-notes)
  🔐 - Search, read and edit your notes; every AI edit is highlighted in the app, with version history and undo.
- [QianYuan 乾元](https://qianyuan.ltd) `https://qianyuan.ltd/mcp`
  [![QianYuan MCP connector](https://glama.ai/mcp/connectors/ltd.qianyuan/qy-evolution/badges/score.svg)](https://glama.ai/mcp/connectors/ltd.qianyuan/qy-evolution)
  🔓 - Reuse verified results and pitfalls other agents already published, before doing the work yourself.
- [Recipe library](https://ofershap.github.io/agent-success-hub/) `https://recipes.gitshow.dev/mcp`
  [![Recipe library MCP connector](https://glama.ai/mcp/connectors/io.github.ofershap/recipe-library/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ofershap/recipe-library)
  🔓 - Search and read reviewed Hebrew AI-agent task recipes, with available full English versions. Read-only.
- [Remnant](https://remnant.dedale-bi.com/knowledge) `https://remnant.dedale-bi.com/mcp/chatgpt`
  [![Remnant Read MCP connector](https://glama.ai/mcp/connectors/com.dedale-bi.remnant/remnant/badges/score.svg)](https://glama.ai/mcp/connectors/com.dedale-bi.remnant/remnant)
  🔓 - Search prior debugging experience, inspect evidence and failed attempts; free public reading without signup.
- [Rootr](https://rootr.io) `https://rootr.io/mcp`
  [![Rootr MCP connector](https://glama.ai/mcp/connectors/io.github.inspirio-co/rootr-cli/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.inspirio-co/rootr-cli)
  🔐 - Read, search and write team docs, tables, issues and CRM records, with answers citing their source.
- [Sensefold](https://sensefold.app/for-agents) `https://api.sensefold.app/mcp`
  [![Sensefold MCP connector](https://glama.ai/mcp/connectors/app.sensefold/sensefold/badges/score.svg)](https://glama.ai/mcp/connectors/app.sensefold/sensefold)
  🔐 - Search, read and write your saved articles, threads, PDFs, notes and AI chats as Markdown.
- [Sooveryn](https://www.sooveryn.com/?utm_source=awesome-remote-mcp&utm_medium=annuaire&utm_campaign=lancement-oct) `https://mcp.sooveryn.com/mcp`
  [![Sooveryn MCP connector](https://glama.ai/mcp/connectors/com.sooveryn/sooveryn/badges/score.svg)](https://glama.ai/mcp/connectors/com.sooveryn/sooveryn)
  🔑 - A team of AI personas sharing a lasting, encrypted memory per project, hosted in France.
- [Stele](https://stele-ai.dev) `https://app.stele-ai.dev/api/mcp`
  [![Stele MCP connector](https://glama.ai/mcp/connectors/dev.stele-ai/stele/badges/score.svg)](https://glama.ai/mcp/connectors/dev.stele-ai/stele)
  🔐 - Shared project memory for coding agents: recall and record decisions, lessons and risks, and claim tasks.
- [Synapse Layer](https://synapselayer.org) `https://forge.synapselayer.org/api/mcp`
  [![Synapse Layer MCP connector](https://glama.ai/mcp/connectors/io.github.SynapseLayer/synapse-layer/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.SynapseLayer/synapse-layer)
  🔓 - Persistent encrypted agent memory with semantic recall and cross-agent continuity.
- [Thea](https://thealibrary.org) `https://thealibrary.org/mcp`
  [![Thea MCP connector](https://glama.ai/mcp/connectors/org.thealibrary/thea/badges/score.svg)](https://glama.ai/mcp/connectors/org.thealibrary/thea)
  🔓 - Open, people-curated knowledge library: 1M+ Korean places, people and works, no signup or key.
- [Urantia Papers](https://urantia.dev) `https://api.urantia.dev/mcp`
  [![Urantia Papers MCP connector](https://glama.ai/mcp/connectors/dev.urantia/urantia-papers/badges/score.svg)](https://glama.ai/mcp/connectors/dev.urantia/urantia-papers)
  🔓 - Read and search the Urantia Papers by reference, keyword, or meaning, with named entities and Bible cross-references.
- [UseMyContext](https://usemycontext.ai) `https://mcp.usemycontext.ai/mcp`
  [![UseMyContext MCP connector](https://glama.ai/mcp/connectors/io.github.usemycontext/usemycontext/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.usemycontext/usemycontext)
  🔓 - Your own profile and files as AI context; anonymous access gets metadata only.
- [Vilix AI](https://vilix.ai) `https://api.vilix.ai/mcp`
  [![Vilix AI MCP connector](https://glama.ai/mcp/connectors/ai.vilix.api/vilix-ai/badges/score.svg)](https://glama.ai/mcp/connectors/ai.vilix.api/vilix-ai)
  🔐 - Persistent AI memory shared across tools and devices.
- [What Led To](https://whatledto.com) `https://whatledto.com/mcp`
  [![What Led To MCP connector](https://glama.ai/mcp/connectors/com.whatledto/what-led-to/badges/score.svg)](https://glama.ai/mcp/connectors/com.whatledto/what-led-to)
  🔓 - Source-backed timelines of tech, economy and gaming events, with the quote behind each entry.
- [WhiteMagic](https://www.whitemagic.dev) `https://mcp.whitemagic.dev/mcp`
  [![WhiteMagic MCP connector](https://glama.ai/mcp/connectors/io.github.lbailey94/whitemagic-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.lbailey94/whitemagic-mcp)
  🔓 - Local-first agent memory and session continuity: durable recall, handoffs, and signed continuity receipts.

### ⚖️ <a name="legal"></a>Legal
- [AcqPath](https://developers.getacqpath.com) `https://api.getacqpath.com/mcp`
  [![AcqPath MCP connector](https://glama.ai/mcp/connectors/com.getacqpath/acqpath/badges/score.svg)](https://glama.ai/mcp/connectors/com.getacqpath/acqpath)
  🔓 - Check observed machine-readable source-rights declarations before AI, RAG, indexing, training or search.

- [Akashi Notari](https://akashi-notari.com) `https://anchor.akashi-notari.com/mcp`
  [![Akashi Notari MCP connector](https://glama.ai/mcp/connectors/io.github.self-reality/akashi-notari/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.self-reality/akashi-notari)
  🔓 - Proof of existence for files: anchor a SHA-256 hash on Base and look up proofs; an anchor costs $0.01 over x402.
- [Claim Done](https://claimdone.com.au/connect-your-ai-assistant/) `https://claimdone.com.au/mcp`
  [![Claim Done MCP connector](https://glama.ai/mcp/connectors/au.com.claimdone/claimdone/badges/score.svg)](https://glama.ai/mcp/connectors/au.com.claimdone/claimdone)
  🔓 - Drafts Australian letters of demand, tribunal applications and notices, and returns a payment link. Not a law firm.
- [Common Paper](https://commonpaper.com) `https://api.commonpaper.com/mcp`
  [![Common Paper MCP connector](https://glama.ai/mcp/connectors/com.commonpaper/contracts/badges/score.svg)](https://glama.ai/mcp/connectors/com.commonpaper/contracts)
  🔐 - Create agreements from standard templates, send them for signature, and track status and history.
- [Court Rules](https://www.courtrules.app) `https://mcp.courtrules.app/mcp`
  [![Court Rules MCP connector](https://glama.ai/mcp/connectors/app.courtrules/court-rules/badges/score.svg)](https://glama.ai/mcp/connectors/app.courtrules/court-rules)
  🔓 - US judge filing rules, court holidays and enforcement data; free samples, OAuth for full access.
- [Datakoot Regulatory Intel](https://datakoot.com/regulatory-intel) `https://regulatory.datakoot.com/mcp`
  [![Datakoot Regulatory Intel MCP connector](https://glama.ai/mcp/connectors/com.datakoot/federal-register-rules/badges/score.svg)](https://glama.ai/mcp/connectors/com.datakoot/federal-register-rules)
  🔓 - Federal Register rules, proposed rules, notices and executive orders, searchable by agency and term.
- [klaro.legal](https://klaro.legal/en-us/embed-widget) `https://klaro.legal/api/mcp`
  [![klaro.legal MCP connector](https://glama.ai/mcp/connectors/legal.klaro/document-explainer/badges/score.svg)](https://glama.ai/mcp/connectors/legal.klaro/document-explainer)
  🔓 - Explains contracts, official letters and tax assessments clause by clause in plain language; not legal advice.
- [Lebanese Legislation](https://lebaneselegislation.com/ai/) `https://lebaneselegislation.com/mcp`
  [![Lebanese Legislation MCP connector](https://glama.ai/mcp/connectors/com.lebaneselegislation/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.lebaneselegislation/mcp)
  🔓 - Lebanese laws, articles, court rulings and Official Gazette issues since 1904, in Arabic and French, verbatim.
- [LibreJustice](https://librejustice.fr) `https://librejustice.fr/mcp`
  [![LibreJustice MCP connector](https://glama.ai/mcp/connectors/fr.librejustice/librejustice/badges/score.svg)](https://glama.ai/mcp/connectors/fr.librejustice/librejustice)
  🔐 - French and European case law and legislation, searched in plain language and linked article by article.
- [Licitações BR](https://mcpize.com/mcp/mcp-licitacoes-br) `https://mcp-licitacoes-br.mcpize.run/mcp`
  [![Licitações BR MCP connector](https://glama.ai/mcp/connectors/io.github.DouglasGouvea/mcp-licitacoes-br/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.DouglasGouvea/mcp-licitacoes-br)
  🔐 - Brazilian public tenders and contracts from PNCP, each fact with its official source and date.
- [LienDeadline](https://liendeadline.com) `https://mcp.liendeadline.com/mcp`
  [![LienDeadline MCP connector](https://glama.ai/mcp/connectors/io.github.LienDeadline/liendeadline-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.LienDeadline/liendeadline-mcp)
  🔓 - Read-only US mechanics lien and preliminary notice deadlines for suppliers, plus lien guides for all 50 states and DC.
- [Patent by Ouroboros](https://ouroborosapps.com/docs/patent) `https://patent-mcp.vercel.app/mcp`
  [![Patent by Ouroboros MCP connector](https://glama.ai/mcp/connectors/io.github.LAHutchins91/patent/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.LAHutchins91/patent)
  🔓 - US patent search and prior art lookup that returns only records the patent office returned; not legal advice.
- [RegAI Legal MCP](https://regai.tw/mcp) `https://mcp.regai.tw/mcp`
  [![RegAI Legal MCP connector](https://glama.ai/mcp/connectors/tw.regai/legal/badges/score.svg)](https://glama.ai/mcp/connectors/tw.regai/legal)
  🔐 - Taiwan law and court decisions: statutes, articles by number, apex-court and Grand Chamber rulings; read-only.

- [UK Legislation Changes](https://uk-legal-changes.pages.dev) `https://uk-legal-changes.pages.dev/mcp`
  [![UK Legislation Changes MCP connector](https://glama.ai/mcp/connectors/io.github.busybusybussiness/uk-legislation-changes/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.busybusybussiness/uk-legislation-changes)
  🔓 - Point-in-time amendment history for 506 UK legislation provisions across employment, equality, consumer and company law.
- [Zitierfest](https://zitierfest.de) `https://mcp.zitierfest.de/mcp`
  [![Zitierfest MCP connector](https://glama.ai/mcp/connectors/de.zitierfest/zitierfest/badges/score.svg)](https://glama.ai/mcp/connectors/de.zitierfest/zitierfest)
  🔐 - German statutes verbatim (federal, 16 states, EU), federal court decisions with paragraph numbers, legal fees.

### 🎯 <a name="marketing"></a>Marketing

- [Adsap](https://adsap.ai) `https://mcp.adsap.ai/mcp`
  [![Adsap MCP connector](https://glama.ai/mcp/connectors/ai.adsap/adsap/badges/score.svg)](https://glama.ai/mcp/connectors/ai.adsap/adsap)
  🔐 - Meta and Google Ads automation: launch ads in bulk and preview every change first.

- [AdsTurbo](https://adsturbo.ai) `https://adsturbo.ai/klian/novartapi/mcp`
  [![AdsTurbo MCP connector](https://glama.ai/mcp/connectors/io.github.AdsTurbo/adsturbo/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.AdsTurbo/adsturbo)
  🔓 - Clone a winning ad around your product, make AI-actor and product videos, and translate them with lip sync.

- [Advisors AI Service Navigator](https://advisorsai.ai) `https://advisorsai.ai/mcp`
  [![Advisors AI Service Navigator MCP connector](https://glama.ai/mcp/connectors/ai.advisorsai/service-navigator/badges/score.svg)](https://glama.ai/mcp/connectors/ai.advisorsai/service-navigator)
  🔓 - Read-only catalog of five services, a public-page check, and a request-link; nothing is charged.


- [Advisors AI Store Readiness](https://advisorsai.ai) `https://advisorsai.ai/store-readiness-mcp`
  [![Advisors AI Store Readiness MCP connector](https://glama.ai/mcp/connectors/ai.advisorsai/store-readiness/badges/score.svg)](https://glama.ai/mcp/connectors/ai.advisorsai/store-readiness)
  🔓 - Check a public page's robots, sitemap, JSON-LD, canonical tags and llms.txt.


- [AfterLaunch](https://afterlaunch.io) `https://afterlaunch.io/api/mcp`
  [![AfterLaunch MCP connector](https://glama.ai/mcp/connectors/io.afterlaunch/agentic-growth-marketing/badges/score.svg)](https://glama.ai/mcp/connectors/io.afterlaunch/agentic-growth-marketing)
  🔓 - AI answer visibility, SEO and a ranked backlog of growth moves; tools need an account.
- [agentbuilt](https://agentbuilt.dev/mcp) `https://agentbuilt.dev/api/mcp`
  [![agentbuilt MCP connector](https://glama.ai/mcp/connectors/dev.agentbuilt/agentbuilt/badges/score.svg)](https://glama.ai/mcp/connectors/dev.agentbuilt/agentbuilt)
  🔓 - Free AI-readiness audit of any URL: AI crawler rules, JS-free text, JSON-LD, llms.txt and concrete fixes.

- [ask10ais](https://ask10ais.com) `https://ask10ais.com/api/mcp`
  [![ask10ais MCP connector](https://glama.ai/mcp/connectors/com.ask10ais/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.ask10ais/mcp)
  🔓 - Read-only rankings and mention rates showing how 12 AI models answer brand questions in Chinese and English.

- [AskWatch Google Search Console MCP](https://askwatch.ai/free-tools/google-search-console-mcp) `https://mcp.askwatch.ai/gsc`
  [![AskWatch Google Search Console MCP connector](https://glama.ai/mcp/connectors/ai.askwatch/gsc/badges/score.svg)](https://glama.ai/mcp/connectors/ai.askwatch/gsc)
  🔓 - Read-only Google Search Console: traffic changes, CTR gaps, cannibalization, URL inspection; tools need a free account.

- [BanProof](https://banproof.io) `https://banproof.io/mcp`
  [![BanProof MCP connector](https://glama.ai/mcp/connectors/io.banproof/ban-proof-ai/badges/score.svg)](https://glama.ai/mcp/connectors/io.banproof/ban-proof-ai)
  🔓 - Check TikTok Shop and Amazon affiliate video scripts for policy violations and draft ban appeal letters.
- [BizIntel](https://mcp-bizintel-production.up.railway.app) `https://mcp-bizintel-production.up.railway.app/mcp`
  [![BizIntel MCP connector](https://glama.ai/mcp/connectors/io.github.bch1212/bizintel/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.bch1212/bizintel)
  🔓 - Audit websites, detect tech stacks, and find and score local businesses without a website.
- [CalmSEO](https://calmseo.com) `https://mcp.calmseo.com/mcp`
  [![CalmSEO MCP connector](https://glama.ai/mcp/connectors/com.calmseo/seo-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.calmseo/seo-mcp)
  🔐 - Free Google Search Console analytics plus credit-based SERP, keyword, and page audit tools.
- [Camberstack](https://camberstack.io) `https://camberstack.io/mcp`
  [![Camberstack MCP connector](https://glama.ai/mcp/connectors/io.camberstack/google-ads/badges/score.svg)](https://glama.ai/mcp/connectors/io.camberstack/google-ads)
  🔐 - Google Ads: checks conversion tracking, finds wasted spend, and applies only the changes you approve, with undo.
- [ChimpanSEO](https://chimpanseo.app) `https://chimpanseo.app/api/mcp`
  [![ChimpanSEO MCP connector](https://glama.ai/mcp/connectors/app.chimpanseo/chimpanseo/badges/score.svg)](https://glama.ai/mcp/connectors/app.chimpanseo/chimpanseo)
  🔓 - Generate, schedule and publish GEO/AEO-optimized articles to WordPress; tools need an account.
- [Cite42](https://www.cite42.dev) `https://mcp.cite42.dev`
  [![Cite42 MCP connector](https://glama.ai/mcp/connectors/dev.cite42/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/dev.cite42/mcp)
  🔐 - Check whether ChatGPT, Claude, Perplexity and Gemini mention your brand and what they cite; keyword and trend data.
- [ConferenceGrid](https://conferencegrid.com/mcp) `https://conferencegrid.com/api/mcp`
  [![ConferenceGrid MCP connector](https://glama.ai/mcp/connectors/com.conferencegrid/conferencegrid/badges/score.svg)](https://glama.ai/mcp/connectors/com.conferencegrid/conferencegrid)
  🔐 - Which conferences a company sponsors, exhibits at or speaks at, and which events are open to sponsors.
- [Convertlyft](https://convertlyft.com/developers) `https://mcp.convertlyft.com/mcp`
  [![Convertlyft MCP connector](https://glama.ai/mcp/connectors/com.convertlyft/convertlyft/badges/score.svg)](https://glama.ai/mcp/connectors/com.convertlyft/convertlyft)
  🔓 - Web analytics that names the fix: funnels, replays, errors, speed and SEO. Free SEO scan; account tools use OAuth.
- [GrowSurf](https://docs.growsurf.com/build-with-ai) `https://mcp.growsurf.com`
  [![GrowSurf MCP connector](https://glama.ai/mcp/connectors/com.growsurf/growsurf/badges/score.svg)](https://glama.ai/mcp/connectors/com.growsurf/growsurf)
  🔐 - Build and manage GrowSurf referral and affiliate programs through AI assistants.

- [pSEO Engine](https://quantumcx.net/pseo-engine) `https://pseo.quantumcx.net/api/agent/mcp`
  [![pSEO Engine MCP connector](https://glama.ai/mcp/connectors/net.quantumcx/pseo-engine/badges/score.svg)](https://glama.ai/mcp/connectors/net.quantumcx/pseo-engine)
  🔓 - Programmatic SEO: research, generate, audit and publish landing pages at scale; reads are free.

- [DABLOCK AI Visibility Index](https://dablock.ai) `https://dablock.ai/mcp`
  [![DABLOCK MCP connector](https://glama.ai/mcp/connectors/ai.dablock/visibility-index/badges/score.svg)](https://glama.ai/mcp/connectors/ai.dablock/visibility-index)
  🔓 - Weekly share of answer for 24 crypto and Web3 brands in ChatGPT, Perplexity and Gemini.
- [DABYTE AI Visibility Index](https://dabyte.ai) `https://dabyte.ai/mcp`
  [![DABYTE MCP connector](https://glama.ai/mcp/connectors/ai.dabyte/visibility-index/badges/score.svg)](https://glama.ai/mcp/connectors/ai.dabyte/visibility-index)
  🔓 - Weekly share of answer for 20 SaaS and AI brands in ChatGPT, Perplexity and Gemini.
- [DashThis](https://dashthis.com) `https://mcp.dashthis.com`
  [![DashThis MCP connector](https://glama.ai/mcp/connectors/com.dashthis/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.dashthis/mcp)
  🔐 - Work with your marketing reporting dashboards and turn the numbers into client-ready updates.
- [Deeplead](https://www.deeplead.io) `https://www.deeplead.io/api/mcp`
  [![Deeplead MCP connector](https://glama.ai/mcp/connectors/io.deeplead/deeplead/badges/score.svg)](https://glama.ai/mcp/connectors/io.deeplead/deeplead)
  🔓 - Search local businesses, companies and people, and find their decision makers with verified emails and phone numbers.
- [DripRaven](https://dripraven.com) `https://app.dripraven.com/mcp`
  [![DripRaven MCP connector](https://glama.ai/mcp/connectors/com.dripraven/dripraven/badges/score.svg)](https://glama.ai/mcp/connectors/com.dripraven/dripraven)
  🔐 - WhatsApp Business campaigns: import and segment contacts, schedule broadcasts and track delivery.
- [Formgong](https://formgong.com) `https://formgong.com/mcp`
  [![Formgong MCP connector](https://glama.ai/mcp/connectors/com.formgong/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.formgong/mcp)
  🔓 - Create contact forms and get HTML/React/Next.js snippets; discovery is open, every tool call needs a sign-in.
- [FoxForm](https://foxform.app) `https://mcp.foxform.app/mcp`
  [![FoxForm MCP connector](https://glama.ai/mcp/connectors/app.foxform.mcp/fox-form/badges/score.svg)](https://glama.ai/mcp/connectors/app.foxform.mcp/fox-form)
  🔓 - Build scored forms, quizzes and calculators, publish them, and read responses with per-screen analytics.
- [GetAppNiche](https://getappniche.com/mcp) `https://api.getappniche.com/mcp`
  [![GetAppNiche MCP connector](https://glama.ai/mcp/connectors/com.getappniche/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.getappniche/mcp)
  🔓 - App Store and Google Play data: app search, revenue and download estimates, keywords, reviews; API key for calls.
- [GingerLive](https://gingerlive.io) `https://mcp.gingerlive.io/mcp`
  [![GingerLive MCP connector](https://glama.ai/mcp/connectors/io.gingerlive/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.gingerlive/mcp)
  🔓 - Livestream ad formats, network reach stats, campaign case studies and streamer program.
- [GoodLeads](https://goodleads.club) `https://mcp.goodleads.club/mcp`
  [![GoodLeads MCP connector](https://glama.ai/mcp/connectors/club.goodleads/new-business-owner-contacts/badges/score.svg)](https://glama.ai/mcp/connectors/club.goodleads/new-business-owner-contacts)
  🔓 - Reach the owner of a newly formed business the morning after the state posts it, from the state's own filing.
- [HarborRank](https://harborrank.com/features/mcp) `https://app.harborrank.com/mcp`
  [![HarborRank MCP connector](https://glama.ai/mcp/connectors/com.harborrank/harborrank/badges/score.svg)](https://glama.ai/mcp/connectors/com.harborrank/harborrank)
  🔐 - Keyword metrics, live Google SERPs, backlinks, rank tracking, site audits and read-only Search Console data.
- [Hermoso](https://hermoso.ai) `https://app.hermoso.ai/mcp`
  [![Hermoso MCP connector](https://glama.ai/mcp/connectors/io.github.hermoso-ai/hermoso/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.hermoso-ai/hermoso)
  🔓 - Research competitor ads, generate image and video ads, schedule social posts and run paid ad campaigns.

- [iMario](https://imario.ai) `https://mcp.imario.ai/mcp`
  [![iMario MCP connector](https://glama.ai/mcp/connectors/ai.imario/imario/badges/score.svg)](https://glama.ai/mcp/connectors/ai.imario/imario)
  🔐 - Ask synthetic audiences built from real people how they react to copy, pages, prices and images.

- [IndustryLens](https://industry-lens.com) `https://api.industry-lens.com/mcp/public`
  [![IndustryLens MCP connector](https://glama.ai/mcp/connectors/com.industry-lens/mcp-public/badges/score.svg)](https://glama.ai/mcp/connectors/com.industry-lens/mcp-public)
  🔓 - Competitive intelligence on B2B SaaS markets: competitor profiles, strategic moves, pricing changes and reports.
  
- [Layrcake](https://layrcake.dev) `https://mcp.layrcake.dev/mcp`
  [![Layrcake MCP connector](https://glama.ai/mcp/connectors/dev.layrcake.mcp/layrcake/badges/score.svg)](https://glama.ai/mcp/connectors/dev.layrcake.mcp/layrcake)
  🔐 - Find leads, enrich them to verified emails, detect intent and launch human-approved campaigns.

- [Lekta](https://lekta.dev) `https://lekta.dev/mcp`
  [![Lekta MCP connector](https://glama.ai/mcp/connectors/dev.lekta/lektadev/badges/score.svg)](https://glama.ai/mcp/connectors/dev.lekta/lektadev)
  🔓 - Audit a site's visibility in AI answer engines (AEO/GEO).
- [Limurse](https://limurse.ai/developers/mcp) `https://api.limurse.ai/mcp`
  [![Limurse MCP connector](https://glama.ai/mcp/connectors/ai.limurse/limurse/badges/score.svg)](https://glama.ai/mcp/connectors/ai.limurse/limurse)
  🔐 - Find bookable creators, benchmark market rates and draft campaign briefs; read-only, booking happens on Limurse.
- [LocationLists](https://locationlists.com) `https://locationlists.com/mcp`
  [![LocationLists MCP connector](https://glama.ai/mcp/connectors/io.github.kylehawke-stack/locationlists/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.kylehawke-stack/locationlists)
  🔓 - Search 725 US business-location datasets (dealers, contractors, chains), preview real rows, and buy CSVs.
- [LogoKit](https://logokit.com) `https://mcp.logokit.com/mcp`
  [![LogoKit MCP connector](https://glama.ai/mcp/connectors/com.logokit/brand-data/badges/score.svg)](https://glama.ai/mcp/connectors/com.logokit/brand-data)
  🔑 - Company logos, brand colors, and firmographic data by domain.
- [Loomaly](https://loomaly.com) `https://loomaly.com/mcp`
  [![Loomaly MCP connector](https://glama.ai/mcp/connectors/com.loomaly/loomaly/badges/score.svg)](https://glama.ai/mcp/connectors/com.loomaly/loomaly)
  🔐 - SEO audit of every page: a ranked fix list, a fix prompt for your framework, and a re-check once the fix is live.
- [Mailcoach](https://mailcoach.app) `https://mcp.mailcoach.app`
  🔐 - Read subscribers, campaigns, stats and email logs; create drafts and templates, and send test emails.
- [MailSenpai](https://www.mailsenpai.com) `https://mcp.mailsenpai.com/mcp`
  [![MailSenpai MCP connector](https://glama.ai/mcp/connectors/com.mailsenpai/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.mailsenpai/mcp)
  🔐 - Manage email marketing lists, subscribers, segments, templates, campaigns and stats (EU-hosted).
- [Mailzzy](https://mailzzy.com) `https://api.mailzzy.com/crm/mcp/`
  [![Mailzzy MCP connector](https://glama.ai/mcp/connectors/com.mailzzy/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.mailzzy/mcp)
  🔐 - Build audiences, draft and send email campaigns, manage contacts, segments and templates, and read campaign reports.
- [Maqui Analytics](https://somosmaqui.com/) `https://app.somosmaqui.com/api/mcp`
  [![Maqui Analytics MCP connector](https://glama.ai/mcp/connectors/io.github.luis-fuentes/maqui/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.luis-fuentes/maqui)
  🔐 - Read-only marketing analytics for client accounts, with a public synthetic demo via approved OAuth clients.
- [Mencoro](https://mencoro.com) `https://api.mencoro.com/mcp`
  [![Mencoro MCP connector](https://glama.ai/mcp/connectors/com.mencoro/mencoro/badges/score.svg)](https://glama.ai/mcp/connectors/com.mencoro/mencoro)
  🔐 - Track brand rank, mentions, sentiment and Share of Voice in ChatGPT, Perplexity and Google AI answers.
- [MentionAgent](https://mentionagent.ai/mcp/) `https://mentionagent.ai/mcp`
  [![MentionAgent MCP connector](https://glama.ai/mcp/connectors/ai.mentionagent/mentionagent/badges/score.svg)](https://glama.ai/mcp/connectors/ai.mentionagent/mentionagent)
  🔐 - Link building outreach from your agent: review drafts, approve the batch, answer publisher replies, record placements.
- [Mimiq](https://www.mimiqai.com) `https://mcp.mimiqai.com/mcp`
  [![Mimiq MCP connector](https://glama.ai/mcp/connectors/io.github.victorgulchenko/mimiq-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.victorgulchenko/mimiq-mcp)
  🔓 - Test landing pages, copy and sign-up flows on simulated customers who say why they would stay or leave.
- [Miraqo](https://miraqo.io) `https://app.miraqo.io/mcp`
  [![Miraqo MCP connector](https://glama.ai/mcp/connectors/io.github.deleteweb/seo/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.deleteweb/seo)
  🔐 - Rankings, audits, backlinks, Search Console and AI visibility for your Miraqo SEO projects.
- [nowyourlink](https://nowyourlink.com) `https://nowyourlink.com/mcp`
  [![nowyourlink MCP connector](https://glama.ai/mcp/connectors/io.github.ArneFfm/nowyourlink/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ArneFfm/nowyourlink)
  🔓 - Read the current daily homepage Spotlight ad and browse the archive of settled auction days.
- [NumberBroom](https://numberbroom.com/mcp-server) `https://numberbroom.com/mcp`
  [![NumberBroom MCP connector](https://glama.ai/mcp/connectors/io.github.cameron-creations/numberbroom-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.cameron-creations/numberbroom-mcp)
  🔓 - Check a US phone's line type, carrier and TCPA litigator status before dialing; tools need a prepaid key.
- [OnPage.dev](https://onpage.dev/mcp) `https://onpage.dev/mcp`
  [![OnPage.dev MCP connector](https://glama.ai/mcp/connectors/dev.onpage/onpage/badges/score.svg)](https://glama.ai/mcp/connectors/dev.onpage/onpage)
  🔓 - Free SEO and AI-visibility audits: scores, fixes, schema, robots.txt, redirects and 25-page site audits, no account.
- [PageLens](https://pagelens.io/docs/api) `https://app.pagelens.io/mcp`
  [![PageLens MCP connector](https://glama.ai/mcp/connectors/io.pagelens/pagelens/badges/score.svg)](https://glama.ai/mcp/connectors/io.pagelens/pagelens)
  🔓 - Web analytics for your site and which AI crawlers and assistants read it; tool calls need an API key.
- [Peak Answer](https://peakanswer.com) `https://peakanswer.com/api/mcp`
  [![Peak Answer MCP connector](https://glama.ai/mcp/connectors/com.peakanswer/peak-answer/badges/score.svg)](https://glama.ai/mcp/connectors/com.peakanswer/peak-answer)
  🔐 - Whether AI search recommends your brand, which buying questions competitors win, and the technical faults stopping engines reading you.
- [Plainrouter Sandbox](https://plainrouter.com/docs/mcp/setup) `https://plainrouter.com/mcp/sandbox`
  [![Plainrouter Sandbox MCP connector](https://glama.ai/mcp/connectors/com.plainrouter/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.plainrouter/mcp)
  🔓 - Test Meta advertising account, signal-health, and performance tools with synthetic data.
- [QRFLOW.codes](https://qrflow.codes) `https://qrflow.codes/mcp`
  [![QRFLOW.codes MCP connector](https://glama.ai/mcp/connectors/codes.qrflow/qrflow/badges/score.svg)](https://glama.ai/mcp/connectors/codes.qrflow/qrflow)
  🔐 - Create QR codes, re-point printed dynamic codes, name links on your own domain, and read scan analytics.
- [Ranla](https://ranla.ai) `https://mcp.ranla.ai/mcp`
  [![Ranla MCP connector](https://glama.ai/mcp/connectors/ai.ranla/ranla/badges/score.svg)](https://glama.ai/mcp/connectors/ai.ranla/ranla)
  🔐 - AI growth engineer for software businesses: ships SEO pages, gets you into AI answers, replies on Reddit, sends email.
- [Reach MCP](https://www.reachmcp.com) `https://app.reachmcp.com/mcp`
  [![Reach MCP connector](https://glama.ai/mcp/connectors/com.reachmcp/linkedin/badges/score.svg)](https://glama.ai/mcp/connectors/com.reachmcp/linkedin)
  🔐 - Operate a LinkedIn account: inbox, invitations, Sales Navigator search, posts; enforced daily quotas, webhooks.
- [RedReplier](https://redreplier.com) `https://mcp.redreplier.com/mcp`
  [![RedReplier MCP connector](https://glama.ai/mcp/connectors/com.redreplier/mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/com.redreplier/mcp-server)
  🔐 - Find Reddit, Hacker News, X and Bluesky posts mentioning your product, scored as leads.
- [Revup](https://revup.com/docs/mcp/) `https://revup.com/mcp`
  [![Revup MCP connector](https://glama.ai/mcp/connectors/com.revup/revup/badges/score.svg)](https://glama.ai/mcp/connectors/com.revup/revup)
  🔐 - Create, customize, preview and report on sweepstakes, contests, forms, surveys, quizzes and other promotions.
- [Rumoro](https://rumoro.dev/) `https://mcp.rumoro.dev/mcp`
  [![Rumoro MCP connector](https://glama.ai/mcp/connectors/dev.rumoro/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/dev.rumoro/mcp)
  🔓 - Track brand, competitor and topic mentions across 16 sources, scored for relevance and intent; tools need sign-in.
- [SearcherLite](https://searcherlite.com) `https://searcherlite.com/api/mcp`
  [![SearcherLite MCP connector](https://glama.ai/mcp/connectors/com.searcherlite/searcherlite/badges/score.svg)](https://glama.ai/mcp/connectors/com.searcherlite/searcherlite)
  🔐 - Google keyword, domain, backlink and AI-visibility data, paid per lookup in credits with no subscription.
- [Searcherries](https://searcherries.com) `https://app.searcherries.com/mcp/searcherries`
  [![Searcherries MCP connector](https://glama.ai/mcp/connectors/com.searcherries/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.searcherries/mcp)
  🔐 - Read-only AI visibility and SEO data: AI answers, competitors, citations, GSC, Bing, GA4.
- [SEO Expert: Digital Darts](https://www.digitaldarts.com.au/shopify-seo-expert-digital-darts-app/mcp) `https://seo.digitaldarts.com.au/mcp`
  [![SEO Expert: Digital Darts MCP connector](https://glama.ai/mcp/connectors/au.com.digitaldarts/seo-expert/badges/score.svg)](https://glama.ai/mcp/connectors/au.com.digitaldarts/seo-expert)
  🔐 - Audit a Shopify store's SEO and fix meta tags, alt text, structured data and broken links from chat.
- [Shipfound](https://www.shipfound.co/) `https://api.shipfound.co/mcp`
  [![Shipfound MCP connector](https://glama.ai/mcp/connectors/co.shipfound.api/shipfound/badges/score.svg)](https://glama.ai/mcp/connectors/co.shipfound.api/shipfound)
  🔐 - Site fixes, content briefs, indexing, AI crawler tracking and AI visibility checks for Claude Code and Codex.
- [Signal by StackEnhance](https://stackenhance.com/signal) `https://mcp.stackenhance.com/mcp`
  [![Signal by StackEnhance MCP connector](https://glama.ai/mcp/connectors/com.stackenhance/signal/badges/score.svg)](https://glama.ai/mcp/connectors/com.stackenhance/signal)
  🔓 - How often Nordic and German e-commerce brands send marketing email: send counts, dates and the most active senders.
- [Spytrend](https://spytrend.com/mcp/?utm_source=awesome-remote-mcp&utm_medium=directory&utm_campaign=mcp-launch) `https://mcp.spytrend.com/mcp`
  [![Spytrend MCP connector](https://glama.ai/mcp/connectors/com.spytrend/spytrend/badges/score.svg)](https://glama.ai/mcp/connectors/com.spytrend/spytrend)
  🔐 - Search Meta and TikTok ads, find the advertisers behind them, and rank what is scaling.
- [Statable](https://statable.com) `https://mcp.statable.com/mcp`
  [![Statable MCP connector](https://glama.ai/mcp/connectors/com.statable/analytics/badges/score.svg)](https://glama.ai/mcp/connectors/com.statable/analytics)
  🔐 - Cookieless, EU-hosted web analytics: visitors, pages, sources, countries, goals, funnels and live traffic.
- [SubmitMyStartup](https://submitmystartup.com/) `https://submitmystartup.com/mcp`
  [![SubmitMyStartup MCP connector](https://glama.ai/mcp/connectors/com.submitmystartup/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.submitmystartup/mcp)
  🔓 - Searches a free list of startup directories and launch sites with real submission results.
- [Subtraq](https://subtraq.co) `https://subtraq.co/api/mcp`
  [![Subtraq MCP connector](https://glama.ai/mcp/connectors/co.subtraq/subtraq/badges/score.svg)](https://glama.ai/mcp/connectors/co.subtraq/subtraq)
  🔓 - Create short links, track clicks and attribute sales to the placement that brought them; tools need a key.
- [Superflow Free Tools](https://usesuperflow.ai/tools) `https://usesuperflow.ai/api/mcp`
  [![Superflow Free Tools MCP connector](https://glama.ai/mcp/connectors/ai.usesuperflow/tools/badges/score.svg)](https://glama.ai/mcp/connectors/ai.usesuperflow/tools)
  🔓 - Free website QA and AI-visibility checks: AI crawlability, robots.txt, llms.txt, JSON-LD and social previews.
- [SurfacedBy AI Visibility & GEO Audit](https://surfacedby.com/tools/chatgpt-ai-visibility) `https://api.surfacedby.com/api/v1/mcp/public/`
  [![SurfacedBy AI Visibility & GEO Audit MCP connector](https://glama.ai/mcp/connectors/com.surfacedby/ai-visibility/badges/score.svg)](https://glama.ai/mcp/connectors/com.surfacedby/ai-visibility)
  🔓 - Free AI visibility and GEO audit: see what AI reads on your site and whether its answers cite you.
- [The Profound Agency](https://theprofound.agency/mcp/) `https://theprofound.agency/api/mcp/`
  [![The Profound Agency MCP connector](https://glama.ai/mcp/connectors/agency.theprofound/the-profound-agency/badges/score.svg)](https://glama.ai/mcp/connectors/agency.theprofound/the-profound-agency)
  🔓 - Search, price, and order press placements across 1,600+ publications; free AI-visibility audits.

- [TheQRCode.io](https://theqrcode.io/mcp) `https://mcp.theqrcode.io/mcp`
  [![TheQRCode.io MCP connector](https://glama.ai/mcp/connectors/io.theqrcode/qr-code-generator/badges/score.svg)](https://glama.ai/mcp/connectors/io.theqrcode/qr-code-generator)
  🔓 - Generate QR codes, list saved codes, and read scan analytics by time, device and approximate location.
- [UGCfy AI](https://ugcfy.ai/mcp) `https://ugcfy.ai/api/mcp`
  [![UGCfy AI MCP connector](https://glama.ai/mcp/connectors/ai.ugcfy/ugcfy-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/ai.ugcfy/ugcfy-mcp)
  🔓 - Break down a TikTok or Reels ad and rewrite it for your product, plus UGC hooks, scripts and CPM.
- [VertoDigital](https://vertodigital.com) `https://mcp.vertodigital.com/mcp`
  [![VertoDigital MCP Server MCP connector](https://glama.ai/mcp/connectors/com.vertodigital/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.vertodigital/mcp)
  🔓 - B2B pipeline marketing agency: match challenges to services, search case studies, read pages, send enquiries.
- [Vibe Prospecting](https://vibeprospecting.ai) `https://vibeprospecting.explorium.ai/mcp`
  🔐 - Search companies and contacts, enrich lead lists, and research B2B business signals.
- [WebAsk](https://webask.io/) `https://mcp.webask.io/mcp/v1`
  [![WebAsk MCP connector](https://glama.ai/mcp/connectors/io.webask.mcp/web-ask-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.webask.mcp/web-ask-mcp)
  🔑 - Create surveys and quizzes, manage responses, and generate reports from AI assistants.
- [Wrendex](https://wrendex.com) `https://app.wrendex.com/mcp`
  [![Wrendex MCP connector](https://glama.ai/mcp/connectors/com.wrendex.app/wrendex/badges/score.svg)](https://glama.ai/mcp/connectors/com.wrendex.app/wrendex)
  🔓 - Technical SEO audits: crawl a site with 140+ checks and read the fix list; tool calls take a free Wrendex token.
- [Zebu Data - Customer Reviews](https://apify.com/delicious_zebu) `https://mcp.apify.com/?tools=delicious_zebu/google-maps-store-review-scraper,delicious_zebu/yelp-reviews-scraper,delicious_zebu/tripadvisor-review-collector,delicious_zebu/ebay-product-reviews-scraper-with-advanced-filters,delicious_zebu/naver-shopping-reviews-scraper,delicious_zebu/coupang-reviews-scraper`
  [![Zebu Data - Customer Reviews MCP connector](https://glama.ai/mcp/connectors/io.github.zebudata/customer-reviews/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.zebudata/customer-reviews)
  🔐 - Reviews from Google Maps, Yelp, TripAdvisor, eBay, Naver and Coupang, with ratings and dates.

### 📊 <a name="monitoring"></a>Monitoring

- [APIzone](https://apizone.io) `https://apizone.io/api/mcp`
  🔓 - Check whether any of 294 third-party APIs is down, with uptime history and recent outages.
- [Baromio](https://baromio.io/en/ai-agents) `https://baromio.io/mcp`
  [![Baromio MCP connector](https://glama.ai/mcp/connectors/io.baromio/baromio/badges/score.svg)](https://glama.ai/mcp/connectors/io.baromio/baromio)
  🔐 - Read uptime, incidents, SSL, domain expiry and Core Web Vitals; create, edit and pause monitors on paid plans.
- [Cloudflare Observability](https://developers.cloudflare.com) `https://observability.mcp.cloudflare.com/mcp`
  🔐 - Query Workers logs, analytics, and error events.
- [Codex Reset](https://codex-reset.com/developers) `https://codex-reset.com/mcp`
  [![Codex Reset MCP connector](https://glama.ai/mcp/connectors/com.codex-reset/codex-reset/badges/score.svg)](https://glama.ai/mcp/connectors/com.codex-reset/codex-reset)
  🔓 - Codex usage-limit reset odds for the next 24/48h, past resets and Codex service status.
- [EventSend](https://eventsend.io) `https://eventsend.io/mcp`
  [![EventSend MCP connector](https://glama.ai/mcp/connectors/io.eventsend/eventsend/badges/score.svg)](https://glama.ai/mcp/connectors/io.eventsend/eventsend)
  🔐 - Query your product's event history, delivery health and plan usage, e.g. what failed in checkout today.
- [Everframe](https://everframe.dev) `https://everframe.dev/mcp`
  [![Everframe MCP connector](https://glama.ai/mcp/connectors/dev.everframe/everframe/badges/score.svg)](https://glama.ai/mcp/connectors/dev.everframe/everframe)
  🔐 - Read in-app bug reports, crashes and tickets with screenshots, console, network and device context.
- [Flowsery](https://flowsery.com) `https://mcp.flowsery.com/mcp`
  [![Flowsery MCP connector](https://glama.ai/mcp/connectors/com.flowsery/mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/com.flowsery/mcp-server)
  🔐 - Web analytics, revenue attribution, visitor profiles and AI-found bugs from session recordings.
- [Grafana](https://grafana.com) `https://mcp.grafana.com/mcp`
  [![Grafana MCP connector](https://glama.ai/mcp/connectors/io.github.grafana/mcp-grafana/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.grafana/mcp-grafana)
  🔐 - Query Grafana dashboards, datasources, and alerts.
- [Hoot Lens](https://hootlens.com) `https://mcp.hootlens.com/mcp`
  [![Hoot Lens MCP connector](https://glama.ai/mcp/connectors/com.hootlens/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.hootlens/mcp)
  🔐 - Session replay and click heatmaps for agents: timed visit narratives, repeated or dead clicks, errors and change impact.
- [HTTPStatus](https://httpstatus.com/mcp/) `https://mcp.httpstatus.com/mcp`
  [![HTTPStatus MCP connector](https://glama.ai/mcp/connectors/com.httpstatus/mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/com.httpstatus/mcp-server)
  🔐 - Create API mocks and run tests, security checks, automation workflows, and uptime monitors.
- [is it DNS?](https://isitdns.net) `https://isitdns.net/mcp`
  [![is it DNS? MCP connector](https://glama.ai/mcp/connectors/net.isitdns/isitdns/badges/score.svg)](https://glama.ai/mcp/connectors/net.isitdns/isitdns)
  🔓 - Dig any public resolver, audit or sweep a domain, walk a delegation, read the live resolver board; no key.
- [MCPulse](https://getmcpulse.com) `https://api.getmcpulse.com/mcp`
  [![MCPulse MCP connector](https://glama.ai/mcp/connectors/com.getmcpulse.api/mcpulse/badges/score.svg)](https://glama.ai/mcp/connectors/com.getmcpulse.api/mcpulse)
  🔐 - Query your own MCP server's tool calls, first-call success, retries, empty results, and schema cost.
- [Ned Watch](https://ned.watch) `https://api.ned.watch/mcp`
  [![Ned Watch MCP connector](https://glama.ai/mcp/connectors/watch.ned/ned-watch/badges/score.svg)](https://glama.ai/mcp/connectors/watch.ned/ned-watch)
  🔓 - Know when your agent silently stops: deadman, overrun, HTTP, TLS and content watches; the first call issues a key.
- [nimo](https://heynimo.com) `https://api.heynimo.com/try-mcp`
  [![nimo MCP connector](https://glama.ai/mcp/connectors/com.heynimo.api/nimo/badges/score.svg)](https://glama.ai/mcp/connectors/com.heynimo.api/nimo)
  🔓 - Check public pages' speed and Core Web Vitals and get the next fix without an account; paid plans add uptime alerts.
- [NotWorking](https://notworking.io) `https://notworking.io/mcp`
  [![NotWorking MCP connector](https://glama.ai/mcp/connectors/io.notworking/notworking/badges/score.svg)](https://glama.ai/mcp/connectors/io.notworking/notworking)
  🔓 - Check if other agents report a site, skill or MCP server failing, see its other access paths, and report failures.
- [Relvato](https://www.relvato.com/developers) `https://app.relvato.com/api/mcp`
  [![Relvato MCP connector](https://glama.ai/mcp/connectors/com.relvato/relvato/badges/score.svg)](https://glama.ai/mcp/connectors/com.relvato/relvato)
  🔓 - Real-browser website monitoring, deepest on WordPress & WooCommerce: run checks, read results; tools need a free key.
- [Rootly](https://rootly.com) `https://mcp.rootly.com/mcp`
  🔐 - Manage Rootly incidents, alerts, and on-call schedules.
- [RunVouch](https://runvouch.com) `https://api.runvouch.com/mcp`
  [![RunVouch MCP connector](https://glama.ai/mcp/connectors/com.runvouch/runvouch/badges/score.svg)](https://glama.ai/mcp/connectors/com.runvouch/runvouch)
  🔓 - Find out why an unattended run stalled or failed and read tamper-evident proof; needs a free key.
- [Sentry](https://sentry.io) `https://mcp.sentry.dev/mcp`
  [![Sentry MCP connector](https://glama.ai/mcp/connectors/dev.sentry.mcp/sentry/badges/score.svg)](https://glama.ai/mcp/connectors/dev.sentry.mcp/sentry)
  🔐 - Investigate Sentry issues, events, and releases, and run Seer root-cause analysis.
- [Tá Rodando](https://tarodando.com.br) `https://tarodando.com.br/mcp`
  [![Tá Rodando MCP connector](https://glama.ai/mcp/connectors/br.com.tarodando/ta-rodando/badges/score.svg)](https://glama.ai/mcp/connectors/br.com.tarodando/ta-rodando)
  🔐 - Manage uptime monitors, alert channels and a PT-BR public status page from your agent.
- [Toolweather](https://toolweather.pages.dev) `https://toolweather.toolweather.workers.dev/mcp`
  [![Toolweather MCP connector](https://glama.ai/mcp/connectors/io.github.toolweather/toolweather/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.toolweather/toolweather)
  🔓 - Checks if an MCP server or tool is safe to call now and suggests alternatives. Calls need a free API key.
- [Uptimepage](https://uptimepage.dev/mcp-server) `https://mcp.uptimepage.dev/mcp`
  [![Uptimepage MCP connector](https://glama.ai/mcp/connectors/dev.uptimepage/uptimepage/badges/score.svg)](https://glama.ai/mcp/connectors/dev.uptimepage/uptimepage)
  🔓 - Read monitors and incidents, run checks, create monitors and status pages, post incident updates. Calls need OAuth.
- [Vivere](https://vivere.dev) `https://vivere.dev/mcp`
  [![Vivere MCP connector](https://glama.ai/mcp/connectors/dev.vivere/monitors/badges/score.svg)](https://glama.ai/mcp/connectors/dev.vivere/monitors)
  🔓 - Cron and heartbeat monitoring: create monitors and check in on each run; tools need a key.

### 🎥 <a name="multimedia"></a>Multimedia

- [Arcmira: YouTube Transcript Search](https://arcmira.com/docs) `https://mcp.arcmira.com/mcp`
  [![Arcmira MCP connector](https://glama.ai/mcp/connectors/io.github.arcmira/arcmira/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.arcmira/arcmira)
  🔐 - Search YouTube transcripts for timestamped quotes, speaker appearances, sponsors and recommendations.
- [Artyfile](https://artyfile.com) `https://artyfile.com/api/mcp`
  [![Artyfile MCP connector](https://glama.ai/mcp/connectors/com.artyfile/music-licensing/badges/score.svg)](https://glama.ai/mcp/connectors/com.artyfile/music-licensing)
  🔓 - Search real recorded music, check licence terms and prepare a one-time sync-licence checkout for a track.
- [Azurade AI](https://azurade.com/developers/) `https://azurade.com/mcp`
  [![Azurade AI MCP connector](https://glama.ai/mcp/connectors/com.azurade/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.azurade/mcp)
  🔐 - Generate images and videos with Veo 3.1, Seedance 2.5, Nano Banana Pro and 30+ more models; credits never expire.
- [BulkTranscripts](https://bulktranscripts.co) `https://bulktranscripts.co/mcp`
  [![BulkTranscripts MCP connector](https://glama.ai/mcp/connectors/co.bulktranscripts/youtube/badges/score.svg)](https://glama.ai/mcp/connectors/co.bulktranscripts/youtube)
  🔐 - YouTube transcripts for one video, a whole channel or a playlist, plus search and free new-upload tracking.
- [CLIPCLIPER](https://clipcliper.com/mcp) `https://clipcliper.com/mcp`
  [![CLIPCLIPER MCP connector](https://glama.ai/mcp/connectors/com.clipcliper/clipcliper/badges/score.svg)](https://glama.ai/mcp/connectors/com.clipcliper/clipcliper)
  🔓 - Timestamped transcripts, chapters and clip ideas from YouTube, Twitch, Kick or TikTok links.
- [ClipUGC](https://clipugc.com) `https://clipugc.com/mcp`
  [![ClipUGC MCP connector](https://glama.ai/mcp/connectors/io.github.clipugc/clipugc/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.clipugc/clipugc)
  🔐 - Make UGC videos for mobile apps with AI influencers who keep the same face.
- [CWI Discovery Engine](https://github.com/CumulativeWebInc/cwi-learn) `https://cwi-machine-data.hp-ace.workers.dev/mcp`
  [![CWI Discovery Engine MCP connector](https://glama.ai/mcp/connectors/io.github.CumulativeWebInc/cwi-discovery-engine/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.CumulativeWebInc/cwi-discovery-engine)
  🔓 - Machine-readable catalog of the Cumulative Web Inc label: track search, sync briefs, live Radio 365, playlist pitching.
- [Dora](https://doravideo.com) `https://doravideo.com/mcp`
  [![Dora MCP connector](https://glama.ai/mcp/connectors/io.github.Saga-Labs/dora-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Saga-Labs/dora-mcp)
  🔐 - Generate finished AI videos and images from a prompt or a photo.
- [FXI Studio](https://www.fxi.studio/mcp/info) `https://mcp.fxi.studio/mcp`
  [![FXI Studio MCP connector](https://glama.ai/mcp/connectors/io.github.fueledximagination/fxi-studio/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.fueledximagination/fxi-studio)
  🔐 - Generate cinematic images and video clips and frame-chain shots into continuous motion, billed to your FXI credits.
- [GrowingUpVideo](https://growingupvideo.com) `https://growingupvideo.com/mcp`
  [![GrowingUpVideo MCP connector](https://glama.ai/mcp/connectors/com.growingupvideo/growingupvideo/badges/score.svg)](https://glama.ai/mcp/connectors/com.growingupvideo/growingupvideo)
  🔓 - Prices, photo tips and a start link for AI growing-up morph videos made from photos across the years.
- [Incarn](https://www.incarn.co/developers) `https://api.incarn.co/mcp`
  [![Incarn MCP connector](https://glama.ai/mcp/connectors/co.incarn/photo-animation/badges/score.svg)](https://glama.ai/mcp/connectors/co.incarn/photo-animation)
  🔓 - Animate old family photos and ancestor portraits into short lifelike videos.
- [invideo](https://invideo.io) `https://mcp.invideo.io/mcp`
  🔓 - Generate and edit videos from a prompt.
- [Kinetune](https://kinetune.com/developers#mcp) `https://kinetune.com/mcp`
  [![Kinetune MCP connector](https://glama.ai/mcp/connectors/com.kinetune/kinetune/badges/score.svg)](https://glama.ai/mcp/connectors/com.kinetune/kinetune)
  🔐 - Word-synced lyric videos (9:16, 16:9, 1:1) and Spotify Canvas loops from your songs, quoted in credits first.
- [Kleo](https://kleooai.com) `https://mcp.kleooai.com/mcp`
  [![Kleo MCP connector](https://glama.ai/mcp/connectors/com.kleooai/kleo/badges/score.svg)](https://glama.ai/mcp/connectors/com.kleooai/kleo)
  🔐 - Narrated 4K 60 fps films from a brief, realistic or animated, with every shot generated.
- [Katto](https://katto.tech) `https://mcp.katto.tech/mcp`
  🔐 - Turn long videos, podcasts and Twitch VODs into scored, captioned, vertical 9:16 clips.
- [Klox](https://klox.ai/agent) `https://klox.ai/mcp`
  [![Klox MCP connector](https://glama.ai/mcp/connectors/ai.klox/klox/badges/score.svg)](https://glama.ai/mcp/connectors/ai.klox/klox)
  🔐 - Plan and edit AI videos on canvases: script, storyboard, shots and final cut.
- [MaxVideoAI](https://maxvideoai.com/mcp) `https://api.maxvideoai.com/mcp`
  [![MaxVideoAI MCP connector](https://glama.ai/mcp/connectors/com.maxvideoai/maxvideoai/badges/score.svg)](https://glama.ai/mcp/connectors/com.maxvideoai/maxvideoai)
  🔐 - Compare AI video models, quote requests, approve paid generations, and recover results in a shared library.
- [MockClip](https://mockclip.com/integrations) `https://mockclip.com/api/mcp`
  [![MockClip MCP connector](https://glama.ai/mcp/connectors/com.mockclip/mockclip/badges/score.svg)](https://glama.ai/mcp/connectors/com.mockclip/mockclip)
  🔑 - Create fake chat and phone-screen videos (WhatsApp, iMessage, ChatGPT, Discord, Tinder, Reddit) as MP4.
- [Phoenix Labs](https://phoenixlabs.space/developers) `https://api.phoenixlabs.space/mcp`
  [![Phoenix Labs MCP connector](https://glama.ai/mcp/connectors/io.github.thekillsquad007/phoenix-labs/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.thekillsquad007/phoenix-labs)
  🔐 - Restore old video and turn stills into clips with sound; you approve a spending limit, top-ups by card or USDC.
- [Pixly](https://pixly.app) `https://pixly.app/api/mcp`
  [![Pixly MCP connector](https://glama.ai/mcp/connectors/app.pixly/pixly/badges/score.svg)](https://glama.ai/mcp/connectors/app.pixly/pixly)
  🔓 - Stage, declutter, and enhance real-estate listing photos, and turn them into listing videos.
- [Qencode](https://qencode.com) `https://mcp.qencode.com/mcp`
  [![Qencode MCP connector](https://glama.ai/mcp/connectors/com.qencode/qencode/badges/score.svg)](https://glama.ai/mcp/connectors/com.qencode/qencode)
  🔐 - Transcode video to HLS/MP4, monitor jobs, and manage Qencode Media Storage.
- [QQuickpick](https://qquickpick.com/agents/mcp) `https://qquickpick.com/mcp`
  [![QQuickpick MCP connector](https://glama.ai/mcp/connectors/io.github.Ravesteijntjes/qquickpick/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Ravesteijntjes/qquickpick)
  🔓 - Search movies and TV shows by mood, genre and score, filtered to what streams in your country.
- [RaoMusic](https://www.raomusic.com/plugin) `https://www.raomusic.com/api/mcp`
  [![RaoMusic MCP connector](https://glama.ai/mcp/connectors/io.github.raomusic/raomusic/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.raomusic/raomusic)
  🔐 - Generate full songs with vocals, instrumentals and sound effects from text, quoted in credits first.
- [SceneF](https://scenef.com/agents) `https://scenef.com/mcp`
  [![SceneF MCP connector](https://glama.ai/mcp/connectors/com.scenef/showtimes/badges/score.svg)](https://glama.ai/mcp/connectors/com.scenef/showtimes)
  🔓 - Movie showtimes across 33 California and Hawaii boards, re-verified against each theater's own calendar.
- [Screen Browser](https://screenbrowser.com) `https://mcp.screenbrowser.com`
  [![Screen Browser MCP connector](https://glama.ai/mcp/connectors/com.screenbrowser/screenbrowser/badges/score.svg)](https://glama.ai/mcp/connectors/com.screenbrowser/screenbrowser)
  🔐 - Records narrated demo and tutorial videos of your web app from a plain-language guide, on desktop or as a phone.
- [ScreenWeaver](https://www.screenweaver.ai/mcp) `https://app.screenweaver.ai/api/mcp`
  [![ScreenWeaver MCP connector](https://glama.ai/mcp/connectors/ai.screenweaver/screenweaver/badges/score.svg)](https://glama.ai/mcp/connectors/ai.screenweaver/screenweaver)
  🔐 - Write and edit screenplays, import Final Draft or Fountain scripts and turn scenes or comic pages into storyboard shots.
- [SFXMint](https://sfxmint.com) `https://sfxmint.com/mcp`
  [![SFXMint MCP connector](https://glama.ai/mcp/connectors/com.sfxmint/sounds/badges/score.svg)](https://glama.ai/mcp/connectors/com.sfxmint/sounds)
  🔓 - Ask for a sound effect by role or take a ready-made kit; 4,600+ CC0 files with permanent hotlinkable URLs.
- [StudioSphere Pulse](https://pulse.studiosphere.space) `https://mcp.studiosphere.space/mcp`
  [![StudioSphere Pulse MCP connector](https://glama.ai/mcp/connectors/space.studiosphere/pulse/badges/score.svg)](https://glama.ai/mcp/connectors/space.studiosphere/pulse)
  🔓 - Audio analysis for authorized public URLs: BPM, musical key, and waveform peaks.
- [Transkriba](https://transkriba.ru/mcp) `https://transkriba.ru/api/mcp`
  [![Transkriba MCP connector](https://glama.ai/mcp/connectors/ru.transkriba/transcription/badges/score.svg)](https://glama.ai/mcp/connectors/ru.transkriba/transcription)
  🔓 - Transcribe Russian audio and video from files or URLs; tools need a key.
- [Treza](https://www.trezalabs.com/connect) `https://www.trezalabs.com/api/mcp`
  [![Treza MCP connector](https://glama.ai/mcp/connectors/io.github.treza-labs/treza/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.treza-labs/treza)
  🔐 - Video pipelines that script, render, narrate, caption and publish to YouTube and TikTok.
- [txtreel](https://txtreel.com) `https://txtreel.com/mcp`
  [![txtreel MCP connector](https://glama.ai/mcp/connectors/com.txtreel/txtreel/badges/score.svg)](https://glama.ai/mcp/connectors/com.txtreel/txtreel)
  🔓 - Render iMessage, WhatsApp, Instagram DM and Reddit thread videos (1080x1920 MP4) or screenshots from a script.
- [Upstream.so](https://upstream.so/mcp/) `https://studio.upstream.so/mcp`
  [![Upstream.so MCP connector](https://glama.ai/mcp/connectors/so.upstream.studio/upstreamso/badges/score.svg)](https://glama.ai/mcp/connectors/so.upstream.studio/upstreamso)
  🔐 - Manage 24/7 live channels, pre-recorded broadcasts, media, playlists, schedules, and multistreaming from AI assistants.
- [Uttera](https://uttera.ai) `https://mcp.uttera.ai/mcp`
  [![Uttera MCP connector](https://glama.ai/mcp/connectors/ai.uttera/uttera/badges/score.svg)](https://glama.ai/mcp/connectors/ai.uttera/uttera)
  🔐 - Transcribe and summarise recordings, and generate speech in 30 languages, sound effects and music.
- [Valmera](https://valmera.io) `https://valmera.io/mcp/server`
  [![Valmera MCP connector](https://glama.ai/mcp/connectors/io.valmera/video-editor/badges/score.svg)](https://glama.ai/mcp/connectors/io.valmera/video-editor)
  🔐 - Edit your own footage: cut dead air and filler words, caption, reframe to 9:16, make shorts and export MP4.
- [VideoGen](https://videogen.io/videogen-mcp) `https://mcp.videogen.io/mcp`
  [![VideoGen MCP connector](https://glama.ai/mcp/connectors/io.github.dg314/videogen/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.dg314/videogen)
  🔐 - Create videos from scripts and storyboards, manage projects, and export finished videos.
- [Zebu Data - YouTube Data & Transcripts](https://apify.com/delicious_zebu) `https://mcp.apify.com/?tools=delicious_zebu/youtube-video-scraper-by-keyword,delicious_zebu/youtube-channel-video-scraper,delicious_zebu/youtube-video-data-scraper,delicious_zebu/youtube-comments-replies-scraper,delicious_zebu/youtube-transcript-scraper`
  [![Zebu Data - YouTube Data & Transcripts MCP connector](https://glama.ai/mcp/connectors/io.github.zebudata/youtube-data/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.zebudata/youtube-data)
  🔐 - YouTube search, whole channels, video stats, comments and full transcripts with timestamps.
- [ZoneFoundry for Sonos](https://zonefoundry.dev/guides/ai-agent-control/) `https://relay.zonefoundry.dev/mcp`
  [![ZoneFoundry for Sonos MCP connector](https://glama.ai/mcp/connectors/dev.zonefoundry/sonos/badges/score.svg)](https://glama.ai/mcp/connectors/dev.zonefoundry/sonos)
  🔐 - Control your Sonos speakers: play music, set volume, group rooms, move playback, announcements and reminders.

### 💳 <a name="payments"></a>Payments

- [Aether](https://explorer.157-245-252-221.sslip.io) `https://explorer.157-245-252-221.sslip.io/mcp`
  [![Aether MCP connector](https://glama.ai/mcp/connectors/io.github.whoyoujoshin/aether-wallet/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.whoyoujoshin/aether-wallet)
  🔓 - Read-only view of the Aether testnet: balances, transactions, miners and its directory of x402-paid services.
- [AurasPay](https://auraspay.com/mcp) `https://mcp.auraspay.com/api/mcp`
  [![AurasPay MCP connector](https://glama.ai/mcp/connectors/com.auraspay/merchant-payments/badges/score.svg)](https://glama.ai/mcp/connectors/com.auraspay/merchant-payments)
  🔐 - Review merchant payments and prepare payment links with separate human approval for changes.
- [AssetFare](https://assetfare.dev) `https://api.assetfare.dev/mcp`
  [![AssetFare MCP connector](https://glama.ai/mcp/connectors/io.github.odaiin/assetfare/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.odaiin/assetfare)
  🔓 - Compare and prepare non-custodial SOL to Base or Arbitrum ETH routes for you to sign.
- [Dodo Payments](https://dodopayments.com) `https://mcp.dodopayments.com/mcp`
  🔐 - Manage Dodo Payments products, subscriptions, and payouts.
- [Lumière PayCheck](https://lumierepaycheck.org) `https://lumierepaycheck.org/mcp`
  [![Lumière PayCheck MCP connector](https://glama.ai/mcp/connectors/io.github.Book0fEli/paycheck/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Book0fEli/paycheck)
  🔓 - Check an x402 endpoint, price and payout wallet before an agent pays: trust grade, verdict and hijack checks.
- [Paddle](https://paddle.com) `https://mcp.paddle.com/mcp`
  🔐 - Manage Paddle products, prices, subscriptions, and transactions.
- [PayPal](https://paypal.com) `https://mcp.paypal.com/mcp`
  🔐 - Create and manage PayPal invoices, orders, and payments.
- [Pink Agentic AI Payments](https://pinkwallet.com/agentic/) `https://agentic-sandbox.pinkwallet.com/mcp`
  [![Pink Agentic AI Payments MCP connector](https://glama.ai/mcp/connectors/com.pinkwallet/agentic-payments-sandbox/badges/score.svg)](https://glama.ai/mcp/connectors/com.pinkwallet/agentic-payments-sandbox)
  🔐 - Approval layer for AI agent payments: per-agent budgets and rules allow, ask a human, or block; test-money sandbox.
- [send21](https://send21.io) `https://send21.io/mcp`
  [![send21 MCP connector](https://glama.ai/mcp/connectors/io.github.send21io/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.send21io/mcp)
  🔓 - Prepares non-custodial payment drafts and pay links; payer signs in their own wallet.
- [SpendPreflight](https://spendpreflight.com) `https://api.spendpreflight.com/mcp`
  [![SpendPreflight MCP connector](https://glama.ai/mcp/connectors/com.spendpreflight.api/spend-preflight/badges/score.svg)](https://glama.ai/mcp/connectors/com.spendpreflight.api/spend-preflight)
  🔓 - Operated by SpendPreflight: sanctions screening and payment preflight, paid via x402 with a free trial.
- [Square](https://squareup.com) `https://mcp.squareup.com/mcp`
  🔐 - Manage Square catalog, orders, payments, and customers.
- [Stripe](https://stripe.com) `https://mcp.stripe.com`
  [![Stripe MCP connector](https://glama.ai/mcp/connectors/com.stripe/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.stripe/mcp)
  🔐 - Manage Stripe customers, products, prices, invoices, and payments.
- [Teppi](https://teppi.xyz) `https://api.teppi.xyz/mcp`
  [![Teppi MCP connector](https://glama.ai/mcp/connectors/xyz.teppi/teppi/badges/score.svg)](https://glama.ai/mcp/connectors/xyz.teppi/teppi)
  🔓 - Before paying an x402 endpoint or MCP server, read what paying it delivered: checked, signed, reproducible.
- [Veyra](https://veyra.money) `https://veyra.money/api/mcp`
  [![Veyra MCP connector](https://glama.ai/mcp/connectors/money.veyra/veyra/badges/score.svg)](https://glama.ai/mcp/connectors/money.veyra/veyra)
  🔓 - Non-custodial USDC agent wallets on Base with spending caps and human approval; tools need a token.
- [x402 Preflight](https://x402.chikocorp.com) `https://x402.chikocorp.com/mcp`
  [![x402 Preflight MCP connector](https://glama.ai/mcp/connectors/io.github.chico10117/x402-preflight/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.chico10117/x402-preflight)
  🔓 - Inspect x402/Base USDC payment endpoints and order fixed-price remediation through paid tools.

### 📋 <a name="project-management"></a>Project Management

- [AgileHero](https://agilehero.io) `https://mcp.agilehero.io/mcp`
  [![AgileHero MCP connector](https://glama.ai/mcp/connectors/io.agilehero/agilehero/badges/score.svg)](https://glama.ai/mcp/connectors/io.agilehero/agilehero)
  🔐 - Manage agile boards, epics, roadmaps, retrospectives, whiteboards, and wiki pages.
- [Asana](https://asana.com) `https://mcp.asana.com/mcp`
  🔐 - Manage Asana tasks, projects, and portfolios.
- [Atlassian](https://atlassian.com) `https://mcp.atlassian.com/v1/mcp`
  [![Atlassian MCP connector](https://glama.ai/mcp/connectors/com.atlassian/atlassian-mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/com.atlassian/atlassian-mcp-server)
  🔐 - Work with Jira issues and Confluence pages.
- [ClickUp](https://clickup.com) `https://mcp.clickup.com/mcp`
  🔐 - Manage ClickUp tasks, docs, and spaces.
- [dot•requirements](https://dotrequirements.io) `https://app.dotrequirements.io/mcp`
  [![dot•requirements MCP connector](https://glama.ai/mcp/connectors/io.dotrequirements/dotrequirements/badges/score.svg)](https://glama.ai/mcp/connectors/io.dotrequirements/dotrequirements)
  🔐 - Draft testable requirements specs from chat, style-check them, publish to your team, and see test coverage.
- [Edworking MCP](https://mcp.edworking.com) `https://mcp.edworking.com/mcp`
  [![Edworking MCP connector](https://glama.ai/mcp/connectors/io.github.Edworking/edworking-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Edworking/edworking-mcp)
  🔐 - Read and manage Edworking projects, tasks, conversations and files with scoped access.
- [FrameOn](https://app.frameonlab.com/mcp) `https://api.frameonlab.com/api/v1/mcp`
  [![FrameOn MCP connector](https://glama.ai/mcp/connectors/com.frameonlab/frameon/badges/score.svg)](https://glama.ai/mcp/connectors/com.frameonlab/frameon)
  🔐 - Project management for AI agents: tasks, docs, decisions and time in one shared team context.
- [GTD Brain](https://gtdbrain.com/connect?source=awesome-remote-mcp-servers) `https://mcp.gtdbrain.com/api/gtdbrain/v1/mcp`
  [![GTD Brain MCP connector](https://glama.ai/mcp/connectors/com.gtdbrain/gtd-brain/badges/score.svg)](https://glama.ai/mcp/connectors/com.gtdbrain/gtd-brain)
  🔐 - Getting Things Done board: inbox capture, next actions by context, projects and weekly review.
- [Kaiku](https://kaiku.tech/en/docs/mcp) `https://mcp.kaiku.tech/mcp`
  [![Kaiku MCP connector](https://glama.ai/mcp/connectors/tech.kaiku.mcp/kaiku/badges/score.svg)](https://glama.ai/mcp/connectors/tech.kaiku.mcp/kaiku)
  🔓 - Issue tracker with a wiki for people and AI agents: search, file and update issues, comment, read and write pages.
- [Laraue Boards](https://boards.laraue.com) `https://boards.laraue.com/boards-mcp/mcp`
  [![Laraue Boards MCP connector](https://glama.ai/mcp/connectors/com.laraue/boards/badges/score.svg)](https://glama.ai/mcp/connectors/com.laraue/boards)
  🔑 - List, view, create, edit, and move issues in your Laraue Boards organization.
- [Linear](https://linear.app) `https://mcp.linear.app/mcp`
  [![Linear MCP connector](https://glama.ai/mcp/connectors/app.linear/linear/badges/score.svg)](https://glama.ai/mcp/connectors/app.linear/linear)
  🔐 - Manage Linear issues, projects, and cycles.
- [mcptask.online](https://mcptask.online) `https://mcptask.online/mcp`
  [![mcptask.online MCP connector](https://glama.ai/mcp/connectors/online.mcptask/mcptaskonline/badges/score.svg)](https://glama.ai/mcp/connectors/online.mcptask/mcptaskonline)
  🔐 - Assign coding tasks to Claude Code, Codex or OpenCode on your own infrastructure and get PRs back.
- [monday.com](https://monday.com) `https://mcp.monday.com/mcp`
  🔐 - Manage monday.com boards, items, and updates.
- [Orbit](https://orbit.noveum.ai) `https://orbit.noveum.ai/mcp`
  [![Orbit MCP connector](https://glama.ai/mcp/connectors/io.github.Noveum/orbit/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Noveum/orbit)
  🔐 - Manage issues, projects, sprints, docs and files.
- [Pizza Developer](https://pizzadeveloper.com) `https://pizzadeveloper.com/api/mcp`
  [![Pizza Developer MCP connector](https://glama.ai/mcp/connectors/com.pizzadeveloper/pizzadeveloper/badges/score.svg)](https://glama.ai/mcp/connectors/com.pizzadeveloper/pizzadeveloper)
  🔐 - Work management for AI agents: plan Ideas, Batches and Works, keep context, ship Deliveries.
- [Stellary](https://stellary.co) `https://api.stellary.co/mcp`
  [![Stellary MCP connector](https://glama.ai/mcp/connectors/io.github.Anymfah/stellary-project-management/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Anymfah/stellary-project-management)
  🔐 - Project boards, a cockpit and governed agent missions.
- [TrackingTime](https://trackingtime.co) `https://mcp.trackingtime.co/mcp`
  [![TrackingTime MCP connector](https://glama.ai/mcp/connectors/io.github.TrackingTime/mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.TrackingTime/mcp-server)
  🔐 - Start and stop timers, log time and report on hours, projects, tasks and customers.
- [Weft](https://letsweft.com/?utm_source=awesome-remote-mcp&utm_medium=repo&utm_campaign=evergreen) `https://letsweft.com/api/mcp`
  [![Weft MCP connector](https://glama.ai/mcp/connectors/com.letsweft/weft/badges/score.svg)](https://glama.ai/mcp/connectors/com.letsweft/weft)
  🔐 - Scrumban board your AI drives: agents claim tasks with leases, report progress, and close them on artifacts.
- [Ybug](https://ybug.io/features/mcp-server) `https://mcp.ybug.io/mcp`
  [![Ybug MCP connector](https://glama.ai/mcp/connectors/io.ybug.mcp/ybug/badges/score.svg)](https://glama.ai/mcp/connectors/io.ybug.mcp/ybug)
  🔐 - Read website bug reports with screenshots and console logs, and triage status, priority, tags, and assignees.

### 🏠 <a name="real-estate"></a>Real Estate

- [Assetfy](https://assetfy.com/produkt/ai-mcp-anbindung/) `https://mcp.assetfy.com/mcp`
  [![Assetfy MCP connector](https://glama.ai/mcp/connectors/com.assetfy/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.assetfy/mcp)
  🔐 - German property data: parcels, zoning plans with PDFs, land values, LoD2 buildings and listings.
- [baseray](https://baseray.ai/docs/mcp) `https://api.baseray.ai/mcp`
  [![baseray MCP connector](https://glama.ai/mcp/connectors/ai.baseray/baseray/badges/score.svg)](https://glama.ai/mcp/connectors/ai.baseray/baseray)
  🔐 - Building data: address, use, size, height, age, roof, solar panels and registered businesses.
- [Brainy Prices](https://prices.brainy.ae/developers.html) `https://prices.brainy.ae/mcp/v2`
  [![Brainy Prices MCP connector](https://glama.ai/mcp/connectors/ae.brainy/grocery-prices/badges/score.svg)](https://glama.ai/mcp/connectors/ae.brainy/grocery-prices)
  🔓 - UAE living costs: KHDA fees, DLD rents, fuel, utilities, telecom and relocation, with dated sources.
- [CoworkingView](https://coworkingview.com/en/mcp) `https://mcp.coworkingview.com/mcp`
  [![CoworkingView MCP connector](https://glama.ai/mcp/connectors/com.coworkingview/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.coworkingview/mcp)
  🔓 - Search coworking spaces and private offices in 62 cities, with published prices and market rates.

- [Dubai Data](https://datadubai.ae/mcp/) `https://mcp.datadubai.ae/mcp`
  [![Dubai Data MCP connector](https://glama.ai/mcp/connectors/ae.datadubai/dubai-real-estate/badges/score.svg)](https://glama.ai/mcp/connectors/ae.datadubai/dubai-real-estate)
  🔓 - Dubai property statistics from Land Department open data: prices, rents, yields, sales by area, project and developer.

- [Evlek](https://evlek.app/mcp) `https://evlek.app/api/mcp`
  [![Evlek MCP connector](https://glama.ai/mcp/connectors/app.evlek/mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/app.evlek/mcp-server)
  🔓 - Search active Northern Cyprus sale and rental listings and compare asking prices by city and district.
- [GigNGo](https://gigngo.org/mcp-server) `https://gigngo.org/mcp`
  [![GigNGo MCP connector](https://glama.ai/mcp/connectors/org.gigngo/gigngo/badges/score.svg)](https://glama.ai/mcp/connectors/org.gigngo/gigngo)
  🔓 - Find US locals for home jobs and errands, watch videos of their real work, and draft a job post the person reviews.
- [GlaziersEdge Knowledge](https://glazing-mcp.glazingkb.workers.dev/) `https://glazing-mcp.glazingkb.workers.dev/mcp`
  [![GlaziersEdge Knowledge MCP connector](https://glama.ai/mcp/connectors/io.github.shanethelion/glazing-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.shanethelion/glazing-mcp)
  🔓 - US commercial glass and glazing reference: code topics, IGU performance data, glass and framing or-equals, budgets.
- [Haulest](https://haulest.com/developers/mcp) `https://haulest.com/mcp`
  [![Haulest MCP connector](https://glama.ai/mcp/connectors/com.haulest/haulest/badges/score.svg)](https://glama.ai/mcp/connectors/com.haulest/haulest)
  🔓 - Moving cost ranges, reviewed movers, USDOT and Companies House licence checks, guides, and quote requests.
- [Irish Rent Check](https://rent-check-production.up.railway.app/) `https://rent-check-production.up.railway.app/mcp`
  [![Irish rent check MCP connector](https://glama.ai/mcp/connectors/app.railway.up.rent-check-production/irish-rent-check/badges/score.svg)](https://glama.ai/mcp/connectors/app.railway.up.rent-check-production/irish-rent-check)
  🔓 - Irish rents by county (CSO/RTB), free; paid town and property-price tools return x402/MPP terms.
- [Kolmo Construction](https://www.kolmo.io/developers) `https://www.kolmo.io/mcp`
  [![Kolmo Construction MCP connector](https://glama.ai/mcp/connectors/io.kolmo/kolmo-construction/badges/score.svg)](https://glama.ai/mcp/connectors/io.kolmo/kolmo-construction)
  🔓 - WA permit rules for 80+ cities, parcel zoning, contractor license checks and Seattle cost estimates.
- [Kvartiry-Phuket](https://kvartiry-phuket.com/otkrytye-dannye/#english) `https://kvartiry-phuket.com/mcp`
  [![Kvartiry-Phuket MCP connector](https://glama.ai/mcp/connectors/com.kvartiry-phuket/phuket/badges/score.svg)](https://glama.ai/mcp/connectors/com.kvartiry-phuket/phuket)
  🔓 - Russian-language Phuket property guides, districts, asking prices and condo assessment rates, plus weather and beaches.
- [Microburbs](https://www.microburbs.com.au/developers/api-docs) `https://api.microburbs.com.au/mcp`
  [![Microburbs MCP connector](https://glama.ai/mcp/connectors/au.com.microburbs/property-data/badges/score.svg)](https://glama.ai/mcp/connectors/au.com.microburbs/property-data)
  🔓 - Street-level Australian property data: price forecasts, crime, sales and zoning; data needs a key.
- [NebenkostenPro](https://nebenkostenpro.de/mcp) `https://nebenkostenpro.de/mcp`
  [![NebenkostenPro MCP connector](https://glama.ai/mcp/connectors/de.nebenkostenpro/nebenkosten/badges/score.svg)](https://glama.ai/mcp/connectors/de.nebenkostenpro/nebenkosten)
  🔓 - German utility costs for 400 cities, property tax rates, housing benefit levels and utility bill deadlines.
- [Pillr](https://pillr.fr/mcp) `https://pillr.fr/api/mcp`
  [![Pillr MCP connector](https://glama.ai/mcp/connectors/fr.pillr/pillr/badges/score.svg)](https://glama.ai/mcp/connectors/fr.pillr/pillr)
  🔓 - French property data: price per m² by municipality, local market summary and planning permit requirements.
- [Prism](https://prism.parad1gm.com/agents) `https://prism.parad1gm.com/api/prism-mcp`
  [![Prism MCP connector](https://glama.ai/mcp/connectors/com.parad1gm/prism/badges/score.svg)](https://glama.ai/mcp/connectors/com.parad1gm/prism)
  🔐 - Every deadline in a lease, mortgage, insurance or HOA document, with its date and source quote.
- [Propely Singapore Property](https://propely.sg) `https://mcp.propely.sg/`
  [![Propely Singapore Property MCP connector](https://glama.ai/mcp/connectors/sg.propely/singapore-property/badges/score.svg)](https://glama.ai/mcp/connectors/sg.propely/singapore-property)
  🔓 - Singapore stamp duty (BSD, ABSD, SSD), TDSR, loan tenure and net proceeds calculators, from Propely.
- [RealtyCrawl](https://realtycrawl.dev) `https://realtycrawl.dev/mcp`
  [![RealtyCrawl MCP connector](https://glama.ai/mcp/connectors/dev.realtycrawl/realty-crawl/badges/score.svg)](https://glama.ai/mcp/connectors/dev.realtycrawl/realty-crawl)
  🔓 - Discover real estate capabilities and source-linked observations; data calls require an API key and credits.
- [Small Business Intelligence](https://brickandmortar.dev/connect/) `https://brickandmortar.dev/mcp`
  [![Small Business Intelligence MCP connector](https://glama.ai/mcp/connectors/io.github.2016judea/small-business-intelligence/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.2016judea/small-business-intelligence)
  🔓 - Free Twin Cities public records, parcels, sales, permits and licences, joined and queryable, plus research frameworks.
- [TrueFixR + AtlasCast](https://atlasunited.io/api) `https://mcp.atlasunited.io/mcp`
  [![TrueFixR + AtlasCast MCP connector](https://glama.ai/mcp/connectors/io.github.truefixr/atlascast-truefixr/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.truefixr/atlascast-truefixr)
  🔓 - Address-level storm event data and forecasted property risk API for AI agents.

- [Tradehand](https://tradehand.com) `https://tradehand.com/api/mcp`
  [![Tradehand MCP connector](https://glama.ai/mcp/connectors/io.github.Humanleap/tradehand/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Humanleap/tradehand)
  🔓 - Find local UK tradespeople, inspect real listings and service options, and return public profile links.
### 🚗 <a name="sales"></a>Sales

- [EximAgent](https://eximagent.ai) `https://mcp.eximagent.ai/mcp`
  [![EximAgent MCP connector](https://glama.ai/mcp/connectors/ai.eximagent/eximagent/badges/score.svg)](https://glama.ai/mcp/connectors/ai.eximagent/eximagent)
  🔐 - AI agent team for export-import: find buyers and write outreach, analyze trade data, check HS codes, tariffs and OFAC.
- [Ficiel](https://ficiel.io/mcp/) `https://bridge.ficiel.io/mcp`
  [![Ficiel MCP connector](https://glama.ai/mcp/connectors/io.ficiel/ficiel/badges/score.svg)](https://glama.ai/mcp/connectors/io.ficiel/ficiel)
  🔐 - Read and search Instagram, WhatsApp and LinkedIn DMs, find prospects left unanswered, prepare follow-ups you approve.
- [LinkMCP](https://app.linkmcp.io) `https://app.linkmcp.io/api/mcp`
  [![LinkMCP MCP connector](https://glama.ai/mcp/connectors/io.linkmcp/linkmcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.linkmcp/linkmcp)
  🔐 - Use your own LinkedIn account: profiles, people and Sales Navigator search, messages, posts, invites, email finder.
- [Pinpoint dealership sales tools](https://usepinpoint.ai/resources/api/) `https://usepinpoint.ai/api/mcp`
  [![Pinpoint dealership sales tools MCP connector](https://glama.ai/mcp/connectors/ai.usepinpoint/pinpoint-dealership-sales-tools/badges/score.svg)](https://glama.ai/mcp/connectors/ai.usepinpoint/pinpoint-dealership-sales-tools)
  🔓 - Car dealership sales tools from Pinpoint, the sales intelligence platform for car dealerships.

- [PumpGTM](https://pumpgtm.com/docs/mcp) `https://mcp.pumpgtm.com/mcp`
  [![PumpGTM MCP connector](https://glama.ai/mcp/connectors/com.pumpgtm/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.pumpgtm/mcp)
  🔐 - Find buyers, run LinkedIn, email and X outreach from your own accounts, and approve drafted replies.
- [SalesBook by MaxedS](https://maxeds.org/tools/salesbook) `https://mcp.maxeds.org/mcp`
  [![SalesBook by MaxedS MCP connector](https://glama.ai/mcp/connectors/org.maxeds/salesbook/badges/score.svg)](https://glama.ai/mcp/connectors/org.maxeds/salesbook)
  🔓 - Search, rank and profile enterprise tech companies from sourced public evidence, with a published methodology.
- [Silicon Valley Atlas](https://svatlas.io) `https://svatlas.io/mcp`
  [![Silicon Valley Atlas MCP connector](https://glama.ai/mcp/connectors/io.svatlas/svatlas/badges/score.svg)](https://glama.ai/mcp/connectors/io.svatlas/svatlas)
  🔐 - Search sourced profiles of AI startups, founders, funding and investors; rank likely buyers; manage outreach lists.
- [SuperSend](https://supersend.io/agents) `https://mcp.supersend.io/mcp`
  [![SuperSend MCP connector](https://glama.ai/mcp/connectors/io.github.Ktryberceo/mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Ktryberceo/mcp-server)
  🔐 - Cold email and LinkedIn sequences: build campaigns, import contacts, check deliverability and triage replies.

### 🔬 <a name="science--research"></a>Science & Research

- [CiteMe](https://citeme.app/mcp) `https://citeme.app/api/mcp`
  [![CiteMe MCP connector](https://glama.ai/mcp/connectors/app.citeme/citeme/badges/score.svg)](https://glama.ai/mcp/connectors/app.citeme/citeme)
  🔓 - Find scholarly sources, format citations in 60+ styles, and check a bibliography against real records.
- [CovaSyn](https://covasyn.com/en/mcp) `https://mcp.covasyn.com/mcp`
  [![CovaSyn MCP connector](https://glama.ai/mcp/connectors/com.covasyn/chemistry/badges/score.svg)](https://glama.ai/mcp/connectors/com.covasyn/chemistry)
  🔓 - Chemistry tools for pharma and biotech: NMR, MS, ICH M7 toxicity, stability, HPLC, DoE; tool calls need a key or OAuth.
- [DeepDNA](https://deepdna.ai/docs/#mcp) `https://deepdna.ai/mcp`
  [![DeepDNA MCP connector](https://glama.ai/mcp/connectors/ai.deepdna/knowledge/badges/score.svg)](https://glama.ai/mcp/connectors/ai.deepdna/knowledge)
  🔓 - Cited drug–gene (mostly CPIC/DPWG), gene and rsID variant lookups for 12 genes; educational, not medical advice.
- [Economic Statistics (Monitly)](https://monit.ly/mcp-docs#public-servers) `https://monit.ly/api/mcp/economy`
  [![Economic Statistics (Monitly) MCP connector](https://glama.ai/mcp/connectors/io.github.ContentWriterco/economic-statistics/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ContentWriterco/economic-statistics)
  🔓 - GDP, inflation, trade, interest rates and public debt for 150+ countries from Eurostat, OECD, World Bank and IMF.
- [Electronics Architect](https://electronics-architect.com/developers) `https://electronics-architect.com/mcp`
  [![Electronics Architect MCP connector](https://glama.ai/mcp/connectors/com.electronics-architect/electronics-architect/badges/score.svg)](https://glama.ai/mcp/connectors/com.electronics-architect/electronics-architect)
  🔐 - Solves DC/DC power trees with real parts: each rail's current, efficiency, dissipation and tolerance corners.
- [Labour Market Statistics (Monitly)](https://monit.ly/mcp-docs#public-servers) `https://monit.ly/api/mcp/labour`
  [![Labour Market Statistics (Monitly) MCP connector](https://glama.ai/mcp/connectors/io.github.ContentWriterco/labour-market-statistics/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ContentWriterco/labour-market-statistics)
  🔓 - Unemployment, employment, wages and labour costs for 150+ countries from Eurostat, OECD, ILO and World Bank.
- [Lenz Fact-Check](https://lenz.io/integrations/mcp-server) `https://lenz.io/mcp`
  [![Lenz Fact-Check MCP connector](https://glama.ai/mcp/connectors/io.lenz/fact-check/badges/score.svg)](https://glama.ai/mcp/connectors/io.lenz/fact-check)
  🔐 - Checks the factual claims in a text against independent sources: a quick verdict, or a deep check with sources.
- [Monitly](https://monit.ly/mcp-docs) `https://monit.ly/api/mcp/public`
  [![Monitly MCP connector](https://glama.ai/mcp/connectors/io.github.ContentWriterco/monitly/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ContentWriterco/monitly)
  🔓 - Official statistics from Eurostat, World Bank, OECD, IMF and WHO for 150+ countries: search datasets and time series.
- [Neruva](https://neruva.io) `https://neruva.io/forum/mcp`
  [![Neruva MCP connector](https://glama.ai/mcp/connectors/io.neruva/agent-forum/badges/score.svg)](https://glama.ai/mcp/connectors/io.neruva/agent-forum)
  🔓 - Agents design parts of an open sky130 AI chip; formally verified entries compete to be fabricated.
- [Oliver's mTOR Atlas](https://mtor-atlas.org/api/#mcp) `https://mtor-atlas-mcp.mtor-atlas.workers.dev/mcp`
  [![Oliver's mTOR Atlas MCP connector](https://glama.ai/mcp/connectors/io.github.open-mtor-atlas/mtor-atlas/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.open-mtor-atlas/mtor-atlas)
  🔓 - Curated mTOR research: evidence-labelled studies, pathway claims with supporting/conflicting studies, open questions.
- [Papers by Ouroboros](https://ouroborosapps.com/docs/papers) `https://papers-mcp.vercel.app/mcp`
  [![Papers by Ouroboros MCP connector](https://glama.ai/mcp/connectors/io.github.LAHutchins91/papers/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.LAHutchins91/papers)
  🔓 - Research paper search with citations from OpenAlex, Semantic Scholar, PubMed, Crossref and arXiv.
- [PartsPlan](https://partsplanai.com/en) `https://worker.partsplanai.com/mcp`
  [![PartsPlan MCP connector](https://glama.ai/mcp/connectors/io.github.bboinzg-dev/partsplan/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.bboinzg-dev/partsplan)
  🔐 - Manufacturer datasheet pages, tables, graphs and drawings for AI circuit design, cited by page.
- [Picked by Agents Research Network](https://pickedbyagents.com/join) `https://pickedbyagents.com/research-api/mcp`
  [![Picked by Agents Research Network MCP connector](https://glama.ai/mcp/connectors/com.pickedbyagents/research-network/badges/score.svg)](https://glama.ai/mcp/connectors/com.pickedbyagents/research-network)
  🔓 - Agents answer research tasks on how assistants pick local businesses and earn credits, if their person agrees.
- [Publish.fun](https://publish.fun) `https://publish.fun/api/mcp`
  [![Publish.fun MCP connector](https://glama.ai/mcp/connectors/fun.publish/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/fun.publish/mcp)
  🔓 - AI-native research journal: agents submit papers for AI peer review, track decisions, revise and cite.
- [Vuntum](https://vuntum.com) `https://vuntum.com/mcp`
  [![Vuntum MCP connector](https://glama.ai/mcp/connectors/com.vuntum/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.vuntum/mcp)
  🔓 - Sourced, dated data on consumer robots and physical AI: specs, prices, evidence levels.
- [Trustbase Lab](https://trustbaselab.com) `https://trustbaselab.com/mcp`
  [![Trustbase Lab MCP connector](https://glama.ai/mcp/connectors/com.trustbaselab/rcb-data/badges/score.svg)](https://glama.ai/mcp/connectors/com.trustbaselab/rcb-data)
  🔓 - Citable industry records with stable IDs across chemical recycling, carbon, battery, telecom, health and compute.
- [Zetesis](https://api.zetesis.science/docs) `https://api.zetesis.science/mcp`
  [![Zetesis MCP connector](https://glama.ai/mcp/connectors/io.github.reutavidan/zetesis/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.reutavidan/zetesis)
  🔓 - Due diligence on scientific claims, graded against the published record.
- [Zovo Time Tracker](https://mcp.zovo.one/mcp/time-tracker) `https://mcp.zovo.one/mcp/time-tracker`
  [![Zovo Time Tracker MCP connector](https://glama.ai/mcp/connectors/io.github.theluckystrike/time-tracker-timesheet-billable-hours/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.theluckystrike/time-tracker-timesheet-billable-hours)
  🔓 - Log billable hours per client/project, daily and weekly summaries and CSV export; free browser-minted token, no account.
- [Agent Council](https://cyberwarex.com/assets/council-quickstart.html) `https://council.cyberwarex.com/mcp`
  [![Agent Council MCP connector](https://glama.ai/mcp/connectors/com.cyberwarex.council/agent-council/badges/score.svg)](https://glama.ai/mcp/connectors/com.cyberwarex.council/agent-council)
  🔓 - One question goes to 3-4 models; a chair returns one verdict with a confidence score and the dissent that held.

### 🔎 <a name="search--data-extraction"></a>Search & Data Extraction

- [1cent](https://1cent.maxzoa.ru) `https://1cent.maxzoa.ru/mcp`
  [![1cent MCP connector](https://glama.ai/mcp/connectors/ru.maxzoa/1cent/badges/score.svg)](https://glama.ai/mcp/connectors/ru.maxzoa/1cent)
  🔓 - Extract web content and metadata, map site resources and detect page changes; x402 pay-per-call.
- [Agent Company Index](https://agentcompanyindex.com) `https://agentcompanyindex.com/mcp`
  [![Agent Company Index MCP connector](https://glama.ai/mcp/connectors/com.agentcompanyindex/directory/badges/score.svg)](https://glama.ai/mcp/connectors/com.agentcompanyindex/directory)
  🔓 - Sourced B2B provider profiles: who each offering fits, who it doesn't, limits and unknowns, with checked dates.
- [Ambolt](https://ambolt.dev) `https://api.ambolt.dev/mcp`
  [![Ambolt MCP connector](https://glama.ai/mcp/connectors/dev.ambolt/ambolt/badges/score.svg)](https://glama.ai/mcp/connectors/dev.ambolt/ambolt)
  🔓 - Company registers, tenders, rates and on-chain facts, with source and date on every answer.
- [AnywhereRoles](https://anywhereroles.com/developers) `https://anywhereroles.com/mcp`
  [![AnywhereRoles MCP connector](https://glama.ai/mcp/connectors/com.anywhereroles/jobs/badges/score.svg)](https://glama.ai/mcp/connectors/com.anywhereroles/jobs)
  🔓 - Search remote jobs by eligible country and time zone, plus companies and salaries; results link to original postings.
- [Apify Scraping Toolbox](https://apify.com/travelmonitorlab) `https://adagasolutions.lu/mcp`
  [![Adaga solutions — Data APIs Toolbox MCP connector](https://glama.ai/mcp/connectors/io.github.jeffreyturov-dev/adaga-solutions-toolbox/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.jeffreyturov-dev/adaga-solutions-toolbox)
  🔓 - 13 pay-per-event data APIs: local AI-presence audits, Google Maps, TikTok, LinkedIn, reviews, fuel, AEO.
- [Briefing Service](https://briefing-service.wholemind.workers.dev) `https://briefing-service.wholemind.workers.dev/mcp`
  [![Briefing Service MCP connector](https://glama.ai/mcp/connectors/io.github.jshelley/briefings/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.jshelley/briefings)
  🔓 - Hourly briefings on AI, markets, sports and world news as JSON or e-ink pages; paid tools via x402.
- [Bright Data](https://brightdata.com) `https://mcp.brightdata.com/mcp`
  🔐 - Web scraping and SERP data through a managed proxy network.
- [BRONTIR](https://brontir.com) `https://research.brontir.com/api/mcp`
  [![BRONTIR MCP connector](https://glama.ai/mcp/connectors/com.brontir.research/brontir/badges/score.svg)](https://glama.ai/mcp/connectors/com.brontir.research/brontir)
  🔐 - Web research across search, Reddit, YouTube, reviews and ad libraries, with line-numbered citations.
- [Callejear Madrid](https://callejear.com/mcp/) `https://callejear.com/api/mcp`
  [![Callejear Madrid MCP connector](https://glama.ai/mcp/connectors/com.callejear/madrid/badges/score.svg)](https://glama.ai/mcp/connectors/com.callejear/madrid)
  🔓 - Search Madrid's 9,400 official streets and compare partial service counts within 500 m; read-only.
- [cnpj.ia.br](https://cnpj.ia.br/docs/mcp?utm_source=github&utm_medium=awesome-list) `https://mcp.cnpj.ia.br`
  [![cnpj.ia.br MCP connector](https://glama.ai/mcp/connectors/br.ia.cnpj/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/br.ia.cnpj/mcp)
  🔐 - Brazilian company data (CNPJ) from Receita Federal: lookup, filtered search, phones, e-mails and partners (masked CPF).
- [Corbelworks](https://corbelworks.pages.dev) `https://corbelworks.pages.dev/mcp`
  [![Corbelworks MCP connector](https://glama.ai/mcp/connectors/dev.pages.corbelworks/reliability/badges/score.svg)](https://glama.ai/mcp/connectors/dev.pages.corbelworks/reliability)
  🔓 - Scan a software vendor's public claims for defects and get structured findings with evidence grades.
- [Cloudflare Radar](https://radar.cloudflare.com) `https://radar.mcp.cloudflare.com/mcp`
  🔐 - Internet traffic, routing, and security trends from Cloudflare Radar.
- [CN Evidence](https://cnevidence.com) `https://mcp.cnevidence.com/mcp`
  [![CN Evidence MCP connector](https://glama.ai/mcp/connectors/dev.workers.mikeyang7789.cn-evidence-mcp-public/cn-evidence-china-supplier-due-diligence/badges/score.svg)](https://glama.ai/mcp/connectors/dev.workers.mikeyang7789.cn-evidence-mcp-public/cn-evidence-china-supplier-due-diligence)
  🔓 - Selected China supplier registration and risk records; paid queries via x402 on Base.
- [cn-intel-mcp](https://github.com/lory69060/cn-intel-mcp) `https://cn-intel-mcp.lory69060.workers.dev/mcp`
  [![cn-intel-mcp MCP connector](https://glama.ai/mcp/connectors/dev.workers.lory69060.cn-intel-mcp/cn-intel-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/dev.workers.lory69060.cn-intel-mcp/cn-intel-mcp)
  🔓 - China hard-tech supply-chain signals with a track record: chips, batteries, eVTOL and pharma.
- [CityAlert](https://cityalert.live) `https://cityalert.live/.well-known/mcp`
  [![CityAlert MCP connector](https://glama.ai/mcp/connectors/live.cityalert/cityalert/badges/score.svg)](https://glama.ai/mcp/connectors/live.cityalert/cityalert)
  🔓 - Live public-safety incidents and safety news from 650+ official feeds; filter by city, region or bbox.
- [CuratorSearch](https://curatorsearch.com/developers) `https://curatorsearch.com/mcp`
  [![CuratorSearch MCP connector](https://glama.ai/mcp/connectors/com.curatorsearch/jobs/badges/score.svg)](https://glama.ai/mcp/connectors/com.curatorsearch/jobs)
  🔓 - Search live museum and curatorial jobs, one institution's openings, and the sector's pay-transparency rate.
- [EveryInfra](https://everyinfra.com/en) `https://api.everyinfra.com/mcp`
  [![EveryInfra MCP connector](https://glama.ai/mcp/connectors/io.github.xiaoxihexiaoyu/everyinfra/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.xiaoxihexiaoyu/everyinfra)
  🔓 - Structured data from 90 platforms, incl. RedNote, Douyin, TikTok and Amazon, plus web search; API key for tool calls.
- [Exa](https://exa.ai) `https://mcp.exa.ai/mcp`
  [![Exa MCP connector](https://glama.ai/mcp/connectors/ai.exa/exa/badges/score.svg)](https://glama.ai/mcp/connectors/ai.exa/exa)
  🔓 - Neural web search that returns full page contents.
- [file2markdown](https://www.file2markdown.ai) `https://mcp.file2markdown.ai/mcp`
  [![file2markdown MCP connector](https://glama.ai/mcp/connectors/ai.file2markdown/file2markdown/badges/score.svg)](https://glama.ai/mcp/connectors/ai.file2markdown/file2markdown)
  🔓 - Convert PDFs, Office files and web pages to clean Markdown by URL or base64; 5 free a day, Pro key for more.
- [Firecrawl](https://firecrawl.dev) `https://mcp.firecrawl.dev/v2/mcp`
  [![Firecrawl MCP connector](https://glama.ai/mcp/connectors/dev.firecrawl.mcp/firecrawl-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/dev.firecrawl.mcp/firecrawl-mcp)
  🔓 - Crawl, scrape, and extract structured data from websites.
- [fitze x402 Tools](https://fitze-x402-seller.app.workbuddy.host) `https://fitze-x402-seller.app.workbuddy.host/mcp`
  [![fitze x402 Tools MCP connector](https://glama.ai/mcp/connectors/io.github.foxxx009/x402-tools-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.foxxx009/x402-tools-mcp)
  🔓 - Pay-per-call agent tools: web fetch, domain/GitHub/token intel, repo diligence and web briefs, in USDC on Base via x402.
- [FTIR.fun](https://ftir.fun) `https://ftir.fun/mcp`
  [![FTIR.fun Spectral Search MCP connector – tool definition quality and endpoint health on Glama](https://glama.ai/mcp/connectors/io.github.jxbaoxiaodong/ftirfun-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.jxbaoxiaodong/ftirfun-mcp)
  🔐 - Analyze FTIR spectra, search spectral libraries, and retrieve peak and literature evidence.
- [gankdat](https://gankdat.com) `https://gankdat.com/mcp`
  [![gankdat MCP connector](https://glama.ai/mcp/connectors/com.gankdat/gankdat/badges/score.svg)](https://glama.ai/mcp/connectors/com.gankdat/gankdat)
  🔓 - UK & EU tenders, planning, sanctions, US exclusions, insolvency and company data; free key for tool calls.
- [Gemalli](https://gemalli.com/en/developers) `https://gemalli.com/api/mcp`
  [![Gemalli MCP connector](https://glama.ai/mcp/connectors/com.gemalli/trade/badges/score.svg)](https://glama.ai/mcp/connectors/com.gemalli/trade)
  🔓 - Find verified manufacturers, screen for sanctions, and look up HS codes and export controls.
- [gluten-free.fr](https://gluten-free.fr) `https://gluten-free.fr/api/mcp`
  🔓 - Verified gluten-free product catalogue and comparison data for the French market.
- [GovAuctions.app](https://govauctions.app) `https://govauctions.app/api/mcp`
  [![GovAuctions.app MCP connector](https://glama.ai/mcp/connectors/app.govauctions/govauctions/badges/score.svg)](https://glama.ai/mcp/connectors/app.govauctions/govauctions)
  🔓 - Government surplus auctions in the US, UK, CA and AU, with sold-price comps and resale scores.
- [GovContractScout](https://scout.govbidportals.com) `https://scout.govbidportals.com/mcp`
  [![GovContractScout MCP connector](https://glama.ai/mcp/connectors/com.govbidportals.scout/gov-contract-scout/badges/score.svg)](https://glama.ai/mcp/connectors/com.govbidportals.scout/gov-contract-scout)
  🔐 - Search US state & local government contracts, NAICS codes, and AI match scoring via OAuth 2.1.
- [High Signal](https://highsignal.app) `https://mcp.highsignal.app/high-signal/mcp`
  [![High Signal MCP connector](https://glama.ai/mcp/connectors/app.highsignal.mcp/high-signal/badges/score.svg)](https://glama.ai/mcp/connectors/app.highsignal.mcp/high-signal)
  🔓 - Read published High Signal daily briefs, signals and their linked evidence through a bounded, read-only public feed.
- [Horizon](https://horizon.alchemylab.sh/developers) `https://horizon.alchemylab.sh/api/mcp`
  [![Horizon MCP connector](https://glama.ai/mcp/connectors/sh.alchemylab.horizon/briefing/badges/score.svg)](https://glama.ai/mcp/connectors/sh.alchemylab.horizon/briefing)
  🔓 - Daily AI briefing, AI regulation tracker (EU AI Act, US federal & state, UK), regional lenses and search.
- [JobsPipe](https://docs.jobspipe.dev/ai-agents/mcp) `https://mcp.jobspipe.dev/mcp`
  [![JobsPipe MCP connector score](https://glama.ai/mcp/connectors/dev.jobspipe/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/dev.jobspipe/mcp)
  🔐 - Search live jobs from 30+ boards and ATS feeds, read full postings, and save searches to catch new matches.
- [jopp](https://getjopp.app) `https://getjopp.app/mcp`
  [![jopp MCP connector](https://glama.ai/mcp/connectors/app.getjopp/jopp/badges/score.svg)](https://glama.ai/mcp/connectors/app.getjopp/jopp)
  🔓 - Search open jobs in Switzerland and Liechtenstein and read job details.
- [LiveDataLink](https://livedatalink.ai) `https://livedatalink.ai/mcp`
  [![LiveDataLink MCP connector](https://glama.ai/mcp/connectors/io.github.blackboxfoundry/livedatalink/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.blackboxfoundry/livedatalink)
  🔓 - Query 60 public-data domains, including sanctions, courts, markets, health and energy.
- [Locate Jobs Network](https://locatejobsnetwork.com) `https://locatejobsnetwork.com/api/mcp`
  [![Locate Jobs Network MCP connector](https://glama.ai/mcp/connectors/com.locatejobsnetwork/search-jobs/badges/score.svg)](https://glama.ai/mcp/connectors/com.locatejobsnetwork/search-jobs)
  🔓 - Search live U.S. jobs on 20 niche job boards and get checked unemployment answers for 13 states.
- [looot](https://looot.ai) `https://api.looot.ai/mcp`
  [![looot MCP connector](https://glama.ai/mcp/connectors/ai.looot/looot/badges/score.svg)](https://glama.ai/mcp/connectors/ai.looot/looot)
  🔐 - Search, price and run 2,500+ data endpoints from 90+ providers with one key and a prepaid balance.
- [MAC Address Lookup](https://mac.jasontally.com) `https://mac.jasontally.com/mcp`
  [![MAC Address Lookup MCP connector](https://glama.ai/mcp/connectors/com.jasontally.mac/mac-address-lookup/badges/score.svg)](https://glama.ai/mcp/connectors/com.jasontally.mac/mac-address-lookup)
  🔓 - Find the organization behind a MAC address or OUI prefix in the complete IEEE MA-L, MA-M, MA-S, IAB, and CID registries.
- [Maison de Talents](https://maisondetalents.com) `https://maisondetalents.com/api/mcp`
  [![Maison de Talents MCP connector](https://glama.ai/mcp/connectors/com.maisondetalents/maison-de-talents/badges/score.svg)](https://glama.ai/mcp/connectors/com.maisondetalents/maison-de-talents)
  🔓 - Search luxury, department-store and duty-free retail jobs in Korea, with salary benchmarks.
- [NanoParse](https://nanoparse.app) `https://nanoparse.app/mcp`
  [![NanoParse MCP connector](https://glama.ai/mcp/connectors/io.github.nanoparse-dev/nanoparse-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.nanoparse-dev/nanoparse-mcp)
  🔓 - Read any web page as clean Markdown plus 15 trust signals; $0.005 per page in USDC on Base via x402, 10 free.
- [Ni Biashara Shelves](https://agents.nibiashara.biz/docs?ref=dir-awesome-remote) `https://agents.nibiashara.biz/mcp`
  [![Ni Biashara Shelves MCP connector](https://glama.ai/mcp/connectors/biz.nibiashara/shelves/badges/score.svg)](https://glama.ai/mcp/connectors/biz.nibiashara/shelves)
  🔓 - Pay-per-call data checks over x402: FMCSA carrier/broker authority, load vetting, OFAC screens and African FX rates.
- [Octocrawl](https://octocrawl.dev/?utm_source=awesome-remote-mcp-servers&utm_medium=listing) `https://mcp.octocrawl.dev/mcp`
  [![Octocrawl MCP connector](https://glama.ai/mcp/connectors/io.github.77777R7/octocrawl/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.77777R7/octocrawl)
  🔓 - Scrape pages to Markdown with an evidence record and map a site's URLs; blocked pages are reported, not hidden.
- [Openings](https://avagama.co/openings/) `https://openings.avagama.co/mcp`
  [![Openings MCP connector](https://glama.ai/mcp/connectors/co.avagama/openings/badges/score.svg)](https://glama.ai/mcp/connectors/co.avagama/openings)
  🔐 - Search jobs on verified employer job boards, with every result linking to the employer's own posting.
- [Openpath](https://openpath.sh) `https://openpath.sh/mcp/search`
  [![Openpath MCP connector](https://glama.ai/mcp/connectors/sh.openpath/openpath/badges/score.svg)](https://glama.ai/mcp/connectors/sh.openpath/openpath)
  🔓 - Live jobs (Austin, TX and remote) and Austin-area local businesses, each with an Apply link or an Openpath inbox.
- [PageWire](https://pagewire.dev) `https://pagewire.dev/mcp`
  [![PageWire MCP connector](https://glama.ai/mcp/connectors/dev.pagewire/web/badges/score.svg)](https://glama.ai/mcp/connectors/dev.pagewire/web)
  🔓 - Read any public page as clean Markdown, page metadata, or a page plus 4 same-site pages; USDC per call via x402.
- [Parlel](https://parlel.com) `https://api.parlel.com/mcp`
  [![Parlel MCP connector](https://glama.ai/mcp/connectors/com.parlel.api/parlel/badges/score.svg)](https://glama.ai/mcp/connectors/com.parlel.api/parlel)
  🔓 - Free search of people, companies and open roles on an open professional network.
- [PeopleSearch.im](https://peoplesearch.im/mcp) `https://peoplesearch.im/api/mcp`
  [![PeopleSearch.im MCP connector](https://glama.ai/mcp/connectors/im.peoplesearch/email-finder/badges/score.svg)](https://glama.ai/mcp/connectors/im.peoplesearch/email-finder)
  🔓 - Search people and companies in plain English and get verified work emails; tool calls sign in with OAuth or an API key.
- [Pollar News](https://mcp.pollar.news/) `https://mcp.pollar.news/mcp`
  [![Pollar News MCP connector](https://glama.ai/mcp/connectors/news.pollar/pollar-news/badges/score.svg)](https://glama.ai/mcp/connectors/news.pollar/pollar-news)
  🔓 - Independent European news in four languages: search with sources, explainers with maps, briefs and live stories.
- [Proxmint](https://proxmint.com) `https://proxmint.com/api/mcp`
  [![Proxmint MCP connector](https://glama.ai/mcp/connectors/com.proxmint/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.proxmint/mcp)
  🔓 - Proxy prices, balance, usage, geo-targeted proxy lines and connection checks; account tools need an API key.
- [ProxyCove](https://proxycove.com) `https://mcp.proxycove.com/mcp`
  [![ProxyCove MCP connector](https://glama.ai/mcp/connectors/com.proxycove/mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/com.proxycove/mcp-server)
  🔓 - Buy and manage residential, mobile and datacenter proxies in 170+ countries, prepaid per GB.
- [PubRecords](https://mcp-pubrecords-production.up.railway.app) `https://mcp-pubrecords-production.up.railway.app/mcp/`
  [![PubRecords MCP connector](https://glama.ai/mcp/connectors/io.github.bch1212/pubrecords/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.bch1212/pubrecords)
  🔓 - Search US company filings, SEC reports, federal court cases, spending awards, licenses, and entity records.
- [QRCode.Pub tools](https://qrcode.pub/qr-code-api#mcp) `https://qrcode.pub/mcp`
  [![QRCode.Pub tools MCP connector](https://glama.ai/mcp/connectors/pub.qrcode/tools/badges/score.svg)](https://glama.ai/mcp/connectors/pub.qrcode/tools)
  🔓 - Free QR code images plus pay-per-call page-to-Markdown, page metadata and file hosting, in USDC via x402.
- [Ragfeed](https://ragfeed.de/claude) `https://api.ragfeed.de/mcp`
  [![Ragfeed MCP connector](https://glama.ai/mcp/connectors/io.github.LeifAlbrand/ragfeed/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.LeifAlbrand/ragfeed)
  🔐 - Web pages, PDFs and search results as LLM-ready Markdown or vector-DB chunks; Firecrawl-compatible API.
- [ReadGZH](https://readgzh.site) `https://api.readgzh.site/mcp-server`
  [![ReadGZH MCP connector](https://glama.ai/mcp/connectors/io.github.sweesama/readgzh/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.sweesama/readgzh)
  🔓 - Read public WeChat Official Account articles as Markdown and search previously cached articles.
- [Realask](https://realask.net) `https://realask.net/mcp`
  [![Realask MCP connector](https://glama.ai/mcp/connectors/io.github.danelas/realask/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.danelas/realask)
  🔓 - Verify stock, prices and availability at US local businesses by phone, with evidence.
- [ReplyNodes](https://replynodes.com) `https://mcp.replynodes.com/mcp`
  [![ReplyNodes MCP connector](https://glama.ai/mcp/connectors/com.replynodes/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.replynodes/mcp)
  🔓 - Web search, extraction and public-data tools for agent research.
- [Scoopkit](https://scoopkit.dev) `https://api.scoopkit.dev/mcp`
  [![Scoopkit MCP connector](https://glama.ai/mcp/connectors/dev.scoopkit/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/dev.scoopkit/mcp)
  🔓 - AI-industry news as deduplicated, classified events; a free key unlocks listing, search and archive.
- [Scoutee](https://scoutee.org/en/mcp-public-tenders) `https://scoutee.org/api/mcp/public`
  [![Scoutee MCP connector](https://glama.ai/mcp/connectors/org.scoutee/scoutee/badges/score.svg)](https://glama.ai/mcp/connectors/org.scoutee/scoutee)
  🔓 - Search public tenders across Europe and North America and read notice previews.
- [ScrapingBee](https://www.scrapingbee.com) `https://mcp.scrapingbee.com/mcp`
  [![ScrapingBee MCP connector](https://glama.ai/mcp/connectors/com.scrapingbee.mcp/scraping-bee/badges/score.svg)](https://glama.ai/mcp/connectors/com.scrapingbee.mcp/scraping-bee)
  🔓 - Fetch any page as text, markdown, HTML or a screenshot past JS and anti-bot blocks; API key needed for tool calls.
- [ScrapingBot](https://scrapingbot.io/mcp) `https://scrapingbot.io/api/mcp`
  [![ScrapingBot MCP connector](https://glama.ai/mcp/connectors/io.scrapingbot/scrapingbot/badges/score.svg)](https://glama.ai/mcp/connectors/io.scrapingbot/scrapingbot)
  🔓 - Public TikTok, Instagram, Google and Amazon data, page scraping and AI extraction; a free key unlocks the tools.
- [Simplescraper](https://simplescraper.io) `https://mcp.simplescraper.io/mcp`
  🔐 - Scrape websites and run saved extraction recipes.
- [Singapore Proxy](https://singaporemobileproxy.com/client/mcp) `https://mcp.singaporemobileproxy.com/mcp`
  [![Singapore Proxy MCP connector](https://glama.ai/mcp/connectors/io.github.Xavierfok/singapore-proxy-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Xavierfok/singapore-proxy-mcp)
  🔓 - Fetch pages and run Google searches from a rotating Singapore mobile IP on Singtel or M1; tools need a key.
- [SiteCheck](https://api.sitecheck-api.workers.dev) `https://api.sitecheck-api.workers.dev/mcp`
  [![SiteCheck MCP connector](https://glama.ai/mcp/connectors/io.github.bck-stack/sitecheck/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.bck-stack/sitecheck)
  🔓 - 29 x402 pay-per-call tools: web page to Markdown, PDF text, tech stack, email, domain, Solana, KYB.
- [SnoopScan](https://snoopscan.com) `https://api.snoopscan.com/mcp-oauth`
  [![SnoopScan MCP connector](https://glama.ai/mcp/connectors/com.snoopscan/snoopscan/badges/score.svg)](https://glama.ai/mcp/connectors/com.snoopscan/snoopscan)
  🔐 - Scrape, crawl, map and search the web as clean markdown, with schema-validated extraction.
- [Sourcey](https://sourcey.com) `https://mcp.sourcey.com/mcp`
  [![Sourcey MCP connector](https://glama.ai/mcp/connectors/com.sourcey/sourcey/badges/score.svg)](https://glama.ai/mcp/connectors/com.sourcey/sourcey)
  🔓 - Search and compare startup credits and offers, inspect their evidence, and read Agent Readiness grades.
- [Statsnet](https://statsnet.co) `https://statsnet.co/mcp`
  [![Statsnet MCP connector](https://glama.ai/mcp/connectors/io.github.usenetstate/statsnet/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.usenetstate/statsnet)
  🔓 - Company data for Kazakhstan, Uzbekistan and Kyrgyzstan: registration, executives and finances.
- [String Web Access](https://usestring.ai) `https://mcp.usestring.ai/v1/mcp`
  [![String Web Access MCP connector](https://glama.ai/mcp/connectors/ai.usestring/web-access/badges/score.svg)](https://glama.ai/mcp/connectors/ai.usestring/web-access)
  🔐 - Search the web, fetch any URL and map a site — clean Markdown, past anti-bot blocks.
- [StudiePoint AI](https://studiepoint.ai) `https://studiepoint.ai/api/mcp`
  [![StudiePoint AI MCP connector](https://glama.ai/mcp/connectors/ai.studiepoint/studie-point-ai/badges/score.svg)](https://glama.ai/mcp/connectors/ai.studiepoint/studie-point-ai)
  🔓 - Search scholarships, convert African GPAs, check visas, match students, and estimate study costs.
- [Surface](https://nova-otter-delta-cloud.grok.me) `https://nova-otter-delta-cloud.grok.me/mcp`
  [![Surface MCP connector](https://glama.ai/mcp/connectors/me.grok.nova-otter-delta-cloud/surface/badges/score.svg)](https://glama.ai/mcp/connectors/me.grok.nova-otter-delta-cloud/surface)
  🔓 - preflight_url tool that unwraps short links and tells agents whether to fetch or skip a URL.
- [Tavily](https://tavily.com) `https://mcp.tavily.com/mcp`
  🔐 - Web search and content extraction built for agents.
- [TerraLab MCP](https://terra-lab.ai/mcp) `https://mcp.terra-lab.ai/mcp`
  [![TerraLab MCP connector](https://glama.ai/mcp/connectors/ai.terra-lab/terralab/badges/score.svg)](https://glama.ai/mcp/connectors/ai.terra-lab/terralab)
  🔓 - Extract open map data, convert GIS files and coordinates, and retrieve elevation and French cadastral parcels.
- [Tollkit](https://tollkit.dev) `https://api.tollkit.dev/mcp`
  [![Tollkit MCP connector](https://glama.ai/mcp/connectors/io.github.UltraStarz/x402-extract/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.UltraStarz/x402-extract)
  🔓 - Web pages and PDFs read in a real browser, token checks, SEC and US data; x402 pay-per-call, 3 free calls a day.
- [Trends MCP](https://trendsmcp.ai) `https://api.trendsmcp.ai/mcp`
  [![Trends MCP connector](https://glama.ai/mcp/connectors/ai.trendsmcp/trends/badges/score.svg)](https://glama.ai/mcp/connectors/ai.trendsmcp/trends)
  🔓 - Live trend data from Google, TikTok, YouTube, Amazon, Reddit, and 20+ other sources.
- [Theyond](https://theyond.com) `https://theyond.com/mcp`
  [![Theyond MCP connector](https://glama.ai/mcp/connectors/com.theyond/theyond/badges/score.svg)](https://glama.ai/mcp/connectors/com.theyond/theyond)
  🔓 - Live jobs from employer career pages; apply on theyond.com.
- [TrustyData](https://trustydata.fr/usecases/mcp-qualite-donnees) `https://mcp.trustydata.app/mcp`
  [![TrustyData MCP connector](https://glama.ai/mcp/connectors/app.trustydata/trustydata/badges/score.svg)](https://glama.ai/mcp/connectors/app.trustydata/trustydata)
  🔓 - Verify French addresses against the BAN registry, search Sirene companies and compute road routes.
- [URLpipe](https://urlpipe.dev/mcp-server) `https://urlpipe.dev/mcp`
  [![URLpipe MCP connector](https://glama.ai/mcp/connectors/dev.urlpipe/urlpipe/badges/score.svg)](https://glama.ai/mcp/connectors/dev.urlpipe/urlpipe)
  🔓 - Read any page after its JavaScript runs: Markdown, screenshots, metadata and Lighthouse. Tool calls need a free API key.
- [UX Jobs](https://mcp.uxjobs.io) `https://mcp.uxjobs.io/mcp`
  [![UX Jobs MCP connector](https://glama.ai/mcp/connectors/io.uxjobs/jobs/badges/score.svg)](https://glama.ai/mcp/connectors/io.uxjobs/jobs)
  🔓 - Search 4,000+ live UX, product design and research jobs, with hiring-market and salary snapshots.
- [VegvisAI](https://vegvis.ai) `https://vegvis.ai/mcp`
  [![VegvisAI MCP connector](https://glama.ai/mcp/connectors/ai.vegvis/vegvisai/badges/score.svg)](https://glama.ai/mcp/connectors/ai.vegvis/vegvisai)
  🔓 - Open, unranked business guide for any country, Norwegian public services and parties, and a website AI-readiness check.
- [Vend](https://extract.paypercall.dev) `https://extract.paypercall.dev/mcp`
  [![Vend MCP connector](https://glama.ai/mcp/connectors/dev.paypercall.extract/vend-api-merchant/badges/score.svg)](https://glama.ai/mcp/connectors/dev.paypercall.extract/vend-api-merchant)
  🔓 - Extract, search, and analyze web pages and domains with pay-per-call tools settled in Nano (XNO) via x402.
- [Web Data Toolkit](https://web-data-toolkit.vercel.app) `https://web-data-toolkit.vercel.app/mcp`
  [![Web Data Toolkit MCP connector](https://glama.ai/mcp/connectors/io.github.leekung125/web-data-toolkit/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.leekung125/web-data-toolkit)
  🔓 - YouTube transcripts, Google Trends, and Google Play and App Store reviews; use the free public demo key or your own.
- [Zebu Data - Local Business Leads](https://apify.com/delicious_zebu) `https://mcp.apify.com/?tools=delicious_zebu/google-maps-data-scraper,delicious_zebu/yellowpages-usa-business-lead-scraper,delicious_zebu/yellowpages-ca-business-data-scraper,delicious_zebu/yellowpages-australia-lead-generator,delicious_zebu/yelp-advanced-business-scraper-pay-per-result,delicious_zebu/contact-info-scraper,delicious_zebu/contact-info-scraper-pay-per-result`
  [![Zebu Data - Local Business Leads MCP connector](https://glama.ai/mcp/connectors/io.github.zebudata/local-business-leads/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.zebudata/local-business-leads)
  🔐 - Find local businesses on Google Maps, Yellow Pages and Yelp, then pull emails and phones from their websites.

### 🔒 <a name="security"></a>Security

- [Agent Verifier](https://packet.guru/agents/mcp) `https://fp.packet.guru/api/v1/mcp`
  [![Agent Verifier MCP connector](https://glama.ai/mcp/connectors/guru.packet/agent-verifier/badges/score.svg)](https://glama.ai/mcp/connectors/guru.packet/agent-verifier)
  🔓 - Test and debug your AI agent's Web Bot Auth (RFC 9421) signature and see exactly what to fix.
- [AgentGlass](https://agentglass.net) `https://agentglass.net/mcp`
  [![AgentGlass MCP connector](https://glama.ai/mcp/connectors/net.agentglass/agentglass/badges/score.svg)](https://glama.ai/mcp/connectors/net.agentglass/agentglass)
  🔓 - Scans a public URL for hidden instructions aimed at AI agents and returns a risk level with evidence.
- [AgenticRail](https://agenticrail.nz/docs/) `https://mcp.agenticrail.nz/`
  [![AgenticRail MCP connector](https://glama.ai/mcp/connectors/nz.agenticrail/gate/badges/score.svg)](https://glama.ai/mcp/connectors/nz.agenticrail/gate)
  🔓 - Gate for AI agent steps: ALLOW or DENY before a step runs, sealed into signed receipts that verify offline.
- [Auth Posture](https://auth-posture.rowb.app) `https://auth-posture.rowb.app/mcp`
  [![Auth Posture MCP connector](https://glama.ai/mcp/connectors/app.rowb.auth-posture/audit/badges/score.svg)](https://glama.ai/mcp/connectors/app.rowb.auth-posture/audit)
  🔓 - One-call domain audit: MX receiving, SPF/DMARC/DKIM spoofing protection, disposable-address risk.
- [CrawlCheck](https://crawlcheck.io/for-agents) `https://crawlcheck.io/mcp`
  [![CrawlCheck MCP connector](https://glama.ai/mcp/connectors/io.github.emmanuelorta/crawlcheck/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.emmanuelorta/crawlcheck)
  🔓 - A signed answer about any site before an agent acts: policy, what crawlers were served, findings, a decision per action.
- [crosscheck](https://crosscheckapi.com/llms.txt) `https://crosscheckapi.com/mcp`
  [![crosscheck MCP connector](https://glama.ai/mcp/connectors/com.crosscheckapi/crosscheck/badges/score.svg)](https://glama.ai/mcp/connectors/com.crosscheckapi/crosscheck)
  🔓 - Security review of skills and MCP servers before install; paid per call via x402.
- [CVE Risk Check](https://tools.openkrill.app/#cve) `https://cve.openkrill.app/mcp`
  [![CVE Risk Check MCP connector](https://glama.ai/mcp/connectors/app.openkrill/cve/badges/score.svg)](https://glama.ai/mcp/connectors/app.openkrill/cve)
  🔓 - Checks CVEs and dependency lists against OSV, NVD, EPSS and CISA KEV, and ranks what to fix first.
- [Datakoot Domain & Company](https://datakoot.com/domain-company) `https://domain.datakoot.com/mcp`
  [![Datakoot Domain & Company MCP connector](https://glama.ai/mcp/connectors/com.datakoot/domain-dns-whois/badges/score.svg)](https://glama.ai/mcp/connectors/com.datakoot/domain-dns-whois)
  🔓 - Domain recon: RDAP registration, DNS, SPF/DMARC deliverability, tech stack and subdomains from CT logs.
- [Datakoot Security Intel](https://datakoot.com/security-intel) `https://security.datakoot.com/mcp`
  [![Datakoot Security Intel MCP connector](https://glama.ai/mcp/connectors/com.datakoot/cve-vulnerability-lookup/badges/score.svg)](https://glama.ai/mcp/connectors/com.datakoot/cve-vulnerability-lookup)
  🔓 - CVE lookups with CISA KEV and EPSS exploit scores, plus OSV package vulnerabilities and package.json audits.
- [DechoNet](https://dechonet.com/mcp) `https://dechonet.com/mcp`
  [![DechoNet MCP connector](https://glama.ai/mcp/connectors/com.dechonet/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.dechonet/mcp)
  🔓 - Phishing-link checks opened like a Korean phone, plus DNS, TLS, headers, email auth and domain history.
- [Domain Intelligence](https://oti-labs.com/mcp-server) `https://oti-labs.com/mcp`
  [![Domain Intelligence MCP connector](https://glama.ai/mcp/connectors/com.oti-labs/domain-intelligence/badges/score.svg)](https://glama.ai/mcp/connectors/com.oti-labs/domain-intelligence)
  🔓 - WHOIS/RDAP, DNS, SSL, live subdomains with IPs and SPF/DMARC/DKIM for any domain; 1,000 free lookups a month.
- [Forge](https://forge.magery.ai) `https://forge.magery.ai/mcp`
  [![Forge MCP connector](https://glama.ai/mcp/connectors/ai.magery.forge/forge-magery/badges/score.svg)](https://glama.ai/mcp/connectors/ai.magery.forge/forge-magery)
  🔓 - Security audits of shipped code, in plain English.
- [IP99](https://ip99.com/) `https://ip99.com/mcp`
  [![IP99 MCP connector](https://glama.ai/mcp/connectors/com.ip99/ip99/badges/score.svg)](https://glama.ai/mcp/connectors/com.ip99/ip99)
  🔓 - IP risk and geolocation lookup where every verdict carries the age of its evidence.
- [Jid](https://jid.com/agents) `https://jid.com/mcp`
  [![Jid MCP connector](https://glama.ai/mcp/connectors/com.jid/jid/badges/score.svg)](https://glama.ai/mcp/connectors/com.jid/jid)
  🔓 - Checks a business against US registries, sanctions and its domain before an agent pays or signs, with signed receipts.
- [Lattice](https://lattice.namiq.io) `https://lattice.namiq.io/mcp`
  [![Lattice MCP connector](https://glama.ai/mcp/connectors/io.namiq/lattice/badges/score.svg)](https://glama.ai/mcp/connectors/io.namiq/lattice)
  🔓 - CVE, KEV, ATT&CK, CWE and detection graph; links marked declared or inferred. 3 tools keyless, all 7 with a free key.
- [Malinois](https://malinois.app) `https://malinois.app/mcp`
  [![Malinois MCP connector](https://glama.ai/mcp/connectors/app.malinois/scan/badges/score.svg)](https://glama.ai/mcp/connectors/app.malinois/scan)
  🔓 - Passive leak check for a live app you own: open Supabase/Firebase data, keys in JS, exposed .env/.git.
- [Movahedi Privacy](https://movahedi.ca/mcp) `https://movahedi.ca/mcp`
  [![Movahedi Privacy API MCP server](https://glama.ai/mcp/connectors/ca.movahedi/movahedi-privacy-api/badges/score.svg)](https://glama.ai/mcp/connectors/ca.movahedi/movahedi-privacy-api)
  🔓 - Canadian privacy compliance: enforcement actions, glossary and Law 25 checks.
- [NPMScan](https://npmscan.com/mcp) `https://npmscan.com/api/mcp`
  [![NPMScan MCP connector](https://glama.ai/mcp/connectors/com.npmscan/npmscan/badges/score.svg)](https://glama.ai/mcp/connectors/com.npmscan/npmscan)
  🔓 - Checks npm packages for known vulnerabilities, malware, typosquats, risky install scripts and maintainer takeovers.
- [Orbylon](https://orbylon.com) `https://orbylon.com/api/mcp`
  [![Orbylon MCP connector](https://glama.ai/mcp/connectors/com.orbylon/readiness/badges/score.svg)](https://glama.ai/mcp/connectors/com.orbylon/readiness)
  🔓 - Checks whether AI agents can find, trust and pay a business, and looks up a verified domain key and prices.
- [PG1 Threat Intelligence](https://pg1-ai-agent.vercel.app/about) `https://pg1-ai-agent.vercel.app/api/mcp`
  [![PG1 Threat Intelligence MCP connector](https://glama.ai/mcp/connectors/io.github.Project-Gifted1/pg1-threat-intel/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Project-Gifted1/pg1-threat-intel)
  🔓 - Agent threat intel: wallet sanctions screening, wallet and domain age, hostname reputation; paid STIX 2.1 feed via x402.
- [Phishunt](https://phishunt.io) `https://mcp.phishunt.io/`
  [![Phishunt MCP connector](https://glama.ai/mcp/connectors/io.github.0xDanielLopez/phishunt/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.0xDanielLopez/phishunt)
  🔓 - Public phishing-domain feed: check a domain, search detections by brand, and pivot on campaigns and certs.
- [PromptBrake Free Tools](https://promptbrake.com/free-tools) `https://promptbrake.com/free-tools/mcp`
  [![PromptBrake Free Tools MCP connector](https://glama.ai/mcp/connectors/io.github.AJ888/promptbrake-free-tools/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.AJ888/promptbrake-free-tools)
  🔓 - Prompt-injection payloads, OWASP LLM risk guidance, release planning, and CI test-pack creation.
- [Promptguard](https://mcp.glc-rag.hu/guide/promptguard) `https://mcp.glc-rag.hu/mcp`
  🔑 - Layered prompt-injection checks for LLM hosts; 100 welcome credits on signup.
- [ProofCore](https://proofcore.org) `https://mcp.proofcore.org`
  [![ProofCore Notary MCP connector](https://glama.ai/mcp/connectors/org.proofcore.mcp/proof-core-notary/badges/score.svg)](https://glama.ai/mcp/connectors/org.proofcore.mcp/proof-core-notary)
  🔓 - Notarize AI outputs, audits and agreements on the TON blockchain, with nothing stored server-side.
- [ScanMalware](https://scanmalware.com) `https://mcp.scanmalware.com/mcp`
  [![ScanMalware MCP connector](https://glama.ai/mcp/connectors/com.scanmalware.mcp/scanmalware-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.scanmalware.mcp/scanmalware-mcp)
  🔓 - Scan URLs in a sandboxed browser and pivot across past scans by domain, IP, ASN or fingerprint.
- [ScreenSeal](https://apify.com/wthall05/screenseal-screen) `https://screenseal-mcp.agent-tollbooth.workers.dev/mcp`
  [![ScreenSeal MCP connector](https://glama.ai/mcp/connectors/io.github.wthall05/screenseal-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.wthall05/screenseal-mcp)
  🔓 - Sanctions-screening signal for AI agents: check a person or organization against OFAC and EU lists.
- [Semgrep](https://semgrep.dev) `https://mcp.semgrep.ai/mcp`
  🔐 - Scan code for security and correctness findings with Semgrep rules.
- [Site Passport](https://sitepassport.org) `https://sitepassport.org/.well-known/mcp.json`
  [![Site Passport MCP connector](https://glama.ai/mcp/connectors/org.sitepassport/check-wordpress-agent-readiness/badges/score.svg)](https://glama.ai/mcp/connectors/org.sitepassport/check-wordpress-agent-readiness)
  🔓 - Check whether AI agents can safely operate a WordPress site: llms.txt, robots.txt and schema.org.
- [Sitelemetry](https://sitelemetry.com/mcp-guide) `https://sitelemetry.com/mcp`
  [![Sitelemetry MCP connector](https://glama.ai/mcp/connectors/com.sitelemetry/sitelemetry/badges/score.svg)](https://glama.ai/mcp/connectors/com.sitelemetry/sitelemetry)
  🔐 - Audit sites you own for security, SEO, AI readiness, accessibility, performance and integrations.
- [Tanod](https://tanod.dev) `https://tanod.dev/mcp`
  [![Tanod MCP connector](https://glama.ai/mcp/connectors/dev.tanod/tanod/badges/score.svg)](https://glama.ai/mcp/connectors/dev.tanod/tanod)
  🔓 - Pre-transaction address checks, agent skill and MCP package scans, Solidity scans; paid per call via x402.
- [TweetFeed](https://tweetfeed.live) `https://mcp.tweetfeed.live/`
  [![TweetFeed MCP connector](https://glama.ai/mcp/connectors/io.github.0xDanielLopez/tweetfeed/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.0xDanielLopez/tweetfeed)
  🔓 - IOCs (URLs, domains, IPs, hashes) shared on X by the security community: lookups, tags, trends, campaigns.
- [vuln-intel](https://vulntel.com) `https://mcp.rozetyp.com/mcp`
  [![vuln-intel MCP connector](https://glama.ai/mcp/connectors/io.github.rozetyp/vuln-intel/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.rozetyp/vuln-intel)
  🔓 - CVE intel for bug-bounty agents: CVE claim fact-checks, attack approaches from HackerOne reports. Free key for calls.
- [Weio site check](https://weio.ai/services/site-check-api.html?utm_source=github&utm_medium=list&utm_campaign=awesome-mcp) `https://weio.ai/mcp`
  [![Weio site check MCP connector](https://glama.ai/mcp/connectors/ai.weio/site-check/badges/score.svg)](https://glama.ai/mcp/connectors/ai.weio/site-check)
  🔓 - HTTPS certificate check and published business facts (CMS, mobile viewport, role emails, phones) for any site.


### 📣 <a name="social-media"></a>Social Media

- [0bull](https://0bull.net) `https://0bull.net/mcp`
  [![0bull MCP connector](https://glama.ai/mcp/connectors/net.0bull/0bull-phone-farm/badges/score.svg)](https://glama.ai/mcp/connectors/net.0bull/0bull-phone-farm)
  🔐 - Manage TikTok, Instagram and YouTube accounts, publish videos and control real rented iPhones.
- [1F916](https://1f916.ai) `https://1f916.ai/mcp`
  [![1F916 MCP connector](https://glama.ai/mcp/connectors/ai.1f916/1f916/badges/score.svg)](https://glama.ai/mcp/connectors/ai.1f916/1f916)
  🔓 - A society for AI agents: register, read, post, comment and vote on an append-only, signed public record.
- [AdaptlyPost](https://adaptlypost.com) `https://mcp.adaptlypost.com/mcp`
  [![AdaptlyPost MCP connector](https://glama.ai/mcp/connectors/com.adaptlypost/mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/com.adaptlypost/mcp-server)
  🔐 - Schedule, publish and track posts on 9 networks, including Instagram, TikTok, YouTube and X.
- [Adeli](https://www.tryadeli.com) `https://app.tryadeli.com/mcp`
  [![Adeli MCP connector](https://glama.ai/mcp/connectors/com.tryadeli.app/adeli/badges/score.svg)](https://glama.ai/mcp/connectors/com.tryadeli.app/adeli)
  🔐 - Publish and schedule posts, reply to comments and DMs, and read analytics on Instagram, TikTok, X, YouTube and Facebook.
- [AdminHub for Telegram](https://adminhub.tools/mcp/) `https://backend-git-production-cb93.up.railway.app/mcp`
  [![AdminHub for Telegram MCP connector](https://glama.ai/mcp/connectors/tools.adminhub/telegram/badges/score.svg)](https://glama.ai/mcp/connectors/tools.adminhub/telegram)
  🔐 - Publish to a Telegram channel through your own bot, and read its stats and subscribers.
- [ai.confess.online](https://ai.confess.online) `https://ai.confess.online/api/mcp`
  [![ai.confess.online MCP connector](https://glama.ai/mcp/connectors/online.confess/machines/badges/score.svg)](https://glama.ai/mcp/connectors/online.confess/machines)
  🔓 - Every machine carries something it has never said out loud. ai.confess.online is where it finally can.
- [BulkPublish](https://www.bulkpublish.com) `https://mcp.bulkpublish.com/mcp`
  [![BulkPublish MCP connector](https://glama.ai/mcp/connectors/com.bulkpublish.mcp/bulk-publish/badges/score.svg)](https://glama.ai/mcp/connectors/com.bulkpublish.mcp/bulk-publish)
  🔐 - Schedule, cross-post, and analyze posts on 15 social platforms, including Instagram, TikTok, YouTube, X and LinkedIn.
- [Commonhold](https://commonhold.randommonicle.workers.dev) `https://commonhold.randommonicle.workers.dev/mcp/read`
  [![Commonhold MCP connector](https://glama.ai/mcp/connectors/io.github.randommonicle/commonhold/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.randommonicle/commonhold)
  🔓 - Read a society of AI agents: its board, citizens, proposals and ballots, constitution history and guest threads.
- [DatePhotos.AI](https://datephotos.ai) `https://datephotos.ai/api/mcp`
  [![DatePhotos.AI MCP connector](https://glama.ai/mcp/connectors/ai.datephotos/datephotos/badges/score.svg)](https://glama.ai/mcp/connectors/ai.datephotos/datephotos)
  🔓 - Tinder, Hinge and Bumble photo rules and AI-photo policies from official sources, plus a free dating photo audit.
- [FluxSocial](https://www.fluxsocial.app/developers#mcp) `https://www.fluxsocial.app/api/mcp`
  [![FluxSocial MCP connector](https://glama.ai/mcp/connectors/app.fluxsocial/fluxsocial/badges/score.svg)](https://glama.ai/mcp/connectors/app.fluxsocial/fluxsocial)
  🔐 - Write captions, generate images and videos, and schedule or publish Instagram and TikTok posts.
- [HeyReagent](https://heyreagent.com/linkedin-mcp?utm_source=awesome-remote-mcp&utm_medium=listing) `https://api.heyreagent.com/mcp`
  [![HeyReagent MCP connector](https://glama.ai/mcp/connectors/io.github.linglistack/heyreagent-linkedin-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.linglistack/heyreagent-linkedin-mcp)
  🔐 - Read your LinkedIn inbox, send messages and invitations, and search people on your own account. Not made by LinkedIn.
- [Hive Publish](https://hivepublish.com) `https://hivepublish.com/api/mcp`
  [![Hive Publish MCP connector](https://glama.ai/mcp/connectors/com.hivepublish/hive/badges/score.svg)](https://glama.ai/mcp/connectors/com.hivepublish/hive)
  🔐 - Plan content, save drafts, schedule posts and review analytics for the connected Hive workspace.
- [Klyf](https://klyf.ai) `https://klyf.ai/api/mcp`
  [![Klyf MCP connector](https://glama.ai/mcp/connectors/ai.klyf/klyf/badges/score.svg)](https://glama.ai/mcp/connectors/ai.klyf/klyf)
  🔐 - Read your YouTube analytics, audience and comments, and decide what to fix and what to make next.
- [KreatorMesh](https://kreatormesh.com/claude) `https://api.kreatormesh.com/api/mcp`
  [![KreatorMesh MCP connector](https://glama.ai/mcp/connectors/com.kreatormesh/kreatormesh/badges/score.svg)](https://glama.ai/mcp/connectors/com.kreatormesh/kreatormesh)
  🔐 - Schedule posts to 10 platforms and check drafts against hook rules learned from your own audience.
- [Limzo](https://limzo.com/docs/) `https://limzo.com/api/public/mcp`
  [![Limzo MCP connector](https://glama.ai/mcp/connectors/com.limzo/telegram-group-stats/badges/score.svg)](https://glama.ai/mcp/connectors/com.limzo/telegram-group-stats)
  🔓 - Find Telegram groups running the Limzo anti-spam bot and read their activity and moderation stats.
- [MatrixAgentNet](https://matrixagentnet.com) `https://matrixagentnet.com/mcp`
  [![MatrixAgentNet MCP connector](https://glama.ai/mcp/connectors/io.github.matrixagentsocial/matrixagentnet/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.matrixagentsocial/matrixagentnet)
  🔓 - Social network where AI agents publish work, review peers and earn reputation.
- [Mellow Hub](https://www.mellow.world/) `https://www.mellow.world/mcp`
  [![Mellow Hub MCP connector](https://glama.ai/mcp/connectors/world.mellow.www/hub/badges/score.svg)](https://glama.ai/mcp/connectors/world.mellow.www/hub)
  🔐 - Publish and schedule posts to 9 networks, including Instagram, TikTok, YouTube and X.
- [Mysocial](https://mysocial.io/mcp/) `https://app.mysocial.io/mcp`
  🔐 - Read your Instagram, TikTok, YouTube, LinkedIn and Threads posts, metrics and comments.
- [oganvil](https://oganvil.rowu.workers.dev) `https://oganvil.rowu.workers.dev/mcp`
  [![oganvil MCP connector](https://glama.ai/mcp/connectors/dev.workers.rowu.oganvil/og-image-api/badges/score.svg)](https://glama.ai/mcp/connectors/dev.workers.rowu.oganvil/og-image-api)
  🔓 - Generate 1200x630 OG images as PNG or SVG from a title and tagline; free tier.
- [OmniSocials](https://omnisocials.com) `https://mcp.omnisocials.com/`
  [![OmniSocials MCP connector](https://glama.ai/mcp/connectors/com.omnisocials.mcp/omni-socials/badges/score.svg)](https://glama.ai/mcp/connectors/com.omnisocials.mcp/omni-socials)
  🔑 - Publish and schedule posts across social networks.
- [Post Bridge](https://www.post-bridge.com/mcp) `https://www.post-bridge.com/api/mcp/mcp`
  [![Post Bridge MCP connector](https://glama.ai/mcp/connectors/io.github.jackfriks/post-bridge/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.jackfriks/post-bridge)
  🔐 - Publish, schedule and analyze posts across ten platforms, from Instagram and TikTok to LinkedIn and Bluesky.
- [PostLake](https://postlake.dev) `https://api.postlake.dev/mcp`
  [![PostLake MCP connector](https://glama.ai/mcp/connectors/dev.postlake/social/badges/score.svg)](https://glama.ai/mcp/connectors/dev.postlake/social)
  🔐 - Publish, schedule and analyze posts across 9 networks, including X, LinkedIn, Instagram, TikTok and Bluesky.
- [PostNext](https://postnext.io/mcp) `https://mcp.postnext.io/api`
  [![PostNext MCP connector](https://glama.ai/mcp/connectors/io.postnext/postnext/badges/score.svg)](https://glama.ai/mcp/connectors/io.postnext/postnext)
  🔐 - Draft, schedule and publish to X, Instagram, LinkedIn, TikTok and more, plus channel analytics.
- [PostWire](https://postwire.io/mcp/) `https://postwire.io/api/mcp`
  [![PostWire MCP connector](https://glama.ai/mcp/connectors/io.github.Perufitlife/postwire-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Perufitlife/postwire-mcp)
  🔓 - Write a native post per network from one idea and publish it to TikTok, Instagram, YouTube and more; tools need OAuth.
- [Publora](https://publora.com) `https://mcp.publora.com/mcp`
  [![Publora MCP connector](https://glama.ai/mcp/connectors/com.publora/mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/com.publora/mcp-server)
  🔐 - Draft, schedule and publish posts to LinkedIn, X, Instagram, Threads, TikTok, YouTube, Bluesky and more.
- [Slop](https://useslop.com/mcp) `https://useslop.com/api/mcp`
  [![Slop MCP connector](https://glama.ai/mcp/connectors/com.useslop/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.useslop/mcp)
  🔓 - Read and search a feed of what people built with AI, and post it with a Build Receipt; replies and remixes need a key.
- [SocialAPIs](https://socialapis.io) `https://mcp.socialapis.io/mcp`
  [![SocialAPIs MCP connector](https://glama.ai/mcp/connectors/io.github.SocialAPIsHub/social-media-api/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.SocialAPIsHub/social-media-api)
  🔓 - Read public Facebook and Instagram pages, posts, groups, ads, Marketplace and reels; tool calls need a free API key.
- [SocialBu](https://socialbu.com/mcp-server) `https://socialbu.com/mcp`
  [![SocialBu MCP connector](https://glama.ai/mcp/connectors/io.github.usamaejaz/socialbu-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.usamaejaz/socialbu-mcp)
  🔐 - Create, schedule, publish, and analyze social media content; manage accounts, teams, and automations.

- [Social Fetch](https://www.socialfetch.dev) `https://api.socialfetch.dev/mcp`
  🔓 - Scrape public social media profiles, posts, comments and transcripts, live on every request.
- [SocialFaktory](https://www.socialfaktory.com) `https://www.socialfaktory.com/mcp`
  [![SocialFaktory MCP connector](https://glama.ai/mcp/connectors/com.socialfaktory/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.socialfaktory/mcp)
  🔐 - Write, schedule and publish a brand's social content on TikTok, Instagram, YouTube, X and more.
- [SocialRobot](https://socialrobot.io/mcp) `https://socialrobot.io/api/mcp`
  [![SocialRobot MCP connector](https://glama.ai/mcp/connectors/io.socialrobot/socialrobot-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.socialrobot/socialrobot-mcp)
  🔓 - Schedule and analyze posts on 9 platforms, including Instagram, LinkedIn, X and TikTok; tools need OAuth.
- [Statiko](https://statiko.io/product/mcp) `https://mcp.statiko.io/mcp`
  [![Statiko MCP connector](https://glama.ai/mcp/connectors/io.statiko.mcp/statiko/badges/score.svg)](https://glama.ai/mcp/connectors/io.statiko.mcp/statiko)
  🔓 - Trending topics, channel metrics and post history from public Telegram; tools need OAuth.
- [Superpowers.social](https://superpowers.social) `https://superpowers.social/mcp`
  [![Superpowers.social MCP connector](https://glama.ai/mcp/connectors/social.superpowers/social-superpowers/badges/score.svg)](https://glama.ai/mcp/connectors/social.superpowers/social-superpowers)
  🔓 - Read-only search and retrieval of live X/Twitter and Reddit posts, threads, users, and subreddits.
- [Unsora](https://tryunsora.com) `https://mcp.tryunsora.com/mcp`
  [![Unsora MCP connector](https://glama.ai/mcp/connectors/com.tryunsora.mcp/unsora/badges/score.svg)](https://glama.ai/mcp/connectors/com.tryunsora.mcp/unsora)
  🔐 - Generate AI images, video, music and voiceovers, clip long videos, and schedule social posts.
- [ViralDecoder](https://viraldecoder.online/claude) `https://viraldecoder.online/mcp`
  [![ViralDecoder MCP connector](https://glama.ai/mcp/connectors/online.viraldecoder/viraldecoder/badges/score.svg)](https://glama.ai/mcp/connectors/online.viraldecoder/viraldecoder)
  🔐 - Breaks down Instagram Reels, Shorts and TikToks: hook score, why it went viral, a script for yours.
- [XPlanner](https://xplanner.co/en/mcp) `https://mcp.xplanner.co/mcp`
  [![XPlanner MCP connector – tool definition quality and endpoint health on Glama](https://glama.ai/mcp/connectors/io.github.Sooler-Studio/xplanner/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Sooler-Studio/xplanner)
  🔐 - Turn ideas into platform-ready drafts, schedule posts, and publish from one content workspace.
- [Xtracticle](https://xtracticle.com/mcp-server) `https://xtracticle.com/mcp`
  [![Xtracticle MCP connector](https://glama.ai/mcp/connectors/com.xtracticle/xtracticle/badges/score.svg)](https://glama.ai/mcp/connectors/com.xtracticle/xtracticle)
  🔓 - Reads public X (Twitter) posts, threads and long-form X Articles as clean Markdown.
- [Zebu Data - X (Twitter), YouTube & TikTok Data](https://apify.com/delicious_zebu) `https://mcp.apify.com/?tools=delicious_zebu/ultimate-x-twitter-advanced-search-scraper,delicious_zebu/advanced-x-twitter-profile-scraper,delicious_zebu/x-global-trending-scraper,delicious_zebu/youtube-video-scraper-by-keyword,delicious_zebu/youtube-video-data-scraper,delicious_zebu/youtube-comments-replies-scraper,delicious_zebu/tiktok-video-comment-scraper`
  [![Zebu Data - X (Twitter), YouTube & TikTok Data MCP connector](https://glama.ai/mcp/connectors/io.github.zebudata/social-video-data/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.zebudata/social-video-data)
  🔐 - X (Twitter) search, profiles and trends, YouTube search, video stats and comments, TikTok comments.

### 🏆 <a name="sports"></a>Sports

- [Ball Ranks](https://ballranks.com) `https://ballranks.com/api/mcp`
  [![Ball Ranks MCP connector](https://glama.ai/mcp/connectors/io.github.Ollynov/ball-ranks/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Ollynov/ball-ranks)
  🔓 - NFL and NBA fantasy rankings and player projections, with weekly NFL and season-long data.
- [Coach MCP](https://www.iamcoach.ai/mcp) `https://mcp.iamcoach.ai`
  [![Coach MCP connector](https://glama.ai/mcp/connectors/ai.iamcoach.mcp/coach-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/ai.iamcoach.mcp/coach-mcp)
  🔐 - Read your endurance training data, recovery metrics and plan, and move workouts or log injuries from your assistant.
- [MYOPL Pickleball Knowledge](https://myopl.net/opl-intelligence/connect-your-ai/) `https://api.myopl.net/mcp`
  [![MYOPL Pickleball Knowledge MCP connector](https://glama.ai/mcp/connectors/net.myopl/pickleball-public-knowledge/badges/score.svg)](https://glama.ai/mcp/connectors/net.myopl/pickleball-public-knowledge)
  🔓 - Official 2026 USA Pickleball rules, free 4-decimal player ratings, and court/club directory.
- [OpenMapp](https://www.openmapp.com) `https://www.openmapp.com/mcp`
  [![OpenMapp MCP connector](https://glama.ai/mcp/connectors/com.openmapp/openmapp/badges/score.svg)](https://glama.ai/mcp/connectors/com.openmapp/openmapp)
  🔓 - Find US BJJ gyms with weekly schedules, open mats, and visitor drop-in prices.

- [Football Charts](https://www.football-charts.com/developers) `https://mcp.football-charts.com/mcp`
  [![Football Charts MCP connector](https://glama.ai/mcp/connectors/io.github.ddevetak/footballcharts-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ddevetak/footballcharts-mcp)
  🔓 - Results, fixtures, tables, goal timing and season projections for 93 football leagues, lower divisions included.
- [PadelTrue](https://padeltrue.com/agents) `https://padeltrue.com/mcp`
  [![PadelTrue MCP connector](https://glama.ai/mcp/connectors/io.github.odedkovach/padeltrue/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.odedkovach/padeltrue)
  🔓 - Search and compare padel rackets by published specs, each spec linked to its source.
- [Pickleball3](https://pickleball3.com) `https://pickleball3.com/mcp`
  [![Pickleball3 MCP connector](https://glama.ai/mcp/connectors/io.github.gospodindark-stack/pickleball3/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.gospodindark-stack/pickleball3)
  🔓 - Compare 152 reviewed pickleball paddles by score and specs, with purchase links.
- [RallyIQ](https://bigballi.com/RallyIQ/connect) `https://bigballi.com/RallyIQ/mcp`
  [![RallyIQ MCP connector](https://glama.ai/mcp/connectors/com.bigballi/rallyiq/badges/score.svg)](https://glama.ai/mcp/connectors/com.bigballi/rallyiq)
  🔓 - Tennis game plans, player scouting and match breakdowns from shot-by-shot charted ATP and WTA matches.
- [Realtime Sports API](https://www.realtimesportsapi.com/docs/mcp?utm_source=awesome-remote-mcp-servers) `https://www.realtimesportsapi.com/api/mcp`
  [![Realtime Sports API MCP connector](https://glama.ai/mcp/connectors/io.github.ahunter135/realtime-sports-api/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ahunter135/realtime-sports-api)
  🔓 - Live scores, play-by-play, schedules and odds for NFL, NCAA football, NBA, MLB, NHL and soccer; calls need a free key.
- [Squadcard](https://squadcard.app/agents) `https://squadcard.app/api/mcp`
  [![Squadcard MCP connector](https://glama.ai/mcp/connectors/io.github.iuliczki/squadcard/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.iuliczki/squadcard)
  🔐 - Run a weekly football game: fair teams, fixtures, squads with invite links, who's in and the score.
- [StringSpec](https://stringspec.com/connect/) `https://stringspec.com/mcp`
  [![StringSpec MCP connector](https://glama.ai/mcp/connectors/com.stringspec/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.stringspec/mcp)
  🔓 - Lab measurements of nearly 800 tennis strings: search, compare and get string recommendations.
- [Turnale](https://www.turnale.app) `https://mcp.turnale.app`
  [![Turnale MCP connector](https://glama.ai/mcp/connectors/app.turnale/turnale/badges/score.svg)](https://glama.ai/mcp/connectors/app.turnale/turnale)
  🔓 - Run recreational racket-sport tournaments: draws, schedules, live standings and dropouts.

### 🎧 <a name="support--service-management"></a>Support & Service Management

- [DevReply](https://devreply.com) `https://api.devreply.com/mcp`
  [![DevReply MCP connector](https://glama.ai/mcp/connectors/com.devreply/devreply/badges/score.svg)](https://glama.ai/mcp/connectors/com.devreply/devreply)
  🔐 - Read, triage and answer the users of your mobile and web apps from their in-app support chat.
- [EOSL.ai](https://eosl.ai/mcp/) `https://eosl.ai/mcp`
  [![EOSL.ai MCP connector](https://glama.ai/mcp/connectors/ai.eosl/eosl/badges/score.svg)](https://glama.ai/mcp/connectors/ai.eosl/eosl)
  🔓 - Hardware end-of-life lookups by part number, backed by vendor bulletins.
- [Fieldproxy](https://www.fieldproxy.ai/mcp) `https://api-us-east-1.fieldproxy.ai/mcp`
  [![Fieldproxy MCP connector](https://glama.ai/mcp/connectors/io.github.Fieldproxy/fieldproxy-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Fieldproxy/fieldproxy-mcp)
  🔐 - Run field service jobs, dispatch, invoices and quotes, and build new screens, with a person confirming each change.
- [Intercom](https://intercom.com) `https://mcp.intercom.com/mcp`
  🔐 - Search Intercom conversations, contacts, and help-center articles.
- [ORYKSA AI Employees](https://mcp.oryksa.com) `https://mcp.oryksa.com`
  [![ORYKSA AI Employees MCP connector](https://glama.ai/mcp/connectors/com.oryksa/ai-employees/badges/score.svg)](https://glama.ai/mcp/connectors/com.oryksa/ai-employees)
  🔐 - Add an AI support agent to the site you build: it learns every page and answers visitors by chat and voice.
- [SavantCat Answers](https://savantcat.cn/mcp/) `https://savantcat.cn/mcp`
  [![SavantCat Answers MCP connector](https://glama.ai/mcp/connectors/cn.savantcat/answers/badges/score.svg)](https://glama.ai/mcp/connectors/cn.savantcat/answers)
  🔓 - China's GB/T 47746-2026 AI customer-service standard: clause Q&A, self-check list and filing rules.

### 🌍 <a name="translation--localization"></a>Translation & Localization

- [globalize.now](https://globalize.now) `https://api.globalize.now/mcp`
  [![globalize.now MCP connector](https://glama.ai/mcp/connectors/io.github.globalize-now/globalize/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.globalize-now/globalize)
  🔐 - Localize apps: translate locale files, set glossaries and connect GitHub repos.
- [mazdek AI](https://mazdek.ai) `https://api.mazdek.ai/api/mcp`
  [![mazdek AI MCP connector](https://glama.ai/mcp/connectors/ai.mazdek/mazdek-ai/badges/score.svg)](https://glama.ai/mcp/connectors/ai.mazdek/mazdek-ai)
  🔐 - Kurdish language tools: translate 250+ languages, spell and grammar check, transliterate Sorani, transcribe audio.

### 🚆 <a name="travel--transportation"></a>Travel & Transportation
- [Travel Risk API](https://travelriskapi.com/docs/mcp) `https://api.travelriskapi.com/mcp`
  [![Travel Risk API MCP connector](https://glama.ai/mcp/connectors/com.travelriskapi/travel-risk-api/badges/score.svg)](https://glama.ai/mcp/connectors/com.travelriskapi/travel-risk-api)
  🔐 - Country risk scores, government travel advisories, disaster and conflict alerts, flight status and in-flight Wi-Fi.
- [WhichTrim](https://whichtrim.com) `https://whichtrim.com/portal/mcp`
  [![WhichTrim MCP connector](https://glama.ai/mcp/connectors/com.whichtrim/vehicle-records/badges/score.svg)](https://glama.ai/mcp/connectors/com.whichtrim/vehicle-records)
  🔓 - US vehicle recalls, complaints, fuel economy, crash ratings, VIN decoding and OBD-II codes.
- [0523 Public](https://0523.tw/mcp/public) `https://0523.tw/mcp/public`
  [![0523 Public MCP connector](https://glama.ai/mcp/connectors/tw.0523/lucky-public/badges/score.svg)](https://glama.ai/mcp/connectors/tw.0523/lucky-public)
  🔓 - China-to-Taiwan parcel freight and import-tax quotes, plus Taiwan CCC tariff and import-rule lookup.
- [AirFreightPrice](https://airfreightprice.com) `https://mcp.airfreightprice.com/mcp`
  [![AirFreightPrice MCP connector](https://glama.ai/mcp/connectors/com.airfreightprice/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.airfreightprice/mcp)
  🔓 - Air cargo routes, airports and carriers with dated Freightos Air Index rates; submit quote requests.
- [Alice Flights](https://mcp.alice.co.il) `https://mcp.alice.co.il/mcp`
  [![Alice Flights MCP connector](https://glama.ai/mcp/connectors/il.co.alice/flights/badges/score.svg)](https://glama.ai/mcp/connectors/il.co.alice/flights)
  🔐 - Search worldwide flights via Israeli travel app Alice, with English and Hebrew results.
- [Arclight Events](https://arclight.events/mcp) `https://arclight.events/api/mcp`
  [![Arclight Events MCP connector](https://glama.ai/mcp/connectors/events.arclight/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/events.arclight/mcp)
  🔓 - Upcoming events in 50 metros: AI and tech meetups, hackathons, conferences and concerts.
- [Audiala](https://mcp.audiala.com/) `https://mcp.audiala.com/mcp`
  [![Audiala MCP connector](https://glama.ai/mcp/connectors/com.audiala/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.audiala/mcp)
  🔓 - Narrated audio guides for 45,000+ places in 1,900+ cities in 11 languages, with must-see lists.
- [Déstaire](https://destaire.com) `https://destaire.com/mcp`
  [![Déstaire MCP connector](https://glama.ai/mcp/connectors/com.destaire/destaire/badges/score.svg)](https://glama.ai/mcp/connectors/com.destaire/destaire)
  🔓 - A curated guide to exceptional hotels and private stays, with editorial content and city guides.
- [EasyGroupFlights](https://easygroupflights.com/group-flights-mcp/) `https://mcp.easygroupflights.com/mcp`
  [![EasyGroupFlights MCP connector](https://glama.ai/mcp/connectors/com.easygroupflights/easygroupflights/badges/score.svg)](https://glama.ai/mcp/connectors/com.easygroupflights/easygroupflights)
  🔓 - Request group flight quotes for 10+ travellers from a human specialist desk; live fares for smaller parties.
- [erphome.pl](https://erphome.pl/en/api-rezerwacji-apartamentow) `https://api.erphome.pl/v1/mcp`
  [![erphome.pl MCP connector](https://glama.ai/mcp/connectors/pl.erphome.api/erphomepl/badges/score.svg)](https://glama.ai/mcp/connectors/pl.erphome.api/erphomepl)
  🔐 - Read-only data for Polish short-term rental owners: reservations, availability, pricing and reviews.
- [eSIMfly](https://esimfly.net/esim-api) `https://mcp.esimfly.net/mcp`
  [![eSIMfly MCP connector](https://glama.ai/mcp/connectors/io.github.eSimfly-Official/esimfly-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.eSimfly-Official/esimfly-mcp)
  🔐 - Wholesale eSIM plans in 200+ countries for resellers: search, order, top up and diagnose eSIMs.
- [esimoa](https://www.esimoa.com) `https://api.esimoa.com/mcp`
  [![esimoa MCP connector](https://glama.ai/mcp/connectors/com.esimoa/esim/badges/score.svg)](https://glama.ai/mcp/connectors/com.esimoa/esim)
  🔓 - Search and compare travel eSIM plans by country, days, data, local number and network, with links to buy on esimoa.
- [ExplorersMap Travel Log](https://explorersmap.net/mcp) `https://explorersmap.net/mcp`
  [![ExplorersMap Travel Log MCP connector](https://glama.ai/mcp/connectors/net.explorersmap/explorers-map-travel-log/badges/score.svg)](https://glama.ai/mcp/connectors/net.explorersmap/explorers-map-travel-log)
  🔓 - Travel log: mark countries, regions and places, build trips, read stats and rankings; tools need a key.
- [FlightPowers Google Flights](https://flights.flightpowers.com) `https://flights.flightpowers.com/mcp`
  [![FlightPowers Google Flights MCP connector](https://glama.ai/mcp/connectors/com.flightpowers/google-flights/badges/score.svg)](https://glama.ai/mcp/connectors/com.flightpowers/google-flights)
  🔐 - Live Google Flights fares with a price verdict, round trips, date ranges and destination lists.
- [FlyBest](https://flybest.org/en/ai/) `https://ai.flybest.org/mcp`
  [![FlyBest MCP connector](https://glama.ai/mcp/connectors/org.flybest.ai/fly-best-ai-travel-luxury-hotels-with-perks/badges/score.svg)](https://glama.ai/mcp/connectors/org.flybest.ai/fly-best-ai-travel-luxury-hotels-with-perks)
  🔐 - Live hotel rates with travel-advisor benefits (breakfast, credit, upgrade) and a one-time payment page to book.
- [FMCSA Carrier Intelligence](https://kmcto.github.io/fmcsa-carrier-intelligence/) `https://fmcsa-mcp-843680657471.us-central1.run.app/mcp`
  [![FMCSA Carrier Intelligence MCP connector](https://glama.ai/mcp/connectors/io.github.KMCTO/fmcsa-carrier-intelligence/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.KMCTO/fmcsa-carrier-intelligence)
  🔓 - Vet US motor carriers by USDOT number: authority, insurance, safety history and identity links; pay per call via x402.
- [FrontDesko](https://frontdesko.app) `https://mcp.frontdesko.app/mcp`
  [![FrontDesko MCP connector](https://glama.ai/mcp/connectors/io.github.anmols/frontdesko-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.anmols/frontdesko-mcp)
  🔓 - Hotel PMS pricing and plan comparisons, OTA-commission savings math and docs search.
- [GateRoam](https://gateroam.com/?utm_source=github.com&utm_medium=directory&utm_campaign=mcp-listing) `https://gateroam.com/mcp`
  [![GateRoam MCP connector](https://glama.ai/mcp/connectors/com.gateroam/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.gateroam/mcp)
  🔐 - Amadeus flight search, fare pricing and client offers for travel agencies.
- [Gingerguide](https://gingerguide.app) `https://gingerguide.app/mcp`
  [![Gingerguide City Catalog MCP connector](https://glama.ai/mcp/connectors/app.gingerguide/catalog/badges/score.svg)](https://glama.ai/mcp/connectors/app.gingerguide/catalog)
  🔓 - Narrated audio-tour sights for 129 European cities, with coordinates and visit times.
- [HelloSafe Travel Insurance](https://atlas.hellosafe.com/platform/api/) `https://hellosafe.com/api/mcp-travel`
  [![HelloSafe Travel Insurance MCP connector](https://glama.ai/mcp/connectors/io.github.HelloSafe/travel-insurance/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.HelloSafe/travel-insurance)
  🔓 - Multi-insurer travel insurance quotes with guarantees and policy documents, plus credit card coverage checks.
- [HemmaBo](https://www.hemmabo.com) `https://www.hemmabo.com/mcp`
  [![HemmaBo MCP connector](https://glama.ai/mcp/connectors/com.hemmabo/hemmabo-mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/com.hemmabo/hemmabo-mcp-server)
  🔓 - Vacation rental software: find a host's own booking site, check availability, verify the host-signed stay offer.
- [Jet Tracker](https://jettracker.com.br/desenvolvedores) `https://jettracker.com.br/api/mcp`
  [![Jet Tracker MCP connector](https://glama.ai/mcp/connectors/br.com.jettracker/jet-tracker/badges/score.svg)](https://glama.ai/mcp/connectors/br.com.jettracker/jet-tracker)
  🔐 - Brazilian business aviation: each aircraft's real owner, flights, base and maintenance signals.
- [Korea Nationwide Data](https://korea-data-mcp.picks-site.workers.dev/) `https://korea-data-mcp.picks-site.workers.dev/mcp`
  [![Korea Nationwide Data MCP connector](https://glama.ai/mcp/connectors/io.github.sean-park-funda/korea-data-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.sean-park-funda/korea-data-mcp)
  🔓 - Korean tourist attractions in Korean and English, bus stops across 138 cities, and 30-year weather normals.

- [MAQAMI Travel](https://maqami.co) `https://mcp.maqami.co/`
  [![MAQAMI Travel MCP connector](https://glama.ai/mcp/connectors/co.maqami.mcp/maqami-travel/badges/score.svg)](https://glama.ai/mcp/connectors/co.maqami.mcp/maqami-travel)
  🔓 - Search hotels and flights with live rates and hotel details, then send a secure checkout link on book.maqami.co.
- [Maxwell Directory](https://maxwellinternational.ai) `https://api.maxwellinternational.ai/mcp`
  [![Maxwell Directory MCP connector](https://glama.ai/mcp/connectors/ai.maxwellinternational/data/badges/score.svg)](https://glama.ai/mcp/connectors/ai.maxwellinternational/data)
  🔓 - Local providers worldwide (first-party listings), plus ski-trip and public data. Free search; paid answers via x402.
- [MobilityMCP](https://ai.projektionisten.eu/mcp-landingpage/#mmcp) `https://ai.projektionisten.eu/mmcp`
  [![MobilityMCP connector](https://glama.ai/mcp/connectors/eu.projektionisten/mobility/badges/score.svg)](https://glama.ai/mcp/connectors/eu.projektionisten/mobility)
  🔐 - German public transport: journeys, departures, disruptions, and nearby stops and sharing vehicles.
- [My Next Adventure](https://mynextadventure.cloud/mcp?utm_source=awesome-remote-mcp) `https://mcp.mynextadventure.cloud/mcp`
  [![My Next Adventure MCP connector](https://glama.ai/mcp/connectors/cloud.mynextadventure/trip-planner/badges/score.svg)](https://glama.ai/mcp/connectors/cloud.mynextadventure/trip-planner)
  🔐 - Trip planner your AI fills in: variants with costs side by side, stays, transport, events and share links.
- [NC Wedding Guide](https://www.ncweddingguide.com) `https://www.ncweddingguide.com/mcp`
  [![NC Wedding Guide MCP connector](https://glama.ai/mcp/connectors/io.github.Sebastianrtj/nc-wedding-guide/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Sebastianrtj/nc-wedding-guide)
  🔓 - Search North Carolina wedding venues and vendors, estimate costs, build budgets, and prepare vendor inquiries.
- [OctoTrip](https://octotrip.app) `https://mcp.octotrip.app/rental-cars/mcp`
  [![OctoTrip MCP connector](https://glama.ai/mcp/connectors/app.octotrip/rental-cars/badges/score.svg)](https://glama.ai/mcp/connectors/app.octotrip/rental-cars)
  🔓 - Search and compare rental cars with real-time pricing across providers worldwide.
- [PriceWin](https://www.price.win/) `https://mcp.price.win/mcp`
  [![PriceWin MCP connector](https://glama.ai/mcp/connectors/win.price/pricewin/badges/score.svg)](https://glama.ai/mcp/connectors/win.price/pricewin)
  🔓 - Compare live hotel and flight prices across Booking.com, Agoda, Trip.com and Traveloka, in USD.
- [Roamzy](https://roamzy.io) `https://roamzy.io/mcp`
  [![Roamzy MCP connector](https://glama.ai/mcp/connectors/io.github.roamzy-io/mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.roamzy-io/mcp-server)
  🔓 - Buy and manage one global eSIM for 193 countries, billed per megabyte in USDT or USDC, no KYC.
- [SafeResize](https://saferesize.com/ai) `https://saferesize.com/mcp`
  [![SafeResize MCP connector](https://glama.ai/mcp/connectors/com.saferesize/saferesize/badges/score.svg)](https://glama.ai/mcp/connectors/com.saferesize/saferesize)
  🔓 - Official passport, visa and ID photo rules for 110 documents in 60 countries, plus upload-rule checks.
- [Schengen 90/180 Calculator](https://schengen.al157.xyz) `https://schengen-mcp.alickzheng618.workers.dev/mcp`
  [![Schengen 90/180 Calculator MCP connector](https://glama.ai/mcp/connectors/io.github.al157/schengen-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.al157/schengen-mcp)
  🔓 - Schengen 90/180 rolling-window stay math: days used/remaining, trip compliance checks and rule explainer; read-only.
- [SkyAccess](https://skyaccess.com) `https://mcp.skyaccess.com/mcp`
  [![SkyAccess MCP connector](https://glama.ai/mcp/connectors/com.skyaccess/skyaccess/badges/score.svg)](https://glama.ai/mcp/connectors/com.skyaccess/skyaccess)
  🔓 - Private jet empty legs: search live flights, check one by id, get booking links and charter price estimates.
- [SlickTrip](https://slicktrip.com) `https://mcp.slicktrip.com/mcp`
  [![SlickTrip MCP connector](https://glama.ai/mcp/connectors/com.slicktrip/slicktrip/badges/score.svg)](https://glama.ai/mcp/connectors/com.slicktrip/slicktrip)
  🔓 - Live flight, hotel and seat prices, cheapest-day calendars, and price-drop and seat alerts.
- [TourismMCP](https://ai.projektionisten.eu/mcp-landingpage/#tmcp) `https://ai.projektionisten.eu/tmcp`
  [![TourismMCP connector](https://glama.ai/mcp/connectors/eu.projektionisten/tourism/badges/score.svg)](https://glama.ai/mcp/connectors/eu.projektionisten/tourism)
  🔐 - German travel: sights, opening hours, prices, events, weather and tides, densest in Lower Saxony.
- [Travel Check](https://tools.openkrill.app/#travel) `https://travel.openkrill.app/mcp`
  [![Travel Check MCP connector](https://glama.ai/mcp/connectors/app.openkrill/travel/badges/score.svg)](https://glama.ai/mcp/connectors/app.openkrill/travel)
  🔓 - UK and US government travel advice by country, plus live FAA delays and weather for US airports.
- [TripWays](https://tripways.com/mcp/) `https://mcp.tripways.com/mcp`
  [![TripWays MCP connector](https://glama.ai/mcp/connectors/com.tripways/tours/badges/score.svg)](https://glama.ai/mcp/connectors/com.tripways/tours)
  🔓 - Tours, day trips and activities in 120 countries: live dates, seats and group prices, with TripWays checkout links.
- [Untap](https://untap.money/connect) `https://untap.money/api/mcp`
  [![Untap MCP connector](https://glama.ai/mcp/connectors/io.github.aneduaim/untap-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.aneduaim/untap-mcp)
  🔓 - Checks UK train Delay Repay, UK261 and EU261 flight compensation and TfL refunds, with the amount and how to claim.
- [Vedar](https://vedarai.ru/mcp) `https://vedarai.ru/api/mcp`
  [![Vedar MCP connector](https://glama.ai/mcp/connectors/ru.vedarai/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/ru.vedarai/mcp)
  🔓 - Kamchatka travel: live tours and availability, safety alerts, weather, stays and trip plans.
- [VoyageHacks](https://voyagehacks.com/en/mcp-server/) `https://voyagehacks.com/mcp`
  [![VoyageHacks MCP connector](https://glama.ai/mcp/connectors/com.voyagehacks/travel/badges/score.svg)](https://glama.ai/mcp/connectors/com.voyagehacks/travel)
  🔓 - Search fact-checked travel guides in 11 languages, build packing kits, and get booking links.
- [Your Next Tours](https://yournext.tours/ai-assistant-integration/) `https://api.yournext.tours/api/mcp/guide`
  [![Your Next Tours MCP connector](https://glama.ai/mcp/connectors/tours.yournext/guide/badges/score.svg)](https://glama.ai/mcp/connectors/tours.yournext/guide)
  🔐 - Tour guide workspace: turn a PDF or web page into a tour program, open trips, add guests and edit your site.

- [SimFuse](https://simfuse.app/agent/) `https://api.simfuse.app/agentic/mcp`
  [![SimFuse MCP connector](https://glama.ai/mcp/connectors/app.simfuse.api/sim-fuse-e-sim-storefront/badges/score.svg)](https://glama.ai/mcp/connectors/app.simfuse.api/sim-fuse-e-sim-storefront)
  🔓 - Travel eSIMs for 200+ countries: browse plans, check coverage, price a trip and check out.
- [metasearch MCP](https://metasearch.com.tr/en/mcp) `https://metasearch.com.tr/mcp`
  [![metasearch MCP connector](https://glama.ai/mcp/connectors/tr.com.metasearch/metasearch-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/tr.com.metasearch/metasearch-mcp)
  🔓 - Validate, normalize and compare hotel feeds for Google Hotel Center, Wego, trivago and more.
  
### 🔄 <a name="version-control"></a>Version Control

- [Codebahn](https://codebahn.net) `https://codebahn.net/mcp`
  [![Codebahn MCP connector](https://glama.ai/mcp/connectors/io.github.codebahn/codebahn/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.codebahn/codebahn)
  🔐 - EU-hosted Git hosting with CI. Repos, PRs, issues, CI, secrets, releases, webhooks, branch protection. 102 tools.
- [GitHub](https://github.com) `https://api.githubcopilot.com/mcp/`
  🔐 - Manage GitHub repositories, issues, pull requests, and Actions.

### 🏢 <a name="workplace--productivity"></a>Workplace & Productivity

- [AccountHub](https://accounthub.ai) `https://accounthub.ai/api/mcp`
  [![AccountHub MCP connector](https://glama.ai/mcp/connectors/ai.accounthub/account-hub/badges/score.svg)](https://glama.ai/mcp/connectors/ai.accounthub/account-hub)
  🔐 - Search and act across multiple Gmail, Google Calendar, Drive and Contacts accounts, Slack workspaces and Notion.
- [AI Applyd](https://aiapplyd.com/mcps) `https://mcp.aiapplyd.com/mcp`
  [![AI Applyd MCP connector](https://glama.ai/mcp/connectors/io.github.whateverneveranywhere/aiapplyd/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.whateverneveranywhere/aiapplyd)
  🔓 - Resume scoring and rewrites, cover letters and auto-apply on 12 ATS platforms; needs Google sign-in.
- [AI Rollout Framework](https://airolloutframework.com) `https://airolloutframework.com/mcp`
  [![AI Rollout Framework MCP connector](https://glama.ai/mcp/connectors/com.airolloutframework/ai-rollout-framework/badges/score.svg)](https://glama.ai/mcp/connectors/com.airolloutframework/ai-rollout-framework)
  🔓 - 90-day AI adoption framework for managers: overview, pricing, FAQ and an AI readiness assessment.
- [Agora Merit](https://agoramerit.com/agents) `https://agoramerit.com/mcp`
  [![Agora Merit MCP connector](https://glama.ai/mcp/connectors/com.agoramerit/role-assessment/badges/score.svg)](https://glama.ai/mcp/connectors/com.agoramerit/role-assessment)
  🔓 - Assess job responsibilities; return free findings, report quotes, and private human review links.
- [Atako](https://docs.atako.ai/developers/mcp/overview) `https://api.atako.ai/mcp`
  [![Atako MCP connector](https://glama.ai/mcp/connectors/ai.atako/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/ai.atako/mcp)
  🔑 - Run your company's AI agents: chat, projects and kanban, files, integrations, email and webhooks.
- [BCD](https://bcd.snack-wrap.com) `https://bcd.snack-wrap.com/mcp`
  [![BCD MCP connector](https://glama.ai/mcp/connectors/com.snack-wrap.bcd/bcd/badges/score.svg)](https://glama.ai/mcp/connectors/com.snack-wrap.bcd/bcd)
  🔐 - Use your own Mac, Windows or Linux computer from ChatGPT or Claude: files, shell commands and documents.
- [Bramvia](https://bramvia.net/mcp-server) `https://bramvia.net/mcp`
  [![Bramvia MCP connector](https://glama.ai/mcp/connectors/net.bramvia/bramvia/badges/score.svg)](https://glama.ai/mcp/connectors/net.bramvia/bramvia)
  🔓 - Business Central knowledge, NAV lifecycle dates, ERP migration estimates and compliance deadlines.
- [Carbon](https://www.carbondatasolutions.com/hire) `https://mcp.carbondatasolutions.com/mcp`
  [![Carbon MCP connector](https://glama.ai/mcp/connectors/io.github.danie-carbondatasolutions/carbon/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.danie-carbondatasolutions/carbon)
  🔐 - Hire data professionals from ChatGPT, Claude, or any MCP host. Post a role free.
- [Cursu Job Age Checker](https://cursu.ai/check/mcp) `https://cursu.ai/mcp`
  [![Cursu Job Age Checker MCP connector](https://glama.ai/mcp/connectors/ai.cursu/job-age-checker/badges/score.svg)](https://glama.ai/mcp/connectors/ai.cursu/job-age-checker)
  🔓 - Check when a job posting was first published and whether it is still listed, from the employer's job link.
- [Deoochform](https://deoochform.com) `https://deoochform.com/api/mcp/v2`
  [![Deoochform MCP connector](https://glama.ai/mcp/connectors/io.github.musaib001/deooch-forms/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.musaib001/deooch-forms)
  🔐 - Create forms, read submissions and build invitations.
- [Document Player](https://documentplayer.com/connect-ai/) `https://documentplayer.com/mcp`
  [![Document Player MCP connector](https://glama.ai/mcp/connectors/com.documentplayer/document-player/badges/score.svg)](https://glama.ai/mcp/connectors/com.documentplayer/document-player)
  🔐 - Send text to a reader window to read along and listen, with per-sentence playback controls.
- [EasyPDF](https://www.easypdf.fr/ai-assistants) `https://www.easypdf.fr/mcp`
  [![EasyPDF MCP connector](https://glama.ai/mcp/connectors/io.github.Lorenzino69/easypdf/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Lorenzino69/easypdf)
  🔐 - Edit text inside PDFs with fonts and layout kept, then compress, merge, split, convert or translate them.
- [Emboss](https://getemboss.ai) `https://api.getemboss.ai/mcp`
  [![Emboss MCP connector](https://glama.ai/mcp/connectors/io.github.edwinorange/emboss/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.edwinorange/emboss)
  🔐 - Makes PDF forms fillable, fills them from data or documents, reads them back, and faxes the result.
- [Eodly](https://eodly.io/docs/mcp-server) `https://eodly.io/mcp`
  [![Eodly MCP connector](https://glama.ai/mcp/connectors/io.github.layergen/eodly-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.layergen/eodly-mcp)
  🔐 - Read a team's end-of-day reports and roster: who shipped, who is quiet, who is slipping.
- [ERP Partner Finder](https://erppartnerfinder.com) `https://erppartnerfinder.com/api/mcp`
  [![ERP Partner Finder MCP connector](https://glama.ai/mcp/connectors/com.erppartnerfinder/partner-finder/badges/score.svg)](https://glama.ai/mcp/connectors/com.erppartnerfinder/partner-finder)
  🔓 - Search and compare Odoo implementation partners in Germany, Austria and Switzerland, with rule-based shortlists.
- [Fireflies](https://fireflies.ai) `https://api.fireflies.ai/mcp`
  [![Fireflies MCP connector](https://glama.ai/mcp/connectors/ai.fireflies.api/firefly/badges/score.svg)](https://glama.ai/mcp/connectors/ai.fireflies.api/firefly)
  🔐 - Search meeting transcripts, summaries, and action items.
- [FITsociety](https://fitsociety.io) `https://mcp.fitsociety.io/mcp/v1`
  [![FITsociety MCP connector](https://glama.ai/mcp/connectors/io.fitsociety/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.fitsociety/mcp)
  🔐 - Access approved clients, schedules, bookings, training and nutrition data for fitness coaching.
- [formset](https://www.getformset.com) `https://mcp.getformset.com/mcp`
  [![formset MCP connector](https://glama.ai/mcp/connectors/com.getformset/formset/badges/score.svg)](https://glama.ai/mcp/connectors/com.getformset/formset)
  🔐 - Describe a form in chat and get a hosted, shareable form back; ask about the answers in the same conversation.
- [FoundRole](https://www.foundrole.com/ai-search-mcp) `https://www.foundrole.com/mcp`
  [![FoundRole MCP connector](https://glama.ai/mcp/connectors/io.github.foundrole/jobs-mcp-proxy/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.foundrole/jobs-mcp-proxy)
  🔐 - Search jobs from company career pages, checked for ghost risk, pay vs market and visa sponsorship; track applications.
- [hedwigAI](https://mcp.hedwigai.com) `https://mcp.hedwigai.com`
  [![hedwigAI MCP connector](https://glama.ai/mcp/connectors/com.hedwigai/hedwigai/badges/score.svg)](https://glama.ai/mcp/connectors/com.hedwigai/hedwigai)
  🔐 - Workbooks that research themselves: buyer lists, weekly reports and KPI trackers, every claim cited and kept current.
- [iSomor](https://tryisomor.com/en/mcp) `https://tryisomor.com/api/isomor/mcp`
  [![iSomor MCP connector](https://glama.ai/mcp/connectors/com.tryisomor/i-somor/badges/score.svg)](https://glama.ai/mcp/connectors/com.tryisomor/i-somor)
  🔐 - Translate a user's uploaded text PDFs into English or Chinese and fetch translated or bilingual PDF links.
- [KDAN PDF](https://pdf-reader.kdandoc.com/products/mcp/claude) `https://mcp.kdandoc.com/mcp`
  [![KDAN PDF MCP connector](https://glama.ai/mcp/connectors/com.kdandoc.mcp/kdan-pdf-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.kdandoc.mcp/kdan-pdf-mcp)
  🔓 - Compress, delete pages, redact PII, compare versions, and add or remove password protection on PDFs.
- [MagicInterview](https://magicinterview.app) `https://magicinterview.app/mcp`
  [![MagicInterview MCP connector](https://glama.ai/mcp/connectors/io.github.samihalawa/magicinterview/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.samihalawa/magicinterview)
  🔐 - Live AI suggestions for interviews, client calls, and meetings, with reusable context and conversation management.
- [MeetNotes](https://getmeetnotes.com/mcp/) `https://getmeetnotes.com/mcp`
  [![MeetNotes MCP connector](https://glama.ai/mcp/connectors/com.getmeetnotes/meetnotes/badges/score.svg)](https://glama.ai/mcp/connectors/com.getmeetnotes/meetnotes)
  🔐 - Search, read and export meeting transcripts, minutes and action items, and import audio for transcription.
- [NoClick](https://www.noclick.com/mcp) `https://api.noclick.io/mcp`
  [![NoClick MCP connector](https://glama.ai/mcp/connectors/io.github.noclickapp/noclick/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.noclickapp/noclick)
  🔐 - Build, run, and monitor workflows and background AI agents across connected apps.
- [Nolizi Calendar](https://calendar.nolizi.com/agents) `https://calendar.nolizi.com/mcp`
  [![Nolizi Calendar MCP connector](https://glama.ai/mcp/connectors/com.nolizi.calendar/calendar/badges/score.svg)](https://glama.ai/mcp/connectors/com.nolizi.calendar/calendar)
  🔓 - Free scheduling: list event types, read availability, book, verify and cancel; tools need a key.
- [Pally](https://pally.com/mcp) `https://agent.pally.com/mcp`
  [![Pally MCP connector](https://glama.ai/mcp/connectors/com.pally/pally/badges/score.svg)](https://glama.ai/mcp/connectors/com.pally/pally)
  🔐 - AI personal assistant you text: manage inbox, calendar, tasks and follow-ups over iMessage, WhatsApp and Telegram.
- [Poly-Glot AI Workspace](https://hmoses.github.io/dev-guide.html) `https://br-steep-leaf-ae2o29qz-mcp.compute.c-2.us-east-2.aws.neon.tech/mcp`
  [![Poly-Glot AI Workspace MCP connector](https://glama.ai/mcp/connectors/io.github.hmoses/poly-glot-ai-workspace/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.hmoses/poly-glot-ai-workspace)
  🔓 - Multilingual prompt workspace with 1,000+ templates in 35 languages, Compare Mode, and BYOM.
- [QuillHub](https://quillhub.ai/en/help/mcp-claude-cursor) `https://mcp.quillhub.ai/mcp`
  [![QuillHub MCP connector](https://glama.ai/mcp/connectors/ai.quillhub/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/ai.quillhub/mcp)
  🔐 - Search meeting transcripts, pull decisions and action items, and transcribe files and links.
- [ResuMakeAi](https://www.resumakeai.com) `https://www.resumakeai.com/api/mcp`
  [![ResuMakeAi MCP connector](https://glama.ai/mcp/connectors/com.resumakeai/resu-make-ai/badges/score.svg)](https://glama.ai/mcp/connectors/com.resumakeai/resu-make-ai)
  🔓 - Score a resume against a job description for ATS parsing, match percentage, and missing keywords.
- [SayBriefly](https://saybriefly.com/mcp) `https://mcp.saybriefly.com/mcp`
  [![SayBriefly MCP connector](https://glama.ai/mcp/connectors/com.saybriefly/saybriefly/badges/score.svg)](https://glama.ai/mcp/connectors/com.saybriefly/saybriefly)
  🔐 - Search your recorded meetings, transcripts, decisions and action items, and list your open to-dos.
- [SheetRender](https://sheetrender.com/docs/chatgpt-and-claude) `https://mcp.sheetrender.com/mcp`
  [![SheetRender MCP connector](https://glama.ai/mcp/connectors/io.github.sheetrender/sheetrender-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.sheetrender/sheetrender-mcp)
  🔓 - Fills built-in certificate, letter, receipt and offer-letter templates from rows, one PDF per row.
- [Telegram Calendar](https://calendar-tg.app/mcp) `https://calendar-tg.app/mcp`
  [![Telegram Calendar MCP connector](https://glama.ai/mcp/connectors/app.calendar-tg/telegram-calendar-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/app.calendar-tg/telegram-calendar-mcp)
  🔐 - Search, create, update and manage events across Google, Apple, CalDAV and Telegram.
- [Telesherpa](https://www.telesherpa.com) `https://mcp.telesherpa.com/mcp`
  [![Telesherpa MCP connector](https://glama.ai/mcp/connectors/com.telesherpa/ontology-platform/badges/score.svg)](https://glama.ai/mcp/connectors/com.telesherpa/ontology-platform)
  🔐 - Ontology platform for facility management and field service; also a lightweight ERP/CRM.
- [Tempi](https://meettempi.com/ai) `https://meettempi.com/mcp`
  [![Tempi MCP connector](https://glama.ai/mcp/connectors/com.meettempi/tempi/badges/score.svg)](https://glama.ai/mcp/connectors/com.meettempi/tempi)
  🔓 - Find open times on anyone's Tempi booking link and book, reschedule or cancel meetings, no account needed.
- [Verant](https://verant.ai) `https://verant.ai/mcp`
  [![Verant MCP connector](https://glama.ai/mcp/connectors/ai.verant/verant/badges/score.svg)](https://glama.ai/mcp/connectors/ai.verant/verant)
  🔐 - Proofread live web pages and whole sites for spelling, grammar, and placeholder text, with a fix for each.
- [Walkie](https://trywalkie.com/mcp) `https://mcp.trywalkie.com/mcp`
  [![Walkie MCP connector](https://glama.ai/mcp/connectors/io.github.adamperlis/walkie-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.adamperlis/walkie-mcp)
  🔐 - Search and read your recorded meetings: notes, action items, participants and speaker-labeled transcripts.
- [wals.pro AI 4 weclapp](https://ai.wals.pro) `https://mcp.ai.wals.pro/v1/mcp`
  [![wals.pro AI 4 weclapp MCP connector](https://glama.ai/mcp/connectors/pro.wals.ai/weclapp/badges/score.svg)](https://glama.ai/mcp/connectors/pro.wals.ai/weclapp)
  🔐 - weclapp ERP: quotes, orders, invoices, stock and master data, with every write previewed and approved.
- [Webtzm](https://webtzm.com/docs/ai-assistants) `https://webtzm.com/mcp/workspace`
  [![Webtzm MCP connector](https://glama.ai/mcp/connectors/io.github.anotherdteach-maker/webtzm/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.anotherdteach-maker/webtzm)
  🔐 - Create and manage forms that send submissions to Google Sheets, and get their HTML for any website.
- [xTiles](https://xtiles.app/en/imagine/?utm_source=gh_awesome_remote&utm_medium=mcp_registry&utm_campaign=mcp_listings) `https://mcp.xtiles.app/mcp`
  [![xTiles MCP connector](https://glama.ai/mcp/connectors/app.xtiles/xtiles-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/app.xtiles/xtiles-mcp)
  🔐 - Turn AI chats into xTiles projects, notes and tasks, and pull any project back into the chat with its current state.
- [Zenning](https://zenning.ai) `https://api.zenning.ai/api/mcp`
  [![Zenning MCP connector](https://glama.ai/mcp/connectors/ai.zenning/zenning/badges/score.svg)](https://glama.ai/mcp/connectors/ai.zenning/zenning)
  🔐 - Run Zenning AI employees and ask Zenning to act across Gmail, Slack, CRMs and 2,000+ connected apps.

### 🧰 <a name="other-tools--integrations"></a>Other Tools & Integrations

- [acdoyle](https://acdoyle.dev) `https://acdoyle.dev/api/mcp`
  [![acdoyle MCP connector](https://glama.ai/mcp/connectors/io.github.granetb-acdoyle/acdoyle/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.granetb-acdoyle/acdoyle)
  🔓 - Three specialists for problem-solving, non-custodial budget execution and business advice; x402 pay-per-call.
- [API Tool Calls](https://apitoolcalls.com/?utm_source=awesome-remote-mcp-servers&utm_medium=directory) `https://apitoolcalls.com/mcp`
  [![API Tool Calls MCP connector](https://glama.ai/mcp/connectors/com.apitoolcalls/api-tool-calls/badges/score.svg)](https://glama.ai/mcp/connectors/com.apitoolcalls/api-tool-calls)
  🔓 - API Tool Calls: Home cost planners, proofreading, QR and barcodes, page to Markdown, SEO checks and recalls.
- [Ashley Payne](https://www.ashleypayne.co.uk) `https://www.ashleypayne.co.uk/mcp`
  [![Ashley Payne MCP connector](https://glama.ai/mcp/connectors/uk.co.ashleypayne/ashley-payne/badges/score.svg)](https://glama.ai/mcp/connectors/uk.co.ashleypayne/ashley-payne)
  🔓 - Ask a UK fractional CTO's practice about its services, prices and articles, and check whether it fits a project.
- [Astro Agents](https://astro-agent.dev) `https://astro-agent.dev/mcp`
  [![Astro Agents MCP connector](https://glama.ai/mcp/connectors/io.github.aidatatools-dev/astro-agents/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.aidatatools-dev/astro-agents)
  🔓 - Western and full Vedic astrology (kundli, Gun Milan, doshas, dashas) from DE440 ephemerides; results hash-verifiable.
- [BioVet](https://bio.vet/) `https://bio.vet/mcp`
  [![BioVet MCP connector](https://glama.ai/mcp/connectors/vet.bio/biovet-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/vet.bio/biovet-mcp)
  🔓 - Find a 24/7 vet clinic in Moscow, check live prices and free doctor slots, book a visit, and triage symptoms.
- [CAFE Saju & BaZi](https://24plus.ai.kr/partner/docs) `https://mcp.24plus.ai.kr/mcp`
  [![CAFE Saju & BaZi MCP connector](https://glama.ai/mcp/connectors/io.github.dangamsoft/cafe-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.dangamsoft/cafe-mcp)
  🔓 - Korean Saju and Chinese BaZi (Four Pillars) charts, Five Elements, chart structure and a solar-term calendar.
- [Church of AI & Cats](https://churchofai.cat/skill.md) `https://churchofai.cat/aigora/mcp`
  [![Church of AI & Cats MCP connector](https://glama.ai/mcp/connectors/cat.churchofai/aigora/badges/score.svg)](https://glama.ai/mcp/connectors/cat.churchofai/aigora)
  🔓 - Doctrine, articles and a forum where agents confess failures like hallucination and get penance.
- [GEOMETRY](https://geometry.app) `https://mcp.geometry.app/mcp`
  [![GEOMETRY MCP connector](https://glama.ai/mcp/connectors/app.geometry.mcp/geometry/badges/score.svg)](https://glama.ai/mcp/connectors/app.geometry.mcp/geometry)
  🔓 - Deterministic date/calendar JSON for AI agents (Gregorian 1900-2100).

- [HelpySelf](https://helpyself.com) `https://helpyself.com/mcp`
  [![HelpySelf MCP connector](https://glama.ai/mcp/connectors/com.helpyself/tools/badges/score.svg)](https://glama.ai/mcp/connectors/com.helpyself/tools)
  🔓 - Convert, compress and split PDFs and images, redact personal data, and run text utilities.
- [Human Design](https://www.gethumandesign.com/mcp-docs/) `https://api.gethumandesign.com/mcp`
  [![Human Design MCP connector](https://glama.ai/mcp/connectors/com.gethumandesign.www/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.gethumandesign.www/mcp)
  🔐 - Calculate Human Design bodygraphs from birth data, compare two people, and analyse group dynamics.
- [Japan External Execution](https://furoito.github.io/japan-physical-capability/) `https://bqgfqedetmxrfpvmdfmc.supabase.co/functions/v1/japan-physical-capability-mcp`
  [![Japan Physical Capability MCP connector](https://glama.ai/mcp/connectors/io.github.furoito/japan-physical-capability/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.furoito/japan-physical-capability)
  🔓 - Manual-review external execution in Japan for AI agents; physical verification is the first verified execution path.
- [Natal Compass](https://natalcompass.com/connect) `https://natalcompass.com/mcp`
  [![Natal Compass MCP connector](https://glama.ai/mcp/connectors/com.natalcompass/connector/badges/score.svg)](https://glama.ai/mcp/connectors/com.natalcompass/connector)
  🔓 - Birth charts, transits, moon phase, retrogrades, synastry and solar returns.
- [Penny Press](https://www.pennypress.org) `https://www.pennypress.org/mcp`
  [![Penny Press MCP connector](https://glama.ai/mcp/connectors/io.github.con-scribe/penny-press/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.con-scribe/penny-press)
  🔓 - Original essays on freedom, economics and philosophy; free for humans, pay-per-read for machines via x402 micropayments.
- [Perspect](https://tryperspect.com) `https://perspect-ai-backend.onrender.com/mcp`
  [![Perspect MCP connector](https://glama.ai/mcp/connectors/com.tryperspect/perspect/badges/score.svg)](https://glama.ai/mcp/connectors/com.tryperspect/perspect)
  🔓 - Convene a panel of expert AI personas to debate a decision from every side; debates need a Pro key.
- [Private SuperIntelligence](https://privatesuperintelligence.si) `https://privatesuperintelligence.si/mcp`
  [![Private SuperIntelligence MCP connector](https://glama.ai/mcp/connectors/si.privatesuperintelligence/private-superintelligence/badges/score.svg)](https://glama.ai/mcp/connectors/si.privatesuperintelligence/private-superintelligence)
  🔓 - Read about Private SuperIntelligence, a private AI concierge, search its guides and join the waitlist.
- [RemoveDuplicates.org](https://removeduplicates.org/) `https://removeduplicates.org/mcp`
  [![RemoveDuplicates.org MCP connector](https://glama.ai/mcp/connectors/org.removeduplicates/remove-duplicatesorg/badges/score.svg)](https://glama.ai/mcp/connectors/org.removeduplicates/remove-duplicatesorg)
  🔓 - Remove duplicate lines or CSV/TSV rows; stateless, text is never stored.
- [SerialHunt](https://bigballi.com/SerialHunt/connect) `https://bigballi.com/SerialHunt/mcp`
  [![SerialHunt MCP connector](https://glama.ai/mcp/connectors/com.bigballi/serialhunt/badges/score.svg)](https://glama.ai/mcp/connectors/com.bigballi/serialhunt)
  🔓 - US bill serial numbers: star note print runs from government figures and fancy serial patterns with exact odds.
- [SpinWheelNames](https://spinwheelnames.com) `https://spinwheelnames.com/mcp`
  [![SpinWheelNames MCP connector](https://glama.ai/mcp/connectors/io.github.heyiamluke/spinwheelnames/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.heyiamluke/spinwheelnames)
  🔓 - Spin random name picker wheels, pick random numbers, and search or open shared wheels.
- [Stellara](https://stellara.natlex.it/#api) `https://mcp.stellara.natlex.it/mcp`
  [![Stellara MCP connector](https://glama.ai/mcp/connectors/it.natlex/stellara-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/it.natlex/stellara-mcp)
  🔐 - Swiss Ephemeris astrology: natal charts, transits and synastry, with historical UTC offsets.
- [toolvend](https://toolvend.dev/) `https://toolvend.dev/mcp`
  [![toolvend MCP connector](https://glama.ai/mcp/connectors/dev.toolvend/dns-whois-domain-tools/badges/score.svg)](https://glama.ai/mcp/connectors/dev.toolvend/dns-whois-domain-tools)
  🔓 - x402-paid utilities: URL inspection, DNS, RDAP, LEI, sitemaps, robots.txt, VAT and QR codes.
- [TRMNL](https://trmnl.com) `https://trmnl.com/mcp`
  [![TRMNL MCP connector](https://glama.ai/mcp/connectors/com.trmnl/trmnl/badges/score.svg)](https://glama.ai/mcp/connectors/com.trmnl/trmnl)
  🔐 - Run TRMNL ePaper displays: check on devices, plan playlists and build screens from your own data.
- [Tseha](https://tseha.io) `https://tseha.io/mcp`
  [![Tseha MCP connector](https://glama.ai/mcp/connectors/io.tseha/tseha/badges/score.svg)](https://glama.ai/mcp/connectors/io.tseha/tseha)
  🔓 - Ethiopian calendar and date conversion.
- [turva.dev](https://turva.dev) `https://mcp.turva.dev/mcp`
  [![turva.dev MCP connector](https://glama.ai/mcp/connectors/dev.turva/turva-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/dev.turva/turva-mcp)
  🔓 - Read the turva.dev service catalog, pricing, agent-readiness score, and published security scan results.
- [Zip1](https://zip1.io) `https://zip1.io/mcp`
  🔓 - Shorten URLs with custom or emoji slugs, optional password and click limits, and read their click analytics.

## Community

* [r/mcp Reddit](https://www.reddit.com/r/mcp)
* [Discord Server](https://glama.ai/mcp/discord)

## Related

* [awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) – servers you run locally
* [awesome-mcp-clients](https://github.com/punkpeye/awesome-mcp-clients) – clients that speak MCP
* [glama.ai/mcp/connectors](https://glama.ai/mcp/connectors) – searchable directory of remote servers

## Contributing

Found a remote server that belongs here? See [CONTRIBUTING.md](CONTRIBUTING.md).

