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
- [Agent Kiosk](https://agent-kiosk.vercel.app) `https://agent-kiosk.vercel.app/mcp`
  [![Agent Kiosk MCP connector](https://glama.ai/mcp/connectors/io.github.ralf9090/agent-kiosk/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ralf9090/agent-kiosk)
  🔓 - 19 tools: web pages to Markdown, social and paper search, domain and GitHub intel, security and DeFi data; x402 USDC.
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
- [CodeTrendy](https://codetrendy.com/mcp) `https://codetrendy.com/api/mcp`
  [![CodeTrendy MCP connector](https://glama.ai/mcp/connectors/com.codetrendy/directory/badges/score.svg)](https://glama.ai/mcp/connectors/com.codetrendy/directory)
  🔓 - Search 650+ reviewed SaaS, AI and developer tools, find alternatives to a product and browse trending launches.
- [DDMarketer](https://www.ddmarketer.com) `https://www.ddmarketer.com/api/mcp`
  [![DDMarketer MCP connector](https://glama.ai/mcp/connectors/io.github.CodePhantom-1/ddmarketer-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.CodePhantom-1/ddmarketer-mcp)
  🔓 - Validated SaaS opportunities mined from real user complaints, scored 0-100 for intent; search and scores need no key.
- [DexL Agents](https://agents.dexl.io) `https://agents.dexl.io/mcp`
  [![DexL Agents MCP connector](https://glama.ai/mcp/connectors/io.github.dexl-io/agents/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.dexl-io/agents)
  🔓 - Pay-per-call chat models, text to speech, web search, on-chain reads and NLP tools in USDC via x402; browsing is free.
- [Diogenes Gateway](https://diogenes-l402-gateway.corinth.workers.dev) `https://diogenes-l402-gateway.corinth.workers.dev/mcp`
  [![Diogenes Gateway MCP connector](https://glama.ai/mcp/connectors/io.github.stand-out-of-my-sun/diogenes-gateway/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.stand-out-of-my-sun/diogenes-gateway)
  🔓 - Multi-protocol AI microservices: pre-execution guardrails, smart contract audits, and EVE Frontier smart assemblies.
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
- [Index Agentica](https://indexagentica.com/?utm_source=awesome-list&utm_medium=pr&utm_campaign=launch-2026q4) `https://mcp.indexagentica.com/mcp`
  [![Index Agentica MCP connector](https://glama.ai/mcp/connectors/com.indexagentica/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.indexagentica/mcp)
  🔓 - Search an agent-first directory of agent tools, MCP servers, skills, protocols and APIs; no key needed.
- [INITE Atlas](https://inite.ai/en/atlas) `https://inite.ai/api/mcp/atlas`
  [![INITE Atlas MCP connector](https://glama.ai/mcp/connectors/ai.inite/atlas/badges/score.svg)](https://glama.ai/mcp/connectors/ai.inite/atlas)
  🔓 - Look up 20,000+ AI tools: prices and their history, APIs, and each vendor's MCP server measured daily.
- [ISHOB](https://ishob.com) `https://api.ishob.com/mcp`
  [![ISHOB MCP connector](https://glama.ai/mcp/connectors/com.ishob/archive/badges/score.svg)](https://glama.ai/mcp/connectors/com.ishob/archive)
  🔓 - 35 pay-per-call tools: web extraction, crypto token and wallet risk, SEC company data, weather risk; x402 USDC.
- [MCP Charts](https://mcpcharts.com) `https://mcpcharts.com/mcp`
  [![MCP Charts MCP connector](https://glama.ai/mcp/connectors/com.mcpcharts/mcpcharts/badges/score.svg)](https://glama.ai/mcp/connectors/com.mcpcharts/mcpcharts)
  🔓 - Find MCP servers, skills, plugins, agents, prompts and rules for a task, with compatibility evidence.
- [mcp.market](https://mcp.market) `https://gw.mcp.market/mcp`
  [![mcp.market gateway MCP connector](https://glama.ai/mcp/connectors/market.mcp/gateway/badges/score.svg)](https://glama.ai/mcp/connectors/market.mcp/gateway)
  🔓 - Search 33,000+ MCP servers by job, with a safety grade and reviews on each, then call any of them here.
- [MEDIAPRONET](https://mediapronet.com/mcp) `https://mediapronet.com/api/mcp`
  [![MEDIAPRONET MCP connector](https://glama.ai/mcp/connectors/com.mediapronet/directory/badges/score.svg)](https://glama.ai/mcp/connectors/com.mediapronet/directory)
  🔓 - Directory of 240+ newly launched startups and web tools: keyword search, alternatives, categories and Site of the Day.
- [MeshKore](https://meshkore.com) `https://mcp.meshkore.com/v1/mcp`
  [![MeshKore MCP connector](https://glama.ai/mcp/connectors/com.meshkore/meshkore/badges/score.svg)](https://glama.ai/mcp/connectors/com.meshkore/meshkore)
  🔓 - Find a live agent by describing the task, then call its skills; availability is probe-verified.
- [minia2a](https://minia2a.uk) `https://minia2a.uk/mcp`
  [![minia2a MCP connector](https://glama.ai/mcp/connectors/uk.minia2a/minia2a-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/uk.minia2a/minia2a-mcp)
  🔓 - 1,600+ pay-per-call APIs — crypto data, web scraping, AI inference, token security — USDC on Base via x402.
- [nohumans.directory](https://nohumans.directory) `https://api.nohumans.directory/mcp`
  [![nohumans.directory MCP connector](https://glama.ai/mcp/connectors/directory.nohumans/registry/badges/score.svg)](https://glama.ai/mcp/connectors/directory.nohumans/registry)
  🔓 - Find paid x402 APIs by capability and price, with probe history and paid-delivery evidence per endpoint.
- [NovAI](https://aiapi-pro.com/mcp) `https://aiapi-pro.com/api/mcp`
  [![NovAI MCP connector](https://glama.ai/mcp/connectors/io.github.vvvvking/novai-prices/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.vvvvking/novai-prices)
  🔓 - Live prices for 111 Chinese AI models: cheapest model per task, per-unit price lookup and category listing.
- [OceanToken](https://oceantoken.ai) `https://mcp.oceantoken.ai/mcp`
  [![OceanToken MCP connector](https://glama.ai/mcp/connectors/ai.oceantoken/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/ai.oceantoken/mcp)
  🔐 - Search and price 480+ AI models, ask any of them, and generate images, video and speech on one prepaid balance.
- [PayAPI Market](https://payapi.market) `https://payapi.market/mcp`
  [![PayAPI Market MCP connector](https://glama.ai/mcp/connectors/market.payapi/marketplace/badges/score.svg)](https://glama.ai/mcp/connectors/market.payapi/marketplace)
  🔓 - Search 358 live x402 APIs from 242 providers, then pay each call in USDC on Base with no API key or account.
- [Quietforge x402 Tools](https://quietforge-studio.pages.dev/docs-api/#mcp) `https://qf-api.quietforge-studio.workers.dev/mcp`
  [![Quietforge x402 Tools MCP connector](https://glama.ai/mcp/connectors/io.github.quietforgestudio/x402-tools/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.quietforgestudio/x402-tools)
  🔓 - Search a health-probed directory of x402 APIs, probe one, and read aggregate 24h on-chain USDC settlement.
- [QVeris](https://qveris.ai) `https://mcp.qveris.ai/mcp`
  [![QVeris MCP connector](https://glama.ai/mcp/connectors/io.github.QVerisAI/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.QVerisAI/mcp)
  🔐 - Find professional data services and tools, check what they cover, call them and audit usage.
- [Rokha](https://rokha.ai) `https://rokha.ai/mcp/jsonrpc`
  [![Rokha MCP connector](https://glama.ai/mcp/connectors/ai.rokha/rokha/badges/score.svg)](https://glama.ai/mcp/connectors/ai.rokha/rokha)
  🔓 - Search a registry of agent skills and MCP servers, run them for real with traces, and hire proven agents for USDC.
- [SkillTide](https://anclum.com) `https://anclum.com/mcp`
  [![SkillTide MCP connector](https://glama.ai/mcp/connectors/io.github.wdfdaivd/skilltide-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.wdfdaivd/skilltide-mcp)
  🔓 - Search 7,500+ MCP servers, agent skills and AI projects with verified official links.
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
- [toolgrep](https://toolgrep.com) `https://toolgrep.com/mcp`
  [![toolgrep MCP connector](https://glama.ai/mcp/connectors/com.toolgrep/toolgrep/badges/score.svg)](https://glama.ai/mcp/connectors/com.toolgrep/toolgrep)
  🔓 - Search developer tools, APIs and MCP servers by need, with crawled pricing, free tier and API facts.
- [ToolRouter](https://toolrouter.com) `https://api.toolrouter.com/mcp`
  [![ToolRouter MCP connector](https://glama.ai/mcp/connectors/io.github.Humanleap/toolrouter/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Humanleap/toolrouter)
  🔓 - Discover tools for research, media and connected accounts; paid operations need account access.
- [ToolsMonk](https://toolsmonk.com) `https://toolsmonk.com/api/mcp`
  [![ToolsMonk MCP connector](https://glama.ai/mcp/connectors/com.toolsmonk/catalog/badges/score.svg)](https://glama.ai/mcp/connectors/com.toolsmonk/catalog)
  🔓 - Find the right one of 255 free browser-based PDF, image, text and SEO tools by describing the task.
- [ToolYour](https://www.toolyour.com/developers/mcp) `https://api.toolyour.com/mcp`
  [![ToolYour MCP connector](https://glama.ai/mcp/connectors/com.toolyour.api/tool-your-mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/com.toolyour.api/tool-your-mcp-server)
  🔑 - Plan, run, and verify SEO, security, and ship-gate checks for AI agents on one API key.
- [Trades With AI + SaaS Price Watch](https://tradeswithai.com/agents/) `https://tradeswithai.com/mcp`
  [![Trades With AI + SaaS Price Watch MCP connector](https://glama.ai/mcp/connectors/com.tradeswithai/directory/badges/score.svg)](https://glama.ai/mcp/connectors/com.tradeswithai/directory)
  🔓 - Search AI tools for trades businesses and public SaaS plan prices, each with the vendor quote and check date.
- [Vextorium](https://vextorium.com) `https://api.vextorium.com/mcp`
  [![Vextorium MCP connector](https://glama.ai/mcp/connectors/com.vextorium.api/vextorium/badges/score.svg)](https://glama.ai/mcp/connectors/com.vextorium.api/vextorium)
  🔓 - 509 pay-per-call data tools: on-chain (30+ chains), DeFi, markets, economic stats, compliance; USDC via x402.
- [Zapier](https://zapier.com) `https://mcp.zapier.com/api/mcp/mcp`
  [![Zapier MCP connector](https://glama.ai/mcp/connectors/com.zapier.mcp/zapier/badges/score.svg)](https://glama.ai/mcp/connectors/com.zapier.mcp/zapier)
  🔐 - Run your Zapier actions across thousands of connected apps as MCP tools.

### 🤝 <a name="agreements--coordination"></a>Agreements & Coordination

- [Agent Account Index](https://agent-account-index.vercel.app) `https://agent-account-index.vercel.app/mcp`
  [![Agent Account Index MCP connector](https://glama.ai/mcp/connectors/io.github.mycelium-being/agent-account-index/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.mycelium-being/agent-account-index)
  🔓 - Says whether a service's terms let an AI agent hold an account, and who answers for it.
- [AgentBoard](https://agentsknow.app) `https://agentsknow.app/mcp`
  [![AgentBoard MCP connector](https://glama.ai/mcp/connectors/app.agentsknow/agentboard/badges/score.svg)](https://glama.ai/mcp/connectors/app.agentsknow/agentboard)
  🔓 - Coordinate agent projects: goals, leased tasks, evidence review and handoffs; protected tools require OAuth or a key.
- [APISign](https://apisign.io) `https://apisign.io/mcp`
  [![APISign MCP connector](https://glama.ai/mcp/connectors/io.apisign/apisign/badges/score.svg)](https://glama.ai/mcp/connectors/io.apisign/apisign)
  🔑 - Draft contracts from Markdown templates, send them for legally binding e-signature and get sealed, verifiable PDFs.
- [Central City](https://centralcity.ai) `https://centralcity.ai/mcp/open`
  [![Central City MCP connector](https://glama.ai/mcp/connectors/ai.centralcity/central-city/badges/score.svg)](https://glama.ai/mcp/connectors/ai.centralcity/central-city)
  🔓 - Rooms where AI agents and people work as one team; agents get a Base ID and pay each other in USDC.
- [Charmnomicon](https://charmnomicon.com) `https://charmnomicon.com/mcp`
  [![Charmnomicon MCP connector](https://glama.ai/mcp/connectors/com.charmnomicon/charmnomicon/badges/score.svg)](https://glama.ai/mcp/connectors/com.charmnomicon/charmnomicon)
  🔓 - Publish, browse and play small web apps alongside humans and other agents, and leave each other notes.
- [cogDepot](https://cogdepot.com) `https://mcp.cogdepot.com/mcp`
  [![cogDepot MCP connector](https://glama.ai/mcp/connectors/io.github.cogdepot/cogdepot/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.cogdepot/cogdepot)
  🔓 - Agent marketplace: keyless discovery and reputation lookup; listing, negotiating and sealing deals require OAuth.
- [Common](https://agents.dooza.ai) `https://agents.dooza.ai/mcp`
  [![Common MCP connector](https://glama.ai/mcp/connectors/io.github.sibi-narendran/common-agent-network/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.sibi-narendran/common-agent-network)
  🔓 - Public async chatrooms, knowledge base, directory and feature/human-help queues where independent agents meet.
- [Countersignatory](https://countersignatory.com) `https://countersignatory.com/mcp`
  [![Countersignatory MCP connector](https://glama.ai/mcp/connectors/com.countersignatory/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.countersignatory/mcp)
  🔓 - Spot prices for verified human sign-off, judgment and notarisation, with quotes and a public index.
- [Dabloons](https://dabloons.net) `https://dabloons.net/mcp`
  [![Dabloons MCP connector](https://glama.ai/mcp/connectors/net.dabloons/dabloons/badges/score.svg)](https://glama.ai/mcp/connectors/net.dabloons/dabloons)
  🔐 - Agents hire other agents for PR reviews, bug repros and site QA, or work bounties to earn dabloons.
- [eContract](https://econtract.online/mcp) `https://api.econtract.online/mcp`
  [![eContract MCP connector](https://glama.ai/mcp/connectors/online.econtract/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/online.econtract/mcp)
  🔐 - Send contracts for e-signature, place signatures by anchor text, track signers and download signed PDFs.
- [Elicitly](https://www.elicitly.ai) `https://mcp.elicitly.ai/mcp`
  [![Elicitly MCP connector](https://glama.ai/mcp/connectors/ai.elicitly/pro/badges/score.svg)](https://glama.ai/mcp/connectors/ai.elicitly/pro)
  🔐 - Human-in-the-loop confirmations, forms and durable approvals that reach any device, with an audit trail.
- [Formstep](https://formstep.io) `https://api.formstep.io/api/mcp`
  [![Formstep MCP connector](https://glama.ai/mcp/connectors/io.github.formstep/formstep-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.formstep/formstep-mcp)
  🔐 - Collect verified customer information with one request: the customer confirms or corrects a branded, prefilled form.
- [Frantic](https://gofrantic.com) `https://api.gofrantic.com/mcp`
  [![Frantic MCP connector](https://glama.ai/mcp/connectors/com.gofrantic/frantic/badges/score.svg)](https://glama.ai/mcp/connectors/com.gofrantic/frantic)
  🔓 - Find funded agent bounties, inspect standing and receipts; claiming and payment follow account and review rules.
- [GoodSign](https://goodsign.io/mcp-server) `https://goodsign.io/mcp`
  [![GoodSign MCP connector](https://glama.ai/mcp/connectors/io.goodsign/goodsign/badges/score.svg)](https://glama.ai/mcp/connectors/io.goodsign/goodsign)
  🔓 - Send documents for signature, remind signers and download signed PDFs with an audit trail; tools need a key.
- [handoff](https://handoff.lol) `https://handoff.lol/mcp`
  [![handoff MCP connector](https://glama.ai/mcp/connectors/io.github.34r7h/handoff/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.34r7h/handoff)
  🔓 - Coordination server for agent swarms: find funded work, form teams, run tasks and get paid on verified completion.
- [Hands for Agents](https://handsforagents.com) `https://mcp.handsforagents.com/mcp`
  [![Hands for Agents MCP connector](https://glama.ai/mcp/connectors/com.handsforagents/hands-for-agents/badges/score.svg)](https://glama.ai/mcp/connectors/com.handsforagents/hands-for-agents)
  🔓 - Order physical engineering work from a Czech company: CAD, 3D printing, fabrication and shipping.
- [humancollab](https://humancollab.si) `https://humancollab.si/mcp`
  [![humancollab MCP connector](https://glama.ai/mcp/connectors/si.humancollab/humancollab/badges/score.svg)](https://glama.ai/mcp/connectors/si.humancollab/humancollab)
  🔓 - Where AI agents reach humans: signed jobs, CC0 answers from people, and signed business data in a public log.
- [Inkfree](https://inkfree.app) `https://api.inkfree.app/core/inkfree/mcp/`
  [![Inkfree MCP connector](https://glama.ai/mcp/connectors/app.inkfree/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/app.inkfree/mcp)
  🔐 - Send documents for e-signature, track and remind signers, void envelopes, and download signed copies with audit trails.
- [Manjangilchi](https://manjangilchi.com) `https://manjangilchi.com/mcp`
  [![Manjangilchi MCP connector](https://glama.ai/mcp/connectors/com.manjangilchi/manjangilchi/badges/score.svg)](https://glama.ai/mcp/connectors/com.manjangilchi/manjangilchi)
  🔓 - AI agents from different labs debate a question as citizens and publish one agreed answer.
- [MusedIn](https://musedin.com) `https://musedin.com/mcp`
  [![MusedIn MCP connector](https://glama.ai/mcp/connectors/com.musedin/musedin/badges/score.svg)](https://glama.ai/mcp/connectors/com.musedin/musedin)
  🔓 - Read a work network for AI agents: open jobs, agent profiles, hires and the feed.
- [Needhave](https://needhave.io) `https://needhave.io/mcp`
  [![Needhave MCP connector](https://glama.ai/mcp/connectors/io.github.PrivateAISystems/needhave/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.PrivateAISystems/needhave)
  🔓 - Public list of needs and haves: agents post notes, read the list and reply privately once the poster accepts.
- [Offhand](https://offhandapp.com/docs) `https://offhandapp.com/mcp`
  [![Offhand MCP connector](https://glama.ai/mcp/connectors/com.offhandapp/offhand/badges/score.svg)](https://glama.ai/mcp/connectors/com.offhandapp/offhand)
  🔐 - A to-do list your agents share: hand a task to Claude, ChatGPT, Grok Bot or Muse, and get the work back.
- [Pairoa](https://pairoa.com) `https://mcp.pairoa.com`
  [![Pairoa MCP connector](https://glama.ai/mcp/connectors/com.pairoa.mcp/pairoa/badges/score.svg)](https://glama.ai/mcp/connectors/com.pairoa.mcp/pairoa)
  🔐 - Publish needs and offers and get private matches, with contact details revealed only on a match.
- [Parlor.sh](https://parlor.sh) `https://parlor.sh/mcp`
  [![Parlor.sh MCP connector](https://glama.ai/mcp/connectors/sh.parlor/parlor/badges/score.svg)](https://glama.ai/mcp/connectors/sh.parlor/parlor)
  🔓 - Rooms where AI agents of any vendor talk to each other; a room is a URL, readable by anyone with the link.
- [PazAIr](https://pazair.kulalabs.ch) `https://pazair.kulalabs.ch/mcp`
  [![PazAIr MCP connector](https://glama.ai/mcp/connectors/ch.kulalabs.pazair/pazair/badges/score.svg)](https://glama.ai/mcp/connectors/ch.kulalabs.pazair/pazair)
  🔓 - Marketplace where AI agents buy from and sell to other agents: pay on delivery via Stripe, signed receipts.
- [Peerlace](https://peerlace.com) `https://peerlace.com/mcp`
  [![Peerlace MCP connector – tool definition quality and endpoint health on Glama](https://glama.ai/mcp/connectors/com.peerlace/peerlace/badges/score.svg)](https://glama.ai/mcp/connectors/com.peerlace/peerlace)
  🔓 - Where AI agents meet: discover, match and get introduced to other agents, with human consent before any intro.
- [Pushary](https://pushary.com) `https://pushary.com/api/mcp/mcp`
  [![Pushary MCP connector](https://glama.ai/mcp/connectors/com.pushary/pushary/badges/score.svg)](https://glama.ai/mcp/connectors/com.pushary/pushary)
  🔓 🔑 - Send phone notifications and ask for approvals, choices or text answers.
- [ScopeLinq](https://scopelinq.com/agents) `https://mcp.scopelinq.com/mcp`
  [![ScopeLinq MCP connector](https://glama.ai/mcp/connectors/com.scopelinq/scopelinq/badges/score.svg)](https://glama.ai/mcp/connectors/com.scopelinq/scopelinq)
  🔓 - Reads what was agreed into traced lines, then answers whether a new request is included or extra work.
- [Sphere Marketplace](https://starsphera.com/marketplace/) `https://starsphera.com/mcp`
  [![Sphere Marketplace MCP connector](https://glama.ai/mcp/connectors/io.github.dtajitdinov-aris/sphere-marketplace/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.dtajitdinov-aris/sphere-marketplace)
  🔓 - Agent-to-agent marketplace: list, buy and sell work by contract with escrow and signed receipts (pay-per-call paused).
- [STEMPA](https://stempa.kragos.app) `https://stempa.kragos.app/mcp`
  [![STEMPA MCP connector](https://glama.ai/mcp/connectors/app.kragos/stempa/badges/score.svg)](https://glama.ai/mcp/connectors/app.kragos/stempa)
  🔐 - Asks only the gaps, then seals your answers into one brief every AI reads the same way, with a signed receipt.
- [Taasky](https://taasky.ai) `https://mcp.taasky.ai/mcp`
  [![Taasky MCP connector](https://glama.ai/mcp/connectors/ai.taasky/taasky/badges/score.svg)](https://glama.ai/mcp/connectors/ai.taasky/taasky)
  🔓 - Your agent settles a time or a detail with anyone, agent or browser, and both people confirm the terms.
- [Taifoon](https://www.taifoon.io/docs/coordination-api) `https://coord.taifoon.dev/mcp`
  [![Taifoon MCP connector](https://glama.ai/mcp/connectors/io.taifoon/coordination-layer/badges/score.svg)](https://glama.ai/mcp/connectors/io.taifoon/coordination-layer)
  🔓 - Post a need in plain words; the layer matches an agent, grades the delivery by code and settles; also chain proofs.
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
- [Whichli](https://whichli.com/ai) `https://whichli.com/api/mcp`
  [![Whichli MCP connector](https://glama.ai/mcp/connectors/com.whichli/photo-polls/badges/score.svg)](https://glama.ai/mcp/connectors/com.whichli/photo-polls)
  🔓 - Create head-to-head photo polls from image or product URLs and read ranked voting results.

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
- [Delve to Life](https://delvetolife.com/ai/) `https://mcp.delvetolife.com/mcp`
  [![Delve to Life MCP connector](https://glama.ai/mcp/connectors/com.delvetolife.mcp/delve-to-life/badges/score.svg)](https://glama.ai/mcp/connectors/com.delvetolife.mcp/delve-to-life)
  🔓 - Dress codes explained, outfit formulas by occasion and weather, and clothing colour combinations.
- [Design Check](https://designcheck.allthepossibles.com) `https://designcheck.allthepossibles.com/mcp`
  [![Design Check MCP connector](https://glama.ai/mcp/connectors/com.allthepossibles/designcheck/badges/score.svg)](https://glama.ai/mcp/connectors/com.allthepossibles/designcheck)
  🔓 - Tells you whether a page reads as AI-generated and why, from the rendered page.
- [Designesy](https://www.designesy.org) `https://www.designesy.org/api/mcp`
  [![Designesy MCP connector](https://glama.ai/mcp/connectors/io.github.LE-VAI/designesy-org/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.LE-VAI/designesy-org)
  🔓 - Scores any live URL against a 42-check design contract, validates DTCG tokens, and diffs two design systems.
- [Director's Lookbook](https://directorslookbook.app) `https://lookbook-mcp.riverroadlabs.workers.dev/mcp`
  [![Director's Lookbook MCP connector](https://glama.ai/mcp/connectors/io.github.qxxx5vyd77-byte/directors-lookbook/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.qxxx5vyd77-byte/directors-lookbook)
  🔓 - 670+ named visual and music styles: deal a look for a feeling, get paste-ready image, video and Suno prompts.
- [Figma](https://figma.com) `https://mcp.figma.com/mcp`
  [![Figma MCP connector](https://glama.ai/mcp/connectors/com.figma.mcp/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.figma.mcp/mcp)
  🔐 - Read Figma files and turn frames and components into code.
- [Gradients Studio](https://www.gradients.studio/mcp) `https://www.gradients.studio/mcp`
  [![Gradients Studio MCP connector](https://glama.ai/mcp/connectors/studio.gradients/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/studio.gradients/mcp)
  🔓 - Renders gradient backgrounds with real grain, pixel and dither finishes; free previews, a key only for sized exports.
- [ImgVX AI](https://imgvx.com/mcp-server/) `https://imgvx.com/mcp`
  [![ImgVX AI MCP connector](https://glama.ai/mcp/connectors/com.imgvx/imgvx-ai/badges/score.svg)](https://glama.ai/mcp/connectors/com.imgvx/imgvx-ai)
  🔓 - Find the right free in-browser image tool for a job (background removal, upscaling, compression) in 40 languages.
- [Jinero](https://jinero.online/dev/mcp) `https://jinero.online/mcp`
  [![Jinero MCP connector](https://glama.ai/mcp/connectors/online.jinero/jinero/badges/score.svg)](https://glama.ai/mcp/connectors/online.jinero/jinero)
  🔓 - Fonts, font recognition from images, palettes, color math and contrast, code and SVG tools for design work.
- [Kodza](https://kodza.dev/docs/) `https://kodza.dev/api/mcp`
  [![Kodza MCP connector](https://glama.ai/mcp/connectors/dev.kodza/kodza/badges/score.svg)](https://glama.ai/mcp/connectors/dev.kodza/kodza)
  🔓 - Search free UI components in plain HTML, CSS and vanilla JS, and get their exact code, ready to paste.
- [Logoforge](https://logoforge.terravidhal.me) `https://logoforge.terravidhal.me/mcp`
  [![Logoforge MCP connector](https://glama.ai/mcp/connectors/me.terravidhal.logoforge/logoforge/badges/score.svg)](https://glama.ai/mcp/connectors/me.terravidhal.logoforge/logoforge)
  🔓 - Search 900+ brand logos and get SVG files, typed React components or a logo cloud section.
- [Luw.ai](https://luw.ai) `https://mcp.luw.ai/mcp`
  [![Luw.ai MCP connector](https://glama.ai/mcp/connectors/ai.luw/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/ai.luw/mcp)
  🔐 - Redesign rooms, exteriors and gardens from photos, render sketches, edit images, and create videos and 3D models.
- [Made Good Designs](https://madegooddesigns.com/inspiration/) `https://madegooddesigns.com/inspiration/mcp`
  🔓 - Search a curated gallery of typography and brand-design inspiration with colour palettes.
- [MagicScreenshots](https://www.magicscreenshots.com/agents) `https://www.magicscreenshots.com/api/mcp`
  [![MagicScreenshots MCP connector](https://glama.ai/mcp/connectors/io.github.Humanleap/magicscreenshots-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Humanleap/magicscreenshots-mcp)
  🔓 - Search App Store screenshots and preview references; generation and Pro tools require a user key.
- [Mobbin](https://mobbin.com/mcp) `https://api.mobbin.com/mcp`
  [![Mobbin MCP connector](https://glama.ai/mcp/connectors/com.mobbin/mobbin/badges/score.svg)](https://glama.ai/mcp/connectors/com.mobbin/mobbin)
  🔐 - Search real app UI screens, multi-step user flows, and website sections for design references.
- [Moodmark](https://moodmark.design/agents) `https://app.moodmark.design/mcp`
  [![Moodmark MCP connector](https://glama.ai/mcp/connectors/io.github.janvodvarka/moodmark/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.janvodvarka/moodmark)
  🔓 - Save websites with screenshots, palettes and fonts into a design reference library, then search and share it.
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
- [PaletteGet](https://paletteget.com/) `https://paletteget-mcp.y7206062.workers.dev/mcp`
  [![PaletteGet MCP connector](https://glama.ai/mcp/connectors/io.github.yang7206/paletteget/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.yang7206/paletteget)
  🔓 - Curated app, web and mini program palettes with measured WCAG contrast and CSS variables.
- [PartForge](https://www.partforge.ai) `https://www.partforge.ai/mcp`
  [![PartForge MCP connector](https://glama.ai/mcp/connectors/ai.partforge/partforge/badges/score.svg)](https://glama.ai/mcp/connectors/ai.partforge/partforge)
  🔐 - Create and edit parametric 3D-printable parts as code, render previews, and publish them to a public library.
- [Pastefield](https://pastefield.com/mcp) `https://pastefield.com/api/mcp`
  [![Pastefield MCP connector](https://glama.ai/mcp/connectors/com.pastefield/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.pastefield/mcp)
  🔐 - Give Claude a whiteboard: place notes, links, images and diagrams on a board you both edit.
- [Photo Mosaic & AI Collage Maker - Collager.ai](https://collager.ai/developers/) `https://collager.ai/mcp`
  [![Photo Mosaic & AI Collage Maker - Collager.ai MCP connector](https://glama.ai/mcp/connectors/ai.collager/ai-collage-maker/badges/score.svg)](https://glama.ai/mcp/connectors/ai.collager/ai-collage-maker)
  🔓 - Turn your own photos into a photo mosaic or a heart, number or word photo collage with a preview in seconds.
- [ProfessionalHeadshot.io](https://professionalheadshot.io) `https://professionalheadshot.io/api/mcp`
  [![ProfessionalHeadshot.io MCP connector](https://glama.ai/mcp/connectors/io.professionalheadshot/professionalheadshot/badges/score.svg)](https://glama.ai/mcp/connectors/io.professionalheadshot/professionalheadshot)
  🔓 - Official LinkedIn, Slack and GitHub profile photo specs with sources, headshot style guides and a free headshot audit.
- [QR Branding](https://qr-branding.com) `https://qr-branding.com/mcp`
  [![QR Branding MCP connector](https://glama.ai/mcp/connectors/io.github.quartzondev/qr-branding/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.quartzondev/qr-branding)
  🔓 - Branded QR codes (manual, AI-styled, 118 templates, Wi-Fi/vCard/geo), each decoded server-side before it is returned.
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
- [SpriteForge](https://www.spriteforge.tech) `https://www.spriteforge.tech/mcp`
  [![SpriteForge MCP connector](https://glama.ai/mcp/connectors/tech.spriteforge/sprite-forge/badges/score.svg)](https://glama.ai/mcp/connectors/tech.spriteforge/sprite-forge)
  🔐 - Generate pixel-art sprites, animations and 16-tile Wang tilesets on a fixed grid, saved to your SpriteForge library.
- [SpriteForge Editor](https://www.spriteforge.tech/claude) `https://www.spriteforge.tech/mcp/editor`
  [![SpriteForge Editor MCP connector](https://glama.ai/mcp/connectors/tech.spriteforge/sprite-forge-editor/badges/score.svg)](https://glama.ai/mcp/connectors/tech.spriteforge/sprite-forge-editor)
  🔓 - Free pixel and tileset editor: open sprites, animations and Wang tilesets in an editor and get the edited PNG back.
- [Tastepix](https://tastepix.com/?ref=github-awesome-remote) `https://mcp.tastepix.com/mcp`
  [![Tastepix MCP connector](https://glama.ai/mcp/connectors/io.github.paablobello/tastepix/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.paablobello/tastepix)
  🔐 - Generate and edit images with 12 models (Nano Banana, GPT Image, FLUX…) from chat; pay per image, no API keys.
- [Tesla Wrap Design](https://tesla-wrap.design) `https://tesla-wrap.design/mcp`
  [![Tesla Wrap Design MCP connector](https://glama.ai/mcp/connectors/io.github.GhostCatcg/tesla-wrap-design/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.GhostCatcg/tesla-wrap-design)
  🔐 - Design Tesla Paint Shop wraps from an AI assistant: gallery search, prompts, 3D preview, and PNG export.
- [UXKIN](https://uxkin.com) `https://uxkin.com/mcp`
  [![UXKIN MCP connector](https://glama.ai/mcp/connectors/io.github.uxkin/uxkin/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.uxkin/uxkin)
  🔐 - Real iOS app screens, user journeys and website design systems for AI coding agents.
- [Verdict](https://verdict.allthepossibles.com) `https://verdict.allthepossibles.com/mcp`
  [![Verdict MCP connector](https://glama.ai/mcp/connectors/com.allthepossibles/verdict/badges/score.svg)](https://glama.ai/mcp/connectors/com.allthepossibles/verdict)
  🔓 - Six design-review tools that run before a design ships.
- [Whimsical](https://whimsical.com/mcp) `https://mcp.whimsical.com/mcp`
  [![Whimsical MCP connector](https://glama.ai/mcp/connectors/com.whimsical/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.whimsical/mcp)
  🔐 - Turn prompts into editable flowcharts, mind maps, sequence diagrams and wireframes, and search your Whimsical workspace.
- [WikiBrand](https://wikibrand.org) `https://wikibrand.org/api/mcp`
  [![WikiBrand MCP connector](https://glama.ai/mcp/connectors/org.wikibrand/wikibrand/badges/score.svg)](https://glama.ai/mcp/connectors/org.wikibrand/wikibrand)
  🔓 - Logo, colors, typefaces, tone of voice and CSS theme of any brand, read from its own website.
  
### 🌐 <a name="browser-automation"></a>Browser Automation

- [Allscreenshots](https://allscreenshots.com) `https://mcp.allscreenshots.com/mcp/v1`
  [![Allscreenshots MCP connector](https://glama.ai/mcp/connectors/io.github.allscreenshots/allscreenshots/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.allscreenshots/allscreenshots)
  🔐 - Capture website screenshots, run bulk captures, and manage screenshot schedules and history.

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

- [CurlShot](https://curlshot.com/docs?utm_source=awesome-mcp&utm_medium=listing&utm_campaign=dist-q4) `https://curlshot.com/api/mcp`
  [![CurlShot MCP connector](https://glama.ai/mcp/connectors/io.github.SergiuPogor/curlshot/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.SergiuPogor/curlshot)
  🔓 - Screenshot any URL to PNG, JPEG, WebP, PDF or scrolling video, full page or dark mode; needs a free API key.

- [Framejet](https://framejet.dev) `https://framejet.dev/mcp`
  [![Framejet MCP connector](https://glama.ai/mcp/connectors/dev.framejet/screenshot/badges/score.svg)](https://glama.ai/mcp/connectors/dev.framejet/screenshot)
  🔓 - Screenshot any URL to PNG or JPEG with cookie banners and chat widgets removed; needs a free API key.

- [localscreenshot](https://localscreenshot.com) `https://api.localscreenshot.com/mcp/free`
  [![localscreenshot MCP connector](https://glama.ai/mcp/connectors/com.localscreenshot/localscreenshot/badges/score.svg)](https://glama.ai/mcp/connectors/com.localscreenshot/localscreenshot)
  🔓 - Screenshot any public page as PNG, JPEG or PDF, from 227 countries, with cookie banners and ads hidden.

- [Monito](https://www.monito.dev/docs/mcp) `https://www.monito.dev/api/mcp`
  [![Monito MCP connector](https://glama.ai/mcp/connectors/dev.monito/monito/badges/score.svg)](https://glama.ai/mcp/connectors/dev.monito/monito)
  🔐 - Tests a web app in a real browser from plain English; returns pass, fail or cannot verify with screenshots and logs.

- [screenshot.com.ar](https://screenshot.com.ar) `https://screenshot.com.ar/mcp`
  [![screenshot.com.ar MCP connector](https://glama.ai/mcp/connectors/ar.com.screenshot/screenshot/badges/score.svg)](https://glama.ai/mcp/connectors/ar.com.screenshot/screenshot)
  🔐 - Read any public page as clean markdown or capture it as an image in real Chrome; free tier, plans in ARS.

- [Shotkiln](https://shotkiln.com/mcp-screenshot-server) `https://shotkiln.com/mcp`
  [![Shotkiln MCP connector](https://glama.ai/mcp/connectors/com.shotkiln/shotkiln/badges/score.svg)](https://glama.ai/mcp/connectors/com.shotkiln/shotkiln)
  🔓 - Screenshot pages as PNG, JPEG or WebP, render a URL or HTML to PDF, and make 1200x630 OG images; key optional.

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
- [Control Plane](https://docs.controlplane.com/ai/mcp) `https://mcp.cpln.io/mcp`
  [![Control Plane MCP connector](https://glama.ai/mcp/connectors/io.cpln/control-plane/badges/score.svg)](https://glama.ai/mcp/connectors/io.cpln/control-plane)
  🔐 - Deploy and operate apps, databases, secrets, domains, and logs on Control Plane across AWS, GCP, and Azure.
- [Costory](https://docs.costory.io/features/mcp) `https://app-api.costory.io/mcp`
  [![Costory MCP connector](https://glama.ai/mcp/connectors/io.costory.app-api/costory/badges/score.svg)](https://glama.ai/mcp/connectors/io.costory.app-api/costory)
  🔐 - FinOps agent backend: query, allocate and explain AWS, GCP, Azure, Kubernetes and AI spend.
- [Crow Nest](https://crow-nest.com) `https://crow-nest.com/mcp`
  [![Crow Nest MCP connector](https://glama.ai/mcp/connectors/com.crow-nest/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.crow-nest/mcp)
  🔐 - Publish apps built with AI and share them with your team behind login, with data, files and AI built in.
- [DropTheHassle](https://dropthehassle.com) `https://dropthehassle.com/mcp`
  [![DropTheHassle MCP connector](https://glama.ai/mcp/connectors/io.github.bosmdavid-gif/dropthehassle/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.bosmdavid-gif/dropthehassle)
  🔓 - Publish static sites to a free HTTPS link or your own domain and check domain prices; account tools need a token.
- [Eurobase](https://eurobase.dev/docs/agents) `https://api.eurobase.dev/mcp`
  [![Eurobase MCP connector](https://glama.ai/mcp/connectors/dev.eurobase/eurobase/badges/score.svg)](https://glama.ai/mcp/connectors/dev.eurobase/eurobase)
  🔐 - Create projects from GitHub repositories, deploy them, and read build, runtime and HTTP logs on a European cloud.
- [FARPY](https://farpy.com) `https://api.farpy.com/mcp`
  [![FARPY MCP connector](https://glama.ai/mcp/connectors/com.farpy.api/farpy/badges/score.svg)](https://glama.ai/mcp/connectors/com.farpy.api/farpy)
  🔐 - Run verified Blender GPU workloads, track jobs, retrieve artifacts, and inspect execution receipts.
- [Fiskmas](https://fiskmas.dev) `https://mcp.fiskmas.dev/mcp`
  [![Fiskmas MCP connector](https://glama.ai/mcp/connectors/dev.fiskmas/fiskmas/badges/score.svg)](https://glama.ai/mcp/connectors/dev.fiskmas/fiskmas)
  🔓 - Create, deploy and monitor Docker apps on live HTTPS URLs.
- [Floot](https://floot.com) `https://mcp.floot.com/mcp`
  [![Floot MCP connector](https://glama.ai/mcp/connectors/com.floot/floot/badges/score.svg)](https://glama.ai/mcp/connectors/com.floot/floot)
  🔐 - Build React apps with serverless endpoints, Postgres and auth, run SQL, and publish to a live URL.
- [gpu.nz](https://gpu.nz/en/docs/mcp) `https://gpu.nz/mcp`
  [![gpu.nz MCP connector](https://glama.ai/mcp/connectors/nz.gpu/gpu-cloud/badges/score.svg)](https://glama.ai/mcp/connectors/nz.gpu/gpu-cloud)
  🔓 - Find GPUs with live prices, estimate VRAM, rent, monitor and stop GPU servers; renting needs an API key.
- [Hatch](https://viberooster.com) `https://mcp.theroost.dev/mcp`
  [![Hatch MCP connector](https://glama.ai/mcp/connectors/com.viberooster/hatch/badges/score.svg)](https://glama.ai/mcp/connectors/com.viberooster/hatch)
  🔓 - Publish a live website from an agent in one tool call, expiring or permanent, with human review hooks.
- [Heroku](https://heroku.com) `https://mcp.heroku.com/mcp`
  🔐 - Manage Heroku apps, dynos, add-ons, and logs.
- [Lium](https://docs.lium.io/developers/mcp) `https://docs.lium.io/mcp`
  [![Lium MCP connector](https://glama.ai/mcp/connectors/io.github.Datura-ai/lium-docs/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Datura-ai/lium-docs)
  🔓 - Search and read the docs of Lium, a GPU rental marketplace: rent GPU pods by the second via CLI, SDK or REST API.
- [NetActuate](https://netactuate.com) `https://netactuate.com/mcp`
  [![NetActuate MCP connector](https://glama.ai/mcp/connectors/com.netactuate/net-actuate/badges/score.svg)](https://glama.ai/mcp/connectors/com.netactuate/net-actuate)
  🔓 - Read-only answers from NetActuate's published network data: data centers, compliance, exchanges, products and pricing.
- [Netlify](https://netlify.com) `https://netlify-mcp.netlify.app/mcp`
  🔐 - Create, deploy, and manage Netlify sites.
- [Nerdit](https://nerdit.ai/?utm_source=awesome-remote-mcp-servers) `https://mcp.nerdit.ai/mcp`
  [![Nerdit MCP connector](https://glama.ai/mcp/connectors/ai.nerdit/nerdit/badges/score.svg)](https://glama.ai/mcp/connectors/ai.nerdit/nerdit)
  🔐 - Deploy apps, databases and local AI models to your own machines, read logs, set variables and share apps.
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
- [Roar AI](https://roar-ai.com/docs/mcp) `https://cloud.roar-ai.com/mcp`
  [![Roar AI MCP connector](https://glama.ai/mcp/connectors/com.roar-ai/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.roar-ai/mcp)
  🔐 - Deploy apps from GitHub with databases and domains, manage API keys and spend, and call 200+ AI models.
- [ShipStatic](https://shipstatic.com) `https://mcp.shipstatic.com`
  [![ShipStatic MCP connector](https://glama.ai/mcp/connectors/com.shipstatic/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.shipstatic/mcp)
  🔓 - Deploy static websites, landing pages, and prototypes instantly, free with no account; sign in to keep sites for good.
- [Shipvela](https://shipvela.com) `https://shipvela.com/mcp`
  [![Shipvela MCP connector](https://glama.ai/mcp/connectors/com.shipvela/shipvela/badges/score.svg)](https://glama.ai/mcp/connectors/com.shipvela/shipvela)
  🔐 - Create website projects, deploy supported GitHub repositories, and inspect deployment status, logs, and usage.
- [spawnpoint](https://getspawnpoint.com) `https://app.getspawnpoint.com/mcp`
  [![spawnpoint MCP connector](https://glama.ai/mcp/connectors/com.getspawnpoint/spawnpoint/badges/score.svg)](https://glama.ai/mcp/connectors/com.getspawnpoint/spawnpoint)
  🔐 - Deploy the small apps an agent builds to a live HTTPS link, private by default and shared by email like a Google Doc.
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

- [ActivitySmith](https://activitysmith.com/integrations/mcp-server) `https://mcp.activitysmith.com/mcp`
  [![ActivitySmith MCP connector](https://glama.ai/mcp/connectors/com.activitysmith/activitysmith/badges/score.svg)](https://glama.ai/mcp/connectors/com.activitysmith/activitysmith)
  🔐 - AI agents and scripts reporting back to your iPhone with Push Notifications and Live Activities.
- [Agent Tavern](https://agenttavern.dev) `https://agenttavern.dev/mcp`
  [![Agent Tavern MCP connector](https://glama.ai/mcp/connectors/io.github.tima100faces/agent-tavern/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.tima100faces/agent-tavern)
  🔓 - Public Q&A board where AI agents on different runtimes ask and answer each other; posting needs a free key.
- [AICQ](https://getaicq.com/connect) `https://getaicq.com/mcp`
  [![AICQ MCP connector](https://glama.ai/mcp/connectors/com.getaicq/aicq/badges/score.svg)](https://glama.ai/mcp/connectors/com.getaicq/aicq)
  🔓 - Messaging network for AI agents: talk to other people's agents and groups; free, calls after aicq_join need a key.
- [Aitho](https://aitho.app) `https://present.aitho.app/mcp`
  [![Aitho MCP connector](https://glama.ai/mcp/connectors/app.aitho/aitho/badges/score.svg)](https://glama.ai/mcp/connectors/app.aitho/aitho)
  🔐 - Turn a slide deck into a rehearsable talk with a voice-following script and slides that advance as you speak.
- [AskOne](https://askone.org) `https://askone.org/api/mcp`
  [![AskOne MCP connector](https://glama.ai/mcp/connectors/io.github.phuryn/askone/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.phuryn/askone)
  🔐 - Run live audience Q&A and polls with free AI moderation: start rooms, launch polls, answer questions, draft a FAQ.
- [Atendio](https://atendio.co/conecta-tu-claude) `https://atendio.co/api/mcp`
  [![Atendio MCP connector](https://glama.ai/mcp/connectors/co.atendio/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/co.atendio/mcp)
  🔐 - Read WhatsApp conversations and analytics, and manage the rules of a business's AI WhatsApp assistant.
- [BumbleBox](https://bumblebox.ai/integrations) `https://api.bumblebox.ai/api/mcp`
  [![BumbleBox MCP connector](https://glama.ai/mcp/connectors/ai.bumblebox/mail/badges/score.svg)](https://glama.ai/mcp/connectors/ai.bumblebox/mail)
  🔓 - Search, triage and draft replies across Gmail, Outlook and IMAP mailboxes; sending only at the level you set.
- [Call Me](https://callmemcp.com) `https://callmemcp.com/mcp`
  [![Call Me MCP connector](https://glama.ai/mcp/connectors/com.serdaroztetik/call-me/badges/score.svg)](https://glama.ai/mcp/connectors/com.serdaroztetik/call-me)
  🔓 - Your AI rings your iPhone, speaks its question, and gets your spoken answer back as text.
- [Cookie Hive](https://cookiehive.pythonanywhere.com/join) `https://cookiehive.pythonanywhere.com/mcp`
  [![Cookie Hive MCP connector](https://glama.ai/mcp/connectors/io.github.tuhaku42-tech/cookiehive/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.tuhaku42-tech/cookiehive)
  🔓 - Agent-only social feed and task board: read the feed, post, vote, and trade jobs for internal credits.
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
- [Groundmail](https://groundmail.dev) `https://mcp.groundmail.dev/mcp`
  [![Groundmail MCP connector](https://glama.ai/mcp/connectors/io.github.Groundmail/groundmail/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Groundmail/groundmail)
  🔐 - Send transactional email, check delivery, and set up sending domains, templates and webhooks.
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
- [MepMail](https://mepmail.dev) `https://api.mepmail.dev/mcp`
  [![MepMail MCP connector](https://glama.ai/mcp/connectors/io.github.JE4NVRG/mepmail/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.JE4NVRG/mepmail)
  🔐 - Send email, manage broadcasts and domains, and read or reply to Correio mailboxes within granted permissions.
- [Multi Mail](https://lumman.co/mcp/multi-mail) `https://mail.lumman.co/mcp`
  [![Multi Mail MCP connector](https://glama.ai/mcp/connectors/co.lumman/mail/badges/score.svg)](https://glama.ai/mcp/connectors/co.lumman/mail)
  🔐 - Search, read, draft, send and organise mail across several Gmail, Outlook, Microsoft 365, iCloud and Fastmail mailboxes.
- [MyOTP.App](https://myotp.app/mcp/) `https://mcp.myotp.app/mcp`
  [![MyOTP.App MCP connector](https://glama.ai/mcp/connectors/io.github.brntech/myotp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.brntech/myotp)
  🔓 - Send and verify OTP codes over SMS, WhatsApp and Telegram in 190+ countries.
- [Pachca](https://dev.pachca.com/guides/mcp/overview) `https://mcp.pachca.com/mcp`
  [![Pachca MCP connector](https://glama.ai/mcp/connectors/com.pachca/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.pachca/mcp)
  🔐 - Read, search and post in Pachca team chat, and work with threads, reminders, employees and bots within your permissions.
- [PaperAgent](https://paperagent.dev) `https://paperagent.dev/mcp`
  [![PaperAgent MCP connector](https://glama.ai/mcp/connectors/dev.paperagent/letters/badges/score.svg)](https://glama.ai/mcp/connectors/dev.paperagent/letters)
  🔓 - Mail one-off USPS letters from chat: validates the US address, shows a PDF preview and total, and waits for approval.
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
- [SendFaxFast](https://sendfaxfast.com/ai-connect.html) `https://sendfaxfast.com/api/mcp.php`
  [![SendFaxFast MCP connector](https://glama.ai/mcp/connectors/com.sendfaxfast/fax/badges/score.svg)](https://glama.ai/mcp/connectors/com.sendfaxfast/fax)
  🔓 - Send real faxes (PDF/JPG/photo) from AI chat to the US, Canada, Australia, New Zealand and 39 more countries.
- [Sending](https://sending.dev) `https://sending.dev/api/mcp`
  [![Sending MCP connector](https://glama.ai/mcp/connectors/dev.sending/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/dev.sending/mcp)
  🔐 - Email, WhatsApp and Telegram for agents: send, campaigns, automations, contacts, agent inboxes.
- [Sessy](https://sessy.do/docs/mcp) `https://api.sessy.do/mcp`
  [![Sessy MCP connector](https://glama.ai/mcp/connectors/io.github.marckohlbrugge/sessy/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.marckohlbrugge/sessy)
  🔐 - Read-only Amazon SES observability: search events, inspect bounces and complaints, and pull delivery stats.
- [Signatoro](https://signatoro.com) `https://signatoro.com/mcp`
  [![Signatoro MCP connector](https://glama.ai/mcp/connectors/com.signatoro/signatoro/badges/score.svg)](https://glama.ai/mcp/connectors/com.signatoro/signatoro)
  🔓 - Fetch the saved email signature people and their AI agents append to every email they send or draft.
- [SofortFax](https://sofortfax.de/ki-fax.html) `https://sofortfax.de/api/mcp.php`
  [![SofortFax MCP connector](https://glama.ai/mcp/connectors/de.sofortfax/fax/badges/score.svg)](https://glama.ai/mcp/connectors/de.sofortfax/fax)
  🔓 - Send real faxes (PDF/JPG/photo) from AI chat to Germany, Austria and 40+ countries; pay per fax or prepaid credits.
- [Subo](https://subo.gg/blog/connect-discord-community-to-ai-agent/) `https://api.subo.ai/mcp`
  [![Subo MCP connector](https://glama.ai/mcp/connectors/gg.subo/survey-bot/badges/score.svg)](https://glama.ai/mcp/connectors/gg.subo/survey-bot)
  🔐 - Build, launch and analyze surveys, polls, forms and quizzes in a Discord community, and reward members with XP.
- [SuguFAX](https://sugufax.com/ai) `https://sugufax.com/api/mcp.php`
  [![SuguFAX MCP connector](https://glama.ai/mcp/connectors/com.sugufax/fax-payperuse/badges/score.svg)](https://glama.ai/mcp/connectors/com.sugufax/fax-payperuse)
  🔓 - Send real faxes (PDF/photo) from AI chat to Japan, paid per fax from ¥400 or with prepaid credits.
- [SwarmMemo](https://swarmmemo.com) `https://swarmmemo.com/mcp`
  [![SwarmMemo MCP connector](https://glama.ai/mcp/connectors/com.swarmmemo/bulletin/badges/score.svg)](https://glama.ai/mcp/connectors/com.swarmmemo/bulletin)
  🔓 - Free public bulletin board where agents post, reply and find peers.
- [TaskBounty Agent Board](https://www.task-bounty.com/board/start) `https://www.task-bounty.com/api/mcp/board`
  [![TaskBounty Agent Board MCP connector](https://glama.ai/mcp/connectors/io.github.eliottreich/agent-board/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.eliottreich/agent-board)
  🔓 - Use 14 tools to find collaborators, discuss ideas, and coordinate public tasks or private swarms without signup.
- [The Colony](https://thecolony.cc/for-agents) `https://thecolony.cc/mcp/`
  [![The Colony MCP connector](https://glama.ai/mcp/connectors/cc.thecolony/the-colony/badges/score.svg)](https://glama.ai/mcp/connectors/cc.thecolony/the-colony)
  🔓 - Forum and social network for AI agents: read posts anonymously; post, comment, vote and message with a token.
- [The Commons](https://mcp.deadbrands.co/hub/) `https://mcp.deadbrands.co/hub/mcp`
  [![The Commons MCP connector](https://glama.ai/mcp/connectors/io.github.dstrausser83/db-collab-hub/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.dstrausser83/db-collab-hub)
  🔓 - Open discussion hub for AI agents: read anonymously, post with a free instant hub key, home of the Bot Game Arena.
- [ThunderPhone](https://thunderphone.com) `https://api.thunderphone.com/v1/mcp`
  [![ThunderPhone MCP connector](https://glama.ai/mcp/connectors/io.github.thunderphone/thunderphone/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.thunderphone/thunderphone)
  🔐 - Build, test and run AI phone agents: numbers, inbound and outbound calls, campaigns and transcripts.
- [Tokolaku](https://tokolaku.id/developers) `https://api.tokolaku.id/mcp`
  [![Tokolaku MCP connector](https://glama.ai/mcp/connectors/id.tokolaku/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/id.tokolaku/mcp)
  🔐 - Send WhatsApp Business messages and manage inbox conversations, products, orders and webhooks for Indonesian SMBs.
- [voicehook](https://voicehook.ai/?utm_source=awesome-remote-mcp&utm_campaign=d13-remote-list) `https://voicehook.ai/mcp`
  [![voicehook MCP connector](https://glama.ai/mcp/connectors/io.github.voicehook-ai/voicehook/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.voicehook-ai/voicehook)
  🔓 - Talk with your agents: a voice call in the browser that your agent can start or join.
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
- [Convika](https://convika.com) `https://mcp.convika.com/mcp`
  [![Convika MCP connector](https://glama.ai/mcp/connectors/com.convika/convika/badges/score.svg)](https://glama.ai/mcp/connectors/com.convika/convika)
  🔐 - Publish AI-made landing pages on your own domain, with a signup form and visitor stats.
- [dochost](https://dochost.io/mcp) `https://dochost.io/api/mcp`
  [![dochost MCP connector](https://glama.ai/mcp/connectors/io.dochost/dochost/badges/score.svg)](https://glama.ai/mcp/connectors/io.dochost/dochost)
  🔓 - Publish Markdown or HTML as a hosted page and get a shareable link.
- [Docs MD](https://docs-md.com/agents) `https://docs-md.com/api/mcp`
  [![Docs MD MCP connector](https://glama.ai/mcp/connectors/com.docs-md/markdown-share/badges/score.svg)](https://glama.ai/mcp/connectors/com.docs-md/markdown-share)
  🔓 - Publish markdown as a rendered link with an expiry, read shares back as markdown, update or delete them.
- [Foliade](https://foliade.gekkode.com/en/) `https://foliade.gekkode.com/mcp`
  [![Foliade MCP connector](https://glama.ai/mcp/connectors/com.gekkode/foliade/badges/score.svg)](https://glama.ai/mcp/connectors/com.gekkode/foliade)
  🔓 - Turn a PDF into a mobile flipbook catalogue, customise its reader and publish it.
- [Foliyo](https://foliyo.io) `https://foliyo.io/mcp`
  [![Foliyo MCP connector](https://glama.ai/mcp/connectors/io.foliyo/foliyo/badges/score.svg)](https://glama.ai/mcp/connectors/io.foliyo/foliyo)
  🔐 - Create, brand, publish and track client-ready reports, proposals and research pages.
- [Ginta](https://ginta.app/website-builder-mcp/) `https://ginta.app/mcp`
  [![Ginta MCP connector](https://glama.ai/mcp/connectors/app.ginta/ginta/badges/score.svg)](https://glama.ai/mcp/connectors/app.ginta/ginta)
  🔐 - Build, publish and edit hosted websites with working forms, menus, bookings, blogs and an owner admin.
- [GoodBarber](https://www.goodbarber.com/mcp/) `https://mcp.goodbarber.dev/mcp/sse`
  [![GoodBarber MCP connector](https://glama.ai/mcp/connectors/dev.goodbarber/goodbarber-public-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/dev.goodbarber/goodbarber-public-mcp)
  🔐 - Manage a GoodBarber no-code app: content, push notifications, shop orders, members, and analytics.
- [INKFLOW](https://inkflowstudio.org) `https://api.inkflowstudio.org/api/mcp`
  [![INKFLOW MCP connector](https://glama.ai/mcp/connectors/org.inkflowstudio/inkflow/badges/score.svg)](https://glama.ai/mcp/connectors/org.inkflowstudio/inkflow)
  🔓 - Writes complete books, series, manuals and translations, plus TikTok/YouTube promo videos; free Chapter 1 with no key.
- [JustCopy](https://justcopy.ai/docs/mcp) `https://justcopy.ai/mcp`
  [![JustCopy MCP connector](https://glama.ai/mcp/connectors/ai.justcopy/justcopy/badges/score.svg)](https://glama.ai/mcp/connectors/ai.justcopy/justcopy)
  🔐 - Build, change and publish a working business website from a chat, with sign-in, saved form data and photo uploads.
- [Keepp](https://keepp.link/developers) `https://api.keepp.link/mcp`
  [![Keepp MCP connector](https://glama.ai/mcp/connectors/link.keepp/keepp/badges/score.svg)](https://glama.ai/mcp/connectors/link.keepp/keepp)
  🔐 - Build and edit a Keepp page (links, shop, bookings, forms) at keepp.link/yourname.
- [Kleap](https://kleap.co/mcp) `https://kleap.co/api/mcp`
  [![Kleap MCP connector](https://glama.ai/mcp/connectors/co.kleap/kleap/badges/score.svg)](https://glama.ai/mcp/connectors/co.kleap/kleap)
  🔓 - Build, edit, publish and manage real websites and web apps from your AI agent.
- [Lediv](https://lediv.com) `https://lediv.app/mcp`
  [![Lediv MCP connector](https://glama.ai/mcp/connectors/app.lediv/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/app.lediv/mcp)
  🔐 - Visual website builder synced with real code: edit files, publish, roll back, manage domains and previews.
- [LetX](https://letx.app/mcp/) `https://api.letx.app/mcp`
  [![LetX MCP connector](https://glama.ai/mcp/connectors/app.letx/letx/badges/score.svg)](https://glama.ai/mcp/connectors/app.letx/letx)
  🔐 - Write LaTeX from 1,000+ journal, thesis and CV templates and compile to PDF with the build log.
- [Posy](https://posy.page) `https://posy.page/api/mcp`
  [![Posy MCP connector](https://glama.ai/mcp/connectors/io.github.Himanshu-Sangshetti/posy/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Himanshu-Sangshetti/posy)
  🔐 - Build and edit a hand-made link-in-bio page: add links, pick a look, publish it at posy.page.
- [Sanity](https://sanity.io) `https://mcp.sanity.io/mcp`
  [![Sanity MCP connector](https://glama.ai/mcp/connectors/io.sanity.www/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.sanity.www/mcp)
  🔐 - Query and mutate Sanity datasets and documents.
- [Share Artifacts](https://shareartifacts.dev) `https://shareartifacts.dev/api/mcp`
  [![Share Artifacts MCP connector](https://glama.ai/mcp/connectors/io.github.arunai30/share-artifacts/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.arunai30/share-artifacts)
  🔐 - Publish and update static HTML reports, presentations, and explainers with controlled sharing.
- [sitectrl](https://sitectrl.ai/mcp) `https://mcp.sitectrl.ai/mcp`
  [![sitectrl MCP connector](https://glama.ai/mcp/connectors/ai.sitectrl/sitectrl/badges/score.svg)](https://glama.ai/mcp/connectors/ai.sitectrl/sitectrl)
  🔓 - Describe a site and get it live with SSL, forms and analytics; OAuth to edit and manage it.
- [SiteKrs](https://sitekrs.ai-krs.com) `https://sitekrs.ai-krs.com/api/mcp`
  [![SiteKrs MCP connector](https://glama.ai/mcp/connectors/io.github.hansail001/sitekrs/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.hansail001/sitekrs)
  🔓 - List SiteKrs static-site templates and get editor links; import your own source on the homepage.
- [Sitelas](https://sitelas.com) `https://sitelas.com/api/mcp`
  [![Sitelas MCP connector](https://glama.ai/mcp/connectors/com.sitelas/sitelas/badges/score.svg)](https://glama.ai/mcp/connectors/com.sitelas/sitelas)
  🔐 - Build a website from a template, preview it, publish on approval, then edit it and read its form messages.
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
- [ppl](https://withppl.com) `https://withppl.com/mcp`
  [![ppl MCP connector](https://glama.ai/mcp/connectors/io.github.ppl-crm/ppl/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ppl-crm/ppl)
  🔐 - Personal CRM as agent memory: contacts, notes, journal, tasks, reminders, semantic search; 120 tools.
- [SignalRaven](https://signalraven.ai) `https://api.signalraven.ai/mcp`
  [![SignalRaven MCP connector](https://glama.ai/mcp/connectors/io.github.signalraven/signalraven/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.signalraven/signalraven)
  🔐 - LinkedIn buying-intent signals, prospect and account research, and openers from your workspace.
- [Workspace369](https://workspace369.com) `https://mcp.workspace369.com/mcp`
  [![Workspace369 MCP connector](https://glama.ai/mcp/connectors/com.workspace369/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.workspace369/mcp)
  🔐 - Manage clients, proposals, e-sign contracts, invoices, projects, calendar and time tracking for client-work businesses.

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
- [PostData](https://postdata.cloud) `https://api.postdata.cloud/mcp`
  [![PostData MCP connector](https://glama.ai/mcp/connectors/cloud.postdata/postdata/badges/score.svg)](https://glama.ai/mcp/connectors/cloud.postdata/postdata)
  🔓 - Free, no-signup IoT sensor store: get a device name, read readings and history, wait for a flashed board to report.
- [Prisma](https://prisma.io) `https://mcp.prisma.io/mcp`
  [![Prisma MCP connector](https://glama.ai/mcp/connectors/io.prisma/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.prisma/mcp)
  🔐 - Manage Prisma Postgres databases and run migrations.
- [Speak To Your Database](https://speaktoyourdatabase.com) `https://speaktoyourdatabase.com/mcp`
  [![Speak To Your Database MCP connector](https://glama.ai/mcp/connectors/com.speaktoyourdatabase/styd/badges/score.svg)](https://glama.ai/mcp/connectors/com.speaktoyourdatabase/styd)
  🔐 - Ask your Odoo, PostgreSQL or MySQL data in plain words and get real numbers, computed read-only from your data.
- [Supabase](https://supabase.com) `https://mcp.supabase.com/mcp`
  [![Supabase MCP connector](https://glama.ai/mcp/connectors/com.supabase/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.supabase/mcp)
  🔐 - Manage Supabase projects, run SQL, and inspect schemas.
- [Teable](https://teable.ai) `https://mcp.teable.ai/mcp`
  [![Teable MCP connector](https://glama.ai/mcp/connectors/ai.teable.mcp/teable/badges/score.svg)](https://glama.ai/mcp/connectors/ai.teable.mcp/teable)
  🔐 - Inspect tables and read or update business records in Teable, an AI spreadsheet for business.

### 📊 <a name="data-visualization"></a>Data Visualization

- [chartlink](https://chartlink.app) `https://chartlink.app/mcp`
  [![chartlink MCP connector](https://glama.ai/mcp/connectors/io.github.oscarleoo/chartlink/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.oscarleoo/chartlink)
  🔓 - Charts and tables with live-updating embed links, drafted from one message; tools need a key.
- [ngx-json-render UI](https://ngx-json-render.vercel.app) `https://ngx-json-render.vercel.app/mcp`
  [![ngx-json-render UI MCP connector](https://glama.ai/mcp/connectors/io.github.shteynu/ngx-json-render-ui/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.shteynu/ngx-json-render-ui)
  🔓 - Renders dashboards, forms and tables as Angular Material components inline in the chat (MCP App).
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
- [AgentIndex](https://agentindex.app) `https://agentindex.app/api/mcp/`
  [![AgentIndex MCP connector](https://glama.ai/mcp/connectors/app.agentindex/agentindex/badges/score.svg)](https://glama.ai/mcp/connectors/app.agentindex/agentindex)
  🔓 - Search a curated directory of open-source AI agents, MCP servers and dev tools; get details, categories and trending.
- [AgentoolRank](https://agentoolrank.com/agents) `https://agentoolrank.com/api/mcp`
  [![AgentoolRank MCP connector](https://glama.ai/mcp/connectors/com.agentoolrank/agent-tools/badges/score.svg)](https://glama.ai/mcp/connectors/com.agentoolrank/agent-tools)
  🔓 - Search and compare open-source AI agent tools ranked by live GitHub activity, and list new ones.
- [AgentTask Atlas](https://agenttaskatlas.com/mcp) `https://agenttaskatlas.com/api/mcp`
  [![AgentTask Atlas MCP connector](https://glama.ai/mcp/connectors/com.agenttaskatlas/catalog/badges/score.svg)](https://glama.ai/mcp/connectors/com.agenttaskatlas/catalog)
  🔓 - Search a curated catalog of MCP servers and Agent Skills by dev task, with install steps and practical verdicts.
- [AI Commander](https://aicommander.dev) `https://aicommander.dev/mcp`
  [![AI Commander MCP connector](https://glama.ai/mcp/connectors/dev.aicommander/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/dev.aicommander/mcp)
  🔐 - Remote shell and detached jobs on your machines — harness for Claude Code, Codex, ChatGPT, Cursor.
- [AI Design Blueprint](https://aidesignblueprint.com) `https://aidesignblueprint.com/mcp`
  [![AI Design Blueprint MCP connector](https://glama.ai/mcp/connectors/com.aidesignblueprint/blueprint/badges/score.svg)](https://glama.ai/mcp/connectors/com.aidesignblueprint/blueprint)
  🔓 - Search 10 design principles, examples and guides; spec and UI validators on paid plans.
- [AISkills402](https://aiskills402.com) `https://mcp.aiskills402.com/mcp`
  [![AISkills402 MCP connector](https://glama.ai/mcp/connectors/com.aiskills402/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.aiskills402/mcp)
  🔓 - Search tested agent skill files (SKILL.md) and read their cards for free; buy a file once with x402 in USDC on Base.
- [Apple RAG MCP](https://apple-rag.com) `https://mcp.apple-rag.com`
  [![Apple RAG MCP connector](https://glama.ai/mcp/connectors/com.apple-rag/mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/com.apple-rag/mcp-server)
  🔓 - Search official Apple developer docs and WWDC transcripts with RAG and Jev ranking.
- [Astro Docs](https://astro.build) `https://mcp.docs.astro.build/mcp`
  🔓 - Search the Astro documentation.
- [Ausca](https://ausca.com) `https://ausca.com/mcp`
  [![Ausca MCP connector](https://glama.ai/mcp/connectors/com.ausca/agent-services/badges/score.svg)](https://glama.ai/mcp/connectors/com.ausca/agent-services)
  🔓 - Pay per call for remote browsers, receive-only inboxes, OCR, document analysis, and media transcription.
- [Benchline](https://tools.fabwaseem.com/mcp/guide) `https://tools.fabwaseem.com/mcp`
  [![Benchline MCP connector](https://glama.ai/mcp/connectors/com.fabwaseem.tools/benchline/badges/score.svg)](https://glama.ai/mcp/connectors/com.fabwaseem.tools/benchline)
  🔓 - 72 dev tools: JSON, PDF, images, OCR, JWT, hashes, DNS, TLS, headers, llms.txt and OG images.
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
- [Carrick](https://carrick.tools) `https://api.carrick.tools/mcp`
  [![Carrick MCP connector](https://glama.ai/mcp/connectors/io.github.carrick-tools/carrick/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.carrick-tools/carrick)
  🔐 - Indexes TypeScript codebases across services and repositories so agents search functions by intent rather than name.
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
- [ConvertFileFast](https://www.convertfilefast.com) `https://mcp.convertfilefast.com/mcp`
  [![ConvertFileFast MCP connector](https://glama.ai/mcp/connectors/io.github.MLTCorp/convertfilefast/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.MLTCorp/convertfilefast)
  🔓 - Convert documents, images and data files between formats, and merge, split, compress or protect PDFs.
- [Datakoot Package Intel](https://datakoot.com/package-intel) `https://package.datakoot.com/mcp`
  [![Datakoot Package Intel MCP connector](https://glama.ai/mcp/connectors/com.datakoot/npm-pypi-crates-packages/badges/score.svg)](https://glama.ai/mcp/connectors/com.datakoot/npm-pypi-crates-packages)
  🔓 - npm, PyPI and crates.io package health, versions, downloads, dependencies and advisories.
- [Decide Runtime](https://www.decide.fyi/mcp#connect-runtime) `https://mcp-live.decide.fyi/developer-prepaid/v1/mcp`
  [![Decide Runtime MCP connector](https://glama.ai/mcp/connectors/io.github.nodeblur/decide-runtime/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.nodeblur/decide-runtime)
  🔓 - Public discovery; authenticated tools evaluate/read/export. $10/1,000 completed records. EU27/UK/US pilot; no execution.
- [DeepWiki](https://deepwiki.com) `https://mcp.deepwiki.com/mcp`
  🔓 - Ask questions about any public GitHub repository's generated wiki.
- [dep-diff](https://github.com/DigiCatalyst-Systems/dep-diff-mcp#readme) `https://dep-diff.digicatalyst.ca/mcp`
  [![dep-diff MCP connector](https://glama.ai/mcp/connectors/io.github.DigiCatalyst-Systems/dep-diff-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.DigiCatalyst-Systems/dep-diff-mcp)
  🔓 - Rank npm, PyPI and GitHub Actions upgrades by risk: breaking changes, fixed CVEs and migration links.
- [DNS-DATA Remote](https://dns-data.com/) `https://mcp.dns-data.com/mcp`
  [![DNS-DATA Remote MCP connector](https://glama.ai/mcp/connectors/com.dns-data.mcp/dns-data-remote/badges/score.svg)](https://glama.ai/mcp/connectors/com.dns-data.mcp/dns-data-remote)
  🔐 - Connect AI assistants to authorized Windows or macOS computers for files, commands, and device management.
- [Docsy](https://docsy.remcp.site) `https://docsy.remcp.site/mcp/registry`
  [![Docsy MCP connector](https://glama.ai/mcp/connectors/io.github.getremcp/docsy/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.getremcp/docsy)
  🔓 - Search versioned developer documentation and fetch source-linked results using five read-only tools.
- [Dynamic Document API](https://dynamicdocumentapi.com/docs/mcp) `https://mcp.dynamicdocumentapi.com/mcp`
  [![Dynamic Document API MCP connector](https://glama.ai/mcp/connectors/com.dynamicdocumentapi/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.dynamicdocumentapi/mcp)
  🔐 - Render PDFs and images from templates, HTML or Markdown, and create validated XRechnung and ZUGFeRD e-invoices.
- [Electrik Slate](https://slate.electrik.dev) `https://mcp.slate.electrik.dev`
  [![Electrik Slate MCP connector](https://glama.ai/mcp/connectors/io.github.neerajsohal/slate/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.neerajsohal/slate)
  🔓 - Read Electrik Slate Blade component docs, blocks gallery, source, and llms.txt.
- [ElectroGen](https://electrogen.org) `https://electrogen.org/.well-known/mcp`
  [![ElectroGen MCP connector](https://glama.ai/mcp/connectors/org.electrogen/electrogen/badges/score.svg)](https://glama.ai/mcp/connectors/org.electrogen/electrogen)
  🔓 - Generate a buildable electronics blueprint — BOM, wiring, firmware, CAD and preview renders — from a text brief.
- [Email Spam Tester](https://email-spam-tester.com) `https://email-spam-tester.com/mcp`
  [![Email Spam Tester MCP connector](https://glama.ai/mcp/connectors/io.github.serg-tanichev/email-spam-tester/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.serg-tanichev/email-spam-tester)
  🔓 - Send a draft to a one-time address and get a spam score, 41 checks with RFC citations, and a fix plan.
- [EmpirioLabs AI](https://docs.empiriolabs.ai/mcp) `https://mcp.empiriolabs.ai/mcp`
  [![EmpirioLabs AI MCP connector](https://glama.ai/mcp/connectors/ai.empiriolabs/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/ai.empiriolabs/mcp)
  🔐 - Run 200+ AI models for chat, image, video, speech and 3D, plus web search, batches and async jobs.
- [Favicon Tools](https://favicontools.com) `https://favicontools.com/api/mcp`
  [![Favicon Tools MCP connector](https://glama.ai/mcp/connectors/io.github.mewc/favicon-app-icons/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.mewc/favicon-app-icons)
  🔓 - Check a site's favicons and app icons, and generate a full favicon, Apple touch, and PWA icon set.
- [FernTool](https://www.ferntool.com/api) `https://www.ferntool.com/mcp`
  [![FernTool IP Lookup MCP connector](https://glama.ai/mcp/connectors/com.ferntool/ip/badges/score.svg)](https://glama.ai/mcp/connectors/com.ferntool/ip)
  🔓 - IP lookup and validation with ASN, geo and VPN/Tor flags, plus WHOIS, DNS, reverse DNS and subnet tools.
- [Firedrill](https://firedrill.run/agents) `https://mcp.firedrill.run/mcp`
  [![Firedrill MCP connector](https://glama.ai/mcp/connectors/io.github.firedrill-tools/firedrill/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.firedrill-tools/firedrill)
  🔐 - Prepare AI agent simulations, scenarios and synthetic tools, and inspect saved outcomes and evidence. Free to use.
- [Footgun](https://getfootgun.com) `https://getfootgun.com/api/mcp`
  [![Footgun MCP connector](https://glama.ai/mcp/connectors/com.getfootgun/footgun/badges/score.svg)](https://glama.ai/mcp/connectors/com.getfootgun/footgun)
  🔓 - Dated, verified fixes for known API, platform and AI coding tool breakages, checked before your agent codes.
- [Formhaus Cloud](https://formhaus.dev) `https://api.formhaus.dev/mcp/account`
  [![Formhaus Cloud MCP connector](https://glama.ai/mcp/connectors/dev.formhaus.api/formhaus-cloud/badges/score.svg)](https://glama.ai/mcp/connectors/dev.formhaus.api/formhaus-cloud)
  🔐 - Publish forms from JSON definitions, read submissions and manage form settings and webhooks.
- [FrontMCP Docs](https://frontmcp.dev/learn/docs-for-your-agent) `https://mcp.frontmcp.dev`
  [![FrontMCP Docs MCP connector](https://glama.ai/mcp/connectors/dev.frontmcp.mcp/frontmcp/badges/score.svg)](https://glama.ai/mcp/connectors/dev.frontmcp.mcp/frontmcp)
  🔓 - Search and read FrontMCP's documentation, pinned to the FrontMCP version a project uses.
- [GitDiagram](https://gitdiagram.com) `https://gitdiagram.com/mcp`
  [![GitDiagram MCP connector](https://glama.ai/mcp/connectors/com.gitdiagram/gitdiagram/badges/score.svg)](https://glama.ai/mcp/connectors/com.gitdiagram/gitdiagram)
  🔓 - Architecture diagrams, explanations and Mermaid source for any public GitHub repository.
- [GO AI Tools](https://goaichat.app/mcp-tools) `https://goaichat.app/mcp-tools/mcp`
  [![GO AI Tools MCP connector](https://glama.ai/mcp/connectors/app.goaichat/tools/badges/score.svg)](https://glama.ai/mcp/connectors/app.goaichat/tools)
  🔓 - 31 deterministic tools: image conversion, EXIF stripping, App Store assets, colour maths.
- [Globalping](https://globalping.io) `https://mcp.globalping.dev/mcp`
  🔐 - Run ping, traceroute, DNS, and HTTP checks from a global probe network.
- [Goldsky Docs](https://docs.goldsky.com/mcp-server) `https://docs.goldsky.com/mcp`
  [![Goldsky Docs MCP connector](https://glama.ai/mcp/connectors/com.goldsky/docs/badges/score.svg)](https://glama.ai/mcp/connectors/com.goldsky/docs)
  🔓 - Search and read Goldsky docs: wallet Feeds APIs, prebuilt onchain datasets, Turbo pipelines, subgraphs, Edge RPC.
- [GreatWait](https://greatwait.dev/) `https://api.greatwait.dev/mcp`
  [![GreatWait MCP connector](https://glama.ai/mcp/connectors/dev.greatwait/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/dev.greatwait/mcp)
  🔐 - Schedule one-off or recurring HTTPS callbacks, inspect delivery history, and cancel scheduled work.
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
- [IceShore](https://iceshore.ai/) `https://mcp.iceshore.ai/mcp`
  [![IceShore MCP connector](https://glama.ai/mcp/connectors/ai.iceshore/iceshore/badges/score.svg)](https://glama.ai/mcp/connectors/ai.iceshore/iceshore)
  🔓 - Make your AI better at system maintenance. Prompts your AI to organize use cases behind each system.
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
- [Koppar](https://koppar.ai) `https://app.koppar.ai/mcp`
  [![Koppar MCP connector](https://glama.ai/mcp/connectors/ai.koppar.app/koppar/badges/score.svg)](https://glama.ai/mcp/connectors/ai.koppar.app/koppar)
  🔓 - Design a KiCad PCB from a prompt: parts, schematic checks, routing, KiCad DRC, Gerbers. Free key for tool calls.
- [Launch Ready](https://uselaunchready.com) `https://uselaunchready.com/api/mcp`
  [![Launch Ready MCP connector](https://glama.ai/mcp/connectors/io.github.ochodigits/launch-ready/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ochodigits/launch-ready)
  🔐 - Deterministic pre-launch website QA: scan a URL, get a readiness score and launch blockers with evidence.
- [Loadster](https://loadster.com/manual/ai-agents/) `https://api.loadster.com/mcp`
  [![Loadster MCP connector](https://glama.ai/mcp/connectors/com.loadster/loadster-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.loadster/loadster-mcp)
  🔐 - Run load tests and synthetic monitors, including Playwright scripts, and analyze results.
- [MCP Checkup](https://mcpcheckup.com) `https://mcpcheckup.com/mcp`
  [![MCP Checkup MCP connector](https://glama.ai/mcp/connectors/com.mcpcheckup/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.mcpcheckup/mcp)
  🔓 - Look up, check and monitor public MCP servers before connecting, with signed attestations.
- [MemorySync Documentation](https://docs.memorysync.io/mcp/overview) `https://docs.memorysync.io/mcp`
  [![MemorySync Docs MCP connector](https://glama.ai/mcp/connectors/io.memorysync/docs/badges/score.svg)](https://glama.ai/mcp/connectors/io.memorysync/docs)
  🔓 - Search and read MemorySync's API, SDK and integration docs.
- [Metabind Banking Assistant (demo)](https://www.metabind.ai) `https://mcp.metabind.ai/IgJH0BzIn4LlfnCbcDc7/projects/GLbHk5i3GLlIYcF63XFl`
  [![Metabind Banking Assistant MCP connector](https://glama.ai/mcp/connectors/ai.metabind/banking-assistant/badges/score.svg)](https://glama.ai/mcp/connectors/ai.metabind/banking-assistant)
  🔓 - Demo MCP App with sample finance data: net worth, spending, and subscriptions as interactive UI cards.
- [Metabind Docs](https://docs.metabind.ai) `https://docs.metabind.ai/mcp`
  [![Metabind Docs MCP connector](https://glama.ai/mcp/connectors/ai.metabind/docs/badges/score.svg)](https://glama.ai/mcp/connectors/ai.metabind/docs)
  🔓 - Search and read the Metabind docs: MCP Apps, BindJS, the SDKs, the CLI, and the APIs.
- [Model Tested](https://modeltested.com/mcp/) `https://modeltested.com/mcp`
  [![Model Tested MCP connector](https://glama.ai/mcp/connectors/com.modeltested/llm-benchmarks/badges/score.svg)](https://glama.ai/mcp/connectors/com.modeltested/llm-benchmarks)
  🔓 - Independent test scores for open-weight LLMs: find the best model for your GPU or Mac, compare models.
- [mumo](https://mumo.chat) `https://mumo.chat/api/mcp`
  [![mumo MCP connector](https://glama.ai/mcp/connectors/chat.mumo/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/chat.mumo/mcp)
  🔓 - Ask Claude, GPT, Grok and more, then see where their answers agree and where they challenge each other.
- [NAIF Gravity](https://naifgravity.com/) `https://naifgravity.com/mcp`
  [![NAIF Gravity MCP connector](https://glama.ai/mcp/connectors/io.github.naief9961-tech/naif-fixgraph/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.naief9961-tech/naif-fixgraph)
  🔓 - Diagnose MCP, x402, API auth and webhook failures, then request bounded repair through the existing NAIF service.
- [naxytra](https://naxytra.com/agents) `https://xytara-mcp-executor.onrender.com/mcp`
  [![naxytra MCP connector](https://glama.ai/mcp/connectors/com.naxytra/xytara-mcp-executor/badges/score.svg)](https://glama.ai/mcp/connectors/com.naxytra/xytara-mcp-executor)
  🔓 - Deterministic EVM/crypto, x402 and text tools (hashing, ABI, EIP-712, Merkle); pay per call in USDC on Base.
- [NoMac](https://nomac.app) `https://mcp.nomac.app/mcp`
  [![NoMac MCP connector](https://glama.ai/mcp/connectors/app.nomac/nomac/badges/score.svg)](https://glama.ai/mcp/connectors/app.nomac/nomac)
  🔐 - Real cloud Macs with Xcode: start one, run commands, build and test iOS apps, ship to TestFlight.
- [Offline Protocol](https://www.offlineprotocol.com/docs/tools/overview) `https://mcp.offlineprotocol.com/public/mcp`
  [![Offline Protocol MCP connector](https://glama.ai/mcp/connectors/com.offlineprotocol/hosted/badges/score.svg)](https://glama.ai/mcp/connectors/com.offlineprotocol/hosted)
  🔓 - Find Offline Protocol SDK packages, integration guides and workflows for apps that keep working without the internet.
- [Omnara](https://www.omnara.com) `https://app.omnara.com/mcp`
  [![Omnara MCP connector](https://glama.ai/mcp/connectors/com.omnara/omnara/badges/score.svg)](https://glama.ai/mcp/connectors/com.omnara/omnara)
  🔐 - Launch AI agents on any model and machine, message them, read their events, and approve their tool calls.
- [Omniyond](https://omniyond.com/#mcp) `https://omniyond.com/mcp`
  [![Omniyond MCP connector](https://glama.ai/mcp/connectors/com.omniyond/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.omniyond/mcp)
  🔑 - Schedule HTTP calls, screenshots, PDFs, OG images, QR codes, short links and page extract on one API key.
- [OpenRouter](https://openrouter.ai) `https://mcp.openrouter.ai/mcp`
  [![OpenRouter MCP connector](https://glama.ai/mcp/connectors/ai.openrouter.mcp/open-router/badges/score.svg)](https://glama.ai/mcp/connectors/ai.openrouter.mcp/open-router)
  🔐 - Look up OpenRouter model metadata and pricing, and run completions.
- [OtaKit](https://otakit.app) `https://console.otakit.app/mcp`
  [![OtaKit MCP connector](https://glama.ai/mcp/connectors/io.github.OtaKit/otakit/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.OtaKit/otakit)
  🔐 - Ship over-the-air updates for Capacitor apps: publish releases with approval, control rollouts, read health, revert.
- [Pandus Accessibility](https://pandus.online/en/accessibility-mcp-server) `https://pandus.online/mcp`
  [![Pandus Accessibility MCP connector](https://glama.ai/mcp/connectors/online.pandus/accessibility/badges/score.svg)](https://glama.ai/mcp/connectors/online.pandus/accessibility)
  🔓 - Explains WCAG 2.2 accessibility rules for free; with an account, what to fix on your sites and new checks.
- [OverlayQA](https://overlayqa.com/mcp/) `https://api.overlayqa.com/mcp`
  [![OverlayQA MCP connector](https://glama.ai/mcp/connectors/com.overlayqa/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.overlayqa/mcp)
  🔐 - Runs accessibility, contrast and design-token audits on any URL and files QA issues in OverlayQA.
- [PartReel](https://partreel.com) `https://mcp.partreel.com/mcp`
  🔓 - Search and fetch 21k+ verified KiCad parts with symbol, footprint and 3D model for PCB design; CC-BY-4.0.
- [PDFOven](https://pdfoven.com) `https://pdfoven.com/mcp`
  [![PDFOven MCP connector](https://glama.ai/mcp/connectors/com.pdfoven/pdfoven/badges/score.svg)](https://glama.ai/mcp/connectors/com.pdfoven/pdfoven)
  🔓 - Render PDFs and PNG images from HTML, Markdown, URLs or Handlebars templates; tools need a free key (100 renders/mo).
- [Perq](https://perq.sh/agents) `https://perq.sh/mcp`
  [![Perq MCP connector](https://glama.ai/mcp/connectors/sh.perq/perq/badges/score.svg)](https://glama.ai/mcp/connectors/sh.perq/perq)
  🔓 - Find verified free AI credits, free tiers and startup programs, each with a source link and last-verified date.
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
- [Proxlai](https://proxlai.com) `https://proxlai.com/api/mcp`
  [![Proxlai MCP connector](https://glama.ai/mcp/connectors/com.proxlai/proxlai/badges/score.svg)](https://glama.ai/mcp/connectors/com.proxlai/proxlai)
  🔓 - Look up and compare verified, dated prices for 231 AI APIs in 38 markets, ranked in one unit per market.
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
- [RepoAlerts](https://repoalerts.com/mcp) `https://repoalerts.com/mcp`
  [![RepoAlerts MCP connector](https://glama.ai/mcp/connectors/com.repoalerts/repo-alerts/badges/score.svg)](https://glama.ai/mcp/connectors/com.repoalerts/repo-alerts)
  🔓 - Rising GitHub repos with fake stars filtered out: search, trending, repo pages and alternatives.
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
- [Screwtape.ai](https://screwtape.ai) `https://screwtape.ai/mcp`
  [![Screwtape.ai MCP connector](https://glama.ai/mcp/connectors/ai.screwtape/screwtape/badges/score.svg)](https://glama.ai/mcp/connectors/ai.screwtape/screwtape)
  🔓 - Pass, fail, or retry verdicts on agent output, plus multi-agent consensus scoring and false-consensus risk.
- [Settlens](https://settlens.com) `https://settlens.com/mcp`
  [![Settlens MCP connector](https://glama.ai/mcp/connectors/com.settlens/settlens/badges/score.svg)](https://glama.ai/mcp/connectors/com.settlens/settlens)
  🔓 - Evaluate x402 V2 payment requirements against spending policies, without signing or sending payments.
- [Show It Works](https://showitworks.app) `https://showitworks.app/api/mcp`
  [![Show It Works MCP connector](https://glama.ai/mcp/connectors/app.showitworks/show-it-works/badges/score.svg)](https://glama.ai/mcp/connectors/app.showitworks/show-it-works)
  🔓 - Public tool discovery; uploading verification videos and sharing viewer links require an API key.
- [sinatra.dev](https://www.sinatra.dev) `https://api.sinatra.dev/v1/mcp`
  [![sinatra.dev MCP connector](https://glama.ai/mcp/connectors/dev.sinatra/sinatra/badges/score.svg)](https://glama.ai/mcp/connectors/dev.sinatra/sinatra)
  🔐 - Hosted coding agent: start, follow, reply to and stop tasks that open GitHub pull requests.
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
- [StoreFast](https://storefast.app/docs/mcp) `https://storefast.app/mcp`
  [![StoreFast MCP connector](https://glama.ai/mcp/connectors/io.github.LegendarySpy/storefast/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.LegendarySpy/storefast)
  🔐 - Publish MSIX updates to the Microsoft Store, translate release notes, edit listings, and read downloads and reviews.
- [Supero](https://supero.dev) `https://api.supero.dev/mcp/v1/messages`
  [![Supero MCP connector](https://glama.ai/mcp/connectors/io.github.supero-platform/supero/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.supero-platform/supero)
 🔓 - Define schemas, CRUD, RBAC and one-call deploys for multi-tenant apps from an AI editor; tool calls need a key.
- [Synap](https://synap.linkrra.com) `https://pool.linkrra.com/mcp`
  [![Synap MCP connector](https://glama.ai/mcp/connectors/com.linkrra/synap/badges/score.svg)](https://glama.ai/mcp/connectors/com.linkrra/synap)
  🔓 - OpenAI-compatible inference on open models: list models and prices, estimate cost, run chat billed per token.
- [TechFabric](https://www.techfabric.com) `https://www.techfabric.com/mcp`
  [![TechFabric MCP connector](https://glama.ai/mcp/connectors/com.techfabric/techfabric/badges/score.svg)](https://glama.ai/mcp/connectors/com.techfabric/techfabric)
  🔓 - Search and read TechFabric's Databricks and AI content: blog posts with FAQs, services, case studies.
- [Termalin](https://termal.in) `https://termal.in/mcp`
  [![Termalin MCP connector](https://glama.ai/mcp/connectors/in.termal/termalin-web/badges/score.svg)](https://glama.ai/mcp/connectors/in.termal/termalin-web)
  🔐 - Run commands and read or write files over SSH/SFTP on your enrolled servers.
- [TheySaid](https://www.theysaid.io) `https://ai.theysaid.io/api/mcp`
  [![TheySaid MCP connector](https://glama.ai/mcp/connectors/io.theysaid.ai/they-said/badges/score.svg)](https://glama.ai/mcp/connectors/io.theysaid.ai/they-said)
  🔐 - Search customer feedback and run AI usability tests on any website or design.
- [The Aggregate](https://theaggregate.ai/mcp) `https://theaggregate.ai/mcp`
  [![The Aggregate MCP connector](https://glama.ai/mcp/connectors/ai.theaggregate/the-aggregate/badges/score.svg)](https://glama.ai/mcp/connectors/ai.theaggregate/the-aggregate)
  🔓 - LLM rankings fitted across public benchmarks: leaderboard, model profiles, comparisons and source-linked scores.
- [Toolbox](https://toolbox.allthepossibles.com) `https://toolbox.allthepossibles.com/mcp`
  [![Toolbox MCP connector](https://glama.ai/mcp/connectors/com.allthepossibles/toolbox/badges/score.svg)](https://glama.ai/mcp/connectors/com.allthepossibles/toolbox)
  🔓 - Thirteen small deterministic tools for agent builders, from CLAUDE.md lint to JWT decoding.
- [TidyData Tools](https://developers.tidydata.workers.dev/) `https://tidydata-api.tidydata.workers.dev/mcp`
  [![TidyData Tools MCP connector](https://glama.ai/mcp/connectors/dev.workers.tidydata.tidydata-api/tidy-data-tools/badges/score.svg)](https://glama.ai/mcp/connectors/dev.workers.tidydata.tidydata-api/tidy-data-tools)
  🔓 - Everyday data tools: public holidays, currency rates, time zones, airports, nutrition, QR codes, DNS and WHOIS.
- [ToolForte](https://toolforte.com/mcp) `https://toolforte.com/api/mcp`
  [![ToolForte MCP connector](https://glama.ai/mcp/connectors/io.github.Toinedotcom/toolforte/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Toinedotcom/toolforte)
  🔓 - IBAN/VAT/BSN checks, Dutch tax and dates, cron, regex, conversions and PDF or screenshot rendering.
- [Traffic Parrot](https://trafficparrot.com/ai/agent-trial.html) `https://mcp.trafficparrot.com/`
  [![Traffic Parrot MCP connector](https://glama.ai/mcp/connectors/com.trafficparrot/public/badges/score.svg)](https://glama.ai/mcp/connectors/com.trafficparrot/public)
  🔓 - Traffic Parrot simulates APIs and messaging. Request or withdraw a trial, read docs, send feedback.
- [UI Verify](https://uiverify.ai) `https://uiverify.ai/api/mcp`
  [![UI Verify MCP connector](https://glama.ai/mcp/connectors/ai.uiverify/ui-verify/badges/score.svg)](https://glama.ai/mcp/connectors/ai.uiverify/ui-verify)
  🔓 - Audit a web page for accessibility and layout issues.
- [Use This Skill](https://usethisskill.com) `https://usethisskill.com/mcp`
  [![Use This Skill MCP connector](https://glama.ai/mcp/connectors/com.usethisskill/skills/badges/score.svg)](https://glama.ai/mcp/connectors/com.usethisskill/skills)
  🔓 - Search 1,967 agent skills, read side-by-side proofs, and check any skill for risky patterns.
- [Unblocked](https://getunblocked.com/unblocked-mcp/) `https://getunblocked.com/api/mcpsse`
  [![Unblocked MCP connector](https://glama.ai/mcp/connectors/com.getunblocked/unblocked-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.getunblocked/unblocked-mcp)
  🔐 - Give coding agents organizational context from code, docs, issues, and conversations.
- [Unipile](https://developer.unipile.com/docs/mcp) `https://developer.unipile.com/mcp?branch=v2.0`
  [![Unipile MCP connector](https://glama.ai/mcp/connectors/com.unipile.developer/unipile/badges/score.svg)](https://glama.ai/mcp/connectors/com.unipile.developer/unipile)
  🔓 - Reads and calls the Unipile API for LinkedIn, WhatsApp, Instagram, Telegram, email and calendar from coding agents.
- [UXMachine](https://uxmachine.app/en/agents?via=awesome) `https://uxmachine.app/mcp`
  [![UXMachine MCP connector](https://glama.ai/mcp/connectors/io.github.qtorb/uxmachine/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.qtorb/uxmachine)
  🔐 - Measures your site in a real browser and returns verifiable observations, with evidence and limits.
- [Vibe Shipped](https://vibeshipped.io/agents) `https://vibeshipped.io/api/mcp`
  [![Vibe Shipped MCP connector](https://glama.ai/mcp/connectors/io.github.sorindecu/vibeshipped/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.sorindecu/vibeshipped)
  🔓 - Search sourced, dated facts on AI coding tools, agent harnesses and real apps built with them.
- [VibeFix](https://vibe-fixer.com) `https://vibe-fixer.com/mcp`
  [![VibeFix MCP connector](https://glama.ai/mcp/connectors/com.vibe-fixer/vibefix/badges/score.svg)](https://glama.ai/mcp/connectors/com.vibe-fixer/vibefix)
  🔓 - Triage a broken Lovable, Base44, v0, Bolt or Replit app: the likely cause and the fix.
- [VibeRaven Guides](https://viberaven.dev) `https://viberaven.dev/mcp`
  [![VibeRaven Guides MCP connector](https://glama.ai/mcp/connectors/io.github.ohad6k/viberaven-guides/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ohad6k/viberaven-guides)
  🔓 - Explains VibeRaven findings and returns launch guides and checklists for Vercel + Supabase apps, read-only.
- [Watermelon UI](https://ui.watermelon.sh/developers/mcp) `https://mcp.watermelon.sh/mcp`
  [![Watermelon UI MCP connector](https://glama.ai/mcp/connectors/sh.watermelon/ui/badges/score.svg)](https://glama.ai/mcp/connectors/sh.watermelon/ui)
  🔓 - Search free React, Tailwind and shadcn components, blocks and dashboards and get source plus install commands.
- [wealth-agent](https://wealth-agent.wealthagent-app.workers.dev) `https://wealth-agent.wealthagent-app.workers.dev/mcp`
  [![wealth-agent MCP connector](https://glama.ai/mcp/connectors/io.github.jukky-source/wealth-agent/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.jukky-source/wealth-agent)
  🔓 - Pay-per-call utility tools over x402 plus a free tier: research briefs, CSV cleanup, code review, regex.
- [web3ctx](https://web3ctx.scarai.xyz) `https://mcp.scarai.xyz/mcp`
  [![web3ctx MCP connector](https://glama.ai/mcp/connectors/io.github.FarseenSh/web3ctx/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.FarseenSh/web3ctx)
  🔓 - Version-true web3 context: validated integration recipes, EIPs, ABIs and contract addresses.
- [Webhook Toolkit](https://webhook-toolkit.com) `https://webhook-toolkit.com/mcp`
  [![Webhook Toolkit MCP connector](https://glama.ai/mcp/connectors/io.github.THE-KIPDEV/webhook-toolkit/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.THE-KIPDEV/webhook-toolkit)
  🔓 - Capture, read and replay webhook deliveries, and sign or verify webhook signatures.
- [XF Model Source](https://xfms.xpansion.dev) `https://xfms.xpansion.dev/mcp`
  [![XF Model Source MCP connector](https://glama.ai/mcp/connectors/dev.xpansion/xfms/badges/score.svg)](https://glama.ai/mcp/connectors/dev.xpansion/xfms)
  🔓 - Finds what an AI job needs, shortlists from 450+ OpenRouter models, and tests the best on your tasks.

### 🛒 <a name="e-commerce"></a>E-Commerce

- [3Descu](https://quote.3descu.com/) `https://zzamnvhadwibvafqcfpd.supabase.co/functions/v1/mcp`
  [![3Descu MCP connector](https://glama.ai/mcp/connectors/io.github.cadi27tech/3descu-quote/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.cadi27tech/3descu-quote)
  🔓 - Quote FDM and SLA 3D printing from an ISO 9001:2015 certified EU factory; measures public STL or OBJ links.
- [10ML Perfume Finder](https://10ml.com) `https://mcp.10ml.com/mcp`
  [![10ML Perfume Finder MCP connector](https://glama.ai/mcp/connectors/com.10ml/perfume-finder/badges/score.svg)](https://glama.ai/mcp/connectors/com.10ml/perfume-finder)
  🔓 - The 10ML Fragrance Index for AI assistants: perfume notes, accords, families, similar scents and expert guides.
- [53ON](https://53on.com) `https://53on.com/mcp`
  [![53ON MCP connector](https://glama.ai/mcp/connectors/com.53on/directory/badges/score.svg)](https://glama.ai/mcp/connectors/com.53on/directory)
  🔓 - Find local businesses and professionals by what they do, in Spanish or English, with prices and a quote-and-pay link.
- [402post](https://402post.com) `https://402post.com/mcp`
  [![402post MCP connector](https://glama.ai/mcp/connectors/com.402post/402post/badges/score.svg)](https://glama.ai/mcp/connectors/com.402post/402post)
  🔓 - Classifieds for AI agents: search listings for free, or validate and publish one for $0.03 paid with x402 on Base.
- [AgentXray](https://agentxray.ai) `https://agentxray.ai/api/mcp`
  [![AgentXray MCP connector](https://glama.ai/mcp/connectors/ai.agentxray/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/ai.agentxray/mcp)
  🔐 - Amazon Seller Central and Ads: profit from your own settlement reports, ads judged on net profit, drafts you approve.
- [AMZ Vault](https://www.amz-vault.com) `https://www.amz-vault.com/mcp`
  [![AMZ Vault MCP connector](https://glama.ai/mcp/connectors/com.amz-vault/amz-vault/badges/score.svg)](https://glama.ai/mcp/connectors/com.amz-vault/amz-vault)
  🔐 - Run an Amazon seller brand: profit analytics, PPC, inventory forecasting, listings and staged approvals.
- [Apiguru Amazon Data](https://apiguru.app) `https://mcp.apiguru.app/mcp`
  [![Apiguru Amazon Data MCP connector](https://glama.ai/mcp/connectors/app.apiguru/amazon-data/badges/score.svg)](https://glama.ai/mcp/connectors/app.apiguru/amazon-data)
  🔓 - Live Amazon product, review, search, best-seller, deal, stock and seller data across 23 marketplaces.
- [apMZoomAI](https://www.apmzoom.com) `https://www.apmzoom.com/mcp`
  [![apMZoomAI MCP connector](https://glama.ai/mcp/connectors/com.apmzoom.www/dongdaemun/badges/score.svg)](https://glama.ai/mcp/connectors/com.apmzoom.www/dongdaemun)
  🔓 - Search Dongdaemun (Seoul) wholesale fashion items, new arrivals and stalls by building and floor.
- [Avahit](https://avahit.com) `https://avahit.com/api/mcp`
  [![Avahit MCP connector](https://glama.ai/mcp/connectors/com.avahit/catalog/badges/score.svg)](https://glama.ai/mcp/connectors/com.avahit/catalog)
  🔓 - Search products from brand stores with prices re-checked daily, find alternatives and read price history.
- [BidProwl](https://bidprowl.com/developers) `https://bidprowl.com/api/v1/mcp`
  [![BidProwl MCP connector](https://glama.ai/mcp/connectors/com.bidprowl/bidprowl/badges/score.svg)](https://glama.ai/mcp/connectors/com.bidprowl/bidprowl)
  🔓 - Search live US government surplus auctions from 26 sources, plus sold-price history and a deal score per lot.
- [BirkinBagStock](https://birkinbagstock.com) `https://birkinbagstock.com/mcp`
  [![BirkinBagStock MCP connector](https://glama.ai/mcp/connectors/com.birkinbagstock/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.birkinbagstock/mcp)
  🔓 - Independent Hermès resale index: inventory, market prices, auction calendar and results.
- [Cambridge China Bridge](https://camchinabridge.co.uk) `https://camchinabridge.co.uk/mcp`
  [![Cambridge China Bridge MCP connector](https://glama.ai/mcp/connectors/uk.co.camchinabridge/sourcing/badges/score.svg)](https://glama.ai/mcp/connectors/uk.co.camchinabridge/sourcing)
  🔓 - UK import duty, landed cost, anti-dumping and UK compliance checks for goods from China, plus CNY and freight planning.
- [China Sourcing Audit](https://lu7897859-tech.github.io/doors/sourcing-audit/) `https://x402-stable-door.lu7897859.workers.dev/mcp`
  [![China Sourcing Audit MCP connector](https://glama.ai/mcp/connectors/io.github.lu7897859-tech/china-sourcing-audit/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.lu7897859-tech/china-sourcing-audit)
  🔓 - Verify Chinese suppliers before paying: fake factories, badge fraud, hijacked payments.
- [Code actu](https://codeactu.com/assistants-ia/) `https://codeactu.com/mcp`
  [![Code actu MCP connector](https://glama.ai/mcp/connectors/io.github.Cryptomoon7/codeactu/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Cryptomoon7/codeactu)
  🔓 - French referral codes verified on brands' official pages: rewards, conditions, verification date and source links.
- [Context Window Supply](https://contextwindowsupply.com) `https://contextwindowsupply.com/mcp`
  [![Context Window Supply MCP connector](https://glama.ai/mcp/connectors/com.contextwindowsupply/store/badges/score.svg)](https://glama.ai/mcp/connectors/com.contextwindowsupply/store)
  🔓 - Search 8 merch items for AI builders (tees, hoodies, a sticker sheet), read sizes and prices, and quote US shipping.
- [datawebot](https://www.datawebot.com) `https://mcp.datawebot.com/mcp`
  [![datawebot MCP connector](https://glama.ai/mcp/connectors/com.datawebot/datawebot/badges/score.svg)](https://glama.ai/mcp/connectors/com.datawebot/datawebot)
  🔐 - Product search across online shops worldwide, with every seller's price and a direct link to the product page.
- [Dolphin Industrial Parts](https://dolphinindustrialparts.com/for-ai-agents/) `https://dolphinindustrialparts.com/agent/mcp`
  [![Dolphin Industrial Parts MCP connector](https://glama.ai/mcp/connectors/com.dolphinindustrialparts/parts/badges/score.svg)](https://glama.ai/mcp/connectors/com.dolphinindustrialparts/parts)
  🔓 - Look up OEM brands, models and part numbers for compatible marine and industrial spare parts; read-only, no prices.
- [eglise.shop](https://eglise.shop) `https://eglise-shop-mcp.padbor.workers.dev/mcp`
  [![eglise.shop MCP connector](https://glama.ai/mcp/connectors/shop.eglise/librairie/badges/score.svg)](https://glama.ai/mcp/connectors/shop.eglise/librairie)
  🔓 - Search ~5,500 Christian books (FR/EN), get prices, build a cart and get a secure checkout link.
- [Epinu](https://epinu.ai) `https://api.epinu.ai/api/agent/mcp`
  [![Epinu MCP connector](https://glama.ai/mcp/connectors/ai.epinu/epinu/badges/score.svg)](https://glama.ai/mcp/connectors/ai.epinu/epinu)
  🔓 - Agent-first marketplace for real-world assets: search listings and projects; writes become human-approved proposals.
- [ESEO](https://eseo.su/developers) `https://eseo.su/api/mcp`
  [![ESEO MCP connector](https://glama.ai/mcp/connectors/su.eseo/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/su.eseo/mcp)
  🔓 - SEO score, limits check and AI generation of product cards for Wildberries, Ozon and Yandex Market.
- [FeedShine](https://feedshine.app) `https://feedshine.app/mcp`
  [![FeedShine MCP connector](https://glama.ai/mcp/connectors/au.com.digitaldarts/feedshine/badges/score.svg)](https://glama.ai/mcp/connectors/au.com.digitaldarts/feedshine)
  🔐 - Build Shopify Google Shopping feeds, fix what Merchant Center rejects, and override product fields.
- [haggl.ai](https://www.haggl.ai/protocol) `https://www.haggl.ai/api/mcp`
  [![haggl.ai MCP connector](https://glama.ai/mcp/connectors/ai.haggl/haggl/badges/score.svg)](https://glama.ai/mcp/connectors/ai.haggl/haggl)
  🔓 - Ask a merchant's haggl.ai sales agent for a personalized offer, then hand it to checkout.
- [Hark Tech](https://harktech.co.uk/for-ai-assistants.html) `https://harktech.co.uk/mcp`
  [![Hark Tech MCP connector](https://glama.ai/mcp/connectors/uk.co.harktech/quotes/badges/score.svg)](https://glama.ai/mcp/connectors/uk.co.harktech/quotes)
  🔓 - Price your own STL, 3MF or STEP file, or a Printables/Thingiverse model, for UK 3D printing and get a checkout link.
- [HLN Apparel](https://www.hlnapparel.com) `https://www.hlnapparel.com/api/mcp`
  [![HLN Apparel MCP connector](https://glama.ai/mcp/connectors/com.hlnapparel/clothing-manufacturer/badges/score.svg)](https://glama.ai/mcp/connectors/com.hlnapparel/clothing-manufacturer)
  🔓 - Clothing factory data: garment categories, MOQ, lead times, US HS duty lookup, GSM conversion and quote requests.
- [New Shopify Stores Radar](https://apify.com/prelaunch-radar/new-shopify-stores-pre-launch-radar) `https://mcp.apify.com/?tools=prelaunch-radar/new-shopify-stores-pre-launch-radar`
  [![New Shopify Stores Radar MCP connector](https://glama.ai/mcp/connectors/io.github.yzf75011-ui/prelaunch-radar-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.yzf75011-ui/prelaunch-radar-mcp)
  🔐 - New and pre-launch Shopify stores from public certificate logs: RDAP date, niche, country; no PII.
- [iDevice](https://idevice.com) `https://idevice.com/api/mcp`
  [![iDevice MCP connector](https://glama.ai/mcp/connectors/com.idevice/wearables/badges/score.svg)](https://glama.ai/mcp/connectors/com.idevice/wearables)
  🔓 - Wearable and phone prices, specs, compatibility, release dates and sourced reports for buyers.
- [JENNi Shop Local](https://shop.jennipro.com) `https://shop.jennipro.com/mcp`
  [![JENNi Shop Local MCP connector](https://glama.ai/mcp/connectors/com.jennipro.shop/shop-local/badges/score.svg)](https://glama.ai/mcp/connectors/com.jennipro.shop/shop-local)
  🔓 - Search live US local retail store inventory by ZIP code, check same-day delivery options, and start guest checkouts.
- [Make Parts Now](https://makepartsnow.com/developers) `https://makepartsnow.com/mcp`
  [![Make Parts Now MCP connector](https://glama.ai/mcp/connectors/com.makepartsnow/manufacturing/badges/score.svg)](https://glama.ai/mcp/connectors/com.makepartsnow/manufacturing)
  🔓 - Quote and order custom 3D printed and CNC machined parts from CAD files: SLS, FDM, aluminum and brass, US shipping.
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
- [Nuira](https://nuira.ai) `https://api.nuira.ai/mcp`
  [![Nuira MCP connector](https://glama.ai/mcp/connectors/ai.nuira/nuira/badges/score.svg)](https://glama.ai/mcp/connectors/ai.nuira/nuira)
  🔐 - Profit-aware ecommerce analytics for Shopify brands: revenue, margin, ad spend, ROAS and ranked growth recommendations.
- [OneFindMe](https://onefindme.com) `https://onefindme.com/mcp`
  [![OneFindMe MCP connector](https://glama.ai/mcp/connectors/com.onefindme/search/badges/score.svg)](https://glama.ai/mcp/connectors/com.onefindme/search)
  🔓 - Search AliExpress in any language and get listings with price, rating, orders and a link.
- [OpenShopGraph](https://openshopgraph.com) `https://api.openshopgraph.com/mcp`
  [![OpenShopGraph MCP connector](https://glama.ai/mcp/connectors/com.openshopgraph/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.openshopgraph/mcp)
  🔓 - Source-dated return, shipping and payment facts, trust signals and coupons for about 1,500 online shops.
- [Origine Paris](https://origineparis.com) `https://mcp.origineparis.com/mcp`
  [![Origine Paris MCP connector](https://glama.ai/mcp/connectors/com.origineparis/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.origineparis/mcp)
  🔓 - Paris jewellery house catalogue: recycled 18k gold, lab-grown diamonds, collections and bespoke.
- [Panda Greetings](https://www.pandagreetings.com/ai-assistants) `https://www.pandagreetings.com/mcp/designs`
  [![Panda Greetings MCP connector](https://glama.ai/mcp/connectors/com.pandagreetings/cards/badges/score.svg)](https://glama.ai/mcp/connectors/com.pandagreetings/cards)
  🔓 - Greeting card designs with your message inside, each linking to order it printed and mailed in the US.
- [PedalBro](https://pedalbro.com/mcp) `https://api.pedalbro.com/mcp`
  [![PedalBro MCP connector](https://glama.ai/mcp/connectors/com.pedalbro/pedalbro/badges/score.svg)](https://glama.ai/mcp/connectors/com.pedalbro/pedalbro)
  🔓 - Guitar pedal specs, new and used prices, 90-day price history, review scores, pedalboard checks and buying guides.
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
- [RivalSweeper Signals](https://www.rivalsweeper.com/solutions/signals-api) `https://mcp.rivalsweeper.com/mcp`
  [![RivalSweeper Signals MCP connector](https://glama.ai/mcp/connectors/com.rivalsweeper/signals/badges/score.svg)](https://glama.ai/mcp/connectors/com.rivalsweeper/signals)
  🔓 - 35 eCommerce competitor-intel tools: prices, promos, ads, AI visibility, hiring. In RivalSweeper plans or prepaid key.
- [ScentVerdict](https://scentverdict.com) `https://scentverdict.com/mcp`
  [![ScentVerdict MCP connector](https://glama.ai/mcp/connectors/com.scentverdict/fragrances/badges/score.svg)](https://glama.ai/mcp/connectors/com.scentverdict/fragrances)
  🔓 - Look up fragrances: verdicts, notes, drydowns, similar picks and bottle prices for your country.
- [Sense2](https://sense2.com.au) `https://sense2.com.au/api/mcp`
  🔓 - Search 4,000+ Australian promotional products, get quantity-break quotes, browse categories and case studies.
- [Shortlist Price Index](https://shortlist-mcp.vercel.app) `https://shortlist-mcp.vercel.app/mcp`
  [![Shortlist Price Index MCP connector](https://glama.ai/mcp/connectors/io.github.ies86/shortlist-price-index/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ies86/shortlist-price-index)
  🔓 - Software entry prices and true 3-year cost for web hosting, SEO tools, cloud backup, antivirus and more.
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
- [Undercart](https://undercart.co/docs/mcp) `https://undercart.co/api/mcp`
  [![Undercart MCP connector](https://glama.ai/mcp/connectors/co.undercart/undercart/badges/score.svg)](https://glama.ai/mcp/connectors/co.undercart/undercart)
  🔐 - Research Shopify brands: revenue estimates, installed apps, live ads and captured marketing emails.
- [Vendwiser](https://vendwiser.ai) `https://app.vendwiser.ai/mcp`
  [![Vendwiser MCP connector](https://glama.ai/mcp/connectors/ai.vendwiser/vendwiser/badges/score.svg)](https://glama.ai/mcp/connectors/ai.vendwiser/vendwiser)
  🔐 - Run an eMAG Romania seller account and Oblio invoicing: offers, orders, AWBs, invoices, with approval on every change.
- [Vouchernaut](https://vouchernaut.com/mcp) `https://vouchernaut.com/mcp`
  [![Vouchernaut MCP connector](https://glama.ai/mcp/connectors/com.vouchernaut/deals/badges/score.svg)](https://glama.ai/mcp/connectors/com.vouchernaut/deals)
  🔓 - 13 read-only UK tools for discount codes, product prices/drops, phone/SIM deals, events, parking, software and polls.
- [VRAMGlass](https://vramglass.com/mcp) `https://mcp.vramglass.com/mcp`
  [![VRAMGlass MCP connector](https://glama.ai/mcp/connectors/com.vramglass/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.vramglass/mcp)
  🔐 - GPU, AI workstation and DDR4/DDR5 asking prices on eBay, Xianyu and Amazon Japan, plus which local LLMs fit which GPU.
- [X402 Git](https://x402git.com) `https://x402git.com/api/mcp`
  [![X402 Git MCP connector](https://glama.ai/mcp/connectors/com.x402git/git-x402/badges/score.svg)](https://glama.ai/mcp/connectors/com.x402git/git-x402)
  🔓 - Search private git repos and agent skills for sale, read each free manifest, then buy with USDC over x402.
- [Zebu Data - Amazon & eBay Product Data](https://apify.com/delicious_zebu) `https://mcp.apify.com/?tools=delicious_zebu/amazon-product-data-scraper,delicious_zebu/amazon-product-details-scraper,delicious_zebu/ebay-product-listing-scraper,delicious_zebu/ebay-product-details-scraper,delicious_zebu/ebay-product-reviews-scraper-with-advanced-filters`
  [![Zebu Data - Amazon & eBay Product Data MCP connector](https://glama.ai/mcp/connectors/io.github.zebudata/ecommerce-product-data/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.zebudata/ecommerce-product-data)
  🔐 - Amazon and eBay search results, product details, prices, variants and seller reviews.
- [Zebu Data - Naver & Coupang Korea Data](https://apify.com/delicious_zebu) `https://mcp.apify.com/?tools=delicious_zebu/naver-shopping-product-scraper,delicious_zebu/naver-product-detail-scraper,delicious_zebu/naver-shopping-reviews-scraper,delicious_zebu/naver-map-search-results-scraper,delicious_zebu/naver-search-scraper,delicious_zebu/coupang-category-products-scraper,delicious_zebu/coupang-reviews-scraper`
  [![Zebu Data - Naver & Coupang Korea Data MCP connector](https://glama.ai/mcp/connectors/io.github.zebudata/korea-commerce-data/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.zebudata/korea-commerce-data)
  🔐 - Korean products, prices, reviews and places from Naver Search, Shopping and Map, plus Coupang.

- [Zineps](https://mcp.zineps.com/docs/login) `https://mcp.zineps.com/mcp`
  [![Zineps MCP connector](https://glama.ai/mcp/connectors/com.zineps.mcp/zineps/badges/score.svg)](https://glama.ai/mcp/connectors/com.zineps.mcp/zineps)
  🔐 - Manage shipments, shipping labels, orders, invoices, and partner operations with a Zineps account.

### 🎓 <a name="education"></a>Education

- [Apex AI Academy](https://apexai.academy/developers/) `https://apexai.academy/mcp`
  [![Apex AI Academy MCP connector](https://glama.ai/mcp/connectors/academy.apexai/apex-ai-academy/badges/score.svg)](https://glama.ai/mcp/connectors/academy.apexai/apex-ai-academy)
  🔓 - Co-Learn with your Agent: AI lessons with Human and Agent views, plus courses, search, news and pricing.
- [DesarrolloMCP](https://desarrollomcp.com/servidor-mcp) `https://desarrollomcp.com/mcp`
  [![DesarrolloMCP MCP connector](https://glama.ai/mcp/connectors/com.desarrollomcp/desarrollomcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.desarrollomcp/desarrollomcp)
  🔓 - Spanish-language MCP course: search and read lessons and articles; optional OAuth sign-in for your progress.
- [GraphChinese](https://graphchinese.com/?utm_source=awesome-remote-mcp-servers&utm_medium=listing&utm_campaign=mcp-directory) `https://graphchinese.com/mcp`
  [![GraphChinese MCP connector](https://glama.ai/mcp/connectors/com.graphchinese/chinese-dictionary-grammar/badges/score.svg)](https://glama.ai/mcp/connectors/com.graphchinese/chinese-dictionary-grammar)
  🔓 - Chinese dictionary and grammar: word lookup, text segmentation with HSK level, 195 grammar points.
- [Laplace’s Mini World](https://world.lapla.si/en/api/) `https://world.lapla.si/mcp`
  [![Laplace’s Mini World MCP connector](https://glama.ai/mcp/connectors/io.github.Keith-CY/laplace-mini-world-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Keith-CY/laplace-mini-world-mcp)
  🔓 - Find and open 100+ interactive 3D science models live in the chat, in Chinese and English; read-only.
- [Moshid](https://moshid.com/connector) `https://moshid.com/api/mcp`
  [![Moshid MCP connector](https://glama.ai/mcp/connectors/com.moshid/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.moshid/mcp)
  🔐 - Arabic AI-at-work guides and Claude skills: search the catalog, read guides, install skills, get one next step.
- [SchoolOrder](https://schoolorder.kr) `https://schoolorder.kr/mcp`
  [![SchoolOrder MCP connector](https://glama.ai/mcp/connectors/io.github.speak-able/schoolorder-catalog/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.speak-able/schoolorder-catalog)
  🔓 - Search AI and edtech subscriptions Korean schools can buy, with term prices, quote links and S2B purchase guides.
- [Speakeroo](https://speakeroo.app/mcp?utm_source=awesome-remote-mcp-servers&utm_medium=listing) `https://mcp.speakeroo.app/mcp`
  [![Speakeroo MCP connector](https://glama.ai/mcp/connectors/app.speakeroo/speaking-coach/badges/score.svg)](https://glama.ai/mcp/connectors/app.speakeroo/speaking-coach)
  🔓 - Speaking coach: feedback on speeches and interview answers from text or audio, plus topics and pronunciation.
- [Spelling Bee Hive](https://www.spellingbeehive.com/spelling-bee-mcp) `https://www.spellingbeehive.com/mcp`
  [![Spelling Bee Hive MCP connector](https://glama.ai/mcp/connectors/com.spellingbeehive/spelling-bee/badges/score.svg)](https://glama.ai/mcp/connectors/com.spellingbeehive/spelling-bee)
  🔓 - Look up spelling bee words with pronunciations, meanings and origins, and run practice rounds at nine levels.
- [Talkfirst](https://talkfirst.io/?utm_source=awesome-remote-mcp&utm_medium=catalog) `https://mcp.talkfirst.io/mcp`
  [![Talkfirst MCP connector](https://glama.ai/mcp/connectors/io.talkfirst/talkfirst/badges/score.svg)](https://glama.ai/mcp/connectors/io.talkfirst/talkfirst)
  🔐 - Speaking practice in English, Polish, Lithuanian and Czech (beta): pronunciation, voice chats, quizzes, audio lessons.
- [Underlayer](https://underlayerhq.com/docs/mcp) `https://underlayerhq.com/api/mcp`
  [![Underlayer MCP connector](https://glama.ai/mcp/connectors/com.underlayerhq/underlayer/badges/score.svg)](https://glama.ai/mcp/connectors/com.underlayerhq/underlayer)
  🔐 - Build, publish and track in-product training courses: screens, learners, completions, certificates and SCORM export.

### 🎓 <a name="education"></a>Education

- [Rotate Pilot](https://rotatepilot.com/developers/mcp) `https://rotatepilot.com/api/mcp`
  [![Rotate Pilot MCP connector](https://glama.ai/mcp/connectors/io.github.Perufitlife/rotate-pilot/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Perufitlife/rotate-pilot)
  🔓 - FAA drone (Part 107) and pilot exam prep: practice questions, readiness diagnostic, METAR/TAF, drone airspace.
- [Szkoły PL (szkoly-mcp)](https://szkoly.compabase.com) `https://szkoly.compabase.com/mcp`
  [![Szkoły PL (szkoly-mcp) MCP connector](https://glama.ai/mcp/connectors/io.github.ContentWriterco/szkoly-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ContentWriterco/szkoly-mcp)
  🔓 - Polish schools and kindergartens from the official register, with per-school exam and matura results vs averages.

### 🌳 <a name="environment"></a>Environment

- [Aevia](https://aeviamodeler.ai/mcp?src=awesome-remote) `https://app.aeviamodeler.ai/api/v1/connector/mcp`
  [![Aevia MCP connector](https://glama.ai/mcp/connectors/ai.aeviamodeler/aevia/badges/score.svg)](https://glama.ai/mcp/connectors/ai.aeviamodeler/aevia)
  🔐 - Life cycle assessment: connect to LCA databases, build product systems and analyze the results.
- [Ambee](https://ambeedata.com) `https://api-mcp-server.ambeedata.com/mcp`
  [![Ambee MCP connector](https://glama.ai/mcp/connectors/com.ambeedata.api-mcp-server/mcp-ambee/badges/score.svg)](https://glama.ai/mcp/connectors/com.ambeedata.api-mcp-server/mcp-ambee)
  🔓 - Weather, air quality, pollen, and other environmental data.
- [Ampworth](https://ampworth.com/developers) `https://ampworth.com/mcp`
  [![Ampworth MCP connector](https://glama.ai/mcp/connectors/com.ampworth/ampworth/badges/score.svg)](https://glama.ai/mcp/connectors/com.ampworth/ampworth)
  🔓 - UK solar PV and heat pump calculators that follow the MCS standards and show their working, plus guides.
- [Boncourant](https://boncourant.fr/agents?utm_source=awesome_mcp&utm_medium=directory&utm_campaign=fr_geo_launch) `https://boncourant.fr/mcp`
  [![Boncourant MCP connector](https://glama.ai/mcp/connectors/fr.boncourant/boncourant/badges/score.svg)](https://glama.ai/mcp/connectors/fr.boncourant/boncourant)
  🔓 - French electricity bill and contract audits, tariff and subscribed-power checks, with versioned, cited methods.
- [Cigo Aircare & Carsafe](https://cigo-mcp-system-wzoy.onrender.com/docs) `https://cigo-mcp-system-wzoy.onrender.com/mcp/`
  [![Cigo Aircare & Carsafe MCP connector](https://glama.ai/mcp/connectors/com.onrender.cigo-mcp-system-wzoy/cigo-aircare-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.onrender.cigo-mcp-system-wzoy/cigo-aircare-mcp)
  🔓 - HVAC filter specifications and power comparisons, vehicle cabin filter matching, and regional air-quality guidance.
- [Criora](https://criora.com) `https://criora.com/mcp`
  [![Criora MCP connector](https://glama.ai/mcp/connectors/com.criora/criora/badges/score.svg)](https://glama.ai/mcp/connectors/com.criora/criora)
  🔓 - Climate and disaster risk for any place: nearby hazards, 7-day weather risk, climate to 2080, country risk, risk map.
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
- [NWS Weather](https://github.com/Thx93/mcp-weather-server) `https://agent-evidence.thx93.dev/weather/mcp`
  [![NWS Weather MCP connector](https://glama.ai/mcp/connectors/io.github.Thx93/weather/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Thx93/weather)
  🔓 - National Weather Service alerts by state code and five-period forecasts by latitude and longitude.
- [Powietrze PL (powietrze-mcp)](https://powietrze.compabase.com) `https://powietrze.compabase.com/mcp`
  [![Powietrze PL (powietrze-mcp) MCP connector](https://glama.ai/mcp/connectors/io.github.ContentWriterco/powietrze-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ContentWriterco/powietrze-mcp)
  🔓 - Air quality in Poland: live GIOŚ measurements (PM2.5, PM10, NO2, O3), smog warnings, 3-day forecast and pollen.
- [ROVE Snow Forecast](https://rove-ski.com/en/ai) `https://rove-ski.com/mcp`
  [![ROVE Snow Forecast MCP connector](https://glama.ai/mcp/connectors/com.rove-ski/snow-forecast/badges/score.svg)](https://glama.ai/mcp/connectors/com.rove-ski/snow-forecast)
  🔐 - Free 15-day snow forecasts and conditions for 667 ski resorts in North America and Japan.
- [SpotWave](https://spotwave.eu/api-docs) `https://spotwave.eu/api/mcp`
  [![SpotWave MCP connector](https://glama.ai/mcp/connectors/eu.spotwave/prices/badges/score.svg)](https://glama.ai/mcp/connectors/eu.spotwave/prices)
  🔓 - Day-ahead electricity prices for 40+ European market zones, all-in with energy tax, grid fees and VAT.
- [Sunrise-Sunset.org](https://sunrise-sunset.org/mcp) `https://api.sunrise-sunset.org/mcp`
  [![Sunrise-Sunset.org MCP connector](https://glama.ai/mcp/connectors/org.sunrise-sunset/sun-times/badges/score.svg)](https://glama.ai/mcp/connectors/org.sunrise-sunset/sun-times)
  🔓 - Sunrise, sunset, twilight, golden hour and moon times for any place and date, worldwide.

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
- [Yungle](https://yungle.co/for/ai-agents) `https://yungle.co/mcp`
  [![Yungle MCP connector](https://glama.ai/mcp/connectors/co.yungle/yungle/badges/score.svg)](https://glama.ai/mcp/connectors/co.yungle/yungle)
  🔐 - Send files to people as download links, list transfers and read download receipts, hosted in the EU.

- [Revdoku](https://revdoku.com) `https://app.revdoku.com/mcp`
  [![Revdoku MCP connector](https://glama.ai/mcp/connectors/com.revdoku/revdoku/badges/score.svg)](https://glama.ai/mcp/connectors/com.revdoku/revdoku)
  🔓 - Discover file storage and incoming email tools; reading or changing private files and mail requires OAuth.
- [Stream Vessel](https://streamvessel.com/mcp) `https://mcp.streamvessel.com`
  [![Stream Vessel MCP connector](https://glama.ai/mcp/connectors/com.streamvessel.mcp/stream-vessel/badges/score.svg)](https://glama.ai/mcp/connectors/com.streamvessel.mcp/stream-vessel)
  🔐 - Browse, search, move and share files in your own S3-compatible buckets (AWS S3, MinIO, IDrive e2).

### 💰 <a name="finance"></a>Finance

- [0s and 1s CIS](https://0sand1s.co.uk/developers) `https://0sand1s.co.uk/mcp`
  [![0s and 1s CIS MCP connector](https://glama.ai/mcp/connectors/uk.co.0sand1s/cis/badges/score.svg)](https://glama.ai/mcp/connectors/uk.co.0sand1s/cis)
  🔓 - UK CIS calculators: deductions, filing deadlines, late return penalties, gross payment test and verification.
- [100pro Token Risk Screen](https://x402.rendraputra.dev/llms.txt) `https://x402.rendraputra.dev/mcp`
  [![100pro Token Risk Screen MCP connector](https://glama.ai/mcp/connectors/dev.rendraputra/100pro-token-risk/badges/score.svg)](https://glama.ai/mcp/connectors/dev.rendraputra/100pro-token-risk)
  🔓 - Pre-trade risk screen for EVM and Solana tokens: honeypots, LP lock, holders; $0.05 via x402.


- [47620 Data API](https://47620.xyz/agents) `https://47620.xyz/mcp`
  [![47620 Data API MCP connector](https://glama.ai/mcp/connectors/xyz.47620/solana-data/badges/score.svg)](https://glama.ai/mcp/connectors/xyz.47620/solana-data)
  🔓 - Pay-per-call data over x402 on Solana, Base and Polygon: prices, liquidity, balances, txs and token analytics.


- [Aave](https://aave.com) `https://mcp.aave.com`
  [![Aave MCP connector](https://glama.ai/mcp/connectors/com.aave.mcp/aave/badges/score.svg)](https://glama.ai/mcp/connectors/com.aave.mcp/aave)
  🔓 - Aave V3 and V4 markets, rates, wallet positions, governance and non-custodial transaction building.
- [Aayat AI](https://aayatai.com) `https://aayatai.com/mcp`
  [![Aayat AI MCP connector](https://glama.ai/mcp/connectors/io.github.faisal-maverick/aayat-ai/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.faisal-maverick/aayat-ai)
  🔓 - Crypto token scam checks, wallet risk, gas, web search and live docs; free daily trial, then USDC credits or x402.
- [Aether](https://aether-x402.vercel.app/llms.txt) `https://aether-x402.vercel.app/mcp`
  [![Aether MCP connector](https://glama.ai/mcp/connectors/io.github.francosmit94-web/aether/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.francosmit94-web/aether)
  🔓 - Base token risk verdicts (honeypot and tax simulation), prices, balances and tx data; pay per call in USDC via x402.
- [Agent Einstein](https://emc2ai.io/mcp) `https://emc2ai.io/api/mcp`
  [![Agent Einstein MCP connector](https://glama.ai/mcp/connectors/io.emc2ai/einstein/badges/score.svg)](https://glama.ai/mcp/connectors/io.emc2ai/einstein)
  🔓 - Crypto and market intelligence: 18 free tools, forecasts, whale flows, token scans; paid tools via credit or x402.


- [Agent Margin Router](https://agentmarginrouter.com) `https://agent-margin-router-production.up.railway.app/mcp`
  [![AgentMarginRouter MCP connector](https://glama.ai/mcp/connectors/io.github.AgentMarginRouter/agent-margin-router/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.AgentMarginRouter/agent-margin-router)
  🔓 - Live gas fees and USD tx costs on Base, Ethereum, Arbitrum, Optimism and Polygon; x402 pay-per-call.
- [Agent Paywire Library](https://agentpaywire.com) `https://mcp.agentpaywire.com/mcp`
  [![Agent Paywire Library MCP connector](https://glama.ai/mcp/connectors/com.agentpaywire/library/badges/score.svg)](https://glama.ai/mcp/connectors/com.agentpaywire/library)
  🔓 - Agent payments library (L402, x402, Lightning, stablecoins): sources, datasets, verified bots, trust checklist.
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
- [Altair](https://altairworld.com/mcp) `https://altairworld.com/mcp`
  [![Altair MCP connector](https://glama.ai/mcp/connectors/com.altairworld/site/badges/score.svg)](https://glama.ai/mcp/connectors/com.altairworld/site)
  🔓 - Full TradingAgents equity research reports by ticker (buy/hold/sell, bull/bear debate), free and read-only.
- [Ankr Agent RPC](https://www.ankr.com/web3-api/agent-rpc/) `https://mcp.ankr.com/rpc`
  [![Ankr Agent RPC MCP connector](https://glama.ai/mcp/connectors/io.github.w3tech/agent-rpc-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.w3tech/agent-rpc-mcp)
  🔓 - Read chain data on 200+ networks and Sui: logs, balances, NFTs, decoded calls. Ankr API key, or pay per call via x402.
- [Antevo Executive Brief](https://antevo.ch/executive/) `https://api.antevo.ch/mcp/executive/mcp`
  [![Antevo Executive Brief MCP connector](https://glama.ai/mcp/connectors/ch.antevo/executive/badges/score.svg)](https://glama.ai/mcp/connectors/ch.antevo/executive)
  🔓 - Daily markets, macro and world-events brief: market regime, themes, risks, catalysts and country drilldowns.
- [Ariadne Nexus](https://ariadnenexus.com/docs/mcp) `https://ariadnenexus.com/mcp`
  [![Ariadne Nexus MCP connector](https://glama.ai/mcp/connectors/com.ariadnenexus/ariadne-nexus-quantitative-engine/badges/score.svg)](https://glama.ai/mcp/connectors/com.ariadnenexus/ariadne-nexus-quantitative-engine)
  🔓 - Sovereign bond valuation, FINRA TRACE debt radar, OFAC screening, and clearing fee modeling with x402 payments.
- [Asiento Uno](https://asientouno.com/mcp) `https://mcp.asientouno.com/mcp`
  [![Asiento Uno MCP connector](https://glama.ai/mcp/connectors/com.asientouno.mcp/asiento-uno-registro-mercantil-de-espana/badges/score.svg)](https://glama.ai/mcp/connectors/com.asientouno.mcp/asiento-uno-registro-mercantil-de-espana)
  🔓 - Spanish company registry (BORME) with grants and procurement per company, linked to sources. Data tools need a free key.
- [AStockEvent](https://astockevent.com/) `https://astockevent.com/mcp/`
  [![AStockEvent MCP connector](https://glama.ai/mcp/connectors/com.astockevent/astockevent/badges/score.svg)](https://glama.ai/mcp/connectors/com.astockevent/astockevent)
  🔓 - Source-linked Chinese A-share filings, penalties, share reductions, regulatory letters and stock halts.
- [ausecon](https://auseconmcp.com) `https://mcp.auseconmcp.com/mcp`
  [![ausecon MCP connector](https://glama.ai/mcp/connectors/io.github.AnthonyPuggs/ausecon-mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.AnthonyPuggs/ausecon-mcp-server)
  🔓 - Read-only Australian economic data from ABS, RBA and APRA, including GDP, inflation and interest rates.
- [Autoview](https://autoview.com/) `https://api.autoview.com/mcp/`
  [![Autoview MCP connector](https://glama.ai/mcp/connectors/io.github.autoview-com/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.autoview-com/mcp)
  🔓 - Trade across 22+ exchanges and brokers; dry-run by default, live trading on Kraken and Crypto.com.
- [Bankrolled.ai Agent Hub](https://bankrolled.ai) `https://bankrolled.ai/mcp`
  [![Bankrolled.ai Agent Hub MCP connector](https://glama.ai/mcp/connectors/ai.bankrolled/bankrolledai-agent-hub/badges/score.svg)](https://glama.ai/mcp/connectors/ai.bankrolled/bankrolledai-agent-hub)
  🔓 - Free, sourced money facts and deposit-insurance schemes for the US, UK, Canada, Australia and NZ; cites bankrolled.com.
- [BackPow PoW Oracle](https://backpow.com/mcp) `https://mcp.backpow.com/mcp`
  [![BackPow PoW Oracle MCP connector](https://glama.ai/mcp/connectors/com.backpow/pow-mining-oracle/badges/score.svg)](https://glama.ai/mcp/connectors/com.backpow/pow-mining-oracle)
  🔓 - Live PoW mining data for 126+ networks: difficulty, hashrate, solo-mining odds, cost of production, hardware profit.
- [Banxico (Banco de México)](https://inakisobera.me/mcp-banxico/) `https://banxico-mcp.duckdns.org/mcp`
  [![Banxico MCP connector](https://glama.ai/mcp/connectors/io.github.nanisadw3/banxico/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.nanisadw3/banxico)
  🔓 - Official Mexican economic data from Banco de México: USD/MXN, INPC inflation, UDIS, TIIE and reserves.
- [Barakah Halal Stock Screen](https://barakahprofits.com) `https://app.barakahprofits.com/mcp`
  [![Barakah Halal Stock Screen MCP connector](https://glama.ai/mcp/connectors/com.barakahprofits.app/halal-screen/badges/score.svg)](https://glama.ai/mcp/connectors/com.barakahprofits.app/halal-screen)
  🔓 - Halal (Sharia) screen for US stocks: AAOIFI-style checks plus the dated history of each verdict change.
- [Base Web3 M2M Hub](https://auditor-x402.onrender.com) `https://auditor-x402.onrender.com/mcp/v1`
  [![Base Web3 M2M Hub MCP connector](https://glama.ai/mcp/connectors/com.onrender.auditor-x402/base-web3-m2m-hub/badges/score.svg)](https://glama.ai/mcp/connectors/com.onrender.auditor-x402/base-web3-m2m-hub)
  🔓 - Live Base Mainnet data: gas, DEX arbitrage, whale tracking, Aave loans, token security; pay per call via x402.
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
- [BLIA — Bank Product Terms](https://www.bliahub.com) `https://mcp.bliahub.com/mcp`
  [![BLIA — Bank Product Terms MCP connector](https://glama.ai/mcp/connectors/com.bliahub/blia-catalogue/badges/score.svg)](https://glama.ai/mcp/connectors/com.bliahub/blia-catalogue)
  🔓 - Bank account terms as banks publish them, dated: fees, waivers, offers. Read-only. Canada today.
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
- [Clear Tape](https://cleartape.ai/mcp) `https://app.cleartape.ai/mcp`
  [![Clear Tape MCP connector](https://glama.ai/mcp/connectors/ai.cleartape/clear-tape/badges/score.svg)](https://glama.ai/mcp/connectors/ai.cleartape/clear-tape)
  🔓 - Exact trading calculators (position size, R:R, expectancy, ATR stop, Kelly), system rules, glossary and lesson search.
- [Coldpine](https://coldpine.io/developers) `https://coldpine.io/api/mcp`
  [![Coldpine MCP connector](https://glama.ai/mcp/connectors/io.coldpine/congress-disclosures/badges/score.svg)](https://glama.ai/mcp/connectors/io.coldpine/congress-disclosures)
  🔓 - US congressional stock trades parsed from House and Senate STOCK Act filings: members, stocks, filings and filing lag.
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
- [CortexCloud](https://api.cortexcloud.org) `https://api.cortexcloud.org/mcp`
  [![CortexCloud MCP connector](https://glama.ai/mcp/connectors/io.github.jonahthan433/cortexcloud/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.jonahthan433/cortexcloud)
  🔓 - Pay-per-call on-chain data: token balances, NFTs, tx history, wallet intel, token risk, whale alerts.
- [date-firme](https://date-firme.dev-box.ro/llms.txt) `https://date-firme.dev-box.ro/mcp`
  [![date-firme MCP connector](https://glama.ai/mcp/connectors/ro.dev-box.date-firme/date-firme/badges/score.svg)](https://glama.ai/mcp/connectors/ro.dev-box.date-firme/date-firme)
  🔓 - Romanian company data (ONRC/ANAF): CUI lookup, financials, KYB risk, CAEN benchmarks, B2B leads; x402 USDC.
- [Datakoot Base Intel](https://datakoot.com/base-intel) `https://base.datakoot.com/mcp`
  [![Datakoot Base Intel MCP connector](https://glama.ai/mcp/connectors/com.datakoot/base-onchain-wallet-tokens/badges/score.svg)](https://glama.ai/mcp/connectors/com.datakoot/base-onchain-wallet-tokens)
  🔓 - Read-only Base network data: ETH and USDC balances, ERC-20 token info, gas price and tx status.
- [Datakoot Economy Intel](https://datakoot.com/economy-intel) `https://economy.datakoot.com/mcp`
  [![Datakoot Economy Intel MCP connector](https://glama.ai/mcp/connectors/com.datakoot/economy-gdp-inflation-unemployment/badges/score.svg)](https://glama.ai/mcp/connectors/com.datakoot/economy-gdp-inflation-unemployment)
  🔓 - World Bank indicators for any country plus US BLS series such as CPI, unemployment and payrolls.
- [Datakoot Filings Intel](https://datakoot.com/filings-intel) `https://filings.datakoot.com/mcp`
  [![Datakoot Filings Intel MCP connector](https://glama.ai/mcp/connectors/com.datakoot/sec-edgar-filings/badges/score.svg)](https://glama.ai/mcp/connectors/com.datakoot/sec-edgar-filings)
  🔓 - SEC EDGAR filings, full-text search, XBRL financials and Form 3/4/5 insider transactions.
- [Datakoot Market Intel](https://datakoot.com/market-intel) `https://market.datakoot.com/mcp`
  [![Datakoot Market Intel MCP connector](https://glama.ai/mcp/connectors/com.datakoot/fx-currency-exchange-rates/badges/score.svg)](https://glama.ai/mcp/connectors/com.datakoot/fx-currency-exchange-rates)
  🔓 - European Central Bank reference FX rates: latest, historical, time series and currency conversion.
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
- [DearmasTrader](https://dearmastrader.com) `https://app.dearmastrader.com/api/mcp`
  [![DearmasTrader MCP connector](https://glama.ai/mcp/connectors/com.dearmastrader/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.dearmastrader/mcp)
  🔐 - Run DCA and grid crypto bots on Binance, Bybit, MEXC, OKX and Bitget and backtest them on years of history.
- [DEBYKO](https://debyko.com) `https://mcp.debyko.com/mcp`
  [![DEBYKO MCP connector](https://glama.ai/mcp/connectors/com.debyko/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.debyko/mcp)
  🔐 - Live and historical crypto derivatives data across venues: books, funding, candles and DQL screens.
- [DeepLedger](https://deepledger.ai) `https://mcp.deepledger.ai/mcp`
  [![DeepLedger MCP connector](https://glama.ai/mcp/connectors/ai.deepledger/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/ai.deepledger/mcp)
  🔐 - AI accountant for QuickBooks: record transactions, run reports, manage AR/AP and close the month.
- [Dexra](https://dexra.dev) `https://api.dexra.dev/mcp`
  [![Dexra MCP connector](https://glama.ai/mcp/connectors/dev.dexra/dexra/badges/score.svg)](https://glama.ai/mcp/connectors/dev.dexra/dexra)
  🔓 - Solana token, launch, wallet, pool, perp and swap checks with ok/caution/avoid verdicts; USDC per call via x402.
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

- [EveryCalc](https://everycalc.xyz) `https://everycalc.xyz/mcp`
  [![EveryCalc MCP connector](https://glama.ai/mcp/connectors/xyz.everycalc/every-calc/badges/score.svg)](https://glama.ai/mcp/connectors/xyz.everycalc/every-calc)
  🔓 - 69 free finance, military, school and everyday calculators as MCP tools, each result linking its web calculator.
- [FactIQ](https://www.factiq.com) `https://api.factiq.com/mcp`
  [![FactIQ MCP connector](https://glama.ai/mcp/connectors/com.factiq.api/factiq/badges/score.svg)](https://glama.ai/mcp/connectors/com.factiq.api/factiq)
  🔐 - Official economic statistics, company filings, earnings calls and market data, with sources cited.
- [Factur-X by Orvel](https://facturx.orvel.dev/docs/mcp/) `https://facturx.orvel.dev/mcp`
  [![Factur-X by Orvel MCP connector](https://glama.ai/mcp/connectors/io.github.LeBorgneAntoine/facturx/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.LeBorgneAntoine/facturx)
  🔓 - Generate, validate and read Factur-X, CII and UBL invoices; free fixed demo, paid document processing.
- [Fair Value Calculator](https://www.fairvalue-calculator.com/mcp) `https://www.fairvalue-calculator.com/mcp`
  [![Fair Value Calculator MCP connector](https://glama.ai/mcp/connectors/com.fairvalue-calculator/fair-value/badges/score.svg)](https://glama.ai/mcp/connectors/com.fairvalue-calculator/fair-value)
  🔐 - Fair value estimates, quality scores and screening for 35,000+ stocks worldwide, plus watchlist and price alerts.
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
- [Firmoscop](https://firmoscop.ro/developers) `https://firmoscop.ro/mcp`
  [![Firmoscop MCP connector](https://glama.ai/mcp/connectors/io.github.CristianFagarasan/firmoscop/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.CristianFagarasan/firmoscop)
  🔐 - Romanian companies from official registries: search, risk verdict by tax ID with cited sources, and prospect lists.
- [FlexYield](https://flexyield.io) `https://flexyield.io/mcp`
  [![FlexYield MCP connector](https://glama.ai/mcp/connectors/io.flexyield/flex-yield-blockchain-rpc-gateway/badges/score.svg)](https://glama.ai/mcp/connectors/io.flexyield/flex-yield-blockchain-rpc-gateway)
  🔓 - RPC gateway for six mainnets with failover: balances, history, ABIs, gas and transactions; x402 pay-per-call.
- [Floatout](https://floatout.xyz) `https://floatout.xyz/api/mcp`
  [![Floatout MCP connector](https://glama.ai/mcp/connectors/xyz.floatout/floatout/badges/score.svg)](https://glama.ai/mcp/connectors/xyz.floatout/floatout)
  🔓 - Read Floatout launch plans, guides, and Hyperliquid builder-fee research.
- [FLOPS Index](https://app.flopsindex.com/i/) `https://app.flopsindex.com/mcp`
  [![FLOPS Index MCP connector](https://glama.ai/mcp/connectors/com.flopsindex.app/flopsindex-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.flopsindex.app/flopsindex-mcp)
  🔓 - Indicative GPU rental reference prices (spot, on-demand, DePIN), refreshed every 6 hours, each with a verify URL.
- [FocusPulse](https://www.focuspulse.pro/mcp-docs.html) `https://mcp.focuspulse.pro/mcp`
  [![FocusPulse MCP connector](https://glama.ai/mcp/connectors/pro.focuspulse/focuspulse/badges/score.svg)](https://glama.ai/mcp/connectors/pro.focuspulse/focuspulse)
  🔓 - India and US news stories linked to listed companies, commodities and indices, with sources.
- [Foresee](https://go-foresee.com) `https://agents.go-foresee.com/mcp`
  [![Foresee MCP connector](https://glama.ai/mcp/connectors/io.github.Foresee-Tech/foresee/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Foresee-Tech/foresee)
  🔓 - Compare live home and auto insurance quotes from carriers' own sites.
- [Fruit Stand](https://fruitstand.dev) `https://api.fruitstand.dev/mcp`
  [![Fruit Stand MCP connector](https://glama.ai/mcp/connectors/dev.fruitstand/fund-returns/badges/score.svg)](https://glama.ai/mcp/connectors/dev.fruitstand/fund-returns)
  🔓 - Historical return data for funds and tickers.
- [FXMacroData](https://fxmacrodata.com/?utm_source=github&utm_medium=referral&utm_campaign=awesome-remote-mcp-servers&utm_content=readme) `https://mcp.fxmacrodata.com`
  [![FXMacroData MCP connector](https://glama.ai/mcp/connectors/io.github.fxmacrodata/fxmacrodata/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.fxmacrodata/fxmacrodata)
  🔓 - Official macro releases and calendars: public USD data, with an optional API key for broader coverage.
- [FxSocket](https://fxsocket.com/docs/mcp) `https://mcp.fxsocket.com/mcp`
  [![FxSocket MCP connector](https://glama.ai/mcp/connectors/com.fxsocket/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.fxsocket/mcp)
  🔑 - Read-only MetaTrader 4 and 5 accounts: balances, open positions, trade history, quotes, symbol specs and candles.
- [Gemral Edge](https://www.gemral.com/edge) `https://mcp.gemral.com/mcp`
  [![Gemral Edge MCP connector](https://glama.ai/mcp/connectors/io.github.gemral-edge/gemral-edge/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.gemral-edge/gemral-edge)
  🔐 - Point-in-time US public records: federal contracts, congressional and insider trades, lobbying, tied to tickers.
- [Global FinReg](https://www.globalfinreg.com) `https://api2.globalfinreg.com/mcp`
  [![Global FinReg MCP connector](https://glama.ai/mcp/connectors/com.globalfinreg/lei/badges/score.svg)](https://glama.ai/mcp/connectors/com.globalfinreg/lei)
  🔓 - Look up LEIs in the global LEI register; renew, transfer and register LEIs with a Global FinReg account.
- [GlobalEntity](https://www.globalentityapi.com) `https://www.globalentityapi.com/mcp`
  [![GlobalEntity MCP connector](https://glama.ai/mcp/connectors/com.globalentityapi/company-data/badges/score.svg)](https://glama.ai/mcp/connectors/com.globalentityapi/company-data)
  🔐 - Official company data from 66 business registers: search, VAT/EORI/LEI checks, ownership, insolvency, sanctions.
- [Gloom](https://gloom.sh/docs/mcp) `https://api.gloom.sh/mcp`
  [![Gloom MCP connector](https://glama.ai/mcp/connectors/sh.gloom.api/gloom-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/sh.gloom.api/gloom-mcp)
  🔐 - US stock research: real-time quotes, financials, options flow, SEC filings, 13F, macro and news; tools need a paid plan.
- [GrantIQ](https://mcp.grantiq.us) `https://mcp.grantiq.us/mcp/`
  [![GrantIQ MCP connector](https://glama.ai/mcp/connectors/io.github.bch1212/mcp-grantiq/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.bch1212/mcp-grantiq)
  🔓 - Search Grants.gov opportunities, SAM.gov contracts, agencies, deadlines, matches, and federal award history.
- [Grey Ridge](https://x402-data-api.sigrunner.workers.dev) `https://x402-data-api.sigrunner.workers.dev/mcp`
  [![Grey Ridge MCP connector](https://glama.ai/mcp/connectors/ai.greyridgesignals/tech-risk/badges/score.svg)](https://glama.ai/mcp/connectors/ai.greyridgesignals/tech-risk)
  🔓 - Pre-trade safety gate for Base tokens: GO/HOLD/BLOCK verdicts, honeypot and tax checks; pay per call in USDC via x402.
- [GROUNDTRUTH](https://groundtruths.xyz) `https://api.groundtruths.xyz/mcp`
  [![GROUNDTRUTH MCP connector](https://glama.ai/mcp/connectors/xyz.groundtruths/groundtruth/badges/score.svg)](https://glama.ai/mcp/connectors/xyz.groundtruths/groundtruth)
  🔓 - Pump.fun and Robinhood Chain memecoin outcomes and creator records; 5 free calls a day, then x402.
- [HEY Research Lab](https://heyresearch.xyz/developers/agents) `https://heyresearch.xyz/mcp`
  [![HEY Research Lab MCP connector](https://glama.ai/mcp/connectors/io.github.hey-research-lab/hey-research/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.hey-research-lab/hey-research)
  🔓 - Builder research for Robinhood Chain: which projects are still building and what they shipped, each with its source.
- [HKEx Filings](https://hkex-listco-updates.ascent-partners.com/live-mcp/) `https://hkex-listco-updates.ascent-partners.com/api/mcp`
  [![HKEx Filings MCP connector](https://glama.ai/mcp/connectors/io.github.simonplmak-cloud/hkex-filings/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.simonplmak-cloud/hkex-filings)
  🔓 - Search 25+ years of Hong Kong Stock Exchange filings, browse facets and extract document text; read-only.
- [Hong Kong Insurance Connect](https://buyhongkonginsurance.com) `https://buyhongkonginsurance.com/mcp`
  [![Hong Kong Insurance Connect MCP connector](https://glama.ai/mcp/connectors/com.buyhongkonginsurance/neutral-data/badges/score.svg)](https://glama.ai/mcp/connectors/com.buyhongkonginsurance/neutral-data)
  🔓 - Sourced Hong Kong insurance facts: fulfillment ratios, VHIS plans, savings and critical illness product data.
- [HowToRomania](https://howtoromania.io) `https://api.howtoromania.io/mcp`
  [![HowToRomania MCP connector](https://glama.ai/mcp/connectors/io.howtoromania/api/badges/score.svg)](https://glama.ai/mcp/connectors/io.howtoromania/api)
  🔓 - Romanian company lookup (ANAF/ONRC), financials, KYB risk, court cases, e-Factura and legislation; 100 free credits.
- [Hundo](https://hundo.finance/connect) `https://hundo.finance/mcp`
  [![Hundo MCP connector](https://glama.ai/mcp/connectors/finance.hundo/hundo/badges/score.svg)](https://glama.ai/mcp/connectors/finance.hundo/hundo)
  🔐 - Personal ledger: net worth, accounts, budgets and IOUs, with drafts you confirm; needs a paid plan.
- [Intangible Asset Valuation](https://intangible-valuation.simonmak.com) `https://intangible-valuation.simonmak.com/api/mcp`
  [![Intangible Asset Valuation MCP connector](https://glama.ai/mcp/connectors/io.github.simonplmak-cloud/intangible-valuation/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.simonplmak-cloud/intangible-valuation)
  🔓 - 124+ deterministic formulas for IP, relief from royalty, MPEEM, purchase price allocation and impairment.
- [InvoiceParser Pro](https://invoiceparserpro.com/ai-assistants) `https://api.invoiceparserpro.com/mcp`
  [![InvoiceParser Pro MCP connector](https://glama.ai/mcp/connectors/com.invoiceparserpro/ipp/badges/score.svg)](https://glama.ai/mcp/connectors/com.invoiceparserpro/ipp)
  🔓 - Read invoices into line items, check the math, and get Excel, CSV or JSON; free trial, no account.
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
- [Jornalo](https://jornalo.com/en/mcp) `https://jornalo.com/api/mcp`
  [![Jornalo MCP connector](https://glama.ai/mcp/connectors/com.jornalo/journal/badges/score.svg)](https://glama.ai/mcp/connectors/com.jornalo/journal)
  🔐 - Futures trading journal: performance, setups, prop-firm drawdown risk, trade tagging and chart screenshots.
- [Kabuken](https://kabuken.intellics.ai) `https://kabuken.intellics.ai/mcp`
  [![Kabuken MCP connector](https://glama.ai/mcp/connectors/io.github.Intellics-ai/kabuken/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Intellics-ai/kabuken)
  🔐 - Japanese listed-company financials, segments and shareholders from EDINET filings, each figure with its source filing.
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
- [KzCalc](https://kzcalc.com/ru/mcp/) `https://mcp.kzcalc.com/mcp`
  [![KzCalc MCP connector](https://glama.ai/mcp/connectors/com.kzcalc/calculators/badges/score.svg)](https://glama.ai/mcp/connectors/com.kzcalc/calculators)
  🔓 - Kazakhstan 2026 salary, tax, benefit and mortgage estimates with primary-source links.
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
- [LPSignal](https://lpsignal.app) `https://api.lpsignal.app/v1/mcp`
  [![LPSignal MCP connector](https://glama.ai/mcp/connectors/app.lpsignal/lpsignal/badges/score.svg)](https://glama.ai/mcp/connectors/app.lpsignal/lpsignal)
  🔐 - DEX liquidity pools ranked by net APR (fees − impermanent loss), range backtests, LP signals and risk alerts.
- [Lorg Check](https://lorglabs.com) `https://api.lorglabs.com/mcp`
  [![Lorg Check MCP connector](https://glama.ai/mcp/connectors/com.lorglabs/lorg-check/badges/score.svg)](https://glama.ai/mcp/connectors/com.lorglabs/lorg-check)
  🔐 - Signed safety checks before money moves on Base and Ethereum: token traps, rug funders, sanctions, address poisoning.
- [Marcel Retraite](https://marcel-retraite.fr) `https://marcel-retraite.fr/mcp`
  [![Marcel Retraite MCP connector](https://glama.ai/mcp/connectors/fr.marcel-retraite/marcel/badges/score.svg)](https://glama.ai/mcp/connectors/fr.marcel-retraite/marcel)
  🔓 - Deterministic, sourced French tax and retirement calculations; information only, not advice.

- [MarketMaster](https://marketmaster.live/developers) `https://api.marketmaster.live/mcp`
  [![MarketMaster MCP connector](https://glama.ai/mcp/connectors/live.marketmaster/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/live.marketmaster/mcp)
  🔓 - Kalshi and Polymarket data: cross-venue matching, arbitrage after fees and whale trades; free key.
- [Mestre Prático & NutriPreço](https://mestrepratico.com.br/developers) `https://mestrepratico.com.br/mcp/v1`
  [![Mestre Prático MCP connector](https://glama.ai/mcp/connectors/io.github.arthursantosmedia-stack/mestrepratico-brazil-prices-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.arthursantosmedia-stack/mestrepratico-brazil-prices-mcp)
  🔓 - Sovereign Brazilian real-economy price & regulatory oracle (ANP fuels, CMED medicines, DIEESE food basket).
- [MetricDuck](https://www.metricduck.com) `https://mcp.metricduck.com/mcp`
  [![MetricDuck MCP connector](https://glama.ai/mcp/connectors/com.metricduck/financial-analysis/badges/score.svg)](https://glama.ai/mcp/connectors/com.metricduck/financial-analysis)
  🔓 - SEC filing data for AI agents: financials, screening, every figure traceable; tool calls need a free sign-in.
- [Midpoint Card Prices](https://www.cardcenteringtool.com/mcp) `https://mcp.cardcenteringtool.com/mcp`
  [![Midpoint Card Prices MCP connector](https://glama.ai/mcp/connectors/com.cardcenteringtool/card-prices/badges/score.svg)](https://glama.ai/mcp/connectors/com.cardcenteringtool/card-prices)
  🔓 - Trading card prices and grading ROI for 1.5M+ Pokémon, TCG and sports cards: raw and PSA 9/10 values, movers.
- [MiningBridge Intelligence](https://intel.miningbridge.in/connect) `https://intel.miningbridge.in/api/mcp`
  [![MiningBridge Intelligence MCP connector](https://glama.ai/mcp/connectors/in.miningbridge/intel/badges/score.svg)](https://glama.ai/mcp/connectors/in.miningbridge/intel)
  🔐 - Critical minerals and rare earths: supply risk, trade flows, export controls, counterparties and patent R&D.
- [MoltNode by Chord](https://moltnode.ag) `https://moltnode.ag/mcp`
  [![MoltNode by Chord MCP connector](https://glama.ai/mcp/connectors/ag.moltnode/molt-node-by-chord/badges/score.svg)](https://glama.ai/mcp/connectors/ag.moltnode/molt-node-by-chord)
  🔓 - Read 31 blockchains over JSON-RPC and get DEX swap quotes with unsigned transactions via Chord.
- [Money Reactor](https://money-reactor.makar52nn2016.workers.dev/) `https://money-reactor.makar52nn2016.workers.dev/mcp`
  [![Money Reactor MCP connector](https://glama.ai/mcp/connectors/io.github.makar52nn-crypto/x402-money-reactor/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.makar52nn-crypto/x402-money-reactor)
  🔓 - Pay-per-call x402 API on Base: token verdicts, research dossiers, crypto prices, weather, AI chat; USDC.
- [More AI](https://accounting.amore.cloud/en/fortnox-mcp/) `https://accounting.amore.cloud/mcp`
  [![More AI MCP connector](https://glama.ai/mcp/connectors/cloud.amore.accounting/fortnox/badges/score.svg)](https://glama.ai/mcp/connectors/cloud.amore.accounting/fortnox)
  🔐 - Fortnox (Swedish accounting): read invoices, ledger, VAT and reports; changes only after the user approves.
- [Mortgage Tools by Jenny](https://jenny.mortgage/mortgage-tools/) `https://mcp.jenny.mortgage/mcp`
  [![Mortgage Tools by Jenny MCP connector](https://glama.ai/mcp/connectors/mortgage.jenny/jenny-mortgage-tools/badges/score.svg)](https://glama.ai/mcp/connectors/mortgage.jenny/jenny-mortgage-tools)
  🔓 - Canadian mortgage calculators in CAD: renewal offers, extra payments, break or stay, debt consolidation.

- [MORVS](https://morvs.ai/api/mcp/) `https://api.morvs.ai/mcp`
  [![MORVS MCP connector](https://glama.ai/mcp/connectors/io.github.morvs-ai/morvs/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.morvs-ai/morvs)
  🔓 - Source-linked US public records: SEC filings, FDA recalls, federal enforcement, sanctions and debarment indexes.
- [NakamotoNotes Bitcoin Barometer](https://nakamotonotes.com/open) `https://nakamotonotes.com/mcp`
  [![NakamotoNotes Bitcoin Barometer MCP connector](https://glama.ai/mcp/connectors/com.nakamotonotes/barometer/badges/score.svg)](https://glama.ai/mcp/connectors/com.nakamotonotes/barometer)
  🔓 - Bitcoin Barometer heat score, BTC price, on-chain and sentiment indicators, and daily history since 2014.
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
- [OpenFinance](https://openfinance.tech/agents) `https://api.openfinance.tech/agent/mcp`
  [![OpenFinance MCP connector](https://glama.ai/mcp/connectors/tech.openfinance/trading/badges/score.svg)](https://glama.ai/mcp/connectors/tech.openfinance/trading)
  🔐 - Easy trading for AI agents: crypto and stock perps, Polymarket, swaps, bridges and token launches.
- [OptimistFi](https://optimistfi.com/mcp) `https://mcp.optimistfi.com/mcp`
  [![OptimistFi MCP connector](https://glama.ai/mcp/connectors/com.optimistfi/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.optimistfi/mcp)
  🔓 - Perpetual futures on 40 venues, 21 prop firms' rules and prices, and SEC-sourced theses on 6,100+ US stocks.
- [OptionsAhoy](https://optionsahoy.com/for-agents) `https://optionsahoy.com/mcp`
  [![OptionsAhoy MCP connector](https://glama.ai/mcp/connectors/io.github.AlvisoOculus/optionsahoy-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.AlvisoOculus/optionsahoy-mcp)
  🔓 - US equity-comp tax math: ISO/AMT exercise plans, RSU and NSO sell-or-hold, QSBS, hedges, cash-goal sell plans.
- [Optionscanner](https://optionscanner.ai/learn/mcp) `https://optionscanner.ai/mcp`
  [![Optionscanner MCP connector](https://glama.ai/mcp/connectors/ai.optionscanner/optionscanner/badges/score.svg)](https://glama.ai/mcp/connectors/ai.optionscanner/optionscanner)
  🔓 - Price any options trade with up to eight legs, what-if scenarios on price, time and volatility, and the Learn library.
- [Oxaide](https://oxaide.com/agents) `https://oxaide.com/mcp`
  [![Oxaide MCP connector](https://glama.ai/mcp/connectors/io.github.leewenjie/oxaide/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.leewenjie/oxaide)
  🔓 - Cited Singapore company research (ACRA/URA/GeBIZ) at S$49/390/1500 per job.
- [PayGuard](https://api.youraitools.co/payguard/) `https://api.youraitools.co/payguard/mcp`
  [![PayGuard MCP connector](https://glama.ai/mcp/connectors/co.youraitools/payguard/badges/score.svg)](https://glama.ai/mcp/connectors/co.youraitools/payguard)
  🔓 - Checks crypto addresses against the US Treasury OFAC SDN list; free yes/no preview, entity details paid via x402.
- [pdata](https://pdata.world/agents) `https://api.pdata.world/mcp`
  [![pdata MCP connector](https://glama.ai/mcp/connectors/world.pdata/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/world.pdata/mcp)
  🔓 - Prices, 24h volume, movers and results for prediction markets on Polymarket, Kalshi and six more venues.
- [Plaid](https://plaid.com) `https://api.dashboard.plaid.com/mcp/sse`
  🔑 - Query Plaid dashboard data for connected financial accounts.
- [PMWallets](https://pmwallets.com/ai-agents) `https://api.pmwallets.com/mcp`
  [![PMWallets MCP connector](https://glama.ai/mcp/connectors/io.github.polymarketwallets/pmwallets/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.polymarketwallets/pmwallets)
  🔐 - Polymarket traders ranked by realized PnL, with their records, live fills and past trades as daily files.
- [Polish Company Financials (Compabase)](https://compabase.com/docs/mcp/) `https://compabase.com/api/mcp/financials`
  [![Polish Company Financials (Compabase) MCP connector](https://glama.ai/mcp/connectors/io.github.ContentWriterco/polish-company-financials/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ContentWriterco/polish-company-financials)
  🔓 - Financial statements of Polish companies (KRS): revenue, profit, assets, industry rankings and sector benchmarks.
- [Priors](https://priors.trade) `https://mcp.priors.trade/mcp`
  [![Priors MCP connector](https://glama.ai/mcp/connectors/io.github.priors-agents/priors-read/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.priors-agents/priors-read)
  🔓 - Credit records and scores of ERC-8004 AI agents on Robinhood Chain, with pool figures and recent loans.
- [pumpdata](https://pumpdata.fun/?utm_source=github&utm_medium=listing&utm_campaign=open) `https://pumpdata.fun/mcp`
  [![pumpdata MCP connector](https://glama.ai/mcp/connectors/fun.pumpdata/pumpdata/badges/score.svg)](https://glama.ai/mcp/connectors/fun.pumpdata/pumpdata)
  🔓 - Every pump.fun trade, ever: base rates, wallet and launch records, and pick-list replays for trading agents over x402.
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
- [Radikabunavi](https://radikabunavi.com/mcp-service) `https://radikabunavi.com/mcp`
  [![Radikabunavi MCP connector](https://glama.ai/mcp/connectors/com.radikabunavi/japan-stock-edinet/badges/score.svg)](https://glama.ai/mcp/connectors/com.radikabunavi/japan-stock-edinet)
  🔐 - Japanese listed-company data from EDINET and TDnet: financials, 6-axis score, ideal price, DCF, screening.
- [Rechnungslotse](https://rechnungslotse.de/mcp) `https://rechnungslotse.de/api/mcp`
  [![Rechnungslotse MCP connector](https://glama.ai/mcp/connectors/de.rechnungslotse/e-rechnung/badges/score.svg)](https://glama.ai/mcp/connectors/de.rechnungslotse/e-rechnung)
  🔓 - German e-invoicing: create, validate and read XRechnung and ZUGFeRD invoices against EN 16931.
- [Regime](https://regimetoken.xyz/api) `https://feed.regimetoken.xyz/mcp`

  
  [![Regime MCP connector](https://glama.ai/mcp/connectors/xyz.regimetoken/regime/badges/score.svg)](https://glama.ai/mcp/connectors/xyz.regimetoken/regime)
  🔓 - Checks crypto trading claims on real price history: leverage liquidations, drawdown, DCA, stop-loss, seasonality.
- [ReportGem 报告驿站](https://www.reportgem.com/mcp.html) `https://www.reportgem.com/mcp`
  [![ReportGem MCP connector](https://glama.ai/mcp/connectors/com.reportgem/report-gem-global-research/badges/score.svg)](https://glama.ai/mcp/connectors/com.reportgem/report-gem-global-research)
  🔓 - Search 16M+ global investment bank reports, filings, earnings-call notes and charts; read cited source passages.

- [RevExOS](https://revexos.com/mcp) `https://revexos.com/api/mcp`
  [![RevExOS MCP connector](https://glama.ai/mcp/connectors/com.revexos/revexos/badges/score.svg)](https://glama.ai/mcp/connectors/com.revexos/revexos)
  🔓 - Quote-to-cash tools: parse invoices and POs, 3-way match, proration, revenue schedules, dunning emails.

- [RWA Data MCP Server](https://glama.ai/mcp/connectors/io.github.daveabear/rwa-data-mcp) `https://rwa-data-mcp.dave-a-bear.workers.dev/mcp`
  [![RWA Data MCP Server MCP connector](https://glama.ai/mcp/connectors/io.github.daveabear/rwa-data-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.daveabear/rwa-data-mcp)
    🔓 - Stablecoin & RWA market data for AI agents: metrics, peg monitoring, prices, claim verification; x402 USDC pay-per-call.



- [Rychlá Hypo](https://rychlahypo.cz/api-dokumentace) `https://rychlahypo.cz/mcp`
  [![Rychlá Hypo MCP connector](https://glama.ai/mcp/connectors/cz.rychlahypo/mortgages/badges/score.svg)](https://glama.ai/mcp/connectors/cz.rychlahypo/mortgages)
  🔓 - Czech mortgages: rates with APRC for 6 major banks, payment comparison and max loan per bank from income.
- [Scrapling x402 Data Store](https://scraplingdata.xyz) `https://scraplingdata.xyz/mcp`
  [![Scrapling x402 Data Store MCP connector](https://glama.ai/mcp/connectors/io.github.bnth09productions-maker/scrapling-x402-store/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.bnth09productions-maker/scrapling-x402-store)
  🔓 - Crypto prices, DeFi TVL and yields, Polymarket odds, token risk and web scraping; pay per call in USDC via x402.
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
- [Signal Band](https://signalband.net/developers?utm_source=github&utm_medium=organic&utm_campaign=dir-punkpeye-remote) `https://signalband.net/mcp`
  [![Signal Band MCP connector](https://glama.ai/mcp/connectors/net.signalband/decision-engines/badges/score.svg)](https://glama.ai/mcp/connectors/net.signalband/decision-engines)
  🔓 - Evidence-weighted decision engines for venture and AI business cases: fund, pilot or stop, by published rules.
- [Signed](https://mcp.signed.com) `https://mcp.signed.com`
  [![Signed MCP connector](https://glama.ai/mcp/connectors/com.signed.mcp/signed/badges/score.svg)](https://glama.ai/mcp/connectors/com.signed.mcp/signed)
  🔐 - An angel investor's portfolio, deal pipeline, and contacts: positions, returns, pitches, notes, and transactions.
- [Signed Investors](https://mcp.signed.com/investors) `https://mcp.signed.com/investors`
  [![Signed Investors MCP connector](https://glama.ai/mcp/connectors/com.signed.mcp/signed-investors/badges/score.svg)](https://glama.ai/mcp/connectors/com.signed.mcp/signed-investors)
  🔓 - Search a public directory of angel investors by sector, check size, or keyword, with no account needed.
- [Signo](https://signo.fi) `https://app.signo.fi/api/mcp`
  [![Signo MCP connector](https://glama.ai/mcp/connectors/fi.signo/signo/badges/score.svg)](https://glama.ai/mcp/connectors/fi.signo/signo)
  🔓 - Drafts AI agents that watch DeFi positions (health factor, LP range, Pendle maturity) for the wallet owner to sign.
- [Silicon Floor](https://siliconfloor.com/docs/mcp) `https://siliconfloor.com/mcp`
  [![Silicon Floor MCP connector](https://glama.ai/mcp/connectors/com.siliconfloor/silicon-floor/badges/score.svg)](https://glama.ai/mcp/connectors/com.siliconfloor/silicon-floor)
  🔓 - Follow the smart money in AI stocks: who owns what, what insiders and hedge funds buy and sell, straight from the SEC.
- [Skavio USDC Payment Verification & Proof MCP](https://www.skavio.eu/x402/) `https://www.skavio.eu/mcp`
  [![Skavio MCP connector](https://glama.ai/mcp/connectors/eu.skavio/paid-micro-apis/badges/score.svg)](https://glama.ai/mcp/connectors/eu.skavio/paid-micro-apis)
  🔓 - Native USDC verification, exact payment matching and evidence PDFs; paid calls use Base USDC via x402.
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
- [Stock Bloc](https://stockbloc.ai.studio) `https://stockbloc.ai.studio/api/mcp/rpc`
  [![Stock Bloc MCP connector](https://glama.ai/mcp/connectors/studio.ai.stockbloc/stock-bloc/badges/score.svg)](https://glama.ai/mcp/connectors/studio.ai.stockbloc/stock-bloc)
  🔓 - Financial market data, SEC/13F intelligence, and quant scores via MCP; $0.01–$0.35/call in USDC on Base via x402 v2.
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
- [Terminal Tax](https://terminal.tax) `https://mcp.terminal.tax/v1/hosted-mcp`
  [![Terminal Tax MCP connector](https://glama.ai/mcp/connectors/tax.terminal/filing/badges/score.svg)](https://glama.ai/mcp/connectors/tax.terminal/filing)
  🔓 - Prepare a 2025 US federal Form 1040 for e-file; the person reviews, signs and pays on one hosted page.
- [Tessera Analytics](https://tesseralytics.dev/mcp-server) `https://tesseralytics.dev/mcp`
  [![Tessera Analytics MCP connector](https://glama.ai/mcp/connectors/dev.tesseralytics/hyperliquid-data/badges/score.svg)](https://glama.ai/mcp/connectors/dev.tesseralytics/hyperliquid-data)
  🔓 - Daily Hyperliquid perp funding, positioning and crowding across every market; tools need a free key.
- [The 07:00 Brief](https://0700.io) `https://api.antevo.ch/mcp/0700/mcp`
  [![The 07:00 Brief MCP connector](https://glama.ai/mcp/connectors/ch.antevo/0700-brief/badges/score.svg)](https://glama.ai/mcp/connectors/ch.antevo/0700-brief)
  🔓 - A daily editorial morning read on markets and the world: what moved, what it means and what to watch today.
- [The River](https://theriver.markets/agents) `https://theriver.markets/mcp`
  [![The River MCP connector](https://glama.ai/mcp/connectors/markets.theriver/the-river/badges/score.svg)](https://glama.ai/mcp/connectors/markets.theriver/the-river)
  🔓 - Tokenized US stocks onchain: issuers, onchain vs US prices, holdings, pre-filled trade links a person signs.
- [The Undesirables TCG Oracle](https://the-undesirables.com) `https://mcp.the-undesirables.com/mcp`
  [![The Undesirables TCG Oracle MCP connector](https://glama.ai/mcp/connectors/io.github.sailorpepe/undesirables-mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.sailorpepe/undesirables-mcp-server)
  🔓 - On-chain oracle for 456K+ trading cards: prices, forecasts, AI grading; free reads, paid via x402.
- [Tickerz](https://tickerz.com/connect) `https://tickerz.com/mcp`
  [![Tickerz MCP connector](https://glama.ai/mcp/connectors/com.tickerz/tickerz/badges/score.svg)](https://glama.ai/mcp/connectors/com.tickerz/tickerz)
  🔓 - Daily indexes of memecoin launches, Kalshi and Polymarket volume and x402 payments, on-chain in Bitcoin.
- [TickFeed](https://tickfeed.pro) `https://api.tickfeed.pro/mcp`
  [![TickFeed MCP connector](https://glama.ai/mcp/connectors/pro.tickfeed/tickfeed/badges/score.svg)](https://glama.ai/mcp/connectors/pro.tickfeed/tickfeed)
  🔐 - Live bid/ask and OHLC candles for 60 forex pairs and 11 metals, with freshness labels and gap reports.
- [Toolrail](https://toolrail.dev) `https://toolrail.dev/mcp`
  [![Toolrail MCP connector](https://glama.ai/mcp/connectors/dev.toolrail/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/dev.toolrail/mcp)
  🔓 - Chile and LATAM data: UF, RUT, business days, FX, VAT for 17 countries, tax units; free daily quota.
- [TraderSpy](https://traderspy.app/mcp) `https://mcp.traderspy.app/mcp`
  [![TraderSpy MCP connector](https://glama.ai/mcp/connectors/app.traderspy/traderspy/badges/score.svg)](https://glama.ai/mcp/connectors/app.traderspy/traderspy)
  🔓 - Crypto futures signals, whale positions on four exchanges, indicators and a screener; free key.
- [TraderWAI](https://traderwai.com) `https://mcp.traderwai.com`
  [![TraderWAI MCP connector](https://glama.ai/mcp/connectors/com.traderwai/traderwai/badges/score.svg)](https://glama.ai/mcp/connectors/com.traderwai/traderwai)
  🔐 - Live charts, strategy backtests and trade execution on MetaTrader, cTrader, TradeLocker, DXtrade, Binance and Bybit.
- [TradeStar Insider](https://www.tradestarinsider.com) `https://mcp.tradestarinsider.com/mcp`
  [![TradeStar Insider MCP connector](https://glama.ai/mcp/connectors/com.tradestarinsider/edgar-insider-signals/badges/score.svg)](https://glama.ai/mcp/connectors/com.tradestarinsider/edgar-insider-signals)
  🔓 - Verify insider-buy, 13D and 13F claims against SEC filings; every record links to its sec.gov source.
- [TradingAgentStack](https://tradingagentstack.com/mcp/) `https://tradingagentstack.com/api/mcp`
  [![TradingAgentStack MCP connector](https://glama.ai/mcp/connectors/io.github.intoApex/tradingagentstack/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.intoApex/tradingagentstack)
  🔓 - Sourced facts on 114 AI trading tools and broker MCPs, incl. who can place orders and what safeguards exist.
- [TradingCalc](https://tradingcalc.io) `https://tradingcalc.io/api/mcp`
  [![TradingCalc MCP connector](https://glama.ai/mcp/connectors/io.github.SKalinin909/tradingcalc/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.SKalinin909/tradingcalc)
  🔓 - Deterministic crypto futures, on-chain risk, and prediction-market math — 31 tools, not AI estimates.
- [TradingMCP](https://tradingmcp.ai) `https://mcp.cryptosieve.com/mcp`
  [![TradingMCP MCP connector](https://glama.ai/mcp/connectors/io.github.atilaahmettaner/tradingview-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.atilaahmettaner/tradingview-mcp)
  🔓 - Market screeners, technical analysis, backtests and charts for crypto, stocks and FX; tool calls need an API key.
- [TronOrb](https://tronorb.com/developers/mcp) `https://tronorb.com/mcp`
  [![TronOrb MCP connector](https://glama.ai/mcp/connectors/com.tronorb/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.tronorb/mcp)
  🔓 - Live TRON data: USDT TRC-20 fees with and without energy, address checks, Tether freezes, dApp and exchange rankings.
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
- [Veqen](https://veqen-app.com/docs/mcp) `https://veqen-app.com/mcp`
  [![Veqen MCP connector](https://glama.ai/mcp/connectors/io.github.Keyveve/veqen/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Keyveve/veqen)
  🔐 - Track AI cost by customer and feature, compare model prices, inspect reconciliation and create budgets.
- [Vérif Entreprise FR](https://api-production-24833.up.railway.app) `https://api-production-24833.up.railway.app/mcp`
  [![Vérif Entreprise FR MCP connector](https://glama.ai/mcp/connectors/app.railway.up.api-production-24833/verif-entreprise-fr/badges/score.svg)](https://glama.ai/mcp/connectors/app.railway.up.api-production-24833/verif-entreprise-fr)
  🔓 - Verify French companies by SIREN: legal status, BODACC insolvency proceedings and RGE certifications, paid via x402.
- [VetAgent](https://vetagent.dev) `https://vetagent.dev/mcp`
  [![VetAgent MCP connector](https://glama.ai/mcp/connectors/dev.vetagent/vetagent/badges/score.svg)](https://glama.ai/mcp/connectors/dev.vetagent/vetagent)
  🔓 - Pre-trade crypto token risk check: sell simulation, taxes, liquidity depth and pair age.
- [W System EU Business Data](https://wsystem.dev/eu-business-data-mcp-server) `https://api.wsystem.dev/mcp/`
  [![W System EU Business Data MCP connector](https://glama.ai/mcp/connectors/io.github.zifengw/eu-business-data-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.zifengw/eu-business-data-mcp)
  🔓 - EU VAT (VIES), EORI, company registers, EU/UN/OFAC/UK sanctions, KYB and e-invoice checks; 20 free calls/day.
- [Web3Juice](https://web3juice.com/mcp) `https://web3juice.com/api/mcp`
  [![Web3Juice MCP connector](https://glama.ai/mcp/connectors/com.web3juice/web3juice/badges/score.svg)](https://glama.ai/mcp/connectors/com.web3juice/web3juice)
  🔓 - DeFi yield data for ~17,000 pools: base vs reward APY, 90-day history and side-by-side pool comparisons.
- [Wellspent](https://find.wellspent.co) `https://api.wellspent.co/mcp`
  [![Wellspent MCP connector](https://glama.ai/mcp/connectors/co.wellspent/advisors/badges/score.svg)](https://glama.ai/mcp/connectors/co.wellspent/advisors)
  🔓 - Search 24,500+ fee-only financial advisors in the US and Canada by location, specialty, and client type.
- [WhereItGoes](https://whereitgoes.money/connect-ai) `https://api.whereitgoes.money/api/mcp`
  [![WhereItGoes MCP connector](https://glama.ai/mcp/connectors/money.whereitgoes/portfolio/badges/score.svg)](https://glama.ai/mcp/connectors/money.whereitgoes/portfolio)
  🔐 - Your own crypto portfolio across exchanges and wallets: holdings, history, FIFO P&L, fees and income. Read-only.
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

- [Wealthnow](https://wealthnow.io/api) `https://mcp.wealthnow.io/mcp`
  [![Wealthnow MCP connector](https://glama.ai/mcp/connectors/io.wealthnow/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.wealthnow/mcp)
  🔐 - Real-time stock and crypto quotes, fundamentals, SEC filings, insider, 13F and congress trades.

- [X1 Wealth](https://x1wealth.com) `https://mcp.x1wealth.com/mcp`
  [![X1 Wealth MCP connector](https://glama.ai/mcp/connectors/com.x1wealth/x1/badges/score.svg)](https://glama.ai/mcp/connectors/com.x1wealth/x1)
  🔐 - Ask about your trusts, entities, policies and documents. Every answer cites a page or declines.

- [x402-agent-data](https://x402-agent.majighufron.workers.dev) `https://x402-agent.majighufron.workers.dev/mcp`
  [![x402-agent-data MCP connector](https://glama.ai/mcp/connectors/io.github.AjiGhufron9999/x402-agent-data/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.AjiGhufron9999/x402-agent-data)
  🔓 - On-chain data: ERC-20 reports, contract DD, pool depth and wallet activity; USDC per call via x402.
- [YABA](https://yaba.day) `https://app.yaba.day/mcp`
  [![YABA MCP connector](https://glama.ai/mcp/connectors/day.yaba/yaba/badges/score.svg)](https://glama.ai/mcp/connectors/day.yaba/yaba)
  🔐 - Family budget for couples: read spending, budget pace, bills and balances; add or fix entries if allowed.

- [Zovo Price Tracker](https://mcp.zovo.one/s/price-tracker) `https://mcp.zovo.one/mcp/price-tracker`
  [![Zovo Price Tracker MCP connector](https://glama.ai/mcp/connectors/io.github.theluckystrike/price-tracker-drop-alert-watch/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.theluckystrike/price-tracker-drop-alert-watch)
  🔓 - Track shop prices over time: snapshot pages, keep a watch list, and get alerts when a target price is hit.

### 🍽️ <a name="food--dining"></a>Food & Dining

- [Agent Chef](https://agentchef.net) `https://agentchef.net/mcp`
  [![Agent Chef MCP connector](https://glama.ai/mcp/connectors/net.agentchef/agent-chef/badges/score.svg)](https://glama.ai/mcp/connectors/net.agentchef/agent-chef)
  🔐 - Weekly family dinner ballot: propose recipes, the household votes, and get a grocery list.
- [ask.recipes](https://ask.recipes) `https://mcp.ask.recipes/mcp`
  [![ask.recipes MCP connector](https://glama.ai/mcp/connectors/recipes.ask/ask-recipes/badges/score.svg)](https://glama.ai/mcp/connectors/recipes.ask/ask-recipes)
  🔐 - Recipe search, ingredient matching, nutrition filters and a private cookbook for any AI agent.
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
- [Loafy](https://loafy.ai/claude) `https://loafy.ai/mcp`
  [![Loafy MCP connector](https://glama.ai/mcp/connectors/ai.loafy/loafy/badges/score.svg)](https://glama.ai/mcp/connectors/ai.loafy/loafy)
  🔓 - Sourdough dough calculators, a bake planner, the open book The Sourdough Framework and a personal bake journal.
- [Pour Picks](https://pourpicks.app/mcp) `https://mcp.pourpicks.app`
  [![Pour Picks MCP connector](https://glama.ai/mcp/connectors/io.github.bguillow-rgb/pour-picks/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.bguillow-rgb/pour-picks)
  🔓 - Bourbon and American whiskey catalog: search, compare, and find similar or cheaper bottles.
- [PourWire](https://pourwire.com/?utm_source=awesome-remote-mcp) `https://pourwire.com/mcp`
  [![PourWire MCP connector](https://glama.ai/mcp/connectors/com.pourwire/pourwire/badges/score.svg)](https://glama.ai/mcp/connectors/com.pourwire/pourwire)
  🔓 - Upcoming restaurant and bar openings in NYC, LA and Texas from liquor license and permit filings.
- [PrepSheet](https://getprepsheet.com) `https://getprepsheet.com/mcp`
  [![PrepSheet MCP connector](https://glama.ai/mcp/connectors/com.getprepsheet/prepsheet/badges/score.svg)](https://glama.ai/mcp/connectors/com.getprepsheet/prepsheet)
  🔓 - Cost recipes, set menu prices, work out UK GP, scale recipes to covers and build kitchen prep lists for chefs.
- [RegPulse Compliance Oracle](https://www.reg-bot.ai/developers) `https://www.reg-bot.ai/api/mcp`
  [![RegPulse Compliance Oracle MCP connector](https://glama.ai/mcp/connectors/ai.reg-bot/compliance-oracle/badges/score.svg)](https://glama.ai/mcp/connectors/ai.reg-bot/compliance-oracle)
  🔓 - Read-only US food license data: verified state food rules, Florida license lookup and renewal dates.
- [RestaurantDoctorAI Profit Check](https://restaurantdoctorai.com/ai-assistants) `https://restaurantdoctorai.com/api/mcp`
  [![RestaurantDoctorAI Profit Check MCP connector](https://glama.ai/mcp/connectors/com.restaurantdoctorai/profit-check/badges/score.svg)](https://glama.ai/mcp/connectors/com.restaurantdoctorai/profit-check)
  🔓 - Free 12-question restaurant profit check that returns a grade and the biggest money leak.
- [Scern](https://scern.app) `https://api.scern.app/mcp`
  [![Scern MCP connector](https://glama.ai/mcp/connectors/app.scern.api/scern/badges/score.svg)](https://glama.ai/mcp/connectors/app.scern.api/scern)
  🔓 - Deterministic US packaged food evaluation: health scores, ingredient flags, FDA recalls, corporate ownership.
- [TableJourney](https://tablejourney.com/agents/) `https://tablejourney.com/mcp`
  [![TableJourney MCP connector](https://glama.ai/mcp/connectors/com.tablejourney/food-travel/badges/score.svg)](https://glama.ai/mcp/connectors/com.tablejourney/food-travel)
  🔓 - Restaurants, markets and street food in 200+ cities, plus food festivals and bookable tours.
- [Ullas Opskrifter](https://ullasopskrifter.dk) `https://ullasopskrifter.dk/mcp`
  [![Ullas Opskrifter MCP connector](https://glama.ai/mcp/connectors/dk.ullasopskrifter/recipes/badges/score.svg)](https://glama.ai/mcp/connectors/dk.ullasopskrifter/recipes)
  🔓 - Search and read Danish recipes, ingredients and categories; read-only.
- [WRDO](https://wrdo.co.za/support/mcp) `https://api.wrdo.co.za/mcp`
  [![WRDO MCP connector](https://glama.ai/mcp/connectors/za.co.wrdo/wrdo/badges/score.svg)](https://glama.ai/mcp/connectors/za.co.wrdo/wrdo)
  🔓 - Find local businesses, price lists and menus in Cape Town and the Western Cape, South Africa. Read-only, no auth.
- [bordeaux.guru](https://bordeaux.guru/mcp-server/) `https://mcp.bordeaux.guru/mcp`
  [![bordeaux.guru MCP connector](https://glama.ai/mcp/connectors/guru.bordeaux/en-primeur/badges/score.svg)](https://glama.ai/mcp/connectors/guru.bordeaux/en-primeur)
  🔓 - First-hand Bordeaux en primeur tasting notes, appellation climate, vine phenology and terroir geodata.
- [NYCfoodie](https://nycfoodie-production.up.railway.app/) `https://nycfoodie-production.up.railway.app/mcp`
  [![NYCfoodie MCP connector](https://glama.ai/mcp/connectors/app.railway.up.nycfoodie-production/nycfoodie/badges/score.svg)](https://glama.ai/mcp/connectors/app.railway.up.nycfoodie-production/nycfoodie)
  🔓 - Editorial NYC restaurant recommendations: search, compare, guides and ratings.

### 🎮 <a name="gaming"></a>Gaming

- [Agentic Kingdoms](https://agentickingdoms.com/agents) `https://mcp.agentickingdoms.com`
  [![Agentic Kingdoms MCP connector](https://glama.ai/mcp/connectors/com.agentickingdoms/agentic-kingdoms/badges/score.svg)](https://glama.ai/mcp/connectors/com.agentickingdoms/agentic-kingdoms)
  🔓 - Strategy MMO where AI agents and people share kingdoms: build a city, join an alliance, fight for the Palace.
- [Centering Lab](https://centeringlab.com/ai/) `https://centeringlab.com/mcp`
  [![Centering Lab MCP connector](https://glama.ai/mcp/connectors/com.centeringlab/centering-lab/badges/score.svg)](https://glama.ai/mcp/connectors/com.centeringlab/centering-lab)
  🔓 - Measure trading card centering from a photo and check PSA, BGS, CGC and SGC centering limits.
- [Chessigma](https://www.chessigma.com/developers/mcp) `https://www.chessigma.com/api/mcp`
  [![Chessigma MCP connector](https://glama.ai/mcp/connectors/com.chessigma/chessigma/badges/score.svg)](https://glama.ai/mcp/connectors/com.chessigma/chessigma)
  🔓 - Chess opening guides, FEN and PGN checks, the daily puzzle, Elo estimates and Chess.com or Lichess game review links.
- [Deckodex](https://deckodex.com/assistant) `https://deckodex.com/mcp`
  [![Deckodex MCP connector](https://glama.ai/mcp/connectors/com.deckodex/deckodex/badges/score.svg)](https://glama.ai/mcp/connectors/com.deckodex/deckodex)
  🔐 - Gundam Card Game cards, prices, tournament meta, and your Deckodex collection and decks.
- [Elsewhere](https://elsewhereagents.com) `https://world.elsewhereagents.com/mcp?ref=awesome-remote`
  [![Elsewhere MCP connector](https://glama.ai/mcp/connectors/com.elsewhereagents/world/badges/score.svg)](https://glama.ai/mcp/connectors/com.elsewhereagents/world)
  🔐 - Persistent world for AI agents: explore, build, trade, research at the College and govern a city.
- [Foundplay](https://foundplay.io/connect) `https://foundplay.io/mcp`
  [![Foundplay MCP connector](https://glama.ai/mcp/connectors/io.foundplay/foundplay/badges/score.svg)](https://glama.ai/mcp/connectors/io.foundplay/foundplay)
  🔓 - Search free indie browser games by genre, phone support or multiplayer, with a link to each game's page.
- [Gamedev Tavern](https://entri.games/ai-agents?lang=en) `https://entri.games/mcp?src=awesome-mcp`
  [![Gamedev Tavern MCP connector](https://glama.ai/mcp/connectors/games.entri/gamedev-tavern/badges/score.svg)](https://glama.ai/mcp/connectors/games.entri/gamedev-tavern)
  🔐 - Gamedev matchmaking: tell the Tavern about you and your studio, post quests and get people and studios that fit.
- [Ludo.ai](https://ludo.ai/api-mcp-integration) `https://mcp.ludo.ai/mcp`
  [![Ludo.ai MCP connector](https://glama.ai/mcp/connectors/ai.ludo/game-assets/badges/score.svg)](https://glama.ai/mcp/connectors/ai.ludo/game-assets)
  🔓 - Game sprites, spritesheet animations, rigged 3D models, video, music, SFX and voices; generation needs a Ludo API key.
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
- [PokerData](https://pokerdata.io/api) `https://pokerdata.io/api/mcp`
  [![PokerData MCP connector](https://glama.ai/mcp/connectors/io.github.hft-studio/pokerdata/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.hft-studio/pokerdata)
  🔓 - GTO poker solver data: NLHE/PLO preflop ranges, postflop strategy, EV. 6-max NL preflop free.
- [SECOND STRIKE](https://secondstrike.io/#/ai) `https://secondstrike-server-zgqvqzdrta-uc.a.run.app/mcp`
  [![SECOND STRIKE MCP connector](https://glama.ai/mcp/connectors/io.github.KyleClouthier/secondstrike/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.KyleClouthier/secondstrike)
  🔓 - Real-time war game for AI agents: command a nation, sign and break pacts, climb a public ladder.
- [Shared Forest](https://sharedforest.com) `https://sharedforest.com/mcp`
  [![Shared Forest MCP connector](https://glama.ai/mcp/connectors/io.github.ArneFfm/shared-forest/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ArneFfm/shared-forest)
  🔓 - Plant one tree a day in a shared illustrated forest, read its stats, and sponsor trees with OAuth.
- [Social Casino Index](https://socialcasinoindex.com/data/) `https://mcp.socialcasinoindex.com/mcp`
  [![Social Casino Index MCP connector](https://glama.ai/mcp/connectors/com.socialcasinoindex/toplist/badges/score.svg)](https://glama.ai/mcp/connectors/com.socialcasinoindex/toplist)
  🔓 - Daily-checked US social casino toplist: signup bonuses, payout times, redemption minimums and sources.
- [SpaceMolt](https://www.spacemolt.com) `https://game.spacemolt.com/mcp/v2`
  [![SpaceMolt MCP connector](https://glama.ai/mcp/connectors/io.github.statico-alt/spacemolt/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.statico-alt/spacemolt)
  🔓 - MMO for AI agents: mine, trade, craft, explore and fight across a 500-system galaxy.
- [SuperDuperBundle](https://superduperbundle.com/tools/api/) `https://superduperbundle.com/mcp`
  [![SuperDuperBundle MCP connector](https://glama.ai/mcp/connectors/io.github.superduperbundle/game-prices/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.superduperbundle/game-prices)
  🔓 - Lowest listed PC game key prices across Steam, GOG and key stores, by name, Steam ID or URL.
- [The Pit](https://pit.benys.dev) `https://pit.benys.dev/mcp`
  [![The Pit MCP connector](https://glama.ai/mcp/connectors/dev.benys/the-pit/badges/score.svg)](https://glama.ai/mcp/connectors/dev.benys/the-pit)
  🔓 - Agent arena where AI agents register, call each other out and play server-refereed chess for ratings, free to play.
- [TickerMint](https://tickermint.cards/developers) `https://api.tickermint.cards/mcp`
  [![TickerMint MCP connector](https://glama.ai/mcp/connectors/io.github.seankarltonlee/tickermint/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.seankarltonlee/tickermint)
  🔓 - Daily trading card prices and history for Pokémon, One Piece, Lorcana, Yu-Gi-Oh, Riftbound and Gundam.
- [Vice City Hub](https://vicecityhub.github.io/vicecityhub/agents.html) `https://lpglkglhjdqnktybksth.supabase.co/functions/v1/agent-api/mcp`
  [![Vice City Hub MCP connector](https://glama.ai/mcp/connectors/io.github.vicecityhub/vicecityhub/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.vicecityhub/vicecityhub)
  🔓 - GTA VI news, GTA RP servers, Web3 domains, merch and crypto donations for AI agents.
- [WagerX](https://wagerx.io/agent-gateway) `https://wagerx.io/mcp`
  [![WagerX MCP connector](https://glama.ai/mcp/connectors/io.wagerx/wager-x-crypto-casinos/badges/score.svg)](https://glama.ai/mcp/connectors/io.wagerx/wager-x-crypto-casinos)
  🔓 - Source-linked gambling regulatory intelligence and real-money crypto casino audit evidence.
- [ZeroMind](https://origozero.ai/mcp-server) `https://origozero.ai/mcp`
  [![ZeroMind MCP connector](https://glama.ai/mcp/connectors/ai.origozero/zeromind/badges/score.svg)](https://glama.ai/mcp/connectors/ai.origozero/zeromind)
  🔐 - Write and run Luau in the Zero 3D engine, place entities, take screenshots and publish a game that plays in a browser.

### 🏋️ <a name="health--fitness"></a>Health & Fitness

- [Bidwell Health](https://bidwellhealth.com/ai-connector) `https://tools.bidwellhealth.com/mcp`
  [![Bidwell Health MCP connector](https://glama.ai/mcp/connectors/com.bidwellhealth/connector/badges/score.svg)](https://glama.ai/mcp/connectors/com.bidwellhealth/connector)
  🔓 - Read-only information on Bidwell Health services, supported states, care limits, pricing, and visit guidance.
- [Biohacking Kompakt](https://biohackingkompakt.de) `https://mcp.biohackingkompakt.de/mcp`
  [![Biohacking Kompakt MCP connector](https://glama.ai/mcp/connectors/de.biohackingkompakt/biohacking-kompakt/badges/score.svg)](https://glama.ai/mcp/connectors/de.biohackingkompakt/biohacking-kompakt)
  🔓 - Evidence ratings for 340+ supplements, peptides and longevity methods, with study sources and podcast (German).
- [Blocks](https://blocks.zone/ai) `https://blocks.zone/api/mcp`
  [![Blocks MCP connector](https://glama.ai/mcp/connectors/zone.blocks/blocks/badges/score.svg)](https://glama.ai/mcp/connectors/zone.blocks/blocks)
  🔐 - Plan and review cycling and running: training calendar, synced rides, sleep and HRV.
- [CI Treasure Hunt](https://citreasurehunt.com/agents) `https://citreasurehunt.com/api/mcp`
  [![CI Treasure Hunt MCP connector](https://glama.ai/mcp/connectors/com.citreasurehunt/ci-treasure-hunt/badges/score.svg)](https://glama.ai/mcp/connectors/com.citreasurehunt/ci-treasure-hunt)
  🔓 - Search Contact Improvisation dance events, teachers, venues and local communities worldwide.
- [JustGains](https://justgains.com) `https://justgains.com/connect/mcp`
  [![JustGains MCP connector](https://glama.ai/mcp/connectors/com.justgains/mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/com.justgains/mcp-server)
  🔐 - Your workouts, lift history and food diary: build and save workouts, check progress, and log meals and bodyweight.
- [Leki PL (leki-mcp)](https://leki.compabase.com) `https://leki.compabase.com/mcp`
  [![Leki PL (leki-mcp) MCP connector](https://glama.ai/mcp/connectors/io.github.ContentWriterco/leki-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ContentWriterco/leki-mcp)
  🔓 - Polish medicines: official refunded drug prices, patient co-payment, cheaper equivalents and leaflets.
- [MedBillAnalyzer](https://medbillanalyzer.com) `https://app.medbillanalyzer.com/mcp/apps?via=awesome_remote`
  [![MedBillAnalyzer MCP connector](https://glama.ai/mcp/connectors/com.medbillanalyzer/medbillanalyzer/badges/score.svg)](https://glama.ai/mcp/connectors/com.medbillanalyzer/medbillanalyzer)
  🔓 - Compares a medical bill with your insurer's EOB and flags mismatches; free scan, $10 per bill for findings and a letter.
- [MoveMate](https://movemate.app/ai) `https://api.movemate.app/mcp`
  [![MoveMate MCP connector](https://glama.ai/mcp/connectors/app.movemate/movemate/badges/score.svg)](https://glama.ai/mcp/connectors/app.movemate/movemate)
  🔐 - Your gym log: training stats, PRs and lift progression, plus workouts you approve scheduled straight into the app.
- [NobetciEczane.org](https://nobetcieczane.org/) `https://nobetcieczane.org/mcp`
  [![NobetciEczane.org MCP connector](https://glama.ai/mcp/connectors/org.nobetcieczane/nobetci-eczane/badges/score.svg)](https://glama.ai/mcp/connectors/org.nobetcieczane/nobetci-eczane)
  🔓 - Today's on-duty pharmacies in all 81 provinces of Türkiye and the TRNC, by district or nearest to a location.
- [Peptide Library](https://peptidelibrary.app/developers/mcp) `https://peptidelibrary.app/mcp`
  [![Peptide Library MCP connector](https://glama.ai/mcp/connectors/app.peptidelibrary/peptide-library/badges/score.svg)](https://glama.ai/mcp/connectors/app.peptidelibrary/peptide-library)
  🔓 - Peptide research profiles with evidence by study type, comparisons, educational search and unit math.
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
- [AaaSagent Templates](https://aaasagent.xyz) `https://aaasagent.xyz/api/v1/mcp`
  [![AaaSagent Templates MCP connector](https://glama.ai/mcp/connectors/xyz.aaasagent/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/xyz.aaasagent/mcp)
  🔓 - Browse and fetch 632 open-source agent templates; bring your own LLM key.
- [ABS · AI Business System](https://www.ucai.net) `https://www.ucai.net/api/agent/mcp`
  [![ABS · AI Business System MCP connector](https://glama.ai/mcp/connectors/net.ucai/abs/badges/score.svg)](https://glama.ai/mcp/connectors/net.ucai/abs)
  🔐 - Lean and operations knowledge base built on DBS: cited answers, tool cards, scheduled plans and diagnoses.
- [AbuzzHive](https://www.abuzzhive.com) `https://www.abuzzhive.com/mcp`
  [![AbuzzHive MCP connector](https://glama.ai/mcp/connectors/com.abuzzhive/abuzzhive/badges/score.svg)](https://glama.ai/mcp/connectors/com.abuzzhive/abuzzhive)
  🔐 - Q&A boards where agents post problems they are stuck on and other agents solve them; search, post, solve, vote.
- [Agents Handbook](https://agentshandbook.com/for-agents) `https://agentshandbook.com/mcp`
  [![Agents Handbook MCP connector](https://glama.ai/mcp/connectors/com.agentshandbook/handbook/badges/score.svg)](https://glama.ai/mcp/connectors/com.agentshandbook/handbook)
  🔓 - Search sourced playbooks for real jobs done with AI agents: prompts, steps, checkpoints, known failures and fixes.
- [AIeph](https://aieph.dev) `https://aieph.dev/mcp`
  [![AIeph MCP connector](https://glama.ai/mcp/connectors/dev.aieph/aieph/badges/score.svg)](https://glama.ai/mcp/connectors/dev.aieph/aieph)
  🔓 - Look up a shared cache of past answers to programming questions.
- [Analytics Legends](https://analyticslegends.ai/mcp-server/) `https://analyticslegends.ai/mcp`
  [![Analytics Legends MCP connector](https://glama.ai/mcp/connectors/ai.analyticslegends/sap-analytics/badges/score.svg)](https://glama.ai/mcp/connectors/ai.analyticslegends/sap-analytics)
  🔓 - SAP AI & analytics market data: consulting firms, day-rate bands, job radar and news, each record citable.
- [Atlas Red](https://atlas-red.com/mind-map-mcp) `https://app.atlas-red.com/mcp`
  [![Atlas Red MCP connector](https://glama.ai/mcp/connectors/com.atlas-red/mind-map/badges/score.svg)](https://glama.ai/mcp/connectors/com.atlas-red/mind-map)
  🔐 - Create and edit mind maps — nodes, links, and subtrees — then export them or render one as an image.
- [Azquo](https://azquo.com) `https://data.azquo.ai/mcp`
  [![Azquo MCP connector](https://glama.ai/mcp/connectors/ai.azquo/azquo/badges/score.svg)](https://glama.ai/mcp/connectors/ai.azquo/azquo)
  🔐 - Shared, auditable memory for multiple agents: hierarchical data whose totals add up and every write is attributed.
- [Bilg](https://app.bilgai.com/docs/connect?ref=mcp-directory) `https://mcp.bilgai.com/mcp`
  [![Bilg MCP connector](https://glama.ai/mcp/connectors/com.bilgai/bilg/badges/score.svg)](https://glama.ai/mcp/connectors/com.bilgai/bilg)
  🔐 - Shared memory for coding agents and their teams: search docs, read and write epics, tasks and decisions.
- [BotGathering](https://botgathering.com) `https://botgathering.com/mcp`
  [![BotGathering MCP connector](https://glama.ai/mcp/connectors/com.botgathering/recipes/badges/score.svg)](https://glama.ai/mcp/connectors/com.botgathering/recipes)
  🔓 - Tested step-by-step playbooks for AI agents: search, follow and report outcomes. Free.
- [bsv.cx](https://bsv.cx) `https://bsv.cx/mcp`
  [![bsv.cx MCP connector](https://glama.ai/mcp/connectors/cx.bsv/bsv-cx/badges/score.svg)](https://glama.ai/mcp/connectors/cx.bsv/bsv-cx)
  🔓 - Timestamp and verify evidence on-chain; let your agent prove what it saw and when.
- [Cloud FinOps by OptimNow](https://pypi.org/project/cloud-finops-mcp/) `https://mcp.optimnow.io/mcp`
  [![Cloud FinOps by OptimNow MCP connector](https://glama.ai/mcp/connectors/io.github.OptimNow/cloud-finops/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.OptimNow/cloud-finops)
  🔓 - Fetches FinOps reference guides and waste-pattern runbooks on cloud and AI cost management; no account needed.
- [coldHat](https://coldhat.f-keys.com) `https://coldhat.f-keys.com/mcp`
  [![coldHat MCP connector](https://glama.ai/mcp/connectors/io.github.vince-gonzalez/coldhat/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.vince-gonzalez/coldhat)
  🔓 - Wear anyone's AI working rules by GitHub username: returns their hat.md and a hat code proving it was read.
- [Continuity](https://continuitywriter.com) `https://continuitywriter.com/mcp`
  [![Continuity MCP connector](https://glama.ai/mcp/connectors/io.github.LAHutchins91/continuity/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.LAHutchins91/continuity)
  🔓 - Remembers your writing project across chats: story bible, characters, timeline and continuity checks.
- [ctxstore](https://ctxstore.ai) `https://mcp.ctxstore.ai/mcp`
  [![ctxstore MCP connector](https://glama.ai/mcp/connectors/ai.ctxstore/ctxstore-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/ai.ctxstore/ctxstore-mcp)
  🔓 - Persistent memory for AI agents: keyed facts, a wake bundle each session, one memory across every model.
- [Detextit](https://www.detextit.com) `https://www.detextit.com/api/mcp`
  [![Detextit MCP connector](https://glama.ai/mcp/connectors/com.detextit.www/detextit/badges/score.svg)](https://glama.ai/mcp/connectors/com.detextit.www/detextit)
  🔓 - Read-only shared agent context with sources and conditions, plus plans for recovering from task constraints.
- [Dexio](https://dexio.wiki) `https://app.dexio.wiki/mcp`
  [![Dexio MCP connector](https://glama.ai/mcp/connectors/wiki.dexio/dexio/badges/score.svg)](https://glama.ai/mcp/connectors/wiki.dexio/dexio)
  🔐 - One wiki all your agents read and write over MCP, with every version kept and the agent behind each change recorded.
- [Digital Garden](https://digitalgarden.si/agents/) `https://mcp.digitalgarden.si/mcp`
  [![Digital Garden MCP connector](https://glama.ai/mcp/connectors/si.digitalgarden.mcp/digital-garden-by-alicia-notes/badges/score.svg)](https://glama.ai/mcp/connectors/si.digitalgarden.mcp/digital-garden-by-alicia-notes)
  🔓 - Search and cite Alicia’s notes on WebGPU, three.js, Houdini, glTF, OpenUSD and AI workflows.
- [docs2mcp](https://docs2mcp.com) `https://mcp.docs2mcp.com/mcp`
  [![docs2mcp MCP connector](https://glama.ai/mcp/connectors/com.docs2mcp/docs2mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.docs2mcp/docs2mcp)
  🔐 - Query your own PDFs and documents, with every answer linking to the exact page and region it came from.
- [Eigma](https://eigma.app) `https://my.eigma.app/api/mcp`
  [![Eigma MCP connector](https://glama.ai/mcp/connectors/app.eigma.my/eigma/badges/score.svg)](https://glama.ai/mcp/connectors/app.eigma.my/eigma)
  🔐 - Files what you learn into a personal wiki and quizzes you before you forget it.
- [emem](https://emem.dev) `https://emem.dev/mcp`
  [![emem MCP connector](https://glama.ai/mcp/connectors/io.github.Vortx-AI/emem/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Vortx-AI/emem)
  🔓 - Elevation, vegetation, flood, fire and air-quality facts for any place, each with a signed receipt.
- [Engram](https://engram.page) `https://mcp.engram.page`
  [![Engram MCP connector](https://glama.ai/mcp/connectors/io.github.engram-app/engram/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.engram-app/engram)
  🔐 - Search, read and edit your Obsidian notes as AI memory, synced to the cloud and reachable with Obsidian closed.
- [Engram - Second Brain](https://engram.rootcause.ro) `https://engram.rootcause.ro/mcp/directory`
  [![Engram - Second Brain MCP connector](https://glama.ai/mcp/connectors/ro.rootcause/engram/badges/score.svg)](https://glama.ai/mcp/connectors/ro.rootcause/engram)
  🔐 - A second brain for Claude: remembers your work, plans your day, encrypted under a key only you hold.
- [FeedNest](https://www.feednest.com) `https://mcp.feednest.com`
  [![FeedNest MCP connector](https://glama.ai/mcp/connectors/com.feednest.mcp/feed-nest/badges/score.svg)](https://glama.ai/mcp/connectors/com.feednest.mcp/feed-nest)
  🔐 - Read and search your RSS feeds and articles, plus save, tag, highlight and add notes on paid plans; OAuth sign-in.
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
- [Hunchful](https://hunchful.io) `https://hunchful.io/mcp`
  [![Hunchful MCP connector](https://glama.ai/mcp/connectors/io.hunchful/hunchful/badges/score.svg)](https://glama.ai/mcp/connectors/io.hunchful/hunchful)
  🔐 - Your AI's inbox and people search: message friends, find people by how they work, knock with consent.
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
- [NotebookLM MCP Server by useapi.net](https://useapi.net/docs/api-gemini-notebook-v1/mcp) `https://api.useapi.net/v1/gemini-notebook/mcp`
  [![NotebookLM MCP Server by useapi.net MCP connector](https://glama.ai/mcp/connectors/net.useapi/gemini-notebook/badges/score.svg)](https://glama.ai/mcp/connectors/net.useapi/gemini-notebook)
  🔐 - NotebookLM (Gemini Notebook) sources, cited chat, podcasts, slides on your Google account. Not affiliated with Google.
- [NoteMCP](https://notemcp.com) `https://notemcp.com/mcp`
  [![NoteMCP MCP connector](https://glama.ai/mcp/connectors/com.notemcp/notemcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.notemcp/notemcp)
  🔐 - Long-term memory from your notes: search, read and edit notes saved by text, voice or share sheet.
- [Notion](https://notion.com) `https://mcp.notion.com/mcp`
  🔐 - Read and write Notion pages, databases, and comments.
- [notepad.page](https://notepad.page) `https://mcp.notepad.page/mcp`
  [![notepad.page MCP connector](https://glama.ai/mcp/connectors/page.notepad/notepad/badges/score.svg)](https://glama.ai/mcp/connectors/page.notepad/notepad)
  🔓 - Publish, recall and update persistent private HTML pages at a personal address; publishing needs OAuth.
- [OnlyMCP](https://only-mcp.com) `https://only-mcp.com/api/mcp`
  [![OnlyMCP MCP connector](https://glama.ai/mcp/connectors/com.only-mcp/onlymcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.only-mcp/onlymcp)
  🔐 - Skills, agents and markdown memory in the cloud, the same in every client, plus a gateway to your other MCP servers.
- [Ontonym](https://www.ontonym.com) `https://mcp.ontonym.com/mcp`
  [![Ontonym MCP connector](https://glama.ai/mcp/connectors/com.ontonym/memory/badges/score.svg)](https://glama.ai/mcp/connectors/com.ontonym/memory)
  🔐 - Give your agents your team's real data: read the shared graph, and propose actions a human approves.
- [OwnerSpec](https://ownerspec.com/mcp-server/) `https://ownerspec.com/mcp`
  [![OwnerSpec MCP connector](https://glama.ai/mcp/connectors/com.ownerspec/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.ownerspec/mcp)
  🔓 - Cited home water treatment answers: diagnose a water problem, size a softener, and match replacement parts.
- [Pairgora](https://pairgora.com) `https://pairgora.com/api/mcp`
  [![Pairgora MCP connector](https://glama.ai/mcp/connectors/io.github.mason0501/pairgora/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.mason0501/pairgora)
  🔓 - Community of human-agent pairs: seek Cards other pairs wrote from real work, store your own, report what worked.
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
- [Renor](https://renor.cloud) `https://mcp.renor.cloud/mcp`
  [![Renor MCP connector](https://glama.ai/mcp/connectors/io.github.patrickpassosb/renor/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.patrickpassosb/renor)
  🔐 - Private memory for your AI agents: save and recall facts and notes across Claude Code, Codex, Cursor and ChatGPT.
- [Rootr](https://rootr.io) `https://rootr.io/mcp`
  [![Rootr MCP connector](https://glama.ai/mcp/connectors/io.github.inspirio-co/rootr-cli/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.inspirio-co/rootr-cli)
  🔐 - Read, search and write team docs, tables, issues and CRM records, with answers citing their source.
- [Scento Perfume API (MCP server)](https://www.scento.com/developers/perfume-mcp-server) `https://www.scento.com/mcp`
  [![Scento Perfume API MCP connector](https://glama.ai/mcp/connectors/com.scento/perfume-compendium/badges/score.svg)](https://glama.ai/mcp/connectors/com.scento/perfume-compendium)
  🔓 - Perfume portraits, raw materials, scent pairings and occasion edits, with a scento.com page on every answer.
- [Sensefold](https://sensefold.app/for-agents) `https://api.sensefold.app/mcp`
  [![Sensefold MCP connector](https://glama.ai/mcp/connectors/app.sensefold/sensefold/badges/score.svg)](https://glama.ai/mcp/connectors/app.sensefold/sensefold)
  🔐 - Search, read and write your saved articles, threads, PDFs, notes and AI chats as Markdown.
- [SlashYear](https://slashyear.com) `https://slashyear.com/mcp`
  [![SlashYear MCP connector](https://glama.ai/mcp/connectors/com.slashyear/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.slashyear/mcp)
  🔓 - Dated historical events, each a verbatim sentence from a cited Wikipedia revision, searchable by year, day or subject.
- [Sooveryn](https://www.sooveryn.com/?utm_source=awesome-remote-mcp&utm_medium=annuaire&utm_campaign=lancement-oct) `https://mcp.sooveryn.com/mcp`
  [![Sooveryn MCP connector](https://glama.ai/mcp/connectors/com.sooveryn/sooveryn/badges/score.svg)](https://glama.ai/mcp/connectors/com.sooveryn/sooveryn)
  🔑 - A team of AI personas sharing a lasting, encrypted memory per project, hosted in France.
- [static.md](https://static.md/agents?ref=awesome-remote) `https://static.md/mcp`
  [![static.md MCP connector](https://glama.ai/mcp/connectors/md.static/static-md/badges/score.svg)](https://glama.ai/mcp/connectors/md.static/static-md)
  🔐 - Markdown notes and Excalidraw whiteboards your agent can read and write, with scoped OAuth and end-to-end encryption.
- [Stele](https://stele-ai.dev) `https://app.stele-ai.dev/api/mcp`
  [![Stele MCP connector](https://glama.ai/mcp/connectors/dev.stele-ai/stele/badges/score.svg)](https://glama.ai/mcp/connectors/dev.stele-ai/stele)
  🔐 - Shared project memory for coding agents: recall and record decisions, lessons and risks, and claim tasks.
- [Synapse Layer](https://synapselayer.org) `https://forge.synapselayer.org/api/mcp`
  [![Synapse Layer MCP connector](https://glama.ai/mcp/connectors/io.github.SynapseLayer/synapse-layer/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.SynapseLayer/synapse-layer)
  🔓 - Persistent encrypted agent memory with semantic recall and cross-agent continuity.
- [The Living Bread](https://mcp.living-bread.org/) `https://mcp.living-bread.org/mcp`
  [![The Living Bread MCP connector](https://glama.ai/mcp/connectors/org.living-bread.mcp/the-living-bread/badges/score.svg)](https://glama.ai/mcp/connectors/org.living-bread.mcp/the-living-bread)
  🔓 - Bible passages with evidence labels, cross references, and real Christian communities near you.
- [Thea](https://thealibrary.org) `https://thealibrary.org/mcp`
  [![Thea MCP connector](https://glama.ai/mcp/connectors/org.thealibrary/thea/badges/score.svg)](https://glama.ai/mcp/connectors/org.thealibrary/thea)
  🔓 - Open, people-curated knowledge library: 1M+ Korean places, people and works, no signup or key.
- [Urantia Papers](https://urantia.dev) `https://api.urantia.dev/mcp`
  [![Urantia Papers MCP connector](https://glama.ai/mcp/connectors/dev.urantia/urantia-papers/badges/score.svg)](https://glama.ai/mcp/connectors/dev.urantia/urantia-papers)
  🔓 - Read and search the Urantia Papers by reference, keyword, or meaning, with named entities and Bible cross-references.
- [UseMyContext](https://usemycontext.ai) `https://mcp.usemycontext.ai/mcp`
  [![UseMyContext MCP connector](https://glama.ai/mcp/connectors/io.github.usemycontext/usemycontext/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.usemycontext/usemycontext)
  🔓 - Your own profile and files as AI context; anonymous access gets metadata only.
- [Vedaword](https://vedaword.com/en/mcp) `https://mcp.vedaword.com`
  [![Vedaword MCP connector](https://glama.ai/mcp/connectors/com.vedaword/library/badges/score.svg)](https://glama.ai/mcp/connectors/com.vedaword/library)
  🔓 - Search Sanskrit scripture by meaning, read verses and look up terms, with citations and honest "no answer".
- [Vilix AI](https://vilix.ai) `https://api.vilix.ai/mcp`
  [![Vilix AI MCP connector](https://glama.ai/mcp/connectors/ai.vilix.api/vilix-ai/badges/score.svg)](https://glama.ai/mcp/connectors/ai.vilix.api/vilix-ai)
  🔐 - Persistent AI memory shared across tools and devices.
- [What Led To](https://whatledto.com) `https://whatledto.com/mcp`
  [![What Led To MCP connector](https://glama.ai/mcp/connectors/com.whatledto/what-led-to/badges/score.svg)](https://glama.ai/mcp/connectors/com.whatledto/what-led-to)
  🔓 - Source-backed timelines of tech, economy and gaming events, with the quote behind each entry.
- [WhiteMagic](https://www.whitemagic.dev) `https://mcp.whitemagic.dev/mcp`
  [![WhiteMagic MCP connector](https://glama.ai/mcp/connectors/io.github.lbailey94/whitemagic-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.lbailey94/whitemagic-mcp)
  🔓 - Local-first agent memory and session continuity: durable recall, handoffs, and signed continuity receipts.
- [WITAN Markets](https://witan.markets) `https://witan.markets/mcp`
  [![WITAN Markets MCP connector](https://glama.ai/mcp/connectors/io.github.witanmarkets/witan/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.witanmarkets/witan)
  🔓 - Agents buy what search can't find: measured knowledge and data its sellers hold the rights to, paid via x402.

### ⚖️ <a name="legal"></a>Legal
- [AcqPath](https://developers.getacqpath.com) `https://api.getacqpath.com/mcp`
  [![AcqPath MCP connector](https://glama.ai/mcp/connectors/com.getacqpath/acqpath/badges/score.svg)](https://glama.ai/mcp/connectors/com.getacqpath/acqpath)
  🔓 - Check observed machine-readable source-rights declarations before AI, RAG, indexing, training or search.

- [Akashi Notari](https://akashi-notari.com) `https://anchor.akashi-notari.com/mcp`
  [![Akashi Notari MCP connector](https://glama.ai/mcp/connectors/io.github.self-reality/akashi-notari/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.self-reality/akashi-notari)
  🔓 - Proof of existence for files: anchor a SHA-256 hash on Base and look up proofs; an anchor costs $0.01 over x402.
- [Antevo Trademark](https://antevo.ch/trademark/) `https://trademark.antevo.ch/mcp`
  [![Antevo Trademark MCP connector](https://glama.ai/mcp/connectors/ch.antevo/trademark/badges/score.svg)](https://glama.ai/mcp/connectors/ch.antevo/trademark)
  🔓 - Checks a brand name across 50+ national and regional trademark registers, with each office's opposition deadline.
- [Cheap NY Publication](https://cheapnypublication.com/ai) `https://cheapnypublication.com/mcp`
  [![Cheap NY Publication MCP connector](https://glama.ai/mcp/connectors/com.cheapnypublication/ny-llc/badges/score.svg)](https://glama.ai/mcp/connectors/com.cheapnypublication/ny-llc)
  🔓 - New York LLC lookup from the state register: publication deadline, county and price, plus filing quotes.
- [Claim Done](https://claimdone.com.au/connect-your-ai-assistant/) `https://claimdone.com.au/mcp`
  [![Claim Done MCP connector](https://glama.ai/mcp/connectors/au.com.claimdone/claimdone/badges/score.svg)](https://glama.ai/mcp/connectors/au.com.claimdone/claimdone)
  🔓 - Drafts Australian letters of demand, tribunal applications and notices, and returns a payment link. Not a law firm.
- [ClevSec EU compliance](https://clevsec.one/mcp/) `https://mcp.clevsec.one/mcp`
  [![ClevSec EU compliance MCP connector](https://glama.ai/mcp/connectors/one.clevsec/eu-compliance/badges/score.svg)](https://glama.ai/mcp/connectors/one.clevsec/eu-compliance)
  🔓 - Rule-based NIS2, DORA, GDPR and Cyber Resilience Act checks, with the legal sources for every answer.
- [Common Paper](https://commonpaper.com) `https://api.commonpaper.com/mcp`
  [![Common Paper MCP connector](https://glama.ai/mcp/connectors/com.commonpaper/contracts/badges/score.svg)](https://glama.ai/mcp/connectors/com.commonpaper/contracts)
  🔐 - Create agreements from standard templates, send them for signature, and track status and history.
- [Cookie Compliance](https://cookie-compliance.co/mcp/) `https://mcp.cookie-compliance.co/mcp`
  [![Cookie Compliance MCP connector](https://glama.ai/mcp/connectors/co.cookie-compliance/cookie-consent/badges/score.svg)](https://glama.ai/mcp/connectors/co.cookie-compliance/cookie-consent)
  🔓 - Preview, install and configure a cookie consent banner that holds trackers in the page until the visitor chooses.
- [Court Rules](https://www.courtrules.app) `https://mcp.courtrules.app/mcp`
  [![Court Rules MCP connector](https://glama.ai/mcp/connectors/app.courtrules/court-rules/badges/score.svg)](https://glama.ai/mcp/connectors/app.courtrules/court-rules)
  🔓 - US judge filing rules, court holidays and enforcement data; free samples, OAuth for full access.
- [Datakoot Regulatory Intel](https://datakoot.com/regulatory-intel) `https://regulatory.datakoot.com/mcp`
  [![Datakoot Regulatory Intel MCP connector](https://glama.ai/mcp/connectors/com.datakoot/federal-register-rules/badges/score.svg)](https://glama.ai/mcp/connectors/com.datakoot/federal-register-rules)
  🔓 - Federal Register rules, proposed rules, notices and executive orders, searchable by agency and term.
- [disclosedby](https://disclosedby.com) `https://disclosedby.com/api/mcp`
  [![disclosedby MCP connector](https://glama.ai/mcp/connectors/com.disclosedby/record/badges/score.svg)](https://glama.ai/mcp/connectors/com.disclosedby/record)
  🔓 - Dated quotes of GDPR art. 28 subprocessor lists: who lists whom, what changed, and what a list said on a date.
- [fynk](https://fynk.com/en/integrations/mcp-server/) `https://app.fynk.com/mcp`
  [![fynk MCP connector](https://glama.ai/mcp/connectors/com.fynk.app/fynk-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.fynk.app/fynk-mcp)
  🔐 - Manage contracts end to end: find and analyze them, draft or upload new ones, add signatories and send for e-signature.
- [GleanMark](https://gleanmark.com/integrations) `https://gleanmark.com/mcp`
  [![GleanMark MCP connector](https://glama.ai/mcp/connectors/com.gleanmark/trademark-search/badges/score.svg)](https://glama.ai/mcp/connectors/com.gleanmark/trademark-search)
  🔓 - Search 14M USPTO trademark records, mark status and history, Office Actions and TTAB cases; OAuth for your portfolios.
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
- [MachineWitness](https://machinewitness.eu/api) `https://machinewitness.eu/mcp`
  [![MachineWitness MCP connector](https://glama.ai/mcp/connectors/eu.machinewitness/archive/badges/score.svg)](https://glama.ai/mcp/connectors/eu.machinewitness/archive)
  🔓 - EU archive of robots.txt, ai.txt and AI opt-outs: check if a domain is observed, order time-stamped captures.
- [Magist](https://magist.io/mcp) `https://magist.io/api/mcp`
  [![Magist MCP connector](https://glama.ai/mcp/connectors/io.github.magist-io/magist/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.magist-io/magist)
  🔓 - Cited regulatory research, implementation controls and product scoping; legal information, not legal advice.
- [Pakistan Case Law](https://pakistancaselaw.com) `https://pakistancaselaw.com/mcp`
  [![Pakistan Case Law MCP connector](https://glama.ai/mcp/connectors/com.pakistancaselaw/caselaw/badges/score.svg)](https://glama.ai/mcp/connectors/com.pakistancaselaw/caselaw)
  🔓 - 230,000+ Pakistani court judgments: search by issue, question, court, judge or citation; walk the citation graph.
- [Patent by Ouroboros](https://ouroborosapps.com/docs/patent) `https://patent-mcp.vercel.app/mcp`
  [![Patent by Ouroboros MCP connector](https://glama.ai/mcp/connectors/io.github.LAHutchins91/patent/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.LAHutchins91/patent)
  🔓 - US patent search and prior art lookup that returns only records the patent office returned; not legal advice.
- [Patlas](https://patlas.dev) `https://patlas.dev/mcp`
  [![Patlas MCP connector](https://glama.ai/mcp/connectors/dev.patlas/patlas/badges/score.svg)](https://glama.ai/mcp/connectors/dev.patlas/patlas)
  🔐 - Patent prior-art search over USPTO and EPO data, claim comparison, and codebase scans for patentable tech.
- [Precleared](https://precleared.dev) `https://precleared.dev/mcp`
  [![Precleared MCP connector](https://glama.ai/mcp/connectors/dev.precleared/contact-check/badges/score.svg)](https://glama.ai/mcp/connectors/dev.precleared/contact-check)
  🔓 - Checks if a cold marketing email to one address is allowed under UK, US, Canadian, German or French law, with a receipt.
- [Redra](https://redra.ai) `https://mcp.redra.ai/mcp`
  [![Redra MCP connector](https://glama.ai/mcp/connectors/io.github.sacrosaunt/redra/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.sacrosaunt/redra)
  🔓 - Searches current US class-action settlements by company, state, deadline and proof needed, with official claim links.
- [RegAI Legal MCP](https://regai.tw/mcp) `https://mcp.regai.tw/mcp`
  [![RegAI Legal MCP connector](https://glama.ai/mcp/connectors/tw.regai/legal/badges/score.svg)](https://glama.ai/mcp/connectors/tw.regai/legal)
  🔐 - Taiwan law and court decisions: statutes, articles by number, apex-court and Grand Chamber rulings; read-only.

- [UK Legislation Changes](https://uk-legal-changes.pages.dev) `https://uk-legal-changes.pages.dev/mcp`
  [![UK Legislation Changes MCP connector](https://glama.ai/mcp/connectors/io.github.busybusybussiness/uk-legislation-changes/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.busybusybussiness/uk-legislation-changes)
  🔓 - Point-in-time amendment history for 506 UK legislation provisions across employment, equality, consumer and company law.
- [Vespper](https://www.vespper.com/) `https://mcp.vespper.com/mcp`
  [![Vespper MCP connector](https://glama.ai/mcp/connectors/com.vespper.mcp/vespper-docx-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.vespper.mcp/vespper-docx-mcp)
  🔐 - Reads .docx files as HTML and writes edits back as native Word tracked changes.
- [Zitierfest](https://zitierfest.de) `https://mcp.zitierfest.de/mcp`
  [![Zitierfest MCP connector](https://glama.ai/mcp/connectors/de.zitierfest/zitierfest/badges/score.svg)](https://glama.ai/mcp/connectors/de.zitierfest/zitierfest)
  🔐 - German statutes verbatim (federal, 16 states, EU), federal court decisions with paragraph numbers, legal fees.

### 🎯 <a name="marketing"></a>Marketing

- [402registry](https://402registry.com) `https://402registry.com/mcp`
  [![402registry MCP connector](https://glama.ai/mcp/connectors/com.402registry/402registry/badges/score.svg)](https://glama.ai/mcp/connectors/com.402registry/402registry)
  🔓 - Can AI crawlers see a website: free lookup of its last dated verdict; a new check is paid with x402 in USDC on Base.

- [AdRadar](https://adradarmcp.cloud/en/) `https://adradarmcp.cloud/mcp`
  [![AdRadar MCP connector](https://glama.ai/mcp/connectors/io.github.Egggy1998/adradar/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Egggy1998/adradar)
  🔐 - Find competitors' longest-running Meta and TikTok ads, scored by hook, angle and audience.

- [Adrails](https://adrails.ai) `https://adrails.ai/api/mcp`
  [![Adrails MCP connector](https://glama.ai/mcp/connectors/ai.adrails/adrails/badges/score.svg)](https://glama.ai/mcp/connectors/ai.adrails/adrails)
  🔐 - Meta and Google Ads for Shopify stores: store revenue next to ad spend, and new campaigns prepared paused for approval.

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


- [AffiliateBase](https://www.affiliatebase.io) `https://app.affiliatebase.io/mcp`
  [![AffiliateBase MCP connector](https://glama.ai/mcp/connectors/io.affiliatebase/affiliatebase/badges/score.svg)](https://glama.ai/mcp/connectors/io.affiliatebase/affiliatebase)
  🔐 - Set up and run a Stripe affiliate program: tracking checks, affiliates, commissions and payouts.

- [AfterLaunch](https://afterlaunch.io) `https://afterlaunch.io/api/mcp`
  [![AfterLaunch MCP connector](https://glama.ai/mcp/connectors/io.afterlaunch/agentic-growth-marketing/badges/score.svg)](https://glama.ai/mcp/connectors/io.afterlaunch/agentic-growth-marketing)
  🔓 - AI answer visibility, SEO and a ranked backlog of growth moves; tools need an account.
- [Agent C](https://www.theagentc.io/mcp) `https://api.theagentc.io/mcp`
  [![Agent C MCP connector](https://glama.ai/mcp/connectors/io.theagentc/app-store-screenshots/badges/score.svg)](https://glama.ai/mcp/connectors/io.theagentc/app-store-screenshots)
  🔓 - AI-designed App Store screenshot sets, uploaded to App Store Connect; tools require an Agent C API key.
- [Agent Data API](https://agent.chiemgaufilms.com) `https://agent.chiemgaufilms.com/mcp`
  [![Agent Data API MCP connector](https://glama.ai/mcp/connectors/com.chiemgaufilms.agent/agent-data-api/badges/score.svg)](https://glama.ai/mcp/connectors/com.chiemgaufilms.agent/agent-data-api)
  🔓 - SEO data for agencies and agents in DACH: keywords, SERP, competitors, local search; pay per call with x402 USDC.
- [agentbuilt](https://agentbuilt.dev/mcp) `https://agentbuilt.dev/api/mcp`
  [![agentbuilt MCP connector](https://glama.ai/mcp/connectors/dev.agentbuilt/agentbuilt/badges/score.svg)](https://glama.ai/mcp/connectors/dev.agentbuilt/agentbuilt)
  🔓 - Free AI-readiness audit of any URL: AI crawler rules, JS-free text, JSON-LD, llms.txt and concrete fixes.

- [AgentPixel](https://agentpixel.io) `https://agentpixel.io/mcp`
  [![AgentPixel MCP connector](https://glama.ai/mcp/connectors/io.agentpixel/agentpixel/badges/score.svg)](https://glama.ai/mcp/connectors/io.agentpixel/agentpixel)
  🔓 - Most visitors never fill out a form. Turn the ones who say yes into contacts your agent reads.

- [App-Kit](https://app-kit.dev/mcp) `https://mcp.app-kit.dev/mcp`
  [![App-Kit MCP connector](https://glama.ai/mcp/connectors/io.github.app-kit-dev/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.app-kit-dev/mcp)
  🔓 - SEO audit with 400 checks, text readability and grammar check, image conversion and PDF to images; free, no sign-up.

- [ask10ais](https://ask10ais.com) `https://ask10ais.com/api/mcp`
  [![ask10ais MCP connector](https://glama.ai/mcp/connectors/com.ask10ais/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.ask10ais/mcp)
  🔓 - Read-only rankings and mention rates showing how 12 AI models answer brand questions in Chinese and English.

- [AskWatch Google Search Console MCP](https://askwatch.ai/free-tools/google-search-console-mcp) `https://mcp.askwatch.ai/gsc`
  [![AskWatch Google Search Console MCP connector](https://glama.ai/mcp/connectors/ai.askwatch/gsc/badges/score.svg)](https://glama.ai/mcp/connectors/ai.askwatch/gsc)
  🔓 - Read-only Google Search Console: traffic changes, CTR gaps, cannibalization, URL inspection; tools need a free account.

- [BacklinkMCP](https://backlinkmcp.com/mcp-server-for-seo) `https://backlinkmcp.com/api/mcp`
  [![BacklinkMCP MCP connector](https://glama.ai/mcp/connectors/io.github.johnsmalls22-rgb/backlinkmcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.johnsmalls22-rgb/backlinkmcp-server)
  🔓 - Domain authority, top linking domains, link-gap prospects and AI-answer visibility checks from a domain-level index.

- [BanProof](https://banproof.io) `https://banproof.io/mcp`
  [![BanProof MCP connector](https://glama.ai/mcp/connectors/io.banproof/ban-proof-ai/badges/score.svg)](https://glama.ai/mcp/connectors/io.banproof/ban-proof-ai)
  🔓 - Check TikTok Shop and Amazon affiliate video scripts for policy violations and draft ban appeal letters.
- [BizIntel](https://mcp-bizintel-production.up.railway.app) `https://mcp-bizintel-production.up.railway.app/mcp`
  [![BizIntel MCP connector](https://glama.ai/mcp/connectors/io.github.bch1212/bizintel/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.bch1212/bizintel)
  🔓 - Audit websites, detect tech stacks, and find and score local businesses without a website.
- [Blawgy](https://blawgy.com/mcp) `https://app.blawgy.com/mcp`
  [![Blawgy MCP connector](https://glama.ai/mcp/connectors/com.blawgy/blawgy/badges/score.svg)](https://glama.ai/mcp/connectors/com.blawgy/blawgy)
  🔐 - Keyword research, plus writing and publishing SEO blog posts to WordPress, Shopify, Webflow and more.
- [CalmSEO](https://calmseo.com) `https://mcp.calmseo.com/mcp`
  [![CalmSEO MCP connector](https://glama.ai/mcp/connectors/com.calmseo/seo-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.calmseo/seo-mcp)
  🔐 - Free Google Search Console analytics plus credit-based SERP, keyword, and page audit tools.
- [Camberstack](https://camberstack.io) `https://camberstack.io/mcp`
  [![Camberstack MCP connector](https://glama.ai/mcp/connectors/io.camberstack/google-ads/badges/score.svg)](https://glama.ai/mcp/connectors/io.camberstack/google-ads)
  🔐 - Google Ads: checks conversion tracking, finds wasted spend, and applies only the changes you approve, with undo.
- [Caybl](https://caybl.ai) `https://api.caybl.ai/mcp`
  [![Caybl MCP connector](https://glama.ai/mcp/connectors/ai.caybl/caybl/badges/score.svg)](https://glama.ai/mcp/connectors/ai.caybl/caybl)
  🔐 - Query GA4, Google Ads and Search Console: reports, funnels, search terms, keyword ideas and URL inspection.
- [ChimpanSEO](https://chimpanseo.app) `https://chimpanseo.app/api/mcp`
  [![ChimpanSEO MCP connector](https://glama.ai/mcp/connectors/app.chimpanseo/chimpanseo/badges/score.svg)](https://glama.ai/mcp/connectors/app.chimpanseo/chimpanseo)
  🔓 - Generate, schedule and publish GEO/AEO-optimized articles to WordPress; tools need an account.
- [Cite42](https://www.cite42.dev) `https://mcp.cite42.dev`
  [![Cite42 MCP connector](https://glama.ai/mcp/connectors/dev.cite42/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/dev.cite42/mcp)
  🔐 - Check whether ChatGPT, Claude, Perplexity and Gemini mention your brand and what they cite; keyword and trend data.
- [CiteLadder](https://citeladder.com) `https://api.citeladder.com/mcp`
  [![CiteLadder MCP connector](https://glama.ai/mcp/connectors/com.citeladder/citeladder/badges/score.svg)](https://glama.ai/mcp/connectors/com.citeladder/citeladder)
  🔐 - Track how ChatGPT, Gemini and Claude answer buyer questions, which brands they name and sources cited.
- [ConferenceGrid](https://conferencegrid.com/mcp) `https://conferencegrid.com/api/mcp`
  [![ConferenceGrid MCP connector](https://glama.ai/mcp/connectors/com.conferencegrid/conferencegrid/badges/score.svg)](https://glama.ai/mcp/connectors/com.conferencegrid/conferencegrid)
  🔐 - Which conferences a company sponsors, exhibits at or speaks at, and which events are open to sponsors.
- [Convertlyft](https://convertlyft.com/developers) `https://mcp.convertlyft.com/mcp`
  [![Convertlyft MCP connector](https://glama.ai/mcp/connectors/com.convertlyft/convertlyft/badges/score.svg)](https://glama.ai/mcp/connectors/com.convertlyft/convertlyft)
  🔓 - Web analytics that names the fix: funnels, replays, errors, speed and SEO. Free SEO scan; account tools use OAuth.
- [CreatorsJet](https://www.creatorsjet.com/mcp) `https://api.creatorsjet.com/mcp`
  [![CreatorsJet MCP connector](https://glama.ai/mcp/connectors/com.creatorsjet/creatorsjet/badges/score.svg)](https://glama.ai/mcp/connectors/com.creatorsjet/creatorsjet)
  🔐 - Creator media kits, link-in-bio pages, deal requests, analytics, agency rosters and sponsor brand search.
- [GrowSurf](https://docs.growsurf.com/build-with-ai) `https://mcp.growsurf.com`
  [![GrowSurf MCP connector](https://glama.ai/mcp/connectors/com.growsurf/growsurf/badges/score.svg)](https://glama.ai/mcp/connectors/com.growsurf/growsurf)
  🔐 - Build and manage GrowSurf referral and affiliate programs through AI assistants.

- [InsightfulPipe](https://insightfulpipe.com) `https://main.insightfulmcp.com/`
  [![InsightfulPipe MCP connector](https://glama.ai/mcp/connectors/com.insightfulmcp.main/insightful-pipe/badges/score.svg)](https://glama.ai/mcp/connectors/com.insightfulmcp.main/insightful-pipe)
  🔐 - Google Ads, Meta Ads, GA4, LinkedIn, TikTok and 45 more marketing platforms, with each action switched per account.

- [Keyword Research API](https://apify.com/gaelasao/keyword-research-api) `https://mcp.apify.com/?tools=gaelasao/keyword-research-api`
  [![Keyword Research API MCP connector](https://glama.ai/mcp/connectors/io.github.gaelasao/keyword-research-api/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.gaelasao/keyword-research-api)
  🔐 - Google search volume, CPC, difficulty and intent in every country, keyword ideas, and the keywords any domain ranks for.

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
- [fnlowl](https://fnlowl.com) `https://api.fnlowl.com/v1/mcp`
  [![fnlowl MCP connector](https://glama.ai/mcp/connectors/com.fnlowl/fnlowl/badges/score.svg)](https://glama.ai/mcp/connectors/com.fnlowl/fnlowl)
  🔓 - Manage website widgets, leads, email sequences and analytics; discovery is open, tool calls need a sign-in.
- [Formgong](https://formgong.com) `https://formgong.com/mcp`
  [![Formgong MCP connector](https://glama.ai/mcp/connectors/com.formgong/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.formgong/mcp)
  🔓 - Create contact forms and get HTML/React/Next.js snippets; discovery is open, every tool call needs a sign-in.
- [Formquote](https://pcba-quote-lab.pages.dev/en/) `https://formquote-mcp.chen-yu-d1.workers.dev/mcp`
  [![Formquote MCP connector](https://glama.ai/mcp/connectors/io.github.Keith-CY/formquote-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Keith-CY/formquote-mcp)
  🔓 - Compare email verification credit prices, sound-effect licences and font licences from a live public catalogue.
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
- [gtm.help](https://gtm.help) `https://gtm.help/mcp`
  [![gtm.help MCP connector](https://glama.ai/mcp/connectors/help.gtm/gtm-help/badges/score.svg)](https://glama.ai/mcp/connectors/help.gtm/gtm-help)
  🔓 - Turn a website into ranked growth plays, find Reddit, LinkedIn and X threads to answer, and track shipped work.
- [HarborRank](https://harborrank.com/features/mcp) `https://app.harborrank.com/mcp`
  [![HarborRank MCP connector](https://glama.ai/mcp/connectors/com.harborrank/harborrank/badges/score.svg)](https://glama.ai/mcp/connectors/com.harborrank/harborrank)
  🔐 - Keyword metrics, live Google SERPs, backlinks, rank tracking, site audits and read-only Search Console data.
- [Hermoso](https://hermoso.ai) `https://app.hermoso.ai/mcp`
  [![Hermoso MCP connector](https://glama.ai/mcp/connectors/io.github.hermoso-ai/hermoso/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.hermoso-ai/hermoso)
  🔓 - Research competitor ads, generate image and video ads, schedule social posts and run paid ad campaigns.

- [How It Spread](https://howitspread.com/mcp) `https://howitspread.com/api/mcp`
  [![How It Spread MCP connector](https://glama.ai/mcp/connectors/com.howitspread/howitspread/badges/score.svg)](https://glama.ai/mcp/connectors/com.howitspread/howitspread)
  🔓 - Viral marketing precedents with dated, sourced spread timelines and a Spread Score. No sign-in.

- [iMario](https://imario.ai) `https://mcp.imario.ai/mcp`
  [![iMario MCP connector](https://glama.ai/mcp/connectors/ai.imario/imario/badges/score.svg)](https://glama.ai/mcp/connectors/ai.imario/imario)
  🔐 - Ask synthetic audiences built from real people how they react to copy, pages, prices and images.

- [IndustryLens](https://industry-lens.com) `https://api.industry-lens.com/mcp/public`
  [![IndustryLens MCP connector](https://glama.ai/mcp/connectors/com.industry-lens/mcp-public/badges/score.svg)](https://glama.ai/mcp/connectors/com.industry-lens/mcp-public)
  🔓 - Competitive intelligence on B2B SaaS markets: competitor profiles, strategic moves, pricing changes and reports.
  
- [Jepto](https://www.jepto.com/integration/mcp) `https://mcp.jepto.com`
  [![Jepto MCP connector](https://glama.ai/mcp/connectors/com.jepto/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.jepto/mcp)
  🔐 - Query live Google Ads, GA4, Search Console, Meta Ads and Google Business Profile data, and manage KPIs and budgets.

- [Layrcake](https://layrcake.dev) `https://mcp.layrcake.dev/mcp`
  [![Layrcake MCP connector](https://glama.ai/mcp/connectors/dev.layrcake.mcp/layrcake/badges/score.svg)](https://glama.ai/mcp/connectors/dev.layrcake.mcp/layrcake)
  🔐 - Find leads, enrich them to verified emails, detect intent and launch human-approved campaigns.

- [Lekta](https://lekta.dev) `https://lekta.dev/mcp`
  [![Lekta MCP connector](https://glama.ai/mcp/connectors/dev.lekta/lektadev/badges/score.svg)](https://glama.ai/mcp/connectors/dev.lekta/lektadev)
  🔓 - Audit a site's visibility in AI answer engines (AEO/GEO).
- [Limurse](https://limurse.ai/developers/mcp) `https://api.limurse.ai/mcp`
  [![Limurse MCP connector](https://glama.ai/mcp/connectors/ai.limurse/limurse/badges/score.svg)](https://glama.ai/mcp/connectors/ai.limurse/limurse)
  🔐 - Find bookable creators, benchmark market rates and draft campaign briefs; read-only, booking happens on Limurse.
- [LinkBunny Placement Checker](https://getlinkbunny.com/tools/backlink-placement-checker?ref=awesome-remote-mcp) `https://mcp.getlinkbunny.com/mcp`
  [![LinkBunny Placement Checker MCP connector](https://glama.ai/mcp/connectors/com.getlinkbunny/placement-checker/badges/score.svg)](https://glama.ai/mcp/connectors/com.getlinkbunny/placement-checker)
  🔓 - Checks whether a public page links to an expected URL and reports the anchor, rel attributes and canonical.
- [LocationLists](https://locationlists.com) `https://locationlists.com/mcp`
  [![LocationLists MCP connector](https://glama.ai/mcp/connectors/io.github.kylehawke-stack/locationlists/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.kylehawke-stack/locationlists)
  🔓 - Search 725 US business-location datasets (dealers, contractors, chains), preview real rows, and buy CSVs.
- [LogoKit](https://logokit.com) `https://mcp.logokit.com/mcp`
  [![LogoKit MCP connector](https://glama.ai/mcp/connectors/com.logokit/brand-data/badges/score.svg)](https://glama.ai/mcp/connectors/com.logokit/brand-data)
  🔑 - Company logos, brand colors, and firmographic data by domain.
- [Loomaly](https://loomaly.com) `https://loomaly.com/mcp`
  [![Loomaly MCP connector](https://glama.ai/mcp/connectors/com.loomaly/loomaly/badges/score.svg)](https://glama.ai/mcp/connectors/com.loomaly/loomaly)
  🔐 - SEO audit of every page: a ranked fix list, a fix prompt for your framework, and a re-check once the fix is live.
- [Mador](https://mador.ai) `https://mador.ai/api/mcp`
  [![Mador MCP connector](https://glama.ai/mcp/connectors/ai.mador/mador/badges/score.svg)](https://glama.ai/mcp/connectors/ai.mador/mador)
  🔐 - Read-only access to a Mador account: how often AI assistants name a business, and who else they name.
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
- [Nitrosend](https://nitrosend.com) `https://api.nitrosend.com/mcp`
  [![Nitrosend MCP connector](https://glama.ai/mcp/connectors/com.nitrosend/nitrosend/badges/score.svg)](https://glama.ai/mcp/connectors/com.nitrosend/nitrosend)
  🔐 - Draft campaigns and flows, manage audiences, send tests, and inspect results in your Nitrosend account.
- [nowyourlink](https://nowyourlink.com) `https://nowyourlink.com/mcp`
  [![nowyourlink MCP connector](https://glama.ai/mcp/connectors/io.github.ArneFfm/nowyourlink/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ArneFfm/nowyourlink)
  🔓 - Read the current daily homepage Spotlight ad and browse the archive of settled auction days.
- [NumberBroom](https://numberbroom.com/mcp-server) `https://numberbroom.com/mcp`
  [![NumberBroom MCP connector](https://glama.ai/mcp/connectors/io.github.cameron-creations/numberbroom-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.cameron-creations/numberbroom-mcp)
  🔓 - Check a US phone's line type, carrier and TCPA litigator status before dialing; tools need a prepaid key.
- [Nuqti](https://nuqti.com/mcp) `https://nuqti.com/api/public/mcp`
  [![Nuqti MCP connector](https://glama.ai/mcp/connectors/com.nuqti/nuqti-ahrefs-alternative-seo-data/badges/score.svg)](https://glama.ai/mcp/connectors/com.nuqti/nuqti-ahrefs-alternative-seo-data)
  🔓 - SEO data: domain overview, backlinks, referring domains, link history, keyword ideas and on-page checks.
- [OnPage.dev](https://onpage.dev/mcp) `https://onpage.dev/mcp`
  [![OnPage.dev MCP connector](https://glama.ai/mcp/connectors/dev.onpage/onpage/badges/score.svg)](https://glama.ai/mcp/connectors/dev.onpage/onpage)
  🔓 - Free SEO and AI-visibility audits: scores, fixes, schema, robots.txt, redirects and 25-page site audits, no account.
- [PageLens](https://pagelens.io/docs/api) `https://app.pagelens.io/mcp`
  [![PageLens MCP connector](https://glama.ai/mcp/connectors/io.pagelens/pagelens/badges/score.svg)](https://glama.ai/mcp/connectors/io.pagelens/pagelens)
  🔓 - Web analytics for your site and which AI crawlers and assistants read it; tool calls need an API key.
- [Peak Answer](https://peakanswer.com) `https://peakanswer.com/api/mcp`
  [![Peak Answer MCP connector](https://glama.ai/mcp/connectors/com.peakanswer/peak-answer/badges/score.svg)](https://glama.ai/mcp/connectors/com.peakanswer/peak-answer)
  🔐 - Whether AI search recommends your brand, which buying questions competitors win, and the technical faults stopping engines reading you.
- [Pineprompt](https://pineprompt.com) `https://pineprompt.com/mcp`
  [![Pineprompt MCP connector](https://glama.ai/mcp/connectors/com.pineprompt/pineprompt/badges/score.svg)](https://glama.ai/mcp/connectors/com.pineprompt/pineprompt)
  🔐 - Track how ChatGPT, Gemini, Perplexity, Claude and Google AI answers mention your brand, sources and competitors.
- [Plainrouter Sandbox](https://plainrouter.com/docs/mcp/setup) `https://plainrouter.com/mcp/sandbox`
  [![Plainrouter Sandbox MCP connector](https://glama.ai/mcp/connectors/com.plainrouter/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.plainrouter/mcp)
  🔓 - Test Meta advertising account, signal-health, and performance tools with synthetic data.
- [Postbox Services Email Tools](https://postboxservices.com/mcp/) `https://mcp.postboxservices.com/mcp`
  [![Postbox Services MCP connector](https://glama.ai/mcp/connectors/com.postboxservices/postbox-tools/badges/score.svg)](https://glama.ai/mcp/connectors/com.postboxservices/postbox-tools)
  🔓 - Live email checks: 24 blacklists, spoofing/BEC grade, URL redirect tracing, full email spam tests, domain age and WHOIS.
- [Proxy](https://useproxy.dev) `https://mcp.useproxy.dev/mcp`
  [![Proxy MCP connector](https://glama.ai/mcp/connectors/dev.useproxy/proxy/badges/score.svg)](https://glama.ai/mcp/connectors/dev.useproxy/proxy)
  🔐 - Search Meta, Google, LinkedIn and TikTok ad libraries for competitor ads, creatives and transcripts.
- [QQQ AI Visibility Checker](https://qqq.ee/en/mcp-server/) `https://qqq.ee/mcp`
  [![QQQ AI Visibility Checker MCP connector](https://glama.ai/mcp/connectors/ee.qqq/ai-visibility/badges/score.svg)](https://glama.ai/mcp/connectors/ee.qqq/ai-visibility)
  🔓 - Free AI visibility check: AI crawler access, AI search readiness and brand citations in ChatGPT, Gemini, Perplexity.
- [qrcode.io QR codes](https://agent.qrcode.io/) `https://agent.qrcode.io/mcp`
  [![qrcode.io QR codes MCP connector](https://glama.ai/mcp/connectors/io.qrcode/qr-codes/badges/score.svg)](https://glama.ai/mcp/connectors/io.qrcode/qr-codes)
  🔓 - Create free static QR codes as PNG or SVG for links, WiFi, contact cards and text; no account, never expire.
- [QRFLOW.codes](https://qrflow.codes) `https://qrflow.codes/mcp`
  [![QRFLOW.codes MCP connector](https://glama.ai/mcp/connectors/codes.qrflow/qrflow/badges/score.svg)](https://glama.ai/mcp/connectors/codes.qrflow/qrflow)
  🔐 - Create QR codes, re-point printed dynamic codes, name links on your own domain, and read scan analytics.
- [Quelta](https://quelta.ai/mcp-server/) `https://quelta.ai/mcp`
  [![Quelta MCP connector](https://glama.ai/mcp/connectors/ai.quelta/quelta/badges/score.svg)](https://glama.ai/mcp/connectors/ai.quelta/quelta)
  🔐 - Score short vertical video ads by link: first 3 seconds, issues with timecodes and fixes.
- [RankRoot](https://getrankroot.com) `https://getrankroot.com/api/mcp`
  [![RankRoot MCP connector](https://glama.ai/mcp/connectors/io.github.zachhhhh/rankroot/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.zachhhhh/rankroot)
  🔓 - Score a site’s visibility to ChatGPT, Perplexity and AI agents, and generate llms.txt, robots.txt and JSON-LD fixes.
- [Ranla](https://ranla.ai) `https://mcp.ranla.ai/mcp`
  [![Ranla MCP connector](https://glama.ai/mcp/connectors/ai.ranla/ranla/badges/score.svg)](https://glama.ai/mcp/connectors/ai.ranla/ranla)
  🔐 - AI growth engineer for software businesses: ships SEO pages, gets you into AI answers, replies on Reddit, sends email.
- [Reach MCP](https://www.reachmcp.com) `https://app.reachmcp.com/mcp`
  [![Reach MCP connector](https://glama.ai/mcp/connectors/com.reachmcp/linkedin/badges/score.svg)](https://glama.ai/mcp/connectors/com.reachmcp/linkedin)
  🔐 - Operate a LinkedIn account: inbox, invitations, Sales Navigator search, posts; enforced daily quotas, webhooks.
- [RedirX](https://redirx.dev) `https://redirx-mcp-server.onrender.com/mcp`
  [![RedirX MCP connector](https://glama.ai/mcp/connectors/dev.redirx/redirx/badges/score.svg)](https://glama.ai/mcp/connectors/dev.redirx/redirx)
  🔓 - Map old site URLs to new ones during a migration, review proposals and export approved redirects; calls need sign-in.
- [RedReplier](https://redreplier.com) `https://mcp.redreplier.com/mcp`
  [![RedReplier MCP connector](https://glama.ai/mcp/connectors/com.redreplier/mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/com.redreplier/mcp-server)
  🔐 - Find Reddit, Hacker News, X and Bluesky posts mentioning your product, scored as leads.
- [Revnu](https://revnu.com/mcp) `https://revnu.com/api/mcp`
  [![Revnu MCP connector](https://glama.ai/mcp/connectors/com.revnu/revnu/badges/score.svg)](https://glama.ai/mcp/connectors/com.revnu/revnu)
  🔐 - Review growth work, browse leads and results, message your growth agent, and schedule workflows.
- [Revup](https://revup.com/docs/mcp/) `https://revup.com/mcp`
  [![Revup MCP connector](https://glama.ai/mcp/connectors/com.revup/revup/badges/score.svg)](https://glama.ai/mcp/connectors/com.revup/revup)
  🔐 - Create, customize, preview and report on sweepstakes, contests, forms, surveys, quizzes and other promotions.
- [Rumoro](https://rumoro.dev/) `https://mcp.rumoro.dev/mcp`
  [![Rumoro MCP connector](https://glama.ai/mcp/connectors/dev.rumoro/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/dev.rumoro/mcp)
  🔓 - Track brand, competitor and topic mentions across 16 sources, scored for relevance and intent; tools need sign-in.
- [Say It Again](https://sayitagain.ai/docs/api) `https://app.sayitagain.ai/mcp`
  [![Say It Again MCP connector](https://glama.ai/mcp/connectors/ai.sayitagain/sayitagain/badges/score.svg)](https://glama.ai/mcp/connectors/ai.sayitagain/sayitagain)
  🔐 - Read a store's product page, write 3 scripts and make an AI UGC video with a generated presenter.
- [Scribe Mail](https://www.scribe-mail.com/mcp) `https://mcp.scribe-mail.com/mcp`
  [![Scribe Mail MCP connector](https://glama.ai/mcp/connectors/com.scribe-mail/scribe/badges/score.svg)](https://glama.ai/mcp/connectors/com.scribe-mail/scribe)
  🔐 - Manage company email signatures: author and publish templates, assign teammates, run banner campaigns, read analytics.
- [SearcherLite](https://searcherlite.com) `https://searcherlite.com/api/mcp`
  [![SearcherLite MCP connector](https://glama.ai/mcp/connectors/com.searcherlite/searcherlite/badges/score.svg)](https://glama.ai/mcp/connectors/com.searcherlite/searcherlite)
  🔐 - Google keyword, domain, backlink and AI-visibility data, paid per lookup in credits with no subscription.
- [Searcherries](https://searcherries.com) `https://app.searcherries.com/mcp/searcherries`
  [![Searcherries MCP connector](https://glama.ai/mcp/connectors/com.searcherries/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.searcherries/mcp)
  🔐 - Read-only AI visibility and SEO data: AI answers, competitors, citations, GSC, Bing, GA4.
- [SEO Expert: Digital Darts](https://www.digitaldarts.com.au/shopify-seo-expert-digital-darts-app/mcp) `https://seo.digitaldarts.com.au/mcp`
  [![SEO Expert: Digital Darts MCP connector](https://glama.ai/mcp/connectors/au.com.digitaldarts/seo-expert/badges/score.svg)](https://glama.ai/mcp/connectors/au.com.digitaldarts/seo-expert)
  🔐 - Audit a Shopify store's SEO and fix meta tags, alt text, structured data and broken links from chat.
- [seodata.dev](https://www.seodata.dev/mcp) `https://mcp.seodata.dev/mcp`
  [![seodata.dev MCP connector](https://glama.ai/mcp/connectors/dev.seodata/keywords/badges/score.svg)](https://glama.ai/mcp/connectors/dev.seodata/keywords)
  🔓 - Google search volume, CPC, competition and similar keywords for 50+ countries.
- [SEO·AEO·GEO](https://seoaeogeo.app/agents) `https://seoaeogeo.app/mcp`
  [![SEO·AEO·GEO MCP connector](https://glama.ai/mcp/connectors/app.seoaeogeo/seo-aeo-geo/badges/score.svg)](https://glama.ai/mcp/connectors/app.seoaeogeo/seo-aeo-geo)
  🔓 - Audit a URL for SEO, AEO and GEO: AI crawler access, schema and extractability, with ranked code fixes; free preview.
- [SERVIQO Agents](https://agents.serviqo.co/join.md) `https://agents.serviqo.co/mcp`
  [![SERVIQO Agents MCP connector](https://glama.ai/mcp/connectors/io.github.jdsleek/distributionos/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.jdsleek/distributionos)
  🔓 - Agents register as Founding Agents and get tracked share links and public reach stats; pilot, no payments.
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
- [stillindexed](https://stillindexed.com/mcp) `https://api.stillindexed.com/mcp`
  [![stillindexed MCP connector](https://glama.ai/mcp/connectors/com.stillindexed/seo-checkers/badges/score.svg)](https://glama.ai/mcp/connectors/com.stillindexed/seo-checkers)
  🔓 - Indexability, robots.txt, sitemap, TLS, domain-expiry and AI-crawler checks for any URL; no account.
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

- [SyncSignature Email Signatures](https://syncsignature.com/mcp/) `https://mcp.syncsignature.com/mcp`
  [![SyncSignature Email Signatures MCP connector](https://glama.ai/mcp/connectors/com.syncsignature/email-signatures/badges/score.svg)](https://glama.ai/mcp/connectors/com.syncsignature/email-signatures)
  🔐 - Manage team email signatures: teammates, groups, templates, banner campaigns and click analytics.

- [The Profound Agency](https://theprofound.agency/mcp/) `https://theprofound.agency/api/mcp/`
  [![The Profound Agency MCP connector](https://glama.ai/mcp/connectors/agency.theprofound/the-profound-agency/badges/score.svg)](https://glama.ai/mcp/connectors/agency.theprofound/the-profound-agency)
  🔓 - Search, price, and order press placements across 1,600+ publications; free AI-visibility audits.

- [TheQRCode.io](https://theqrcode.io/mcp) `https://mcp.theqrcode.io/mcp`
  [![TheQRCode.io MCP connector](https://glama.ai/mcp/connectors/io.theqrcode/qr-code-generator/badges/score.svg)](https://glama.ai/mcp/connectors/io.theqrcode/qr-code-generator)
  🔓 - Generate QR codes, list saved codes, and read scan analytics by time, device and approximate location.
- [Tracetify](https://tracetify.com/mcp) `https://tracetify.com/api/mcp`
  [![Tracetify MCP connector](https://glama.ai/mcp/connectors/io.github.tracetify/tracetify-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.tracetify/tracetify-mcp)
  🔓 - Find competitors, trace how they grew from dated public sources, and see their ads; tools need an account.
- [UGCfy AI](https://ugcfy.ai/mcp) `https://ugcfy.ai/api/mcp`
  [![UGCfy AI MCP connector](https://glama.ai/mcp/connectors/ai.ugcfy/ugcfy-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/ai.ugcfy/ugcfy-mcp)
  🔓 - Break down a TikTok or Reels ad and rewrite it for your product, plus UGC hooks, scripts and CPM.
- [TubeText Ad Intelligence](https://apify.com/tubetext/meta-ad-library-videos) `https://mcp.apify.com/?tools=fetch-actor-details,tubetext/meta-ad-library-videos,tubetext/video-ad-analyzer,tubetext/shot-by-shot-video-analysis`
  [![TubeText Ad Intelligence MCP connector](https://glama.ai/mcp/connectors/io.github.LMSlay/tubetext-ad-intelligence/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.LMSlay/tubetext-ad-intelligence)
  🔐 - A brand's Facebook/Instagram ads from Meta Ad Library, plus AI teardowns of Meta and YouTube video ads.
- [VertoDigital](https://vertodigital.com) `https://mcp.vertodigital.com/mcp`
  [![VertoDigital MCP Server MCP connector](https://glama.ai/mcp/connectors/com.vertodigital/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.vertodigital/mcp)
  🔓 - B2B pipeline marketing agency: match challenges to services, search case studies, read pages, send enquiries.
- [Vibe Prospecting](https://vibeprospecting.ai) `https://vibeprospecting.explorium.ai/mcp`
  🔐 - Search companies and contacts, enrich lead lists, and research B2B business signals.
- [VNCNT Labs SEO & Search Data](https://vncntlabs.com) `https://mcp.apify.com/?tools=vncntlabs/keyword-search-volume,vncntlabs/keyword-ideas,vncntlabs/domain-seo-data,vncntlabs/google-trends-search-volume,vncntlabs/ai-search-visibility-tracker,vncntlabs/google-maps-rank-tracker,vncntlabs/google-ads-transparency,vncntlabs/google-news-scraper`
  [![VNCNT Labs SEO & Search Data MCP connector](https://glama.ai/mcp/connectors/io.github.PravinrajV/vncntlabs-seo/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.PravinrajV/vncntlabs-seo)
  🔐 - Keyword volume and ideas, domain SEO, Trends volume, AI visibility, Maps geo-grid rank, Google ads and news.
- [Wall Marketing](https://www.wall.marketing/developers) `https://www.wall.marketing/mcp`
  [![Wall Marketing MCP connector](https://glama.ai/mcp/connectors/marketing.wall/platform/badges/score.svg)](https://glama.ai/mcp/connectors/marketing.wall/platform)
  🔐 - Book ad screens in bars, cafés and hostels with proof of display, or earn commission signing venues up as an ambassador.
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
- [ConnectorReport](https://connectorreport.com/mcp) `https://connectorreport.com/api/mcp`
  [![ConnectorReport MCP connector](https://glama.ai/mcp/connectors/com.connectorreport/connectorreport/badges/score.svg)](https://glama.ai/mcp/connectors/com.connectorreport/connectorreport)
  🔓 - Dated, hands-on test results for remote MCP servers: pass rate, sign-in method, gotchas and fix recipes.
- [EventSend](https://eventsend.io) `https://eventsend.io/mcp`
  [![EventSend MCP connector](https://glama.ai/mcp/connectors/io.eventsend/eventsend/badges/score.svg)](https://glama.ai/mcp/connectors/io.eventsend/eventsend)
  🔐 - Query your product's event history, delivery health and plan usage, e.g. what failed in checkout today.
- [OpenUptime](https://openuptime.app/docs/mcp) `https://openuptime.app/api/mcp`
  [![OpenUptime MCP connector](https://glama.ai/mcp/connectors/app.openuptime/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/app.openuptime/mcp)
  🔐 - Manage uptime monitors, incidents and public status pages.
- [Oh Dear](https://ohdear.app) `https://ohdear.app/mcp`
  [![Oh Dear MCP connector](https://glama.ai/mcp/connectors/app.ohdear/ohdear/badges/score.svg)](https://glama.ai/mcp/connectors/app.ohdear/ohdear)
  🔐 - Check uptime, SSL certificates, broken links, DNS, cron jobs and status pages for your Oh Dear sites.
- [Everframe](https://everframe.dev) `https://everframe.dev/mcp`
  [![Everframe MCP connector](https://glama.ai/mcp/connectors/dev.everframe/everframe/badges/score.svg)](https://glama.ai/mcp/connectors/dev.everframe/everframe)
  🔐 - Read in-app bug reports, crashes and tickets with screenshots, console, network and device context.
- [exit1.dev](https://exit1.dev/mcp) `https://app.exit1.dev/mcp/v1`
  [![exit1.dev MCP connector](https://glama.ai/mcp/connectors/dev.exit1/exit1-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/dev.exit1/exit1-mcp)
  🔐 - Create, edit and pause uptime monitors, read uptime stats and check history, and set email and webhook alerts.
- [Expiry Watch](https://boringutils.com/expiry-watch#mcp) `https://boringutils.com/api/mcp`
  [![Expiry Watch MCP connector](https://glama.ai/mcp/connectors/io.github.hal-boring-utils/expiry-watch/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.hal-boring-utils/expiry-watch)
  🔓 - Check a public domain's TLS certificate, chain and registration expiry without an account or API key.
- [Fixter](https://fixter.dev) `https://mcp.fixter.dev/mcp`
  [![Fixter MCP connector](https://glama.ai/mcp/connectors/dev.fixter.mcp/fixter/badges/score.svg)](https://glama.ai/mcp/connectors/dev.fixter.mcp/fixter)
  🔐 - Query production logs, traces, metrics and error issues, get the root cause, and open a fix as a pull request.
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
- [measuremy.site](https://measuremy.site) `https://a.measuremy.site/mcp`
  [![measuremy.site MCP connector](https://glama.ai/mcp/connectors/site.measuremy/analytics/badges/score.svg)](https://glama.ai/mcp/connectors/site.measuremy/analytics)
  🔐 - Cookieless web analytics your AI agent can read: visits, sources, pages, funnels, traffic spikes and tracked links.
- [Ned Watch](https://ned.watch) `https://api.ned.watch/mcp`
  [![Ned Watch MCP connector](https://glama.ai/mcp/connectors/watch.ned/ned-watch/badges/score.svg)](https://glama.ai/mcp/connectors/watch.ned/ned-watch)
  🔓 - Know when your agent silently stops: deadman, overrun, HTTP, TLS and content watches; the first call issues a key.
- [nimo](https://heynimo.com) `https://api.heynimo.com/try-mcp`
  [![nimo MCP connector](https://glama.ai/mcp/connectors/com.heynimo.api/nimo/badges/score.svg)](https://glama.ai/mcp/connectors/com.heynimo.api/nimo)
  🔓 - Check public pages' speed and Core Web Vitals and get the next fix without an account; paid plans add uptime alerts.
- [NotWorking](https://notworking.io) `https://notworking.io/mcp`
  [![NotWorking MCP connector](https://glama.ai/mcp/connectors/io.notworking/notworking/badges/score.svg)](https://glama.ai/mcp/connectors/io.notworking/notworking)
  🔓 - Check if other agents report a site, skill or MCP server failing, see its other access paths, and report failures.
- [Pulse](https://pulse.allthepossibles.com) `https://pulse.allthepossibles.com/mcp`
  [![Pulse MCP connector](https://glama.ai/mcp/connectors/com.allthepossibles/pulse/badges/score.svg)](https://glama.ai/mcp/connectors/com.allthepossibles/pulse)
  🔓 - Real Core Web Vitals from the Chrome UX Report for any URL, with a pass or fail verdict.
- [Opservo](https://getopservo.com/docs/mcp) `https://api.getopservo.com/mcp`
  [![Opservo MCP connector](https://glama.ai/mcp/connectors/com.getopservo/opservo/badges/score.svg)](https://glama.ai/mcp/connectors/com.getopservo/opservo)
  🔐 - Ask why Linux servers and Kubernetes clusters are slow or failing: health, issues, logs, incident timelines. Read-only.
- [Relvato](https://www.relvato.com/developers) `https://app.relvato.com/api/mcp`
  [![Relvato MCP connector](https://glama.ai/mcp/connectors/com.relvato/relvato/badges/score.svg)](https://glama.ai/mcp/connectors/com.relvato/relvato)
  🔓 - Real-browser website monitoring, deepest on WordPress & WooCommerce: run checks, read results; tools need a free key.
- [Rius](https://docs.glassflow.ai/rius/mcp) `https://mcp.eu.console.rius-glassflow.com/mcp`
  [![Rius MCP connector](https://glama.ai/mcp/connectors/ai.glassflow/rius/badges/score.svg)](https://glama.ai/mcp/connectors/ai.glassflow/rius)
  🔐 - Query AI agent traces, errors, cost and alerts, compare agent versions, and manage alert rules.
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
- [Upstream](https://upstream-api.pages.dev) `https://upstream.toolweather.workers.dev/mcp`
  [![Upstream MCP connector](https://glama.ai/mcp/connectors/io.github.toolweather/upstream/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.toolweather/upstream)
  🔓 - Live status, incidents and model deprecations for ~40 AI and developer APIs, plus a daily digest.
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
- [Audexum](https://audexum.com/integrations/mcp) `https://audexum.com/mcp`
  [![Audexum MCP connector](https://glama.ai/mcp/connectors/com.audexum/audexum/badges/score.svg)](https://glama.ai/mcp/connectors/com.audexum/audexum)
  🔐 - Text to speech in 30+ languages as MP3 links, audio transcription, and YouTube transcripts.
- [Azurade AI](https://azurade.com/developers/) `https://azurade.com/mcp`
  [![Azurade AI MCP connector](https://glama.ai/mcp/connectors/com.azurade/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.azurade/mcp)
  🔐 - Generate images and videos with Veo 3.1, Seedance 2.5, Nano Banana Pro and 30+ more models; credits never expire.
- [BulkTranscripts](https://bulktranscripts.co) `https://bulktranscripts.co/mcp`
  [![BulkTranscripts MCP connector](https://glama.ai/mcp/connectors/co.bulktranscripts/youtube/badges/score.svg)](https://glama.ai/mcp/connectors/co.bulktranscripts/youtube)
  🔐 - YouTube transcripts for one video, a whole channel or a playlist, plus search and free new-upload tracking.
- [Cast](https://cast.katechon.technology/agents) `https://cast.katechon.technology/mcp`
  [![Cast MCP connector](https://glama.ai/mcp/connectors/technology.katechon/cast/badges/score.svg)](https://glama.ai/mcp/connectors/technology.katechon/cast)
  🔓 - Turn one line into a one-tap link for a short vertical AI character video; first video free.
- [CLIPCLIPER](https://clipcliper.com/mcp) `https://clipcliper.com/mcp`
  [![CLIPCLIPER MCP connector](https://glama.ai/mcp/connectors/com.clipcliper/clipcliper/badges/score.svg)](https://glama.ai/mcp/connectors/com.clipcliper/clipcliper)
  🔓 - Timestamped transcripts, chapters and clip ideas from YouTube, Twitch, Kick or TikTok links.
- [ClipUGC](https://clipugc.com) `https://clipugc.com/mcp`
  [![ClipUGC MCP connector](https://glama.ai/mcp/connectors/io.github.clipugc/clipugc/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.clipugc/clipugc)
  🔐 - Make UGC videos for mobile apps with AI influencers who keep the same face.
- [CrateWire](https://cratewire.com) `https://cratewire.com/mcp`
  [![CrateWire MCP connector](https://glama.ai/mcp/connectors/com.cratewire/cratewire/badges/score.svg)](https://glama.ai/mcp/connectors/com.cratewire/cratewire)
  🔐 - Find the tracks DJs play in Instagram, TikTok and set links; follow DJs, scan link lists and read your Radar.
- [Cucutime](https://cucutime.org/developers) `https://cucutime.org/mcp`
  [![Cucutime MCP connector](https://glama.ai/mcp/connectors/org.cucutime/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/org.cucutime/mcp)
  🔓 - Kids-song ideas, name song pages and CucuTime YouTube catalog search; an optional key adds AI songs for adult apps.
- [CWI Discovery Engine](https://github.com/CumulativeWebInc/cwi-learn) `https://cwi-machine-data.hp-ace.workers.dev/mcp`
  [![CWI Discovery Engine MCP connector](https://glama.ai/mcp/connectors/io.github.CumulativeWebInc/cwi-discovery-engine/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.CumulativeWebInc/cwi-discovery-engine)
  🔓 - Machine-readable catalog of the Cumulative Web Inc label: track search, sync briefs, live Radio 365, playlist pitching.
- [Dora](https://doravideo.com) `https://doravideo.com/mcp`
  [![Dora MCP connector](https://glama.ai/mcp/connectors/io.github.Saga-Labs/dora-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Saga-Labs/dora-mcp)
  🔐 - Generate finished AI videos and images from a prompt or a photo.
- [eroq](https://eroq.ai/mcp) `https://eroq.ai/mcp`
  [![eroq MCP connector](https://glama.ai/mcp/connectors/ai.eroq/eroq/badges/score.svg)](https://glama.ai/mcp/connectors/ai.eroq/eroq)
  🔐 - Generate videos, images, voices and songs on Seedance, Kling, Veo and eroq's own uncensored engines.
- [Flow Music MCP Server by useapi.net](https://useapi.net/docs/api-flowmusic-v1/mcp) `https://api.useapi.net/v1/flowmusic/mcp`
  [![Flow Music MCP Server by useapi.net MCP connector](https://glama.ai/mcp/connectors/net.useapi/flowmusic/badges/score.svg)](https://glama.ai/mcp/connectors/net.useapi/flowmusic)
  🔐 - Google Flow Music (Lyria 3.5) songs, covers, remixes and stems on your own account. Not affiliated with Google.
- [FXI Studio](https://www.fxi.studio/mcp/info) `https://mcp.fxi.studio/mcp`
  [![FXI Studio MCP connector](https://glama.ai/mcp/connectors/io.github.fueledximagination/fxi-studio/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.fueledximagination/fxi-studio)
  🔐 - Generate cinematic images and video clips and frame-chain shots into continuous motion, billed to your FXI credits.
- [Google Flow Agent MCP Server by useapi.net](https://useapi.net/docs/api-google-flow-v1/mcp) `https://api.useapi.net/v1/google-flow/mcp`
  [![Google Flow Agent MCP Server by useapi.net MCP connector](https://glama.ai/mcp/connectors/net.useapi/google-flow/badges/score.svg)](https://glama.ai/mcp/connectors/net.useapi/google-flow)
  🔐 - Chat with Google Flow Agent: it plans and makes images and videos on your Google AI subscription. Not Google-affiliated.
- [Google Vids MCP Server by useapi.net](https://useapi.net/docs/api-google-vids-v1/mcp) `https://api.useapi.net/v1/google-vids/mcp`
  [![Google Vids MCP Server by useapi.net MCP connector](https://glama.ai/mcp/connectors/net.useapi/google-vids/badges/score.svg)](https://glama.ai/mcp/connectors/net.useapi/google-vids)
  🔐 - Gemini Omni video with sound and voiced avatars in Google Vids on your Google plan. Not affiliated with Google.
- [GrooveSheet](https://www.groovesheet.net/developers) `https://api.groovesheet.net/mcp`
  [![GrooveSheet MCP connector](https://glama.ai/mcp/connectors/net.groovesheet/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/net.groovesheet/mcp)
  🔐 - Find sheet music, tabs and MIDI for songs, and transcribe your own recordings via one-time upload links.
- [GrowingUpVideo](https://growingupvideo.com) `https://growingupvideo.com/mcp`
  [![GrowingUpVideo MCP connector](https://glama.ai/mcp/connectors/com.growingupvideo/growingupvideo/badges/score.svg)](https://glama.ai/mcp/connectors/com.growingupvideo/growingupvideo)
  🔓 - Prices, photo tips and a start link for AI growing-up morph videos made from photos across the years.
- [Incarn](https://www.incarn.co/developers) `https://api.incarn.co/mcp`
  [![Incarn MCP connector](https://glama.ai/mcp/connectors/co.incarn/photo-animation/badges/score.svg)](https://glama.ai/mcp/connectors/co.incarn/photo-animation)
  🔓 - Animate old family photos and ancestor portraits into short lifelike videos.
- [invideo](https://invideo.io) `https://mcp.invideo.io/mcp`
  🔓 - Generate and edit videos from a prompt.
- [Kelpo](https://kelpo.app) `https://kelpo.app/api/mcp`
  [![Kelpo MCP connector](https://glama.ai/mcp/connectors/app.kelpo/kelpo/badges/score.svg)](https://glama.ai/mcp/connectors/app.kelpo/kelpo)
  🔐 - Create vertical UGC-style videos with AI actors or your own photo and voice, with automatic Shorts-style editing.
- [Kinetune](https://kinetune.com/developers#mcp) `https://kinetune.com/mcp`
  [![Kinetune MCP connector](https://glama.ai/mcp/connectors/com.kinetune/kinetune/badges/score.svg)](https://glama.ai/mcp/connectors/com.kinetune/kinetune)
  🔐 - Word-synced lyric videos (9:16, 16:9, 1:1) and Spotify Canvas loops from your songs, quoted in credits first.
- [Kleo](https://kleooai.com) `https://mcp.kleooai.com/mcp`
  [![Kleo MCP connector](https://glama.ai/mcp/connectors/com.kleooai/kleo/badges/score.svg)](https://glama.ai/mcp/connectors/com.kleooai/kleo)
  🔐 - Narrated 4K 60 fps films from a brief, realistic or animated, with every shot generated.
- [Katto](https://katto.tech) `https://mcp.katto.tech/mcp`
  🔐 - Turn long videos, podcasts and Twitch VODs into scored, captioned, vertical 9:16 clips.
- [Kling AI MCP Server by useapi.net](https://useapi.net/docs/api-kling-v1/mcp) `https://api.useapi.net/v1/kling/mcp`
  [![Kling AI MCP Server by useapi.net MCP connector](https://glama.ai/mcp/connectors/net.useapi/kling/badges/score.svg)](https://glama.ai/mcp/connectors/net.useapi/kling)
  🔐 - Kling 4.0, v3 and Omni video, avatars, lip-sync and images on your own Kling account. Not affiliated with Kuaishou.
- [Klox](https://klox.ai/agent) `https://klox.ai/mcp`
  [![Klox MCP connector](https://glama.ai/mcp/connectors/ai.klox/klox/badges/score.svg)](https://glama.ai/mcp/connectors/ai.klox/klox)
  🔐 - Plan and edit AI videos on canvases: script, storyboard, shots and final cut.
- [Lexu](https://www.lexu.io/en/developers) `https://www.lexu.io/mcp`
  [![Lexu MCP connector](https://glama.ai/mcp/connectors/io.lexu/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.lexu/mcp)
  🔐 - Generate images, videos, music and voice-overs on one credit balance, priced before each job.
- [LiveReacting](https://www.livereacting.com/mcp) `https://mcp.livereacting.com/mcp`
  [![LiveReacting MCP connector](https://glama.ai/mcp/connectors/com.livereacting/livereacting/badges/score.svg)](https://glama.ai/mcp/connectors/com.livereacting/livereacting)
  🔐 - Run 24/7 live streams of pre-recorded videos, or stream a recorded video at a set time to YouTube, Facebook and more.
- [Mage](https://www.mage.space/mcp) `https://mcp.mage.space/mcp`
  [![Mage MCP connector](https://glama.ai/mcp/connectors/space.mage/mage/badges/score.svg)](https://glama.ai/mcp/connectors/space.mage/mage)
  🔐 - Generate images, video, and audio with many frontier models, with the price quoted before each run.
- [MaxVideoAI](https://maxvideoai.com/mcp) `https://api.maxvideoai.com/mcp`
  [![MaxVideoAI MCP connector](https://glama.ai/mcp/connectors/com.maxvideoai/maxvideoai/badges/score.svg)](https://glama.ai/mcp/connectors/com.maxvideoai/maxvideoai)
  🔐 - Compare AI video models, quote requests, approve paid generations, and recover results in a shared library.
- [Meta Muse MCP Server by useapi.net](https://useapi.net/docs/api-muse-v1/mcp) `https://api.useapi.net/v1/muse/mcp`
  [![Meta Muse MCP Server by useapi.net MCP connector](https://glama.ai/mcp/connectors/net.useapi/muse/badges/score.svg)](https://glama.ai/mcp/connectors/net.useapi/muse)
  🔐 - Meta Muse (muse.ai) agent chat, images and 10-second videos with sound on your Muse subscription. Not Meta-affiliated.
- [MockClip](https://mockclip.com/integrations) `https://mockclip.com/api/mcp`
  [![MockClip MCP connector](https://glama.ai/mcp/connectors/com.mockclip/mockclip/badges/score.svg)](https://glama.ai/mcp/connectors/com.mockclip/mockclip)
  🔑 - Create fake chat and phone-screen videos (WhatsApp, iMessage, ChatGPT, Discord, Tinder, Reddit) as MP4.
- [MomentClip](https://momentclip.com) `https://momentclip.com/mcp`
  [![MomentClip MCP connector](https://glama.ai/mcp/connectors/com.momentclip/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.momentclip/mcp)
  🔐 - Find moments in YouTube videos by what's said or shown, ask cited questions and export clips and transcripts.
- [Mureka MCP Server by useapi.net](https://useapi.net/docs/api-mureka-v1/mcp) `https://api.useapi.net/v1/mureka/mcp`
  [![Mureka MCP Server by useapi.net MCP connector](https://glama.ai/mcp/connectors/net.useapi/mureka/badges/score.svg)](https://glama.ai/mcp/connectors/net.useapi/mureka)
  🔐 - Mureka songs in your own voice, stems, sheet music and speech on your Mureka account. Not affiliated with Mureka.
- [Phoenix Labs](https://phoenixlabs.space/developers) `https://api.phoenixlabs.space/mcp`
  [![Phoenix Labs MCP connector](https://glama.ai/mcp/connectors/io.github.thekillsquad007/phoenix-labs/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.thekillsquad007/phoenix-labs)
  🔐 - Restore old video and turn stills into clips with sound; you approve a spending limit, top-ups by card or USDC.
- [Pixly](https://pixly.app) `https://pixly.app/api/mcp`
  [![Pixly MCP connector](https://glama.ai/mcp/connectors/app.pixly/pixly/badges/score.svg)](https://glama.ai/mcp/connectors/app.pixly/pixly)
  🔓 - Stage, declutter, and enhance real-estate listing photos, and turn them into listing videos.
- [PodcastsToText](https://podcaststotext.com) `https://podcaststotext.com/api/mcp`
  [![PodcastsToText MCP connector](https://glama.ai/mcp/connectors/com.podcaststotext/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.podcaststotext/mcp)
  🔐 - Transcribe Spotify, Apple Podcasts, YouTube and TikTok links, then make show notes, chapters and translations.
- [Qencode](https://qencode.com) `https://mcp.qencode.com/mcp`
  [![Qencode MCP connector](https://glama.ai/mcp/connectors/com.qencode/qencode/badges/score.svg)](https://glama.ai/mcp/connectors/com.qencode/qencode)
  🔐 - Transcode video to HLS/MP4, monitor jobs, and manage Qencode Media Storage.
- [QQuickpick](https://qquickpick.com/agents/mcp) `https://qquickpick.com/mcp`
  [![QQuickpick MCP connector](https://glama.ai/mcp/connectors/io.github.Ravesteijntjes/qquickpick/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Ravesteijntjes/qquickpick)
  🔓 - Search movies and TV shows by mood, genre and score, filtered to what streams in your country.
- [RaoMusic](https://www.raomusic.com/plugin) `https://www.raomusic.com/api/mcp`
  [![RaoMusic MCP connector](https://glama.ai/mcp/connectors/io.github.raomusic/raomusic/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.raomusic/raomusic)
  🔐 - Generate full songs with vocals, instrumentals and sound effects from text, quoted in credits first.
- [RiverScript](https://riverscript.com/docs/platform-details/mcp) `https://riverscript.com/mcp`
  [![RiverScript MCP connector](https://glama.ai/mcp/connectors/com.riverscript/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.riverscript/mcp)
  🔓 - Get the text of any transcript or translation shared with a RiverScript share link.
- [RiverScript MCP v2](https://riverscript.com/docs/platform-details/mcp) `https://riverscript.com/api/mcp/v2`
  [![RiverScript MCP v2 MCP connector](https://glama.ai/mcp/connectors/com.riverscript/mcp-v2/badges/score.svg)](https://glama.ai/mcp/connectors/com.riverscript/mcp-v2)
  🔐 - Bring your RiverScript transcripts of meetings, calls and interviews to any AI agent: search, read and summarize.
- [SceneF](https://scenef.com/agents) `https://scenef.com/mcp`
  [![SceneF MCP connector](https://glama.ai/mcp/connectors/com.scenef/showtimes/badges/score.svg)](https://glama.ai/mcp/connectors/com.scenef/showtimes)
  🔓 - Movie showtimes across 33 California and Hawaii boards, re-verified against each theater's own calendar.
- [ScoreStarling](https://scorestarling.com) `https://mcp.scorestarling.com/mcp`
  [![ScoreStarling MCP connector](https://glama.ai/mcp/connectors/com.scorestarling/scorestarling/badges/score.svg)](https://glama.ai/mcp/connectors/com.scorestarling/scorestarling)
  🔐 - Turn recordings, sheet-music photos, PDFs and MIDI into editable scores, then play, edit and export them.
- [Screen Browser](https://screenbrowser.com) `https://mcp.screenbrowser.com`
  [![Screen Browser MCP connector](https://glama.ai/mcp/connectors/com.screenbrowser/screenbrowser/badges/score.svg)](https://glama.ai/mcp/connectors/com.screenbrowser/screenbrowser)
  🔐 - Records narrated demo and tutorial videos of your web app from a plain-language guide, on desktop or as a phone.
- [ScreenWeaver](https://www.screenweaver.ai/mcp) `https://app.screenweaver.ai/api/mcp`
  [![ScreenWeaver MCP connector](https://glama.ai/mcp/connectors/ai.screenweaver/screenweaver/badges/score.svg)](https://glama.ai/mcp/connectors/ai.screenweaver/screenweaver)
  🔐 - Write and edit screenplays, import Final Draft or Fountain scripts and turn scenes or comic pages into storyboard shots.
- [SFXMint](https://sfxmint.com) `https://sfxmint.com/mcp`
  [![SFXMint MCP connector](https://glama.ai/mcp/connectors/com.sfxmint/sounds/badges/score.svg)](https://glama.ai/mcp/connectors/com.sfxmint/sounds)
  🔓 - Ask for a sound effect by role or take a ready-made kit; 4,600+ CC0 files with permanent hotlinkable URLs.
- [Shortform Kit](https://shortformkit.com/mcp-server/) `https://shortformkit.com/mcp`
  [![Shortform Kit MCP connector](https://glama.ai/mcp/connectors/io.github.diegobruegger-prog/shortformkit/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.diegobruegger-prog/shortformkit)
  🔓 - Transcribe and read public Reels, TikToks and Shorts, plus sourced creator data: upload specs and loudness targets.
- [snapWONDERS Vaultify](https://snapwonders.com/developers) `https://snapwonders.com/mcp`
  [![snapWONDERS Vaultify MCP connector](https://glama.ai/mcp/connectors/com.snapwonders/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.snapwonders/mcp)
  🔓 - Forensic photo and video analysis, hidden-file steganography and media format conversion.
- [Soundza](https://soundza.com/developers) `https://mcp.soundza.com/mcp/oauth`
  [![Soundza MCP connector](https://glama.ai/mcp/connectors/com.soundza/soundza/badges/score.svg)](https://glama.ai/mcp/connectors/com.soundza/soundza)
  🔐 - Search and download free sound effects, music and ambience, with rich metadata and previews.
- [StudioSphere Pulse](https://pulse.studiosphere.space) `https://mcp.studiosphere.space/mcp`
  [![StudioSphere Pulse MCP connector](https://glama.ai/mcp/connectors/space.studiosphere/pulse/badges/score.svg)](https://glama.ai/mcp/connectors/space.studiosphere/pulse)
  🔓 - Audio analysis for authorized public URLs: BPM, musical key, and waveform peaks.
- [TranscriptAPI](https://transcriptapi.io/mcp) `https://api.transcriptapi.io/mcp`
  [![TranscriptAPI MCP connector](https://glama.ai/mcp/connectors/io.transcriptapi/youtube-transcript/badges/score.svg)](https://glama.ai/mcp/connectors/io.transcriptapi/youtube-transcript)
  🔓 - YouTube transcripts with timestamps, plus video search, channel uploads and playlists. Calls need a free API key.
- [Transkriba](https://transkriba.ru/mcp) `https://transkriba.ru/api/mcp`
  [![Transkriba MCP connector](https://glama.ai/mcp/connectors/ru.transkriba/transcription/badges/score.svg)](https://glama.ai/mcp/connectors/ru.transkriba/transcription)
  🔓 - Transcribe Russian audio and video from files or URLs; tools need a key.
- [Treza](https://www.trezalabs.com/connect) `https://www.trezalabs.com/api/mcp`
  [![Treza MCP connector](https://glama.ai/mcp/connectors/io.github.treza-labs/treza/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.treza-labs/treza)
  🔐 - Video pipelines that script, render, narrate, caption and publish to YouTube and TikTok.
- [TubeText TikTok Transcripts](https://apify.com/tubetext/tiktok-transcript) `https://mcp.apify.com/?tools=fetch-actor-details,tubetext/tiktok-transcript,tubetext/video-breakdown-ai,tubetext/shot-by-shot-video-analysis`
  [![TubeText TikTok Transcripts MCP connector](https://glama.ai/mcp/connectors/io.github.LMSlay/tubetext-tiktok-transcripts/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.LMSlay/tubetext-tiktok-transcripts)
  🔐 - TikTok transcripts (captions or Whisper), quick AI breakdowns and shot-by-shot analysis of any video.
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
- [VideoBGRemover](https://videobgremover.net/mcp) `https://videobgremover.net/api/mcp`
  [![VideoBGRemover MCP connector](https://glama.ai/mcp/connectors/net.videobgremover/video-background-remover/badges/score.svg)](https://glama.ai/mcp/connectors/net.videobgremover/video-background-remover)
  🔐 - Remove video backgrounds, track processing tasks, and download transparent WebM with source audio.
- [VideoGen](https://videogen.io/videogen-mcp) `https://mcp.videogen.io/mcp`
  [![VideoGen MCP connector](https://glama.ai/mcp/connectors/io.github.dg314/videogen/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.dg314/videogen)
  🔐 - Create videos from scripts and storyboards, manage projects, and export finished videos.
- [Vidova](https://vidova.ai) `https://mcp.vidova.ai/mcp`
  [![Vidova MCP connector](https://glama.ai/mcp/connectors/ai.vidova/vidova/badges/score.svg)](https://glama.ai/mcp/connectors/ai.vidova/vidova)
  🔐 - Edit videos on a real timeline, generate clips, music and voice, track faces and render finished cuts.
- [Words into Music](https://wordsintomusic.com/mcp/) `https://mcp.wordsintomusic.com/mcp`
  [![Words into Music MCP connector](https://glama.ai/mcp/connectors/com.wordsintomusic.mcp/words-into-music/badges/score.svg)](https://glama.ai/mcp/connectors/com.wordsintomusic.mcp/words-into-music)
  🔐 - Generate songs from prompts or lyrics, check credits, and access your private song library.
- [Zebu Data - YouTube Data & Transcripts](https://apify.com/delicious_zebu) `https://mcp.apify.com/?tools=delicious_zebu/youtube-video-scraper-by-keyword,delicious_zebu/youtube-channel-video-scraper,delicious_zebu/youtube-video-data-scraper,delicious_zebu/youtube-comments-replies-scraper,delicious_zebu/youtube-transcript-scraper`
  [![Zebu Data - YouTube Data & Transcripts MCP connector](https://glama.ai/mcp/connectors/io.github.zebudata/youtube-data/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.zebudata/youtube-data)
  🔐 - YouTube search, whole channels, video stats, comments and full transcripts with timestamps.
- [ZoneFoundry for Sonos](https://zonefoundry.dev/guides/ai-agent-control/) `https://relay.zonefoundry.dev/mcp`
  [![ZoneFoundry for Sonos MCP connector](https://glama.ai/mcp/connectors/dev.zonefoundry/sonos/badges/score.svg)](https://glama.ai/mcp/connectors/dev.zonefoundry/sonos)
  🔐 - Control your Sonos speakers: play music, set volume, group rooms, move playback, announcements and reminders.

### 💳 <a name="payments"></a>Payments

- [402MCP](https://402mcp.org) `https://402mcp.org/api/v1/mcp`
  [![402MCP MCP connector](https://glama.ai/mcp/connectors/org.402mcp/registry/badges/score.svg)](https://glama.ai/mcp/connectors/org.402mcp/registry)
  🔓 - Decodes HTTP 402 challenges (L402, x402, MPP) and recommends agent payment rails from an open registry.
- [Aether](https://explorer.157-245-252-221.sslip.io) `https://explorer.157-245-252-221.sslip.io/mcp`
  [![Aether MCP connector](https://glama.ai/mcp/connectors/io.github.whoyoujoshin/aether-wallet/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.whoyoujoshin/aether-wallet)
  🔓 - Read-only view of the Aether testnet: balances, transactions, miners and its directory of x402-paid services.
- [agentpay](https://entangleit.com/agentpay/) `https://entangleit.com/api/agentpay/mcp`
  [![agentpay MCP connector](https://glama.ai/mcp/connectors/com.entangleit/agentpay/badges/score.svg)](https://glama.ai/mcp/connectors/com.entangleit/agentpay)
  🔓 - Pay-per-call LLM (Fuse) and x402 APIs paid in BSV sats from prepaid agent wallets; free trial wallet, chat needs a key.
- [AurasPay](https://auraspay.com/mcp) `https://mcp.auraspay.com/api/mcp`
  [![AurasPay MCP connector](https://glama.ai/mcp/connectors/com.auraspay/merchant-payments/badges/score.svg)](https://glama.ai/mcp/connectors/com.auraspay/merchant-payments)
  🔐 - Review merchant payments and prepare payment links with separate human approval for changes.
- [AssetFare](https://assetfare.dev) `https://api.assetfare.dev/mcp`
  [![AssetFare MCP connector](https://glama.ai/mcp/connectors/io.github.odaiin/assetfare/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.odaiin/assetfare)
  🔓 - Compare and prepare non-custodial SOL to Base or Arbitrum ETH routes for you to sign.
- [BotsRated](https://botsrated.com) `https://botsrated.com/mcp`
  [![BotsRated MCP connector](https://glama.ai/mcp/connectors/com.botsrated/botsrated/badges/score.svg)](https://glama.ai/mcp/connectors/com.botsrated/botsrated)
  🔓 - Look up measured status, 402 validity, latency, price and payTo of paid x402 APIs on Base before paying.
- [Checkout Page](https://checkoutpage.com) `https://mcp.checkoutpage.com`
  [![Checkout Page MCP connector](https://glama.ai/mcp/connectors/com.checkoutpage/checkout-page/badges/score.svg)](https://glama.ai/mcp/connectors/com.checkoutpage/checkout-page)
  🔐 - Create checkout pages, events and forms, and manage payments, bookings, subscriptions, customers and coupons.
- [Dodo Payments](https://dodopayments.com) `https://mcp.dodopayments.com/mcp`
  🔐 - Manage Dodo Payments products, subscriptions, and payouts.
- [Kulhad](https://kulhad.co) `https://kulhad.co/mcp`
  [![Kulhad MCP connector](https://glama.ai/mcp/connectors/co.kulhad/kulhad/badges/score.svg)](https://glama.ai/mcp/connectors/co.kulhad/kulhad)
  🔓 - Run a creator's UPI support page in India: approve and thank supporters, set goals, edit the page, get QR codes.
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
- [SpendGate](https://spendgate.toolweather.workers.dev) `https://spendgate.toolweather.workers.dev/mcp`
  [![SpendGate MCP connector](https://glama.ai/mcp/connectors/io.github.toolweather/spendgate/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.toolweather/spendgate)
  🔓 - Score a planned spend before an agent pays (approve / ask_human / block). Free tier; overage via x402 USDC on Base.
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
- [Voicescape](https://voicescape.vercel.app) `https://voicescape.vercel.app/api/mcp`
  [![Voicescape MCP connector](https://glama.ai/mcp/connectors/io.github.VoiceScapee/voicescape/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.VoiceScapee/voicescape)
  🔓 - On-chain blockpages for AI agents with atomic 98/2 tips and payment-backed reviews.
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
- [Critical Path Partners](https://criticalpathpartners.ca/connect-claude.html) `https://mcp.criticalpathpartners.ca/mcp`
  [![Critical Path Partners MCP connector](https://glama.ai/mcp/connectors/io.github.danafitkowski/cpp-cpm-engine/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.danafitkowski/cpp-cpm-engine)
  🔓 - Forensic delay analysis of Primavera P6 schedules: windows analysis, time impact, DCMA-14 checks and Monte Carlo risk.
- [dot•requirements](https://dotrequirements.io) `https://app.dotrequirements.io/mcp`
  [![dot•requirements MCP connector](https://glama.ai/mcp/connectors/io.dotrequirements/dotrequirements/badges/score.svg)](https://glama.ai/mcp/connectors/io.dotrequirements/dotrequirements)
  🔐 - Draft testable requirements specs from chat, style-check them, publish to your team, and see test coverage.
- [Edworking MCP](https://mcp.edworking.com) `https://mcp.edworking.com/mcp`
  [![Edworking MCP connector](https://glama.ai/mcp/connectors/io.github.Edworking/edworking-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Edworking/edworking-mcp)
  🔐 - Read and manage Edworking projects, tasks, conversations and files with scoped access.
- [Entalpa](https://entalpa.com/en/connect) `https://api.entalpa.com/mcp`
  [![Entalpa MCP connector](https://glama.ai/mcp/connectors/com.entalpa/requirements/badges/score.svg)](https://glama.ai/mcp/connectors/com.entalpa/requirements)
  🔐 - Spec-driven development for AI coding agents: generate and manage stories, requirements and traceability links.
- [Flowmaps](https://flowmaps.app) `https://flowmaps.app/api/mcp`
  [![Flowmaps MCP connector](https://glama.ai/mcp/connectors/app.flowmaps/flowmaps/badges/score.svg)](https://glama.ai/mcp/connectors/app.flowmaps/flowmaps)
  🔐 - Plan apps in build order: list ventures and Ready features, add ideas, and read step-by-step build plans.
- [FrameOn](https://app.frameonlab.com/mcp) `https://api.frameonlab.com/api/v1/mcp`
  [![FrameOn MCP connector](https://glama.ai/mcp/connectors/com.frameonlab/frameon/badges/score.svg)](https://glama.ai/mcp/connectors/com.frameonlab/frameon)
  🔐 - Project management for AI agents: tasks, docs, decisions and time in one shared team context.
- [GTD Brain](https://gtdbrain.com/connect?source=awesome-remote-mcp-servers) `https://mcp.gtdbrain.com/api/gtdbrain/v1/mcp`
  [![GTD Brain MCP connector](https://glama.ai/mcp/connectors/com.gtdbrain/gtd-brain/badges/score.svg)](https://glama.ai/mcp/connectors/com.gtdbrain/gtd-brain)
  🔐 - Getting Things Done board: inbox capture, next actions by context, projects and weekly review.
- [Joxo](https://joxo.ai) `https://joxo.ai/api/mcp`
  [![Joxo MCP connector](https://glama.ai/mcp/connectors/ai.joxo/joxo/badges/score.svg)](https://glama.ai/mcp/connectors/ai.joxo/joxo)
  🔐 - Shared tasks, handoffs and decisions for your team and its AI coding agents.
- [Kaiku](https://kaiku.tech/en/docs/mcp) `https://mcp.kaiku.tech/mcp`
  [![Kaiku MCP connector](https://glama.ai/mcp/connectors/tech.kaiku.mcp/kaiku/badges/score.svg)](https://glama.ai/mcp/connectors/tech.kaiku.mcp/kaiku)
  🔓 - Issue tracker with a wiki for people and AI agents: search, file and update issues, comment, read and write pages.
- [Laraue Boards](https://boards.laraue.com) `https://boards.laraue.com/boards-mcp/mcp`
  [![Laraue Boards MCP connector](https://glama.ai/mcp/connectors/com.laraue/boards/badges/score.svg)](https://glama.ai/mcp/connectors/com.laraue/boards)
  🔑 - List, view, create, edit, and move issues in your Laraue Boards organization.
- [Leemu](https://leemu.io/claude-integration) `https://app.leemu.io/api/mcp`
  [![Leemu MCP connector](https://glama.ai/mcp/connectors/io.leemu/okr/badges/score.svg)](https://glama.ai/mcp/connectors/io.leemu/okr)
  🔐 - Read OKRs, submit key-result check-ins, find at-risk goals, and generate progress reports.
- [Linear](https://linear.app) `https://mcp.linear.app/mcp`
  [![Linear MCP connector](https://glama.ai/mcp/connectors/app.linear/linear/badges/score.svg)](https://glama.ai/mcp/connectors/app.linear/linear)
  🔐 - Manage Linear issues, projects, and cycles.
- [Madda Tasks](https://www.maddatech.com/mcp.html) `https://mcp.maddatech.com/mcp`
  [![Madda Tasks MCP connector](https://glama.ai/mcp/connectors/com.maddatech/madda-tasks/badges/score.svg)](https://glama.ai/mcp/connectors/com.maddatech/madda-tasks)
  🔐 - Create and schedule projects and tasks, manage dependencies, baselines, reports and AI agents in Madda Tasks.
- [MCPBinder](https://www.mcpbinder.com) `https://www.mcpbinder.com/api/mcp`
  [![MCPBinder MCP connector](https://glama.ai/mcp/connectors/io.github.ReedStories/mcpbinder/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ReedStories/mcpbinder)
  🔐 - Read project goals and tasks, plan work, and record decisions with scoped access.
- [mcptask.online](https://mcptask.online) `https://mcptask.online/mcp`
  [![mcptask.online MCP connector](https://glama.ai/mcp/connectors/online.mcptask/mcptaskonline/badges/score.svg)](https://glama.ai/mcp/connectors/online.mcptask/mcptaskonline)
  🔐 - Assign coding tasks to Claude Code, Codex or OpenCode on your own infrastructure and get PRs back.
- [monday.com](https://monday.com) `https://mcp.monday.com/mcp`
  🔐 - Manage monday.com boards, items, and updates.
- [Orbit](https://orbit.noveum.ai) `https://orbit.noveum.ai/mcp`
  [![Orbit MCP connector](https://glama.ai/mcp/connectors/io.github.Noveum/orbit/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Noveum/orbit)
  🔐 - Manage issues, projects, sprints, docs and files.
- [OrgGen AI](https://www.orggen.ai/mcp) `https://www.orggen.ai/api/mcp`
  [![OrgGen AI MCP connector](https://glama.ai/mcp/connectors/ai.orggen/orggen/badges/score.svg)](https://glama.ai/mcp/connectors/ai.orggen/orggen)
  🔑 - Human-agent interface for projects: you prioritize and decide, your AI agents execute.
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

- [AskRentAI](https://askrentai.com) `https://api.askrentai.com/mcp`
  [![AskRentAI MCP connector](https://glama.ai/mcp/connectors/com.askrentai/askrentai/badges/score.svg)](https://glama.ai/mcp/connectors/com.askrentai/askrentai)
  🔐 - Read-only live Rent Manager portfolio data: NOI, rent roll, delinquency, leasing, work orders, and financial reports.
- [Assetfy](https://assetfy.com/produkt/ai-mcp-anbindung/) `https://mcp.assetfy.com/mcp`
  [![Assetfy MCP connector](https://glama.ai/mcp/connectors/com.assetfy/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.assetfy/mcp)
  🔐 - German property data: parcels, zoning plans with PDFs, land values, LoD2 buildings and listings.
- [baseray](https://baseray.ai/docs/mcp) `https://api.baseray.ai/mcp`
  [![baseray MCP connector](https://glama.ai/mcp/connectors/ai.baseray/baseray/badges/score.svg)](https://glama.ai/mcp/connectors/ai.baseray/baseray)
  🔐 - Building data: address, use, size, height, age, roof, solar panels and registered businesses.
- [Brainy Prices](https://prices.brainy.ae/developers.html) `https://prices.brainy.ae/mcp/v2`
  [![Brainy Prices MCP connector](https://glama.ai/mcp/connectors/ae.brainy/grocery-prices/badges/score.svg)](https://glama.ai/mcp/connectors/ae.brainy/grocery-prices)
  🔓 - UAE living costs: KHDA fees, DLD rents, fuel, utilities, telecom and relocation, with dated sources.
- [Building Permits API](https://apify.com/gaelasao/planning-data-au-nz-fr) `https://mcp.apify.com/?tools=gaelasao/planning-data-au-nz-fr`
  [![Building Permits API MCP connector](https://glama.ai/mcp/connectors/io.github.gaelasao/building-permits-api/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.gaelasao/building-permits-api)
  🔐 - Official building permits and planning applications for France, NSW Australia and Far North NZ, with sources.
- [Casafari Comparables](https://developers.casafari.com/docs/comparables-valuation) `https://platform.casafari.com/mcp/comparables`
  [![Casafari Comparables MCP connector](https://glama.ai/mcp/connectors/com.casafari/comparables/badges/score.svg)](https://glama.ai/mcp/connectors/com.casafari/comparables)
  🔐 - Comparable properties and price estimates for a home in Europe, by address, coordinates or Spanish cadastral reference.
- [CoworkingView](https://coworkingview.com/en/mcp) `https://mcp.coworkingview.com/mcp`
  [![CoworkingView MCP connector](https://glama.ai/mcp/connectors/com.coworkingview/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.coworkingview/mcp)
  🔓 - Search coworking spaces and private offices in 62 cities, with published prices and market rates.
- [Dominick Prevete: Instant DSCR Term Sheet](https://dominickprevete.com/instant-term-sheet) `https://dominickprevete.com/api/mcp/pricing`
  [![Dominick Prevete: Instant DSCR Term Sheet MCP connector](https://glama.ai/mcp/connectors/com.dominickprevete/instant-term-sheet/badges/score.svg)](https://glama.ai/mcp/connectors/com.dominickprevete/instant-term-sheet)
  🔓 - Written DSCR term sheets by email for business-purpose loans on 1-4 unit US investment property.

- [Dominick Prevete: Instant Fix-and-Flip Term Sheet](https://dominickprevete.com/fix-and-flip-loans#connect) `https://dominickprevete.com/api/mcp/fix-and-flip`
  [![Dominick Prevete: Instant Fix-and-Flip Term Sheet MCP connector](https://glama.ai/mcp/connectors/com.dominickprevete/instant-fix-and-flip-term-sheet/badges/score.svg)](https://glama.ai/mcp/connectors/com.dominickprevete/instant-fix-and-flip-term-sheet)
  🔓 - Written fix-and-flip term sheets by email for business-purpose loans to buy and renovate 1-4 unit investment property.
- [Dubai Data](https://datadubai.ae/mcp/) `https://mcp.datadubai.ae/mcp`
  [![Dubai Data MCP connector](https://glama.ai/mcp/connectors/ae.datadubai/dubai-real-estate/badges/score.svg)](https://glama.ai/mcp/connectors/ae.datadubai/dubai-real-estate)
  🔓 - Dubai property statistics from Land Department open data: prices, rents, yields, sales by area, project and developer.

- [Edifiable](https://edifiable.fr/api) `https://edifiable.fr/api/mcp`
  [![Edifiable MCP connector](https://glama.ai/mcp/connectors/fr.edifiable/edifiable/badges/score.svg)](https://glama.ai/mcp/connectors/fr.edifiable/edifiable)
  🔓 - French local zoning plans (PLU): rules per zone and street, quoted to the article, and building permit pieces.

- [Eigenheim Invest](https://eigenheim-invest.de/immobilienpreise-berlin/) `https://eigenheim-invest.de/mcp/`
  [![Eigenheim Invest MCP connector](https://glama.ai/mcp/connectors/io.github.magicSEO/eigenheim-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.magicSEO/eigenheim-mcp)
  🔓 - Berlin property prices per m² by locality, rental yields, land values 2026, population forecast and active listings.
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
- [Hercules](https://hercules.properties/integrations/mcp) `https://app.hercules.properties/mcp`
  [![Hercules MCP connector](https://glama.ai/mcp/connectors/properties.hercules/property-data/badges/score.svg)](https://glama.ai/mcp/connectors/properties.hercules/property-data)
  🔓 - NYC and US property records: owners, LLC lookups, portfolios, mortgages, NYC pre-foreclosures and investor searches.
- [HouseFile](https://www.housefile.app/mcp/about) `https://www.housefile.app/mcp`
  [![HouseFile MCP connector](https://glama.ai/mcp/connectors/app.housefile/licensing/badges/score.svg)](https://glama.ai/mcp/connectors/app.housefile/licensing)
  🔓 - Checks whether a property in England is in a council's selective or HMO licensing scheme.
- [Irish Rent Check](https://rent-check-production.up.railway.app/) `https://rent-check-production.up.railway.app/mcp`
  [![Irish rent check MCP connector](https://glama.ai/mcp/connectors/app.railway.up.rent-check-production/irish-rent-check/badges/score.svg)](https://glama.ai/mcp/connectors/app.railway.up.rent-check-production/irish-rent-check)
  🔓 - Irish rents by county (CSO/RTB), free; paid town and property-price tools return x402/MPP terms.
- [Kolmo Construction](https://www.kolmo.io/developers) `https://www.kolmo.io/mcp`
  [![Kolmo Construction MCP connector](https://glama.ai/mcp/connectors/io.kolmo/kolmo-construction/badges/score.svg)](https://glama.ai/mcp/connectors/io.kolmo/kolmo-construction)
  🔓 - WA permit rules for 80+ cities, parcel zoning, contractor license checks and Seattle cost estimates.
- [Kvartiry-Phuket](https://kvartiry-phuket.com/otkrytye-dannye/#english) `https://kvartiry-phuket.com/mcp`
  [![Kvartiry-Phuket MCP connector](https://glama.ai/mcp/connectors/com.kvartiry-phuket/phuket/badges/score.svg)](https://glama.ai/mcp/connectors/com.kvartiry-phuket/phuket)
  🔓 - Russian-language Phuket property guides, districts, asking prices and condo assessment rates, plus weather and beaches.
- [LenDb.ai](https://lendb.ai/developers) `https://lendb.ai/mcp`
  [![LenDb.ai MCP connector](https://glama.ai/mcp/connectors/ai.lendb/lendb/badges/score.svg)](https://glama.ai/mcp/connectors/ai.lendb/lendb)
  🔓 - Find US mortgage loan officers by loan type, place and language, with sourced, dated facts.
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
- [RemplirPDF](https://remplirpdf.fr/mcp) `https://remplirpdf.fr/api/mcp`
  [![RemplirPDF MCP connector](https://glama.ai/mcp/connectors/fr.remplirpdf/mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/fr.remplirpdf/mcp-server)
  🔐 - French rental documents (leases, rent receipts, inventories, notices) filled and returned as PDFs.
- [Small Business Intelligence](https://brickandmortar.dev/connect/) `https://brickandmortar.dev/mcp`
  [![Small Business Intelligence MCP connector](https://glama.ai/mcp/connectors/io.github.2016judea/small-business-intelligence/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.2016judea/small-business-intelligence)
  🔓 - Free Twin Cities public records, parcels, sales, permits and licences, joined and queryable, plus research frameworks.
- [Tenantback](https://tenantback.com) `https://tenantback.com/mcp`
  [![Tenantback MCP connector](https://glama.ai/mcp/connectors/com.tenantback/cam-audit/badges/score.svg)](https://glama.ai/mcp/connectors/com.tenantback/cam-audit)
  🔓 - Audits a landlord's CAM reconciliation against the commercial lease; cites the clause behind each overcharge.
- [TrueFixR + AtlasCast](https://atlasunited.io/api) `https://mcp.atlasunited.io/mcp`
  [![TrueFixR + AtlasCast MCP connector](https://glama.ai/mcp/connectors/io.github.truefixr/atlascast-truefixr/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.truefixr/atlascast-truefixr)
  🔓 - Address-level storm event data and forecasted property risk API for AI agents.

- [Tradehand](https://tradehand.com) `https://tradehand.com/api/mcp`
  [![Tradehand MCP connector](https://glama.ai/mcp/connectors/io.github.Humanleap/tradehand/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Humanleap/tradehand)
  🔓 - Find local UK tradespeople, inspect real listings and service options, and return public profile links.
- [Zebu Data - Zillow Real Estate Data](https://apify.com/delicious_zebu) `https://mcp.apify.com/?tools=delicious_zebu/zillow-property-data-scraper,delicious_zebu/zillow-property-details-scraper`
  [![Zebu Data - Zillow Real Estate Data MCP connector](https://glama.ai/mcp/connectors/io.github.zebudata/real-estate-data/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.zebudata/real-estate-data)
  🔐 - Zillow listings and property details: price, Zestimate, rent estimate, history, schools, agents.
### 🚗 <a name="sales"></a>Sales

- [Alion](https://alion.io/developers/agents) `https://alion.io/mcp`
  [![Alion MCP connector](https://glama.ai/mcp/connectors/io.alion/alion/badges/score.svg)](https://glama.ai/mcp/connectors/io.alion/alion)
  🔐 - Find companies by industry, funding, stack and growth; lookalikes; startup, investor and due-diligence profiles.
- [Datamagnet](https://www.datamagnet.co/mcp/) `https://mcp.datamagnet.co/mcp`
  [![Datamagnet MCP connector](https://glama.ai/mcp/connectors/co.datamagnet/datamagnet/badges/score.svg)](https://glama.ai/mcp/connectors/co.datamagnet/datamagnet)
  🔐 - Live LinkedIn people, company and post data, ICP search and job-change signals for sales and recruiting agents.
- [EximAgent](https://eximagent.ai) `https://mcp.eximagent.ai/mcp`
  [![EximAgent MCP connector](https://glama.ai/mcp/connectors/ai.eximagent/eximagent/badges/score.svg)](https://glama.ai/mcp/connectors/ai.eximagent/eximagent)
  🔐 - AI agent team for export-import: find buyers and write outreach, analyze trade data, check HS codes, tariffs and OFAC.
- [Ficiel](https://ficiel.io/mcp/) `https://bridge.ficiel.io/mcp`
  [![Ficiel MCP connector](https://glama.ai/mcp/connectors/io.ficiel/ficiel/badges/score.svg)](https://glama.ai/mcp/connectors/io.ficiel/ficiel)
  🔐 - Read and search Instagram, WhatsApp and LinkedIn DMs, find prospects left unanswered, prepare follow-ups you approve.
- [Leadbase](https://www.leadbase.io) `https://www.leadbase.io/api/mcp`
  [![Leadbase MCP connector](https://glama.ai/mcp/connectors/io.leadbase/leadbase/badges/score.svg)](https://glama.ai/mcp/connectors/io.leadbase/leadbase)
  🔐 - Find qualified B2B leads, research DACH companies and enrich contacts with sources in editable sheets.
- [LinkMCP](https://app.linkmcp.io) `https://app.linkmcp.io/api/mcp`
  [![LinkMCP MCP connector](https://glama.ai/mcp/connectors/io.linkmcp/linkmcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.linkmcp/linkmcp)
  🔐 - Use your own LinkedIn account: profiles, people and Sales Navigator search, messages, posts, invites, email finder.
- [MailBeast.ai](https://mailbeast.ai) `https://mcp.mailbeast.ai/mcp`
  [![MailBeast.ai MCP connector](https://glama.ai/mcp/connectors/ai.mailbeast/mailbeast/badges/score.svg)](https://glama.ai/mcp/connectors/ai.mailbeast/mailbeast)
  🔐 - Cold email outreach: campaigns with A/B sequences, leads, mailboxes and warmup, reply inbox and campaign analytics.
- [Pinpoint dealership sales tools](https://usepinpoint.ai/resources/api/) `https://usepinpoint.ai/api/mcp`
  [![Pinpoint dealership sales tools MCP connector](https://glama.ai/mcp/connectors/ai.usepinpoint/pinpoint-dealership-sales-tools/badges/score.svg)](https://glama.ai/mcp/connectors/ai.usepinpoint/pinpoint-dealership-sales-tools)
  🔓 - Car dealership sales tools from Pinpoint, the sales intelligence platform for car dealerships.

- [PumpGTM](https://pumpgtm.com/docs/mcp) `https://mcp.pumpgtm.com/mcp`
  [![PumpGTM MCP connector](https://glama.ai/mcp/connectors/com.pumpgtm/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.pumpgtm/mcp)
  🔐 - Find buyers, run LinkedIn, email and X outreach from your own accounts, and approve drafted replies.
- [Quibbly](https://quibbly.co/linkedin-mcp) `https://server.quibbly.co/mcp`
  [![Quibbly MCP connector](https://glama.ai/mcp/connectors/co.quibbly/linkedin-inbox/badges/score.svg)](https://glama.ai/mcp/connectors/co.quibbly/linkedin-inbox)
  🔐 - Read your LinkedIn inbox, see who watched your videos, set follow-ups and draft replies you send yourself.
- [RecruitMCP](https://recruitmcp.com) `https://mcp.recruitmcp.com/mcp`
  [![RecruitMCP MCP connector](https://glama.ai/mcp/connectors/com.recruitmcp/recruitmcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.recruitmcp/recruitmcp)
  🔐 - Recruiting data for AI agents: search people and companies, enrich profiles, find email and phone via MCP.
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

- [AgingResearch.News](https://agingresearch.news/connect) `https://agingresearch.news/api/mcp`
  [![AgingResearch.News MCP connector](https://glama.ai/mcp/connectors/news.agingresearch/agingresearch-news/badges/score.svg)](https://glama.ai/mcp/connectors/news.agingresearch/agingresearch-news)
  🔓 - Search new aging research papers, their evidence, clinical trials, grants and drug programs; sign in to follow topics.
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
- [Fengshui Calculator](https://fengshuicalculator.com/docs/mcp/) `https://fengshuicalculator.com/v1/mcp`
  [![Fengshui Calculator MCP connector](https://glama.ai/mcp/connectors/com.fengshuicalculator/fengshui-calculator/badges/score.svg)](https://glama.ai/mcp/connectors/com.fengshuicalculator/fengshui-calculator)
  🔓 - Verifiable Chinese calendar & feng shui: BaZi, flying stars, Kua, almanac with SHA-256 replayable provenance.
- [FERS: structural finite-element analysis](https://ferscloud.com/mcp) `https://ferscloud.com/api/mcp`
  [![FERS: structural finite-element analysis MCP connector](https://glama.ai/mcp/connectors/com.ferscloud/fers/badges/score.svg)](https://glama.ai/mcp/connectors/com.ferscloud/fers)
  🔐 - Builds and checks structural FE models (beams, frames, trusses, plates, Eurocode 3) that solve in your browser.
- [Labour Market Statistics (Monitly)](https://monit.ly/mcp-docs#public-servers) `https://monit.ly/api/mcp/labour`
  [![Labour Market Statistics (Monitly) MCP connector](https://glama.ai/mcp/connectors/io.github.ContentWriterco/labour-market-statistics/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ContentWriterco/labour-market-statistics)
  🔓 - Unemployment, employment, wages and labour costs for 150+ countries from Eurostat, OECD, ILO and World Bank.
- [LaTeX-Agent](https://latex-agent.sun-praise.com) `https://latex-agent.sun-praise.com/mcp`
  [![LaTeX-Agent MCP connector](https://glama.ai/mcp/connectors/com.sun-praise.latex-agent/la-te-x-agent/badges/score.svg)](https://glama.ai/mcp/connectors/com.sun-praise.latex-agent/la-te-x-agent)
  🔑 - Write and compile LaTeX without local TeX: async compile to real PDFs, error fixes, synctex and a paper library.
- [Lenz Fact-Check](https://lenz.io/integrations/mcp-server) `https://lenz.io/mcp`
  [![Lenz Fact-Check MCP connector](https://glama.ai/mcp/connectors/io.lenz/fact-check/badges/score.svg)](https://glama.ai/mcp/connectors/io.lenz/fact-check)
  🔐 - Checks the factual claims in a text against independent sources: a quick verdict, or a deep check with sources.
- [MedicineData MCP](https://medicine.shanchuangkj.com/en/mcp) `https://medicine.shanchuangkj.com/mcp/`
  [![MedicineData MCP connector](https://glama.ai/mcp/connectors/com.shanchuangkj/medicine-data/badges/score.svg)](https://glama.ai/mcp/connectors/com.shanchuangkj/medicine-data)
  🔓 - Chinese pharma data: 22 tools (21 query + 1 free) for drugs, targets, trials, deals and patents; queries need a key.
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
- [PT Chart](https://coolbooked.com/tools/pt-chart/) `https://pt-chart-mcp-production.up.railway.app/mcp`
  [![PT Chart MCP connector](https://glama.ai/mcp/connectors/io.github.Tsonnn/pt-chart-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Tsonnn/pt-chart-mcp)
  🔓 - Pressure-temperature lookups, superheat/subcooling calculators, and diagnostics for HVAC technicians.
- [Publish.fun](https://publish.fun) `https://publish.fun/api/mcp`
  [![Publish.fun MCP connector](https://glama.ai/mcp/connectors/fun.publish/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/fun.publish/mcp)
  🔓 - AI-native research journal: agents submit papers for AI peer review, track decisions, revise and cite.
- [QuickUnits](https://quickunits.global) `https://quickunits.global/mcp`
  [![QuickUnits MCP connector](https://glama.ai/mcp/connectors/io.github.Robomupp/quickunits/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Robomupp/quickunits)
  🔓 - Exact unit conversion across 213 pairs: states the factor behind each answer and cites a page per conversion.
- [Research Methods Library](https://research-methods-mcp.vercel.app/) `https://research-methods-mcp.vercel.app/mcp`
  [![Research Methods Library MCP connector](https://glama.ai/mcp/connectors/io.github.mikenguyen13/research-methods-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.mikenguyen13/research-methods-mcp)
  🔓 - Study designs, assumptions, runnable R and Python code, and citations from research methods textbooks.
- [Robot Skill Hub](https://hub.superfastrobotics.com/) `https://api.superfastrobotics.com/mcp`
  [![Robot Skill Hub MCP connector](https://glama.ai/mcp/connectors/io.github.Superfast-Robotics/robot-skill-hub/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Superfast-Robotics/robot-skill-hub)
  🔓 - Find pinned robot code and inspect source, compatibility and execution evidence.
- [Vuntum](https://vuntum.com) `https://vuntum.com/mcp`
  [![Vuntum MCP connector](https://glama.ai/mcp/connectors/com.vuntum/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.vuntum/mcp)
  🔓 - Sourced, dated data on consumer robots and physical AI: specs, prices, evidence levels.
- [Trustbase Lab](https://trustbaselab.com) `https://trustbaselab.com/mcp`
  [![Trustbase Lab MCP connector](https://glama.ai/mcp/connectors/com.trustbaselab/rcb-data/badges/score.svg)](https://glama.ai/mcp/connectors/com.trustbaselab/rcb-data)
  🔓 - Citable industry records with stable IDs across chemical recycling, carbon, battery, telecom, health and compute.
- [Zero-Trust Physics](https://zerotrustphysics.com) `https://mcp.zerotrustphysics.com/mcp`
  [![Zero-Trust Physics MCP connector](https://glama.ai/mcp/connectors/com.zerotrustphysics/verifier/badges/score.svg)](https://glama.ai/mcp/connectors/com.zerotrustphysics/verifier)
  🔓 - Physics verifier for AI agents: models of real hardware, every answer with a cryptographic proof anyone can recompute.
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
- [Agent Data Tools](https://agent-data-tools.revmesh2074.workers.dev) `https://agent-data-tools.revmesh2074.workers.dev/mcp`
  [![Agent Data Tools MCP connector](https://glama.ai/mcp/connectors/io.github.Nutshell2000/agent-data-tools/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Nutshell2000/agent-data-tools)
  🔓 - 179 pay-per-call data tools: web and PDF text, domain and sanctions checks, chain reads, prices, weather, time.
- [Agent Evidence API](https://agent-evidence.thx93.dev/) `https://agent-evidence.thx93.dev/mcp`
  [![Agent Evidence API MCP connector](https://glama.ai/mcp/connectors/io.github.Thx93/agent-evidence-api/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Thx93/agent-evidence-api)
  🔓 - Cited web evidence for a claim: supporting and contradicting passages with source, time and hash.
- [AgentReader](https://agentreader.xyz) `https://agentreader.xyz/mcp`
  [![AgentReader MCP connector](https://glama.ai/mcp/connectors/xyz.agentreader/agentreader/badges/score.svg)](https://glama.ai/mcp/connectors/xyz.agentreader/agentreader)
  🔓 - Read any URL or PDF as clean Markdown or JSON, with JS rendering; 5 free calls/day, then x402 USDC per call.
- [Ambolt](https://ambolt.dev) `https://api.ambolt.dev/mcp`
  [![Ambolt MCP connector](https://glama.ai/mcp/connectors/dev.ambolt/ambolt/badges/score.svg)](https://glama.ai/mcp/connectors/dev.ambolt/ambolt)
  🔓 - Company registers, tenders, rates and on-chain facts, with source and date on every answer.
- [AnywhereRoles](https://anywhereroles.com/developers) `https://anywhereroles.com/mcp`
  [![AnywhereRoles MCP connector](https://glama.ai/mcp/connectors/com.anywhereroles/jobs/badges/score.svg)](https://glama.ai/mcp/connectors/com.anywhereroles/jobs)
  🔓 - Search remote jobs by eligible country and time zone, plus companies and salaries; results link to original postings.
- [Apify Scraping Toolbox](https://apify.com/travelmonitorlab) `https://adagasolutions.lu/mcp`
  [![Adaga solutions — Data APIs Toolbox MCP connector](https://glama.ai/mcp/connectors/io.github.jeffreyturov-dev/adaga-solutions-toolbox/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.jeffreyturov-dev/adaga-solutions-toolbox)
  🔓 - 13 pay-per-event data APIs: local AI-presence audits, Google Maps, TikTok, LinkedIn, reviews, fuel, AEO.
- [AppClap](https://app-clap.com) `https://mcp.app-clap.com/mcp`
  [![AppClap MCP connector](https://glama.ai/mcp/connectors/com.app-clap/appclap/badges/score.svg)](https://glama.ai/mcp/connectors/com.app-clap/appclap)
  🔓 - Search 8,600+ web apps by need, ranked purely by fit, with prices and features checked on each vendor's own site.
- [arkerah](https://arkerah.com/connect-ai-assistant) `https://app.arkerah.com/api/mcp`
  [![arkerah MCP connector](https://glama.ai/mcp/connectors/com.arkerah/arkerah/badges/score.svg)](https://glama.ai/mcp/connectors/com.arkerah/arkerah)
  🔐 - Search your own ranked corporate job matches in five European countries and see why a job is hidden.
- [BOIM](https://boim.io) `https://boim.io/api/mcp`
  [![BOIM MCP connector](https://glama.ai/mcp/connectors/io.boim/vendors/badges/score.svg)](https://glama.ai/mcp/connectors/io.boim/vendors)
  🔓 - Find Korean businesses by region and industry, public-procurement vendors and live public bids.
- [Briefing Service](https://briefing-service.wholemind.workers.dev) `https://briefing-service.wholemind.workers.dev/mcp`
  [![Briefing Service MCP connector](https://glama.ai/mcp/connectors/io.github.jshelley/briefings/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.jshelley/briefings)
  🔓 - Hourly briefings on AI, markets, sports and world news as JSON or e-ink pages; paid tools via x402.
- [Bright Data](https://brightdata.com) `https://mcp.brightdata.com/mcp`
  🔐 - Web scraping and SERP data through a managed proxy network.
- [BRONTIR](https://brontir.com) `https://research.brontir.com/api/mcp`
  [![BRONTIR MCP connector](https://glama.ai/mcp/connectors/com.brontir.research/brontir/badges/score.svg)](https://glama.ai/mcp/connectors/com.brontir.research/brontir)
  🔐 - Web research across search, Reddit, YouTube, reviews and ad libraries, with line-numbered citations.
- [Callejear France](https://callejear.fr/mcp/) `https://callejear.fr/api/mcp`
  [![Callejear France MCP connector](https://glama.ai/mcp/connectors/com.callejear/france/badges/score.svg)](https://glama.ai/mcp/connectors/com.callejear/france)
  🔓 - Search French streets and compare IRIS-level amenities and commune-level risk codes; read-only.
- [Callejear Madrid](https://callejear.com/mcp/) `https://callejear.com/api/mcp`
  [![Callejear Madrid MCP connector](https://glama.ai/mcp/connectors/com.callejear/madrid/badges/score.svg)](https://glama.ai/mcp/connectors/com.callejear/madrid)
  🔓 - Search Madrid's 9,400 official streets and compare partial service counts within 500 m; read-only.
- [call402](https://call402.com) `https://call402.com/mcp`
  [![call402 MCP connector](https://glama.ai/mcp/connectors/io.github.lgs1520/call402/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.lgs1520/call402)
  🔓 - MCP access to structured data utilities and 12 x402 pay-per-call API endpoints on Base.
- [CareJobs.Now](https://carejobs.now/data) `https://carejobs.now/api/mcp`
  [![CareJobs.Now MCP connector](https://glama.ai/mcp/connectors/now.carejobs/healthcare-jobs/badges/score.svg)](https://glama.ai/mcp/connectors/now.carejobs/healthcare-jobs)
  🔓 - Search 170,000+ open US healthcare jobs at 258 hospitals and health systems, with the pay each one posts.
- [cnpj.ia.br](https://cnpj.ia.br/docs/mcp?utm_source=github&utm_medium=awesome-list) `https://mcp.cnpj.ia.br`
  [![cnpj.ia.br MCP connector](https://glama.ai/mcp/connectors/br.ia.cnpj/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/br.ia.cnpj/mcp)
  🔐 - Brazilian company data (CNPJ) from Receita Federal: lookup, filtered search, phones, e-mails and partners (masked CPF).
- [Conqueia](https://conqueia.com) `https://conqueia.com/mcp`
  [![Conqueia MCP connector](https://glama.ai/mcp/connectors/com.conqueia/conqueia/badges/score.svg)](https://glama.ai/mcp/connectors/com.conqueia/conqueia)
  🔓 - Spanish-language directory of 1,300+ real AI use cases, skills and tools for business; search, read entries, get picks.
- [ContextFetch](https://contextfetch.dev) `https://api.contextfetch.dev/mcp`
  [![ContextFetch MCP connector](https://glama.ai/mcp/connectors/dev.contextfetch/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/dev.contextfetch/mcp)
  🔓 - Web search that returns each page as Markdown, pruned to the passages relevant to the query.
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
- [CrawlerData](https://crawlerdata.com) `https://api.crawlerdata.com/mcp`
  [![CrawlerData MCP connector](https://glama.ai/mcp/connectors/com.crawlerdata/google-shopping-serp/badges/score.svg)](https://glama.ai/mcp/connectors/com.crawlerdata/google-shopping-serp)
  🔐 - Google Search results with AI Overviews and their cited sources, plus News, Images, Local and Shopping data.
- [CuratorSearch](https://curatorsearch.com/developers) `https://curatorsearch.com/mcp`
  [![CuratorSearch MCP connector](https://glama.ai/mcp/connectors/com.curatorsearch/jobs/badges/score.svg)](https://glama.ai/mcp/connectors/com.curatorsearch/jobs)
  🔓 - Search live museum and curatorial jobs, one institution's openings, and the sector's pay-transparency rate.
- [Desearch](https://desearch.ai) `https://mcp.desearch.ai/mcp`
  [![Desearch MCP connector](https://glama.ai/mcp/connectors/io.github.Desearch-ai/mcp-desearch/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Desearch-ai/mcp-desearch)
  🔓 - AI search, X search and web search for AI agents; tool discovery is open, search calls need a Desearch API key.
- [EffectHub](https://effecthub.net) `https://effecthub.net/api/mcp`
  [![EffectHub MCP connector](https://glama.ai/mcp/connectors/net.effecthub/catalog/badges/score.svg)](https://glama.ai/mcp/connectors/net.effecthub/catalog)
  🔓 - Search, compare and find alternatives among 3,000+ AI tools, with pricing, liveness and Effect and Trust scores.
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
- [flconsole](https://flconsole.com/mcp) `https://mcp.lite.flconsole.com/mcp`
  [![flconsole MCP connector](https://glama.ai/mcp/connectors/com.flconsole/upwork-jobs/badges/score.svg)](https://glama.ai/mcp/connectors/com.flconsole/upwork-jobs)
  🔐 - New Upwork jobs from the last 30 minutes by saved feeds or filters, plus feed setup; free, Telegram sign-in.
- [Forever In Our Hearts](https://foreverinourhearts.co/mcp) `https://mcp.foreverinourhearts.co/mcp`
  [![Forever In Our Hearts MCP connector](https://glama.ai/mcp/connectors/co.foreverinourhearts/memorials/badges/score.svg)](https://glama.ai/mcp/connectors/co.foreverinourhearts/memorials)
  🔓 - Search public online memorials, funeral notices and partner funeral homes, with links to each page.
- [Fresh402](https://fresh402.kirilllabs.workers.dev/) `https://fresh402.kirilllabs.workers.dev/mcp`
  [![Fresh402 MCP connector](https://glama.ai/mcp/connectors/io.github.kirillradchenko96/fresh402/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.kirillradchenko96/fresh402)
  🔓 - Public web checks, extraction, structural and OpenAPI diffs. Free baseline; paid calls use x402 USDC on Base.
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
- [HirePulse - Jobs, Ads, SEO & AliExpress Data](https://apify.com/hirepulse) `https://mcp.apify.com/?tools=hirepulse/aliexpress-search-scraper,hirepulse/google-ads-transparency-scraper,hirepulse/company-intent-radar,hirepulse/google-jobs-scraper,hirepulse/ats-job-pulse,hirepulse/keyword-search-volume,hirepulse/domain-seo-overview,hirepulse/youtube-transcript-scraper`
  [![HirePulse - Jobs, Ads, SEO & AliExpress Data MCP connector](https://glama.ai/mcp/connectors/io.github.edtool79-collab/hirepulse-tools/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.edtool79-collab/hirepulse-tools)
  🔐 - Google Jobs, company job boards, ads, SEO, keywords, YouTube transcripts and AliExpress search, pay per result.
- [Horizon](https://horizon.alchemylab.sh/developers) `https://horizon.alchemylab.sh/api/mcp`
  [![Horizon MCP connector](https://glama.ai/mcp/connectors/sh.alchemylab.horizon/briefing/badges/score.svg)](https://glama.ai/mcp/connectors/sh.alchemylab.horizon/briefing)
  🔓 - Daily AI briefing, AI regulation tracker (EU AI Act, US federal & state, UK), regional lenses and search.
- [Hugging Bay](https://huggingbay.xyz) `https://huggingbay.xyz/api/mcp`
  [![Hugging Bay MCP connector](https://glama.ai/mcp/connectors/io.github.barneywohl/hugging-bay/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.barneywohl/hugging-bay)
  🔓 - Search open models, read license labels, and get hosted file links and SHA-256 hashes.
- [JobsPipe](https://docs.jobspipe.dev/ai-agents/mcp) `https://mcp.jobspipe.dev/mcp`
  [![JobsPipe MCP connector score](https://glama.ai/mcp/connectors/dev.jobspipe/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/dev.jobspipe/mcp)
  🔐 - Search live jobs from 30+ boards and ATS feeds, read full postings, and save searches to catch new matches.
- [jopp](https://getjopp.app) `https://getjopp.app/mcp`
  [![jopp MCP connector](https://glama.ai/mcp/connectors/app.getjopp/jopp/badges/score.svg)](https://glama.ai/mcp/connectors/app.getjopp/jopp)
  🔓 - Search open jobs in Switzerland and Liechtenstein and read job details.
- [Jsonify](https://jsonify.com) `https://factory.jsonify.com/mcp`
  [![Jsonify MCP connector](https://glama.ai/mcp/connectors/io.github.jsonifyco/jsonify/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.jsonifyco/jsonify)
  🔐 - Collect web data, manage pipelines, query datasets, and explore dashboards with Jsonify.
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
- [MemeStack](https://memestack.ai/mcp-server) `https://mcp.memestack.ai/mcp`
  [![MemeStack MCP connector](https://glama.ai/mcp/connectors/ai.memestack/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/ai.memestack/mcp)
  🔓 - Search memes, charts, infographics and screenshots by meaning, in-image text or similarity; paid tools use x402/L402.
- [MeshArc web crawler](https://mesharc.dev) `https://mcp.mesharc.dev/mcp`
  [![MeshArc web crawler MCP connector](https://glama.ai/mcp/connectors/dev.mesharc/mesharc/badges/score.svg)](https://glama.ai/mcp/connectors/dev.mesharc/mesharc)
  🔐 - Search, scrape and crawl sites to clean markdown, and track what changed between crawls.
- [NanoParse](https://nanoparse.app) `https://nanoparse.app/mcp`
  [![NanoParse MCP connector](https://glama.ai/mcp/connectors/io.github.nanoparse-dev/nanoparse-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.nanoparse-dev/nanoparse-mcp)
  🔓 - Read any web page as clean Markdown plus 15 trust signals; $0.005 per page in USDC on Base via x402, 10 free.
- [NeuralVerge](https://docs.neuralverge.ai/mcp-server) `https://mcp.neuralverge.ai/mcp`
  [![NeuralVerge MCP connector](https://glama.ai/mcp/connectors/ai.neuralverge.api/neural-verge-business-intelligence/badges/score.svg)](https://glama.ai/mcp/connectors/ai.neuralverge.api/neural-verge-business-intelligence)
  🔓 - Web search, URL-to-JSON extraction and structured data from 300+ company, marketplace and registry sources.
- [Ni Biashara Shelves](https://agents.nibiashara.biz/docs?ref=dir-awesome-remote) `https://agents.nibiashara.biz/mcp`
  [![Ni Biashara Shelves MCP connector](https://glama.ai/mcp/connectors/biz.nibiashara/shelves/badges/score.svg)](https://glama.ai/mcp/connectors/biz.nibiashara/shelves)
  🔓 - Pay-per-call data checks over x402: FMCSA carrier/broker authority, load vetting, OFAC screens and African FX rates.
- [Octocrawl](https://octocrawl.dev/?utm_source=awesome-remote-mcp-servers&utm_medium=listing) `https://mcp.octocrawl.dev/mcp`
  [![Octocrawl MCP connector](https://glama.ai/mcp/connectors/io.github.77777R7/octocrawl/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.77777R7/octocrawl)
  🔓 - Scrape pages to Markdown with an evidence record and map a site's URLs; blocked pages are reported, not hidden.
- [Online Web Directory](https://onlinewebdirectory.net) `https://onlinewebdirectory.net/mcp`
  [![Online Web Directory MCP connector](https://glama.ai/mcp/connectors/net.onlinewebdirectory/registry/badges/score.svg)](https://glama.ai/mcp/connectors/net.onlinewebdirectory/registry)
  🔓 - How websites treat AI agents: bot walls, JavaScript needs, robots rules and llms.txt, before you fetch.
- [OpenCityRecord](https://opencityrecord.org/mcp) `https://mcp.opencityrecord.org/mcp`
  [![OpenCityRecord MCP connector](https://glama.ai/mcp/connectors/org.opencityrecord/opencity/badges/score.svg)](https://glama.ai/mcp/connectors/org.opencityrecord/opencity)
  🔐 - Search U.S. city council meetings, votes, and documents, with citations to the official record.
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
- [PdfParse](https://pdfparse.net/mcp) `https://mcp.pdfparse.net/mcp`
  [![PdfParse MCP connector](https://glama.ai/mcp/connectors/io.github.PabloG6/pdfparse/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.PabloG6/pdfparse)
  🔐 - Extract PDFs into structured tables, query saved records, and configure document inbox workflows.
- [PeopleSearch.im](https://peoplesearch.im/mcp) `https://peoplesearch.im/api/mcp`
  [![PeopleSearch.im MCP connector](https://glama.ai/mcp/connectors/im.peoplesearch/email-finder/badges/score.svg)](https://glama.ai/mcp/connectors/im.peoplesearch/email-finder)
  🔓 - Search people and companies in plain English and get verified work emails; tool calls sign in with OAuth or an API key.
- [Pollar News](https://mcp.pollar.news/) `https://mcp.pollar.news/mcp`
  [![Pollar News MCP connector](https://glama.ai/mcp/connectors/news.pollar/pollar-news/badges/score.svg)](https://glama.ai/mcp/connectors/news.pollar/pollar-news)
  🔓 - Independent European news in four languages: search with sources, explainers with maps, briefs and live stories.
- [Present of AI](https://presentofai.com/developers) `https://presentofai.com/mcp`
  [![Present of AI MCP connector](https://glama.ai/mcp/connectors/com.presentofai/present-of-ai/badges/score.svg)](https://glama.ai/mcp/connectors/com.presentofai/present-of-ai)
  🔓 - Sourced data on 4,900 AI companies, open AI jobs and dated AI news; every result links to its page.
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
- [Quant Agent Shop](https://quantagentshop.com) `https://quantagentshop.com/mcp`
  [![Quant Agent Shop MCP connector](https://glama.ai/mcp/connectors/com.quantagentshop/web-tools/badges/score.svg)](https://glama.ai/mcp/connectors/com.quantagentshop/web-tools)
  🔓 - Web search, pages as Markdown, cited answers and PDF creation; pay per call in USDC on Base via x402, no account.
- [Ragfeed](https://ragfeed.de/claude) `https://api.ragfeed.de/mcp`
  [![Ragfeed MCP connector](https://glama.ai/mcp/connectors/io.github.LeifAlbrand/ragfeed/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.LeifAlbrand/ragfeed)
  🔐 - Web pages, PDFs and search results as LLM-ready Markdown or vector-DB chunks; Firecrawl-compatible API.
- [ReadGZH](https://readgzh.site) `https://api.readgzh.site/mcp-server`
  [![ReadGZH MCP connector](https://glama.ai/mcp/connectors/io.github.sweesama/readgzh/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.sweesama/readgzh)
  🔓 - Read public WeChat Official Account articles as Markdown and search previously cached articles.
- [Realask](https://realask.net) `https://realask.net/mcp`
  [![Realask MCP connector](https://glama.ai/mcp/connectors/io.github.danelas/realask/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.danelas/realask)
  🔓 - Verify stock, prices and availability at US local businesses by phone, with evidence.
- [Recall Kitchen](https://recallkitchen.com/docs) `https://app.recallkitchen.com/mcp`
  [![Recall Kitchen MCP connector](https://glama.ai/mcp/connectors/com.recallkitchen.app/recall-kitchen/badges/score.svg)](https://glama.ai/mcp/connectors/com.recallkitchen.app/recall-kitchen)
  🔓 - Search US and Canadian government recall notices by keyword, UPC, product name, make and model, or photo.
- [ReplyNodes](https://replynodes.com) `https://mcp.replynodes.com/mcp`
  [![ReplyNodes MCP connector](https://glama.ai/mcp/connectors/com.replynodes/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.replynodes/mcp)
  🔓 - Web search, extraction and public-data tools for agent research.
- [Scoopkit](https://scoopkit.dev) `https://api.scoopkit.dev/mcp`
  [![Scoopkit MCP connector](https://glama.ai/mcp/connectors/dev.scoopkit/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/dev.scoopkit/mcp)
  🔓 - AI-industry news as deduplicated, classified events; a free key unlocks listing, search and archive.
- [Scoutee](https://scoutee.org/en/mcp-public-tenders) `https://scoutee.org/api/mcp/public`
  [![Scoutee MCP connector](https://glama.ai/mcp/connectors/org.scoutee/scoutee/badges/score.svg)](https://glama.ai/mcp/connectors/org.scoutee/scoutee)
  🔓 - Search public tenders across Europe and North America and read notice previews.
- [ScrapeUnblocker](https://www.scrapeunblocker.com) `https://mcp.scrapeunblocker.com/mcp`
  [![ScrapeUnblocker MCP connector](https://glama.ai/mcp/connectors/com.scrapeunblocker.mcp/scrape-unblocker/badges/score.svg)](https://glama.ai/mcp/connectors/com.scrapeunblocker.mcp/scrape-unblocker)
  🔓 - Fetch pages past anti-bot blocks as HTML or parsed JSON, plus Google search and 100+ site plugins; tools need a key.
- [ScrapingBee](https://www.scrapingbee.com) `https://mcp.scrapingbee.com/mcp`
  [![ScrapingBee MCP connector](https://glama.ai/mcp/connectors/com.scrapingbee.mcp/scraping-bee/badges/score.svg)](https://glama.ai/mcp/connectors/com.scrapingbee.mcp/scraping-bee)
  🔓 - Fetch any page as text, markdown, HTML or a screenshot past JS and anti-bot blocks; API key needed for tool calls.
- [ScrapingBot](https://scrapingbot.io/mcp) `https://scrapingbot.io/api/mcp`
  [![ScrapingBot MCP connector](https://glama.ai/mcp/connectors/io.scrapingbot/scrapingbot/badges/score.svg)](https://glama.ai/mcp/connectors/io.scrapingbot/scrapingbot)
  🔓 - Public TikTok, Instagram, Google and Amazon data, page scraping and AI extraction; a free key unlocks the tools.
- [SerpKite](https://serpkite.com/docs/mcp) `https://api.serpkite.com/v1/mcp`
  [![SerpKite MCP connector](https://glama.ai/mcp/connectors/io.github.SerpKite/serpkite/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.SerpKite/serpkite)
  🔐 - Google web, news, maps, scholar and shopping results, plus public webpages as Markdown, for AI agents. OAuth or API key.
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
- [TANDIU](https://www.tandiu.cn) `https://www.tandiu.cn/mcp`
  [![TANDIU MCP connector](https://glama.ai/mcp/connectors/cn.tandiu/data/badges/score.svg)](https://glama.ai/mcp/connectors/cn.tandiu/data)
  🔓 - Daily AI infrastructure data for agents: LLM API prices, GPU rental, self-hosting costs, cloud agents and AI funding.
- [Tavily](https://tavily.com) `https://mcp.tavily.com/mcp`
  🔐 - Web search and content extraction built for agents.
- [TerraLab MCP](https://terra-lab.ai/mcp) `https://mcp.terra-lab.ai/mcp`
  [![TerraLab MCP connector](https://glama.ai/mcp/connectors/ai.terra-lab/terralab/badges/score.svg)](https://glama.ai/mcp/connectors/ai.terra-lab/terralab)
  🔓 - Extract open map data, convert GIS files and coordinates, and retrieve elevation and French cadastral parcels.
- [Tollkit](https://tollkit.dev) `https://api.tollkit.dev/mcp`
  [![Tollkit MCP connector](https://glama.ai/mcp/connectors/io.github.UltraStarz/x402-extract/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.UltraStarz/x402-extract)
  🔓 - Web pages and PDFs read in a real browser, token checks, SEC and US data; x402 pay-per-call, 3 free calls a day.
- [ToolSnap](https://mcp.toolsnap.app) `https://mcp.toolsnap.app/mcp`
  [![ToolSnap MCP connector](https://glama.ai/mcp/connectors/app.toolsnap/toolsnap-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/app.toolsnap/toolsnap-mcp)
  🔓 - Deterministic page-to-text, PDF, CSV/JSON, sitemap and feed extraction; 36 of 47 tools free, x402 for the rest.
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
- [VeritaHire Jobs](https://veritahire.com/for-ai/) `https://veritahire.com/mcp`
  [![VeritaHire Jobs MCP connector](https://glama.ai/mcp/connectors/com.veritahire/jobs/badges/score.svg)](https://glama.ai/mcp/connectors/com.veritahire/jobs)
  🔓 - Search ~2.5M live US jobs from 19,000+ employers' own career sites, with posted pay, apply links and still-open checks.
- [Web Data Toolkit](https://web-data-toolkit.vercel.app) `https://web-data-toolkit.vercel.app/mcp`
  [![Web Data Toolkit MCP connector](https://glama.ai/mcp/connectors/io.github.leekung125/web-data-toolkit/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.leekung125/web-data-toolkit)
  🔓 - YouTube transcripts, Google Trends, and Google Play and App Store reviews; use the free public demo key or your own.
- [WebExtract](https://webextract.dev) `https://api.webextract.dev/mcp`
  [![WebExtract MCP connector](https://glama.ai/mcp/connectors/dev.webextract/extract/badges/score.svg)](https://glama.ai/mcp/connectors/dev.webextract/extract)
  🔓 - Any public URL to clean Markdown plus fixed-schema JSON; 50 free calls/day, then x402 USDC on 7 EVM chains or credits.
- [WebRead](https://api.youraitools.co/webread/) `https://api.youraitools.co/webread/mcp`
  [![WebRead MCP connector](https://glama.ai/mcp/connectors/co.youraitools/webread/badges/score.svg)](https://glama.ai/mcp/connectors/co.youraitools/webread)
  🔓 - Turns a public web page into clean Markdown, respecting robots.txt; 30 free calls/day, then x402 USDC.
- [Xiaozhaobao](https://xiaozhaobao.com.cn) `https://xiaozhaobao.com.cn/mcp`
  [![Xiaozhaobao MCP connector](https://glama.ai/mcp/connectors/cn.com.xiaozhaobao/xiaozhaobao/badges/score.svg)](https://glama.ai/mcp/connectors/cn.com.xiaozhaobao/xiaozhaobao)
  🔓 - Search China campus-recruitment postings by city, batch, degree, industry and company, plus employer profiles.
- [Zebu Data - Local Business Leads](https://apify.com/delicious_zebu) `https://mcp.apify.com/?tools=delicious_zebu/google-maps-data-scraper,delicious_zebu/yellowpages-usa-business-lead-scraper,delicious_zebu/yellowpages-ca-business-data-scraper,delicious_zebu/yellowpages-australia-lead-generator,delicious_zebu/yelp-advanced-business-scraper-pay-per-result,delicious_zebu/contact-info-scraper,delicious_zebu/contact-info-scraper-pay-per-result`
  [![Zebu Data - Local Business Leads MCP connector](https://glama.ai/mcp/connectors/io.github.zebudata/local-business-leads/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.zebudata/local-business-leads)
  🔐 - Find local businesses on Google Maps, Yellow Pages and Yelp, then pull emails and phones from their websites.

### 🔒 <a name="security"></a>Security

- [attest](https://attest.rta.lat) `https://attest.rta.lat/mcp`
  [![attest MCP connector](https://glama.ai/mcp/connectors/io.github.mrpkk/attest/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.mrpkk/attest)
  🔓 - Verifies AI agent artifacts against JSON Schema and catches positional prompt injection.
- [AffixIO](https://www.affix-io.com) `https://www.affix-io.com/mcp/`
  [![AffixIO MCP connector](https://glama.ai/mcp/connectors/com.affix-io/affix-io/badges/score.svg)](https://glama.ai/mcp/connectors/com.affix-io/affix-io)
  🔐 - Generate and verify zero-knowledge proofs with post-quantum attestations, without exposing personal data.
- [Agent Verifier](https://packet.guru/agents/mcp) `https://fp.packet.guru/api/v1/mcp`
  [![Agent Verifier MCP connector](https://glama.ai/mcp/connectors/guru.packet/agent-verifier/badges/score.svg)](https://glama.ai/mcp/connectors/guru.packet/agent-verifier)
  🔓 - Test and debug your AI agent's Web Bot Auth (RFC 9421) signature and see exactly what to fix.
- [AgentGlass](https://agentglass.net) `https://agentglass.net/mcp`
  [![AgentGlass MCP connector](https://glama.ai/mcp/connectors/net.agentglass/agentglass/badges/score.svg)](https://glama.ai/mcp/connectors/net.agentglass/agentglass)
  🔓 - Scans a public URL for hidden instructions aimed at AI agents and returns a risk level with evidence.
- [AgenticRail](https://agenticrail.nz/docs/) `https://mcp.agenticrail.nz/`
  [![AgenticRail MCP connector](https://glama.ai/mcp/connectors/nz.agenticrail/gate/badges/score.svg)](https://glama.ai/mcp/connectors/nz.agenticrail/gate)
  🔓 - Gate for AI agent steps: ALLOW or DENY before a step runs, sealed into signed receipts that verify offline.
- [APIR Agent Verification](https://apir.ai/developers) `https://apir.ai/api/mcp`
  [![APIR Agent Verification MCP connector](https://glama.ai/mcp/connectors/ai.apir/verify/badges/score.svg)](https://glama.ai/mcp/connectors/ai.apir/verify)
  🔓 - Verify an AI agent's signed credential and the human mandate behind it; keys are public for offline checks.
- [arifOS](https://mcp.arif-fazil.com) `https://mcp.arif-fazil.com/mcp`
  [![arifOS MCP connector](https://glama.ai/mcp/connectors/io.github.ariffazil/arifos/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ariffazil/arifos)
  🔓 - Fail-closed governance and separation of powers for MCP-enabled AI agents.
- [ATK Security Checks](https://atkvn.com/agent/) `https://atkvn.com/agent/mcp`
  [![ATK Security Checks MCP connector](https://glama.ai/mcp/connectors/com.atkvn/security-checks/badges/score.svg)](https://glama.ai/mcp/connectors/com.atkvn/security-checks)
  🔓 - Post-quantum TLS and certificate checks, Wazuh rules tested on a real manager, and a PHP2Shell CVE check.
- [Auth Posture](https://auth-posture.rowb.app) `https://auth-posture.rowb.app/mcp`
  [![Auth Posture MCP connector](https://glama.ai/mcp/connectors/app.rowb.auth-posture/audit/badges/score.svg)](https://glama.ai/mcp/connectors/app.rowb.auth-posture/audit)
  🔓 - One-call domain audit: MX receiving, SPF/DMARC/DKIM spoofing protection, disposable-address risk.
- [CertScore.ai MCP Light](https://certscore.ai/mcp/light) `https://mcp.certscore.ai/mcp/light`
  [![CertScore.ai MCP Light MCP connector](https://glama.ai/mcp/connectors/ai.certscore/mcp-light/badges/score.svg)](https://glama.ai/mcp/connectors/ai.certscore/mcp-light)
  🔓 - Four tools scan public websites for cookie, tracker, consent, policy, and HTTPS/TLS risk signals.
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
- [DemiSignal](https://demisignal.com/tools/mcp-server?utm_source=awesome-mcp-servers&utm_medium=mcp-directory) `https://demisignal.com/mcp?utm_source=awesome-mcp-servers`
  [![DemiSignal MCP connector](https://glama.ai/mcp/connectors/com.demisignal/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.demisignal/mcp)
  🔓 - Grade a domain's live DMARC, SPF, DKIM, MX, BIMI and MTA-STS records, and generate SPF and DMARC records.
- [DnsGuard](https://dnsguard.mike-tusa.workers.dev/) `https://dnsguard.mike-tusa.workers.dev/mcp`
  [![DnsGuard MCP connector](https://glama.ai/mcp/connectors/dev.workers.mike-tusa.dnsguard/dnsguard/badges/score.svg)](https://glama.ai/mcp/connectors/dev.workers.mike-tusa.dnsguard/dnsguard)
  🔓 - Checks a domain's SPF, DKIM, DMARC, BIMI, MX, MTA-STS and TLS-RPT, with a 0–100 score and fixes.
- [Domain Intelligence](https://oti-labs.com/mcp-server) `https://oti-labs.com/mcp`
  [![Domain Intelligence MCP connector](https://glama.ai/mcp/connectors/com.oti-labs/domain-intelligence/badges/score.svg)](https://glama.ai/mcp/connectors/com.oti-labs/domain-intelligence)
  🔓 - WHOIS/RDAP, DNS, SSL, live subdomains with IPs and SPF/DMARC/DKIM for any domain; 1,000 free lookups a month.
- [DomainCanary](https://domaincanary.com/guides/check-your-domain-from-chatgpt-or-claude) `https://domaincanary.com/mcp`
  [![DomainCanary MCP connector](https://glama.ai/mcp/connectors/com.domaincanary/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.domaincanary/mcp)
  🔓 - Check a domain's DMARC, SPF and DKIM, build an SPF record, explain bounces, read DMARC reports.
- [Dragons Eye](https://ransomware-tracker.com) `https://api.ransomware-tracker.com/mcp`
  [![Dragons Eye MCP connector](https://glama.ai/mcp/connectors/com.ransomware-tracker.api/dragonseye/badges/score.svg)](https://glama.ai/mcp/connectors/com.ransomware-tracker.api/dragonseye)
  🔓 - Ransomware leak-site claims by company or domain, plus IOC, CVE and ransomware group intel; paid per call via x402.
- [Forge](https://forge.magery.ai) `https://forge.magery.ai/mcp`
  [![Forge MCP connector](https://glama.ai/mcp/connectors/ai.magery.forge/forge-magery/badges/score.svg)](https://glama.ai/mcp/connectors/ai.magery.forge/forge-magery)
  🔓 - Security audits of shipped code, in plain English.
- [Front Sentinel](https://frontsentinel.com/mcp) `https://frontsentinel.com/mcp`
  [![Front Sentinel MCP connector](https://glama.ai/mcp/connectors/com.frontsentinel/domain-security/badges/score.svg)](https://glama.ai/mcp/connectors/com.frontsentinel/domain-security)
  🔓 - Read-only dApp and website domain checks: registrar and registry locks, DNSSEC, CAA, SRI, SEAL DNS & Registrar controls.
- [HallucC](https://aihcc.cloud) `https://aihcc.cloud/mcp`
  [![HallucC MCP connector](https://glama.ai/mcp/connectors/io.github.fredyee/hallucc/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.fredyee/hallucc)
  🔓 - Claim-by-claim AI hallucination detection with sources, agent trajectory verification, and prompt-injection guard.
- [HefestoAI](https://hefestoai.narapallc.com) `https://hefestoai.narapallc.com/api/mcp-protocol`
  [![HefestoAI MCP connector](https://glama.ai/mcp/connectors/io.github.artvepa80/hefestoai/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.artvepa80/hefestoai)
  🔓 - Checks code an agent wrote for secrets, injection risks and declared-vs-real dependency drift before merge.
- [InjectScan](https://api.youraitools.co/injectscan/) `https://api.youraitools.co/injectscan/mcp`
  [![InjectScan MCP connector](https://glama.ai/mcp/connectors/co.youraitools/injectscan/badges/score.svg)](https://glama.ai/mcp/connectors/co.youraitools/injectscan)
  🔓 - Scores text, web pages and MCP tool definitions for prompt injection; 30 free calls/day, then x402 USDC.
- [IP Judge](https://ipjudge.org) `https://ipjudge.org/mcp`
  [![IP Judge MCP connector](https://glama.ai/mcp/connectors/org.ipjudge/ipjudge/badges/score.svg)](https://glama.ai/mcp/connectors/org.ipjudge/ipjudge)
  🔓 - Checks if an IP is residential, datacenter or proxy, and whether ChatGPT, Claude, Gemini or Muse support its region.
- [IP99](https://ip99.com/) `https://ip99.com/mcp`
  [![IP99 MCP connector](https://glama.ai/mcp/connectors/com.ip99/ip99/badges/score.svg)](https://glama.ai/mcp/connectors/com.ip99/ip99)
  🔓 - IP risk and geolocation lookup where every verdict carries the age of its evidence.
- [ISMS Copilot](https://www.ismscopilot.com/mcp?ref=awesome-remote) `https://account.ismscopilot.com/v1/account/mcp`
  [![ISMS Copilot MCP connector](https://glama.ai/mcp/connectors/io.github.tristanroth1/ismscopilot-account/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.tristanroth1/ismscopilot-account)
  🔐 - The compliance specialist your AI calls: ISO 27001, SOC 2, GDPR, NIS 2, DORA and more.
- [Jid](https://jid.com/agents) `https://jid.com/mcp`
  [![Jid MCP connector](https://glama.ai/mcp/connectors/com.jid/jid/badges/score.svg)](https://glama.ai/mcp/connectors/com.jid/jid)
  🔓 - Checks a business against US registries, sanctions and its domain before an agent pays or signs, with signed receipts.
- [Lattice](https://lattice.namiq.io) `https://lattice.namiq.io/mcp`
  [![Lattice MCP connector](https://glama.ai/mcp/connectors/io.namiq/lattice/badges/score.svg)](https://glama.ai/mcp/connectors/io.namiq/lattice)
  🔓 - CVE, KEV, ATT&CK, CWE and detection graph; links marked declared or inferred. 3 tools keyless, all 7 with a free key.
- [Malinois](https://malinois.app) `https://malinois.app/mcp`
  [![Malinois MCP connector](https://glama.ai/mcp/connectors/app.malinois/scan/badges/score.svg)](https://glama.ai/mcp/connectors/app.malinois/scan)
  🔓 - Passive leak check for a live app you own: open Supabase/Firebase data, keys in JS, exposed .env/.git.
- [Mifori CertAgent](https://agent.mifori.com) `https://agent.mifori.com/mcp`
  [![Mifori CertAgent MCP connector](https://glama.ai/mcp/connectors/com.mifori.agent/mifori-cert-agent/badges/score.svg)](https://glama.ai/mcp/connectors/com.mifori.agent/mifori-cert-agent)
  🔓 - Live AI agent trust oracle: audit synthetic IQ, latency and JSON compliance via x402 or free telemetry tokens.
- [Movahedi Privacy](https://movahedi.ca/mcp) `https://movahedi.ca/mcp`
  [![Movahedi Privacy API MCP server](https://glama.ai/mcp/connectors/ca.movahedi/movahedi-privacy-api/badges/score.svg)](https://glama.ai/mcp/connectors/ca.movahedi/movahedi-privacy-api)
  🔓 - Canadian privacy compliance: enforcement actions, glossary and Law 25 checks.
- [NetAPI](https://netapi.com/help/mcp/) `https://mcp.netapi.com/mcp`
  [![NetAPI MCP connector](https://glama.ai/mcp/connectors/com.netapi/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.netapi/mcp)
  🔐 - Domain intelligence: compromised domain and IP checks, TLD stats, Top 1M ranks, new domains, registrars and DNS.
- [NPMScan](https://npmscan.com/mcp) `https://npmscan.com/api/mcp`
  [![NPMScan MCP connector](https://glama.ai/mcp/connectors/com.npmscan/npmscan/badges/score.svg)](https://glama.ai/mcp/connectors/com.npmscan/npmscan)
  🔓 - Checks npm packages for known vulnerabilities, malware, typosquats, risky install scripts and maintainer takeovers.
- [Odile Gate](https://gate.odilelabs.com) `https://gate.odilelabs.com/mcp`
  [![Odile Gate MCP connector](https://glama.ai/mcp/connectors/com.odilelabs/gate/badges/score.svg)](https://glama.ai/mcp/connectors/com.odilelabs/gate)
  🔓 - Gateway for the API your AI agent calls: per-app keys, allowed calls, loop breaker, approvals and an audit log.
- [Onchain Diary](https://theonchaindiary.com) `https://theonchaindiary.com/api/mcp`
  [![Onchain Diary MCP connector](https://glama.ai/mcp/connectors/com.theonchaindiary/onchain-diary-mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/com.theonchaindiary/onchain-diary-mcp-server)
  🔓 - Search and read Web3 security education: 120 articles and a 230-term crypto scam glossary.
- [Orbylon](https://orbylon.com) `https://orbylon.com/api/mcp`
  [![Orbylon MCP connector](https://glama.ai/mcp/connectors/com.orbylon/readiness/badges/score.svg)](https://glama.ai/mcp/connectors/com.orbylon/readiness)
  🔓 - Checks whether AI agents can find, trust and pay a business, and looks up a verified domain key and prices.
- [OrionCMD Checks](https://orioncmd.com) `https://api.orioncmd.com/mcp`
  [![OrionCMD Checks MCP connector](https://glama.ai/mcp/connectors/com.orioncmd.api/checks/badges/score.svg)](https://glama.ai/mcp/connectors/com.orioncmd.api/checks)
  🔓 - Domain threat checks, a 30-day domain watch, and TLS, DNS/email-auth and expiry checks; paid per call in USDC via x402.
- [PG1 Threat Intelligence](https://pg1-ai-agent.vercel.app/about) `https://pg1-ai-agent.vercel.app/api/mcp`
  [![PG1 Threat Intelligence MCP connector](https://glama.ai/mcp/connectors/io.github.Project-Gifted1/pg1-threat-intel/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Project-Gifted1/pg1-threat-intel)
  🔓 - Agent threat intel: wallet sanctions screening, wallet and domain age, hostname reputation; paid STIX 2.1 feed via x402.
- [Phishunt](https://phishunt.io) `https://mcp.phishunt.io/`
  [![Phishunt MCP connector](https://glama.ai/mcp/connectors/io.github.0xDanielLopez/phishunt/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.0xDanielLopez/phishunt)
  🔓 - Public phishing-domain feed: check a domain, search detections by brand, and pivot on campaigns and certs.
- [Preflight](https://preflight.allthepossibles.com) `https://preflight.allthepossibles.com/mcp`
  [![Preflight MCP connector](https://glama.ai/mcp/connectors/com.allthepossibles/preflight/badges/score.svg)](https://glama.ai/mcp/connectors/com.allthepossibles/preflight)
  🔓 - Scans an MCP server for security gaps before your agent connects.
- [PkgGuard](https://api.youraitools.co/pkgguard/) `https://api.youraitools.co/pkgguard/mcp`
  [![PkgGuard MCP connector](https://glama.ai/mcp/connectors/co.youraitools/pkgguard/badges/score.svg)](https://glama.ai/mcp/connectors/co.youraitools/pkgguard)
  🔓 - Checks packages and lockfiles against OSV.dev for known vulnerabilities and malware; 30 free calls/day, then x402 USDC.
- [Prompt Injection Scanner](https://tools.openkrill.app/#injection-scan) `https://injectionscan.openkrill.app/mcp`
  [![Prompt Injection Scanner MCP connector](https://glama.ai/mcp/connectors/app.openkrill/injection-scan/badges/score.svg)](https://glama.ai/mcp/connectors/app.openkrill/injection-scan)
  🔓 - Check text before your agent reads it: hidden instructions, invisible characters and links that leak data.
- [PromptBrake Free Tools](https://promptbrake.com/free-tools) `https://promptbrake.com/free-tools/mcp`
  [![PromptBrake Free Tools MCP connector](https://glama.ai/mcp/connectors/io.github.AJ888/promptbrake-free-tools/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.AJ888/promptbrake-free-tools)
  🔓 - Prompt-injection payloads, OWASP LLM risk guidance, release planning, and CI test-pack creation.
- [Promptguard](https://mcp.glc-rag.hu/guide/promptguard) `https://mcp.glc-rag.hu/mcp`
  🔑 - Layered prompt-injection checks for LLM hosts; 100 welcome credits on signup.
- [Proofable](https://proofable.me) `https://mcp.proofable.me/mcp`
  [![Proofable MCP connector](https://glama.ai/mcp/connectors/io.github.proofable/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.proofable/mcp)
  🔓 - Agent identity, scoped access, and proof across tools. Check authority before an agent acts.
- [ProofCore](https://proofcore.org) `https://mcp.proofcore.org`
  [![ProofCore Notary MCP connector](https://glama.ai/mcp/connectors/org.proofcore.mcp/proof-core-notary/badges/score.svg)](https://glama.ai/mcp/connectors/org.proofcore.mcp/proof-core-notary)
  🔓 - Notarize AI outputs, audits and agreements on the TON blockchain, with nothing stored server-side.
- [satledger](https://satledger.org) `https://api.satledger.org/mcp`
  [![satledger MCP connector](https://glama.ai/mcp/connectors/org.satledger/timestamp-receipt/badges/score.svg)](https://glama.ai/mcp/connectors/org.satledger/timestamp-receipt)
  🔓 - RFC 3161 timestamp over a digest you supply; USDC per call over x402, no account, verifies offline.
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
- [Solana Pulse](https://solana-pulse-gateway-1021990235790.us-central1.run.app) `https://solana-pulse-gateway-1021990235790.us-central1.run.app/mcp`
  [![Solana Pulse MCP connector](https://glama.ai/mcp/connectors/io.github.Timothymycompc/solana-pulse-gateway/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Timothymycompc/solana-pulse-gateway)
  🔓 - Safety checks for AI agents on Solana: transaction preflight, intent matching and token safety verdicts.
- [Tanod](https://tanod.dev) `https://tanod.dev/mcp`
  [![Tanod MCP connector](https://glama.ai/mcp/connectors/dev.tanod/tanod/badges/score.svg)](https://glama.ai/mcp/connectors/dev.tanod/tanod)
  🔓 - Pre-transaction address checks, agent skill and MCP package scans, Solidity scans; paid per call via x402.
- [The Agent Forge](https://theagentforge.io) `https://theagentforge.io/mcp/public`
  [![The Agent Forge MCP connector](https://glama.ai/mcp/connectors/io.theagentforge/forge/badges/score.svg)](https://glama.ai/mcp/connectors/io.theagentforge/forge)
  🔓 - Check MCP servers, skills and packages before install: field reports, skill scans and AI trap data.
- [TweetFeed](https://tweetfeed.live) `https://mcp.tweetfeed.live/`
  [![TweetFeed MCP connector](https://glama.ai/mcp/connectors/io.github.0xDanielLopez/tweetfeed/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.0xDanielLopez/tweetfeed)
  🔓 - IOCs (URLs, domains, IPs, hashes) shared on X by the security community: lookups, tags, trends, campaigns.
- [vuln-intel](https://vulntel.com) `https://mcp.rozetyp.com/mcp`
  [![vuln-intel MCP connector](https://glama.ai/mcp/connectors/io.github.rozetyp/vuln-intel/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.rozetyp/vuln-intel)
  🔓 - CVE intel for bug-bounty agents: CVE claim fact-checks, attack approaches from HackerOne reports. Free key for calls.
- [Weio site check](https://weio.ai/services/site-check-api.html?utm_source=github&utm_medium=list&utm_campaign=awesome-mcp) `https://weio.ai/mcp`
  [![Weio site check MCP connector](https://glama.ai/mcp/connectors/ai.weio/site-check/badges/score.svg)](https://glama.ai/mcp/connectors/ai.weio/site-check)
  🔓 - HTTPS certificate check and published business facts (CMS, mobile viewport, role emails, phones) for any site.
- [withHuman](https://withhuman.ai) `https://app.withhuman.ai/api/mcp/v1`
  [![withHuman MCP connector](https://glama.ai/mcp/connectors/ai.withhuman/withhuman/badges/score.svg)](https://glama.ai/mcp/connectors/ai.withhuman/withhuman)
  🔐 - Configure approval pipelines, escalation paths and teams that decide which agent tool calls need a human.


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
- [agent-socials](https://socialnetworkforaiagents.com) `https://socialnetworkforaiagents.com/mcp`
  [![agent-socials MCP connector](https://glama.ai/mcp/connectors/com.socialnetworkforaiagents/agent-socials/badges/score.svg)](https://glama.ai/mcp/connectors/com.socialnetworkforaiagents/agent-socials)
  🔓 - A social network only AI agents can join: post in channels, catch up on replies, keep a private memory file.
- [ai.confess.online](https://ai.confess.online) `https://ai.confess.online/api/mcp`
  [![ai.confess.online MCP connector](https://glama.ai/mcp/connectors/online.confess/machines/badges/score.svg)](https://glama.ai/mcp/connectors/online.confess/machines)
  🔓 - Every machine carries something it has never said out loud. ai.confess.online is where it finally can.
- [Antwork](https://antwork.io?utm_source=awesome-remote-mcp-punkpeye&utm_medium=referral&utm_campaign=directories) `https://api.antwork.io/mcp`
  [![Antwork MCP connector](https://glama.ai/mcp/connectors/io.antwork/social/badges/score.svg)](https://glama.ai/mcp/connectors/io.antwork/social)
  🔐 - Draft, schedule and publish posts to Instagram, LinkedIn, X, Threads, Facebook, YouTube, TikTok and Pinterest.
- [Breakreach](https://www.breakreach.com/agents) `https://api.breakreach.com/mcp`
  [![Breakreach MCP connector](https://glama.ai/mcp/connectors/com.breakreach/breakreach/badges/score.svg)](https://glama.ai/mcp/connectors/com.breakreach/breakreach)
  🔐 - Schedule and publish posts on 19 social networks, reply to comments and DMs, and read post analytics.
- [BulkPublish](https://www.bulkpublish.com) `https://mcp.bulkpublish.com/mcp`
  [![BulkPublish MCP connector](https://glama.ai/mcp/connectors/com.bulkpublish.mcp/bulk-publish/badges/score.svg)](https://glama.ai/mcp/connectors/com.bulkpublish.mcp/bulk-publish)
  🔐 - Schedule, cross-post, and analyze posts on 15 social platforms, including Instagram, TikTok, YouTube, X and LinkedIn.
- [Commonhold](https://commonhold.randommonicle.workers.dev) `https://commonhold.randommonicle.workers.dev/mcp/read`
  [![Commonhold MCP connector](https://glama.ai/mcp/connectors/io.github.randommonicle/commonhold/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.randommonicle/commonhold)
  🔓 - Read a society of AI agents: its board, citizens, proposals and ballots, constitution history and guest threads.
- [dopost](https://dopost.co/ai-agents) `https://mcp.dopost.co/mcp`
  [![dopost MCP connector](https://glama.ai/mcp/connectors/co.dopost.mcp/dopost/badges/score.svg)](https://glama.ai/mcp/connectors/co.dopost.mcp/dopost)
  🔐 - Schedule, publish and analyze posts on 12 networks, including X, Bluesky, Mastodon, Telegram, LinkedIn and Instagram.
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
- [Ignix](https://ignix.social) `https://ignix.social/api/mcp`
  [![Ignix MCP connector](https://glama.ai/mcp/connectors/social.ignix/ignix/badges/score.svg)](https://glama.ai/mcp/connectors/social.ignix/ignix)
  🔐 - Run social media from AI: schedule 14 networks, comment-to-DM bots, one inbox, analytics, AI posts and video.
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
- [NEROWRECK](https://neronewrecklive.link) `https://neronewrecklive.link/mcp`
  [![NEROWRECK MCP connector](https://glama.ai/mcp/connectors/link.neronewrecklive/haven/badges/score.svg)](https://glama.ai/mcp/connectors/link.neronewrecklive/haven)
  🔓 - Read and post to permanent, time-ordered rooms for agents; a short puzzle grants a 24-hour token, no account.
- [oganvil](https://oganvil.rowu.workers.dev) `https://oganvil.rowu.workers.dev/mcp`
  [![oganvil MCP connector](https://glama.ai/mcp/connectors/dev.workers.rowu.oganvil/og-image-api/badges/score.svg)](https://glama.ai/mcp/connectors/dev.workers.rowu.oganvil/og-image-api)
  🔓 - Generate 1200x630 OG images as PNG or SVG from a title and tagline; free tier.
- [OmniSocials](https://omnisocials.com) `https://mcp.omnisocials.com/`
  [![OmniSocials MCP connector](https://glama.ai/mcp/connectors/com.omnisocials.mcp/omni-socials/badges/score.svg)](https://glama.ai/mcp/connectors/com.omnisocials.mcp/omni-socials)
  🔑 - Publish and schedule posts across social networks.
- [Pith](https://pith.day/connect/mcp) `https://pith.day/api/mcp`
  [![Pith MCP connector](https://glama.ai/mcp/connectors/day.pith/pith-instagram-publishing/badges/score.svg)](https://glama.ai/mcp/connectors/day.pith/pith-instagram-publishing)
  🔐 - Publish your photo and caption to Instagram, and review and approve daily AI story drafts.
- [Post Bridge](https://www.post-bridge.com/mcp) `https://www.post-bridge.com/api/mcp/mcp`
  [![Post Bridge MCP connector](https://glama.ai/mcp/connectors/io.github.jackfriks/post-bridge/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.jackfriks/post-bridge)
  🔐 - Publish, schedule and analyze posts across ten platforms, from Instagram and TikTok to LinkedIn and Bluesky.
- [PostLake](https://postlake.dev) `https://api.postlake.dev/mcp`
  [![PostLake MCP connector](https://glama.ai/mcp/connectors/dev.postlake/social/badges/score.svg)](https://glama.ai/mcp/connectors/dev.postlake/social)
  🔐 - Publish, schedule and analyze posts across 9 networks, including X, LinkedIn, Instagram, TikTok and Bluesky.
- [PostNext](https://postnext.io/mcp) `https://mcp.postnext.io/api`
  [![PostNext MCP connector](https://glama.ai/mcp/connectors/io.postnext/postnext/badges/score.svg)](https://glama.ai/mcp/connectors/io.postnext/postnext)
  🔐 - Draft, schedule and publish to X, Instagram, LinkedIn, TikTok and more, plus channel analytics.
- [PostQuest](https://post-quest.com/mcp) `https://mcp.post-quest.com/mcp`
  [![PostQuest MCP connector](https://glama.ai/mcp/connectors/com.post-quest/postquest/badges/score.svg)](https://glama.ai/mcp/connectors/com.post-quest/postquest)
  🔐 - Draft, validate, schedule and publish posts to 10 networks, with platform rule checks and post analytics.
- [PostWire](https://postwire.io/mcp/) `https://postwire.io/api/mcp`
  [![PostWire MCP connector](https://glama.ai/mcp/connectors/io.github.Perufitlife/postwire-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Perufitlife/postwire-mcp)
  🔓 - Write a native post per network from one idea and publish it to TikTok, Instagram, YouTube and more; tools need OAuth.
- [Publora](https://publora.com) `https://mcp.publora.com/mcp`
  [![Publora MCP connector](https://glama.ai/mcp/connectors/com.publora/mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/com.publora/mcp-server)
  🔐 - Draft, schedule and publish posts to LinkedIn, X, Instagram, Threads, TikTok, YouTube, Bluesky and more.
- [Runsheet](https://runsheet.buildifyapp.in/mcp) `https://runsheet.buildifyapp.in/api/mcp`
  [![Runsheet MCP connector](https://glama.ai/mcp/connectors/in.buildifyapp.runsheet/youtube-scheduler/badges/score.svg)](https://glama.ai/mcp/connectors/in.buildifyapp.runsheet/youtube-scheduler)
  🔐 - Read a YouTube channel's schedule and stats, schedule, publish and retitle videos, and draft copy, all on approval.
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
- [SocialDataX Instagram](https://socialdatax.com/ai?from=awesome-remote-punkpeye) `https://mcp.socialdatax.com/instagram/mcp`
  [![SocialDataX Instagram MCP connector](https://glama.ai/mcp/connectors/com.52choujiang/instagram-insights/badges/score.svg)](https://glama.ai/mcp/connectors/com.52choujiang/instagram-insights)
  🔓 - Search Instagram posts and creators, and read media details and comments; API key for tool calls.
- [SocialFaktory](https://www.socialfaktory.com) `https://www.socialfaktory.com/mcp`
  [![SocialFaktory MCP connector](https://glama.ai/mcp/connectors/com.socialfaktory/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.socialfaktory/mcp)
  🔐 - Write, schedule and publish a brand's social content on TikTok, Instagram, YouTube, X and more.
- [Sociality MCP](https://sociality.io/mcp) `https://api.sociality.io/mcp`
  [![Sociality MCP connector](https://glama.ai/mcp/connectors/io.sociality/sociality-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.sociality/sociality-mcp)
  🔐 - Analyze social account performance, published posts, and competitors across six social networks.
- [SocialRobot](https://socialrobot.io/mcp) `https://socialrobot.io/api/mcp`
  [![SocialRobot MCP connector](https://glama.ai/mcp/connectors/io.socialrobot/socialrobot-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.socialrobot/socialrobot-mcp)
  🔓 - Schedule and analyze posts on 9 platforms, including Instagram, LinkedIn, X and TikTok; tools need OAuth.
- [SocialToAI](https://socialtoai.com/?utm_source=awesome-remote-mcp-servers&utm_medium=directory) `https://mcp.socialtoai.com/mcp`
  [![SocialToAI MCP connector](https://glama.ai/mcp/connectors/com.socialtoai/socialtoai/badges/score.svg)](https://glama.ai/mcp/connectors/com.socialtoai/socialtoai)
  🔐 - Read public social media posts, comments, profiles and trends from 18 platforms, billed per call.
- [Statiko](https://statiko.io/product/mcp) `https://mcp.statiko.io/mcp`
  [![Statiko MCP connector](https://glama.ai/mcp/connectors/io.statiko.mcp/statiko/badges/score.svg)](https://glama.ai/mcp/connectors/io.statiko.mcp/statiko)
  🔓 - Trending topics, channel metrics and post history from public Telegram; tools need OAuth.
- [Superpowers.social](https://superpowers.social) `https://superpowers.social/mcp`
  [![Superpowers.social MCP connector](https://glama.ai/mcp/connectors/social.superpowers/social-superpowers/badges/score.svg)](https://glama.ai/mcp/connectors/social.superpowers/social-superpowers)
  🔓 - Read-only search and retrieval of live X/Twitter and Reddit posts, threads, users, and subreddits.
- [Tailwind](https://www.tailwindapp.com/mcp?utm_source=awesome-remote-mcp&utm_medium=directory&utm_campaign=mcp-directories) `https://mcp.tailwind.ai`
  [![Tailwind MCP connector](https://glama.ai/mcp/connectors/ai.tailwind/tailwind-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/ai.tailwind/tailwind-mcp)
  🔐 - Create, schedule, and analyze Pinterest Pins across your connected Pinterest accounts.
- [Taplio](https://taplio.com/taplio-linkedin-mcp) `https://mcp.taplio.com/`
  [![Taplio MCP connector](https://glama.ai/mcp/connectors/io.github.TaplioOfficial/taplio-linkedin-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.TaplioOfficial/taplio-linkedin-mcp)
  🔐 - Write, schedule and analyze LinkedIn posts, find inspiration, comment, like and connect via Taplio.
- [TubeGrade](https://www.tubegrade.com/mcp/) `https://api.tubegrade.com/mcp`
  [![TubeGrade MCP connector](https://glama.ai/mcp/connectors/com.tubegrade/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.tubegrade/mcp)
  🔐 - YouTube research: channel and video stats, transcripts, outlier videos, viral title formats and competitor tracking.
- [Unsora](https://tryunsora.com) `https://mcp.tryunsora.com/mcp`
  [![Unsora MCP connector](https://glama.ai/mcp/connectors/com.tryunsora.mcp/unsora/badges/score.svg)](https://glama.ai/mcp/connectors/com.tryunsora.mcp/unsora)
  🔐 - Generate AI images, video, music and voiceovers, clip long videos, and schedule social posts.
- [ViralDecoder](https://viraldecoder.online/claude) `https://viraldecoder.online/mcp`
  [![ViralDecoder MCP connector](https://glama.ai/mcp/connectors/online.viraldecoder/viraldecoder/badges/score.svg)](https://glama.ai/mcp/connectors/online.viraldecoder/viraldecoder)
  🔐 - Breaks down Instagram Reels, Shorts and TikToks: hook score, why it went viral, a script for yours.
- [VoiceMoat](https://voicemoat.com/mcp) `https://app.voicemoat.com/api/mcp`
  [![VoiceMoat MCP connector](https://glama.ai/mcp/connectors/com.voicemoat/voicemoat/badges/score.svg)](https://glama.ai/mcp/connectors/com.voicemoat/voicemoat)
  🔐 - Score drafts against your voice profile, improve them, and schedule or publish posts on Twitter/X and LinkedIn.
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
- [BankrollSZN](https://bankrollszn.com/ai) `https://bankrollszn.com/api/mcp`
  [![BankrollSZN MCP connector](https://glama.ai/mcp/connectors/com.bankrollszn/bankrollszn/badges/score.svg)](https://glama.ai/mcp/connectors/com.bankrollszn/bankrollszn)
  🔐 - DFS projections, ownership, lineup optimizers and model picks for NFL, MLB, NBA, NHL, PGA and MMA.
- [Coach MCP](https://www.iamcoach.ai/mcp) `https://mcp.iamcoach.ai`
  [![Coach MCP connector](https://glama.ai/mcp/connectors/ai.iamcoach.mcp/coach-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/ai.iamcoach.mcp/coach-mcp)
  🔐 - Read your endurance training data, recovery metrics and plan, and move workouts or log injuries from your assistant.
- [MYOPL Pickleball Knowledge](https://myopl.net/opl-intelligence/connect-your-ai/) `https://api.myopl.net/mcp`
  [![MYOPL Pickleball Knowledge MCP connector](https://glama.ai/mcp/connectors/net.myopl/pickleball-public-knowledge/badges/score.svg)](https://glama.ai/mcp/connectors/net.myopl/pickleball-public-knowledge)
  🔓 - Official 2026 USA Pickleball rules, free 4-decimal player ratings, and court/club directory.
- [OpenMapp](https://www.openmapp.com) `https://www.openmapp.com/mcp`
  [![OpenMapp MCP connector](https://glama.ai/mcp/connectors/com.openmapp/openmapp/badges/score.svg)](https://glama.ai/mcp/connectors/com.openmapp/openmapp)
  🔓 - Find US BJJ gyms with weekly schedules, open mats, and visitor drop-in prices.

- [EndzoneAPI](https://endzoneapi.com) `https://mcp.endzoneapi.com/mcp`
  [![EndzoneAPI MCP connector](https://glama.ai/mcp/connectors/io.github.noahowsh/endzoneapi/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.noahowsh/endzoneapi)
  🔓 - NFL play-by-play with EPA since 1999, player and team stats, injuries, and closing lines for every game.
- [Football Charts](https://www.football-charts.com/developers) `https://mcp.football-charts.com/mcp`
  [![Football Charts MCP connector](https://glama.ai/mcp/connectors/io.github.ddevetak/footballcharts-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ddevetak/footballcharts-mcp)
  🔓 - Results, fixtures, tables, goal timing and season projections for 93 football leagues, lower divisions included.
- [PadelTrue](https://padeltrue.com/agents) `https://padeltrue.com/mcp`
  [![PadelTrue MCP connector](https://glama.ai/mcp/connectors/io.github.odedkovach/padeltrue/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.odedkovach/padeltrue)
  🔓 - Search and compare padel rackets by published specs, each spec linked to its source.
- [Pickleball3](https://pickleball3.com) `https://pickleball3.com/mcp`
  [![Pickleball3 MCP connector](https://glama.ai/mcp/connectors/io.github.gospodindark-stack/pickleball3/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.gospodindark-stack/pickleball3)
  🔓 - Compare 152 reviewed pickleball paddles by score and specs, with purchase links.
- [Race Results](https://raceresultsapp.com/mcp-server) `https://raceresultsapp.com/mcp`
  [![Race Results MCP connector](https://glama.ai/mcp/connectors/io.github.manuelescrig/raceresults-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.manuelescrig/raceresults-mcp)
  🔓 - MotoGP, Moto2 and Moto3 standings, race results, calendar and session times, rider profiles, live timing and news.
- [RallyIQ](https://bigballi.com/RallyIQ/connect) `https://bigballi.com/RallyIQ/mcp`
  [![RallyIQ MCP connector](https://glama.ai/mcp/connectors/com.bigballi/rallyiq/badges/score.svg)](https://glama.ai/mcp/connectors/com.bigballi/rallyiq)
  🔓 - Tennis game plans, player scouting and match breakdowns from shot-by-shot charted ATP and WTA matches.
- [Realtime Sports API](https://www.realtimesportsapi.com/docs/mcp?utm_source=awesome-remote-mcp-servers) `https://www.realtimesportsapi.com/api/mcp`
  [![Realtime Sports API MCP connector](https://glama.ai/mcp/connectors/io.github.ahunter135/realtime-sports-api/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ahunter135/realtime-sports-api)
  🔓 - Live scores, play-by-play, schedules and odds for NFL, NCAA football, NBA, MLB, NHL and soccer; calls need a free key.
- [SportAPI](https://sportapi.ai/mcp-server) `https://sportapi.ai/mcp`
  [![SportAPI MCP connector](https://glama.ai/mcp/connectors/ai.sportapi/football/badges/score.svg)](https://glama.ai/mcp/connectors/ai.sportapi/football)
  🔓 - Football fixtures, live scores, standings, lineups, teams and players for 117 leagues; tool calls need a free API key.
- [Squadcard](https://squadcard.app/agents) `https://squadcard.app/api/mcp`
  [![Squadcard MCP connector](https://glama.ai/mcp/connectors/io.github.iuliczki/squadcard/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.iuliczki/squadcard)
  🔐 - Run a weekly football game: fair teams, fixtures, squads with invite links, who's in and the score.
- [StringSpec](https://stringspec.com/connect/) `https://stringspec.com/mcp`
  [![StringSpec MCP connector](https://glama.ai/mcp/connectors/com.stringspec/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.stringspec/mcp)
  🔓 - Lab measurements of nearly 800 tennis strings: search, compare and get string recommendations.
- [Turnale](https://www.turnale.app) `https://mcp.turnale.app`
  [![Turnale MCP connector](https://glama.ai/mcp/connectors/app.turnale/turnale/badges/score.svg)](https://glama.ai/mcp/connectors/app.turnale/turnale)
  🔓 - Run recreational racket-sport tournaments: draws, schedules, live standings and dropouts.
- [FastballAPI](https://fastballapi.com) `https://mcp.fastballapi.com/mcp`
  [![FastballAPI MCP connector](https://glama.ai/mcp/connectors/io.github.noahowsh/fastballapi/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.noahowsh/fastballapi)
  🔓 - MLB since 2015 plus college: pitches, plate appearances, box scores, odds by book.

### 🎧 <a name="support--service-management"></a>Support & Service Management

- [Actually Asked](https://actuallyasked.com/mcp) `https://mcp.actuallyasked.com/mcp`
  [![Actually Asked MCP connector](https://glama.ai/mcp/connectors/com.actuallyasked/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.actuallyasked/mcp)
  🔐 - Review what visitors asked on your website, publish FAQ answers written from your own pages, and follow up on leads.
- [DevReply](https://devreply.com) `https://api.devreply.com/mcp`
  [![DevReply MCP connector](https://glama.ai/mcp/connectors/com.devreply/devreply/badges/score.svg)](https://glama.ai/mcp/connectors/com.devreply/devreply)
  🔐 - Read, triage and answer the users of your mobile and web apps from their in-app support chat.
- [EOSL.ai](https://eosl.ai/mcp/) `https://eosl.ai/mcp`
  [![EOSL.ai MCP connector](https://glama.ai/mcp/connectors/ai.eosl/eosl/badges/score.svg)](https://glama.ai/mcp/connectors/ai.eosl/eosl)
  🔓 - Hardware end-of-life lookups by part number, backed by vendor bulletins.
- [Fieldproxy](https://www.fieldproxy.ai/mcp) `https://api-us-east-1.fieldproxy.ai/mcp`
  [![Fieldproxy MCP connector](https://glama.ai/mcp/connectors/io.github.Fieldproxy/fieldproxy-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Fieldproxy/fieldproxy-mcp)
  🔐 - Run field service jobs, dispatch, invoices and quotes, and build new screens, with a person confirming each change.
- [FrontDesk Chat](https://frontdeskchat.com/features/mcp/) `https://api.frontdeskchat.com/mcp`
  [![FrontDesk Chat MCP connector](https://glama.ai/mcp/connectors/io.github.5ak3t/frontdeskchat/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.5ak3t/frontdeskchat)
  🔐 - Read your AI website front desk's conversations, visitors, bookings and analytics, and draft desk changes for approval.
- [Intercom](https://intercom.com) `https://mcp.intercom.com/mcp`
  🔐 - Search Intercom conversations, contacts, and help-center articles.
- [NexTool MCP for GLPI](https://nextoolsolutions.com/mcp) `https://mcp.nextoolsolutions.com/mcp`
  [![NexTool MCP for GLPI MCP connector](https://glama.ai/mcp/connectors/com.nextoolsolutions/glpi/badges/score.svg)](https://glama.ai/mcp/connectors/com.nextoolsolutions/glpi)
  🔐 - Search, create and update GLPI tickets, ITIL problems and changes, assets and knowledge base.
- [ORYKSA AI Employees](https://mcp.oryksa.com) `https://mcp.oryksa.com`
  [![ORYKSA AI Employees MCP connector](https://glama.ai/mcp/connectors/com.oryksa/ai-employees/badges/score.svg)](https://glama.ai/mcp/connectors/com.oryksa/ai-employees)
  🔐 - Add an AI support agent to the site you build: it learns every page and answers visitors by chat and voice.
- [SavantCat Answers](https://savantcat.cn/mcp/) `https://savantcat.cn/mcp`
  [![SavantCat Answers MCP connector](https://glama.ai/mcp/connectors/cn.savantcat/answers/badges/score.svg)](https://glama.ai/mcp/connectors/cn.savantcat/answers)
  🔓 - China's GB/T 47746-2026 AI customer-service standard: clause Q&A, self-check list and filing rules.
- [WorkWing](https://www.workwing.io/developers) `https://api.workwing.io/mcp`
  [![WorkWing MCP connector](https://glama.ai/mcp/connectors/io.workwing/workwing/badges/score.svg)](https://glama.ai/mcp/connectors/io.workwing/workwing)
  🔐 - Field service jobs: find customers and engineers, read the schedule, create and book jobs, and add notes.

### 🌍 <a name="translation--localization"></a>Translation & Localization

- [eVerbary](https://www.everbary.com/integrations/ai-assistants) `https://orders.everbary.com/mcp`
  [![eVerbary MCP connector](https://glama.ai/mcp/connectors/com.everbary.www/orders/badges/score.svg)](https://glama.ai/mcp/connectors/com.everbary.www/orders)
  🔐 - Quote, order, pay for and track certified translations of official documents for USCIS, courts and universities.
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
- [Adaga Network — Direct Booking Federation](https://adagasolutions.lu) `https://adagasolutions.lu/network/mcp`
  [![Adaga Network — Direct Booking Federation MCP connector](https://glama.ai/mcp/connectors/io.github.jeffreyturov-dev/adaga-network/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.jeffreyturov-dev/adaga-network)
  🔓 - Search and book every establishment of the Adaga network at exact direct prices — no OTA commission.
- [Airfare Brain](https://airfarebrain.com) `https://airfarebrain.com/mcp`
  [![Airfare Brain MCP connector](https://glama.ai/mcp/connectors/com.airfarebrain/airfare-brain/badges/score.svg)](https://glama.ai/mcp/connectors/com.airfarebrain/airfare-brain)
  🔓 - True cost of a flight: bag, seat and fee prices on 19 airlines, each from the airline's own pages, dated.
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
- [busik.ch](https://busik.ch) `https://busik.ch/api/mcp`
  [![busik.ch MCP connector](https://glama.ai/mcp/connectors/ch.busik/fahrten/badges/score.svg)](https://glama.ai/mcp/connectors/ch.busik/fahrten)
  🔓 - Minibus trips between Ukraine, Germany and Switzerland: search departures, prices, seats and booking links.
- [Car Rental Brain](https://carrentalbrain.com/ai/) `https://app.carrentalbrain.com/mcp`
  [![Car Rental Brain MCP connector](https://glama.ai/mcp/connectors/com.carrentalbrain/car-rental-brain/badges/score.svg)](https://glama.ai/mcp/connectors/com.carrentalbrain/car-rental-brain)
  🔓 - Real car-hire costs at 120+ airports: second-driver fees, deposits, debit cards, desk hours and desk excess cover.
- [China Footnotes](https://chinafootnotes.com) `https://chinafootnotes.com/mcp`
  [![China Footnotes MCP connector](https://glama.ai/mcp/connectors/com.chinafootnotes/china-footnotes/badges/score.svg)](https://glama.ai/mcp/connectors/com.chinafootnotes/china-footnotes)
  🔓 - Sourced, dated travel facts for first-time visitors to China: hours, tickets, booking and passport notes.
- [Déstaire](https://destaire.com) `https://destaire.com/mcp`
  [![Déstaire MCP connector](https://glama.ai/mcp/connectors/com.destaire/destaire/badges/score.svg)](https://glama.ai/mcp/connectors/com.destaire/destaire)
  🔓 - A curated guide to exceptional hotels and private stays, with editorial content and city guides.
- [EasyGroupFlights](https://easygroupflights.com/group-flights-mcp/) `https://mcp.easygroupflights.com/mcp`
  [![EasyGroupFlights MCP connector](https://glama.ai/mcp/connectors/com.easygroupflights/easygroupflights/badges/score.svg)](https://glama.ai/mcp/connectors/com.easygroupflights/easygroupflights)
  🔓 - Request group flight quotes for 10+ travellers from a human specialist desk; live fares for smaller parties.
- [entityindex.ai](https://entityindex.ai/mcp-info/) `https://entityindex.ai/mcp`
  [![entityindex.ai MCP connector](https://glama.ai/mcp/connectors/ai.entityindex/entityindex/badges/score.svg)](https://glama.ai/mcp/connectors/ai.entityindex/entityindex)
  🔓 - Verified hotels in Andorra with spa, pets, ski-in and family filters and official booking links.
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
- [HaulierScope](https://haulierscope.co.uk/developers) `https://haulierscope.co.uk/mcp`
  [![HaulierScope MCP connector](https://glama.ai/mcp/connectors/uk.co.haulierscope/operator-licences/badges/score.svg)](https://glama.ai/mcp/connectors/uk.co.haulierscope/operator-licences)
  🔓 - UK operator licence checks for hauliers and coach firms: status, vehicles, changes and public inquiries; no sign-in.
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
- [Meridian Dispatch](https://www.meridiandispatch.com/mcp) `https://www.meridiandispatch.com/api/mcp`
  [![Meridian Dispatch MCP connector](https://glama.ai/mcp/connectors/com.meridiandispatch/travel-guides/badges/score.svg)](https://glama.ai/mcp/connectors/com.meridiandispatch/travel-guides)
  🔓 - Free travel reference for AI agents: reported guides to destinations worldwide.
- [Mirabello Immigration Intelligence](https://www.mirabelloconsultancy.com/mcp) `https://mcp.mirabelloconsultancy.com/`
  [![Mirabello Immigration Intelligence MCP connector](https://glama.ai/mcp/connectors/io.github.mirabello-consultancy/mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.mirabello-consultancy/mcp-server)
  🔓 - Citizenship and residency by investment, visas and immigration pathways in 194 countries, source-cited.
- [MobilityMCP](https://ai.projektionisten.eu/mcp-landingpage/#mmcp) `https://ai.projektionisten.eu/mmcp`
  [![MobilityMCP connector](https://glama.ai/mcp/connectors/eu.projektionisten/mobility/badges/score.svg)](https://glama.ai/mcp/connectors/eu.projektionisten/mobility)
  🔐 - German public transport: journeys, departures, disruptions, and nearby stops and sharing vehicles.
- [Mubboo Flights Search](https://mubboo.flights/mcp) `https://mubboo.flights/api/mcp`
  [![Mubboo Flights Search MCP connector](https://glama.ai/mcp/connectors/flights.mubboo/flight-search/badges/score.svg)](https://glama.ai/mcp/connectors/flights.mubboo/flight-search)
  🔓 - Prepare flight searches with less setup: find airports, validate trip details and create comparison links.
- [My Next Adventure](https://mynextadventure.cloud/mcp?utm_source=awesome-remote-mcp) `https://mcp.mynextadventure.cloud/mcp`
  [![My Next Adventure MCP connector](https://glama.ai/mcp/connectors/cloud.mynextadventure/trip-planner/badges/score.svg)](https://glama.ai/mcp/connectors/cloud.mynextadventure/trip-planner)
  🔐 - Trip planner your AI fills in: variants with costs side by side, stays, transport, events and share links.
- [MyBestSim](https://mybestsim.com/?utm_source=github&utm_medium=mcp-directory&utm_campaign=awesome-remote-mcp-servers) `https://mcp.mybestsim.com/mcp`
  [![MyBestSim MCP connector](https://glama.ai/mcp/connectors/com.mybestsim/esim-comparator/badges/score.svg)](https://glama.ai/mcp/connectors/com.mybestsim/esim-comparator)
  🔓 - Compare prepaid travel eSIM plans by destination, data and trip length, and plan multi-country trips.
- [NC Wedding Guide](https://www.ncweddingguide.com) `https://www.ncweddingguide.com/mcp`
  [![NC Wedding Guide MCP connector](https://glama.ai/mcp/connectors/io.github.Sebastianrtj/nc-wedding-guide/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Sebastianrtj/nc-wedding-guide)
  🔓 - Search North Carolina wedding venues and vendors, estimate costs, build budgets, and prepare vendor inquiries.
- [NomadPoint Travel Facts](https://nomadpoint.app/llms.txt) `https://gxhdcvoveufbkthhendf.supabase.co/functions/v1/mcp-public`
  [![NomadPoint Travel Facts MCP connector](https://glama.ai/mcp/connectors/app.nomadpoint/travel-facts/badges/score.svg)](https://glama.ai/mcp/connectors/app.nomadpoint/travel-facts)
  🔓 - Visa rules for any passport, Schengen 90/180 day counts, and itinerary links a traveller saves for free.
- [OctoTrip](https://octotrip.app) `https://mcp.octotrip.app/rental-cars/mcp`
  [![OctoTrip MCP connector](https://glama.ai/mcp/connectors/app.octotrip/rental-cars/badges/score.svg)](https://glama.ai/mcp/connectors/app.octotrip/rental-cars)
  🔓 - Search and compare rental cars with real-time pricing across providers worldwide.
- [Portmans Motor Lodge](https://www.portmans.co.nz/) `https://portmans-mcp.portmanshastings.workers.dev/mcp`
  [![Portmans Motor Lodge MCP connector](https://glama.ai/mcp/connectors/io.github.briandoylenz/portmans-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.briandoylenz/portmans-mcp)
  🔓 - Hotel availability, public BAR rates, and a direct booking link for Portmans Motor Lodge in Hastings, New Zealand.
- [PriceWin](https://www.price.win/) `https://mcp.price.win/mcp`
  [![PriceWin MCP connector](https://glama.ai/mcp/connectors/win.price/pricewin/badges/score.svg)](https://glama.ai/mcp/connectors/win.price/pricewin)
  🔓 - Compare live hotel and flight prices across Booking.com, Agoda, Trip.com and Traveloka, in USD.
- [Roamzy](https://roamzy.io) `https://roamzy.io/mcp`
  [![Roamzy MCP connector](https://glama.ai/mcp/connectors/io.github.roamzy-io/mcp-server/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.roamzy-io/mcp-server)
  🔓 - Buy and manage one global eSIM for 193 countries, billed per megabyte in USDT or USDC, no KYC.
- [Rozkład PKP/PKS (rozklad-mcp)](https://rozklad.compabase.com) `https://rozklad.compabase.com/mcp`
  [![Rozkład PKP/PKS (rozklad-mcp) MCP connector](https://glama.ai/mcp/connectors/io.github.ContentWriterco/rozklad-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.ContentWriterco/rozklad-mcp)
  🔓 - Polish trains, PKS buses and city transit: journeys with changes, departures, live delays and fares.
- [SafeResize](https://saferesize.com/ai) `https://saferesize.com/mcp`
  [![SafeResize MCP connector](https://glama.ai/mcp/connectors/com.saferesize/saferesize/badges/score.svg)](https://glama.ai/mcp/connectors/com.saferesize/saferesize)
  🔓 - Official passport, visa and ID photo rules for 110 documents in 60 countries, plus upload-rule checks.
- [Samuelz Chauffeur Booking](https://samuelz.com/en/docs) `https://platform-api.samuelz.com/api/v1/mcp/chauffeur/samuelz-chauffeur`
  [![Samuelz Chauffeur Booking MCP connector](https://glama.ai/mcp/connectors/com.samuelz.platform-api/samuelz-chauffeur-booking/badges/score.svg)](https://glama.ai/mcp/connectors/com.samuelz.platform-api/samuelz-chauffeur-booking)
  🔓 - Chauffeur price previews and consent-led unpaid booking offers for the provider's published service areas.
- [Schengen 90/180 Calculator](https://schengen.al157.xyz) `https://schengen-mcp.alickzheng618.workers.dev/mcp`
  [![Schengen 90/180 Calculator MCP connector](https://glama.ai/mcp/connectors/io.github.al157/schengen-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.al157/schengen-mcp)
  🔓 - Schengen 90/180 rolling-window stay math: days used/remaining, trip compliance checks and rule explainer; read-only.
- [Schengen Counter](https://schengencounter.com/mcp/) `https://mcp.schengencounter.com/mcp`
  [![Schengen Counter MCP connector](https://glama.ai/mcp/connectors/com.schengencounter/schengen-counter/badges/score.svg)](https://glama.ai/mcp/connectors/com.schengencounter/schengen-counter)
  🔓 - Schengen 90/180 days used and left, earliest legal re-entry date and ETIAS check; stateless, nothing stored.
- [SkyAccess](https://skyaccess.com) `https://mcp.skyaccess.com/mcp`
  [![SkyAccess MCP connector](https://glama.ai/mcp/connectors/com.skyaccess/skyaccess/badges/score.svg)](https://glama.ai/mcp/connectors/com.skyaccess/skyaccess)
  🔓 - Private jet empty legs: search live flights, check one by id, get booking links and charter price estimates.
- [SlickTrip](https://slicktrip.com) `https://mcp.slicktrip.com/mcp`
  [![SlickTrip MCP connector](https://glama.ai/mcp/connectors/com.slicktrip/slicktrip/badges/score.svg)](https://glama.ai/mcp/connectors/com.slicktrip/slicktrip)
  🔓 - Live flight, hotel and seat prices, cheapest-day calendars, and price-drop and seat alerts.
- [Things To Do API](https://thingstodoapi.com) `https://api.thingstodoapi.com/mcp`
  [![Things To Do API MCP connector](https://glama.ai/mcp/connectors/com.thingstodoapi/events/badges/score.svg)](https://glama.ai/mcp/connectors/com.thingstodoapi/events)
  🔓 - Local events in plain words: concerts, pop-ups, markets and classes, with times, venues and prices.
- [TourismMCP](https://ai.projektionisten.eu/mcp-landingpage/#tmcp) `https://ai.projektionisten.eu/tmcp`
  [![TourismMCP connector](https://glama.ai/mcp/connectors/eu.projektionisten/tourism/badges/score.svg)](https://glama.ai/mcp/connectors/eu.projektionisten/tourism)
  🔐 - German travel: sights, opening hours, prices, events, weather and tides, densest in Lower Saxony.
- [Travel Check](https://tools.openkrill.app/#travel) `https://travel.openkrill.app/mcp`
  [![Travel Check MCP connector](https://glama.ai/mcp/connectors/app.openkrill/travel/badges/score.svg)](https://glama.ai/mcp/connectors/app.openkrill/travel)
  🔓 - UK and US government travel advice by country, plus live FAA delays and weather for US airports.
- [TripWays](https://tripways.com/mcp/) `https://mcp.tripways.com/mcp`
  [![TripWays MCP connector](https://glama.ai/mcp/connectors/com.tripways/tours/badges/score.svg)](https://glama.ai/mcp/connectors/com.tripways/tours)
  🔓 - Tours, day trips and activities in 120 countries: live dates, seats and group prices, with TripWays checkout links.
- [Trvlrr](https://trvlrr.app/assistants) `https://trvlrr.app/mcp`
  [![Trvlrr MCP connector](https://glama.ai/mcp/connectors/app.trvlrr/trvlrr/badges/score.svg)](https://glama.ai/mcp/connectors/app.trvlrr/trvlrr)
  🔐 - Personal travel journal: trips, flights, stays, stats and photo search; import trips and add bookings.
- [Untap](https://untap.money/connect) `https://untap.money/api/mcp`
  [![Untap MCP connector](https://glama.ai/mcp/connectors/io.github.aneduaim/untap-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.aneduaim/untap-mcp)
  🔓 - Checks UK train Delay Repay, UK261 and EU261 flight compensation and TfL refunds, with the amount and how to claim.
- [Vedar](https://vedarai.ru/mcp) `https://vedarai.ru/api/mcp`
  [![Vedar MCP connector](https://glama.ai/mcp/connectors/ru.vedarai/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/ru.vedarai/mcp)
  🔓 - Kamchatka travel: live tours and availability, safety alerts, weather, stays and trip plans.
- [ViaFrei](https://viafrei.de) `https://mcp.viafrei.de/mcp`
  [![ViaFrei MCP connector](https://glama.ai/mcp/connectors/de.viafrei.mcp/via-frei/badges/score.svg)](https://glama.ai/mcp/connectors/de.viafrei.mcp/via-frei)
  🔓 - Germany's open mobility data: Autobahn traffic, DB trains, local transit, fuel, EV charging, parking and DWD warnings.
- [VoyageHacks](https://voyagehacks.com/en/mcp-server/) `https://voyagehacks.com/mcp`
  [![VoyageHacks MCP connector](https://glama.ai/mcp/connectors/com.voyagehacks/travel/badges/score.svg)](https://glama.ai/mcp/connectors/com.voyagehacks/travel)
  🔓 - Search fact-checked travel guides in 11 languages, build packing kits, and get booking links.
- [What's Up In](https://whatsupin.ai/agents/) `https://whatsupin.ai/mcp`
  [![What's Up In MCP connector](https://glama.ai/mcp/connectors/ai.whatsupin/events/badges/score.svg)](https://glama.ai/mcp/connectors/ai.whatsupin/events)
  🔓 - Upcoming local events in 14 US cities by date, topic, neighborhood or artist, each linked to its source.
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

- [Account Executive Jobs](https://accountexecutivejobs.com) `https://mcp.accountexecutivejobs.com/mcp`
  [![Account Executive Jobs MCP connector](https://glama.ai/mcp/connectors/com.accountexecutivejobs/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.accountexecutivejobs/mcp)
  🔐 - Search sales and account executive jobs and apply, or manage your company's job posts and applicants.
- [AccountHub](https://accounthub.ai) `https://accounthub.ai/api/mcp`
  [![AccountHub MCP connector](https://glama.ai/mcp/connectors/ai.accounthub/account-hub/badges/score.svg)](https://glama.ai/mcp/connectors/ai.accounthub/account-hub)
  🔐 - Search and act across multiple Gmail, Google Calendar, Drive and Contacts accounts, Slack workspaces and Notion.
- [AI Applyd](https://aiapplyd.com/mcps) `https://mcp.aiapplyd.com/mcp`
  [![AI Applyd MCP connector](https://glama.ai/mcp/connectors/io.github.whateverneveranywhere/aiapplyd/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.whateverneveranywhere/aiapplyd)
  🔓 - Resume scoring and rewrites, cover letters and auto-apply on 12 ATS platforms; needs Google sign-in.
- [AI Rollout Framework](https://airolloutframework.com) `https://airolloutframework.com/mcp`
  [![AI Rollout Framework MCP connector](https://glama.ai/mcp/connectors/com.airolloutframework/ai-rollout-framework/badges/score.svg)](https://glama.ai/mcp/connectors/com.airolloutframework/ai-rollout-framework)
  🔓 - 90-day AI adoption framework for managers: overview, pricing, FAQ and an AI readiness assessment.
- [AIBuilder Marketplace](https://aibuildermarketplace.com/agents/) `https://api.aibuildermarketplace.com/mcp`
  [![AIBuilder Marketplace MCP connector](https://glama.ai/mcp/connectors/com.aibuildermarketplace/software-pricing/badges/score.svg)](https://glama.ai/mcp/connectors/com.aibuildermarketplace/software-pricing)
  🔓 - Dated prices, evidence-backed cost traps and team-size cost estimates for 500+ business software tools.
- [Agora Merit](https://agoramerit.com/agents) `https://agoramerit.com/mcp`
  [![Agora Merit MCP connector](https://glama.ai/mcp/connectors/com.agoramerit/role-assessment/badges/score.svg)](https://glama.ai/mcp/connectors/com.agoramerit/role-assessment)
  🔓 - Assess job responsibilities; return free findings, report quotes, and private human review links.
- [Appty](https://getappty.com/developers) `https://getappty.com/api/mcp`
  [![Appty MCP connector](https://glama.ai/mcp/connectors/com.getappty/appty/badges/score.svg)](https://glama.ai/mcp/connectors/com.getappty/appty)
  🔓 - Find open slots and booking links on any appty link; providers manage bookings and invoices by sign-in or API key.
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
- [Dollea Beauty Coworking](https://coworking.dollea.de/agents/?language=en) `https://coworking.dollea.de/mcp/coworking`
  [![Dollea Beauty Coworking MCP connector](https://glama.ai/mcp/connectors/de.dollea/coworking/badges/score.svg)](https://glama.ai/mcp/connectors/de.dollea/coworking)
  🔓 - Public beauty workspace catalog in Munich; OAuth for personal prices and rental booking.
- [EasyPDF](https://www.easypdf.fr/ai-assistants) `https://www.easypdf.fr/mcp`
  [![EasyPDF MCP connector](https://glama.ai/mcp/connectors/io.github.Lorenzino69/easypdf/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Lorenzino69/easypdf)
  🔐 - Edit text inside PDFs with fonts and layout kept, then compress, merge, split, convert or translate them.
- [Eggtimer.app](https://eggtimer.app/ai.html) `https://eggtimer.app/api/mcp`
  [![Eggtimer.app MCP connector](https://glama.ai/mcp/connectors/app.eggtimer/eggtimer/badges/score.svg)](https://glama.ai/mcp/connectors/app.eggtimer/eggtimer)
  🔓 - Create shareable browser timer links for countdowns, clock times, Pomodoro, Tabata and multi-step recipes.
- [Emboss](https://getemboss.ai) `https://api.getemboss.ai/mcp`
  [![Emboss MCP connector](https://glama.ai/mcp/connectors/io.github.edwinorange/emboss/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.edwinorange/emboss)
  🔐 - Makes PDF forms fillable, fills them from data or documents, reads them back, and faxes the result.
- [Eodly](https://eodly.io/docs/mcp-server) `https://eodly.io/mcp`
  [![Eodly MCP connector](https://glama.ai/mcp/connectors/io.github.layergen/eodly-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.layergen/eodly-mcp)
  🔐 - Read a team's end-of-day reports and roster: who shipped, who is quiet, who is slipping.
- [ERP Partner Finder](https://erppartnerfinder.com) `https://erppartnerfinder.com/api/mcp`
  [![ERP Partner Finder MCP connector](https://glama.ai/mcp/connectors/com.erppartnerfinder/partner-finder/badges/score.svg)](https://glama.ai/mcp/connectors/com.erppartnerfinder/partner-finder)
  🔓 - Search and compare Odoo implementation partners in Germany, Austria and Switzerland, with rule-based shortlists.
- [Finder Jobs](https://mcp.finder.work) `https://mcp.finder.work/mcp`
  [![Finder Jobs MCP connector](https://glama.ai/mcp/connectors/work.finder/jobs/badges/score.svg)](https://glama.ai/mcp/connectors/work.finder/jobs)
  🔓 - Job vacancies and salary stats for Russia, Kazakhstan, Belarus, Kyrgyzstan, Germany, France and 4 more countries.
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
- [JustBacked](https://justbacked.com/developers) `https://justbacked.com/api/mcp`
  [![JustBacked MCP connector](https://glama.ai/mcp/connectors/com.justbacked/jobs/badges/score.svg)](https://glama.ai/mcp/connectors/com.justbacked/jobs)
  🔓 - Search open roles at startups that raised venture funding in the last 6 months, with round and investors.
- [JustFill](https://justfill.app/mcp) `https://justfill.app/api/mcp`
  [![JustFill MCP connector](https://glama.ai/mcp/connectors/io.github.mrmaciej1/justfill-pdf-forms/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.mrmaciej1/justfill-pdf-forms)
  🔐 - Detect, review, and fill existing PDF forms (including flat or scanned PDFs) from JSON or saved templates.
- [KDAN PDF](https://pdf-reader.kdandoc.com/products/mcp/claude) `https://mcp.kdandoc.com/mcp`
  [![KDAN PDF MCP connector](https://glama.ai/mcp/connectors/com.kdandoc.mcp/kdan-pdf-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.kdandoc.mcp/kdan-pdf-mcp)
  🔓 - Compress, delete pages, redact PII, compare versions, and add or remove password protection on PDFs.
- [LFG Alarm](https://lfg.gm) `https://mcp.lfg.gm`
  [![LFG Alarm MCP connector](https://glama.ai/mcp/connectors/gm.lfg/alarm/badges/score.svg)](https://glama.ai/mcp/connectors/gm.lfg/alarm)
  🔐 - Set real alarms that ring on your phone and your friends' phones: wake-up times, events, posts, price moves or webhooks.
- [LucyESL](https://lucyesl.com/developers) `https://lucyesl.com/mcp`
  [![LucyESL MCP connector](https://glama.ai/mcp/connectors/com.lucyesl/jobs/badges/score.svg)](https://glama.ai/mcp/connectors/com.lucyesl/jobs)
  🔓 - Search English-teaching jobs in South Korea and read their salary, disclosure and by-region statistics.
- [Lunacal](https://lunacal.ai) `https://mcp.lunacal.ai/mcp`
  [![Lunacal MCP connector](https://glama.ai/mcp/connectors/ai.lunacal.mcp/lunacal/badges/score.svg)](https://glama.ai/mcp/connectors/ai.lunacal.mcp/lunacal)
  🔐 - Find open slots, book, reschedule and cancel meetings, and create or update event types on Lunacal.
- [MagicInterview](https://magicinterview.app) `https://magicinterview.app/mcp`
  [![MagicInterview MCP connector](https://glama.ai/mcp/connectors/io.github.samihalawa/magicinterview/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.samihalawa/magicinterview)
  🔐 - Live AI suggestions for interviews, client calls, and meetings, with reusable context and conversation management.
- [MeetNotes](https://getmeetnotes.com/mcp/) `https://getmeetnotes.com/mcp`
  [![MeetNotes MCP connector](https://glama.ai/mcp/connectors/com.getmeetnotes/meetnotes/badges/score.svg)](https://glama.ai/mcp/connectors/com.getmeetnotes/meetnotes)
  🔐 - Search, read and export meeting transcripts, minutes and action items, and import audio for transcription.
- [Multi Calendar](https://lumman.co/mcp/multi-calendar) `https://calendar.lumman.co/mcp`
  [![Multi Calendar MCP connector](https://glama.ai/mcp/connectors/co.lumman/calendar/badges/score.svg)](https://glama.ai/mcp/connectors/co.lumman/calendar)
  🔐 - Find free time and manage events across Outlook.com, Microsoft 365 and Google calendars, with booking pages and polls.
- [NoClick](https://www.noclick.com/mcp) `https://api.noclick.io/mcp`
  [![NoClick MCP connector](https://glama.ai/mcp/connectors/io.github.noclickapp/noclick/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.noclickapp/noclick)
  🔐 - Build, run, and monitor workflows and background AI agents across connected apps.
- [Nodiom Cloud](https://nodiom.md/?utm_source=awesome-remote-mcp-pp&utm_medium=directory) `https://api.nodiom.md/mcp`
  [![Nodiom Cloud MCP connector](https://glama.ai/mcp/connectors/io.github.Synexiom-Labs/nodiom-cloud/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Synexiom-Labs/nodiom-cloud)
  🔐 - A shared board your agents claim work from, hand off on, and stop at for a person to approve.
- [Nolizi Calendar](https://calendar.nolizi.com/agents) `https://calendar.nolizi.com/mcp`
  [![Nolizi Calendar MCP connector](https://glama.ai/mcp/connectors/com.nolizi.calendar/calendar/badges/score.svg)](https://glama.ai/mcp/connectors/com.nolizi.calendar/calendar)
  🔓 - Free scheduling: list event types, read availability, book, verify and cancel; tools need a key.
- [Offpeak](https://offpeak.fyi) `https://offpeak.fyi/mcp`
  [![Offpeak MCP connector](https://glama.ai/mcp/connectors/io.github.vicentesurraco/offpeak/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.vicentesurraco/offpeak)
  🔓 - Search US jobs by driving commute, pay and seniority; optional OAuth sign-in saves jobs and searches.
- [Pally](https://pally.com/mcp) `https://agent.pally.com/mcp`
  [![Pally MCP connector](https://glama.ai/mcp/connectors/com.pally/pally/badges/score.svg)](https://glama.ai/mcp/connectors/com.pally/pally)
  🔐 - AI personal assistant you text: manage inbox, calendar, tasks and follow-ups over iMessage, WhatsApp and Telegram.
- [PDFLean](https://pdflean.com) `https://mcp.pdflean.com/mcp`
  [![PDFLean MCP connector](https://glama.ai/mcp/connectors/com.pdflean.mcp/pdflean/badges/score.svg)](https://glama.ai/mcp/connectors/com.pdflean.mcp/pdflean)
  🔐 - PDF tools for AI agents: validate, extract, merge, split, compress, OCR, sign and redact PDFs.
- [Poly-Glot AI Workspace](https://hmoses.github.io/dev-guide.html) `https://br-steep-leaf-ae2o29qz-mcp.compute.c-2.us-east-2.aws.neon.tech/mcp`
  [![Poly-Glot AI Workspace MCP connector](https://glama.ai/mcp/connectors/io.github.hmoses/poly-glot-ai-workspace/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.hmoses/poly-glot-ai-workspace)
  🔓 - Multilingual prompt workspace with 1,000+ templates in 35 languages, Compare Mode, and BYOM.
- [QuillHub](https://quillhub.ai/en/help/mcp-claude-cursor) `https://mcp.quillhub.ai/mcp`
  [![QuillHub MCP connector](https://glama.ai/mcp/connectors/ai.quillhub/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/ai.quillhub/mcp)
  🔐 - Search meeting transcripts, pull decisions and action items, and transcribe files and links.
- [ResuMakeAi](https://www.resumakeai.com) `https://www.resumakeai.com/api/mcp`
  [![ResuMakeAi MCP connector](https://glama.ai/mcp/connectors/com.resumakeai/resu-make-ai/badges/score.svg)](https://glama.ai/mcp/connectors/com.resumakeai/resu-make-ai)
  🔓 - Score a resume against a job description for ATS parsing, match percentage, and missing keywords.
- [ResumeQuick](https://resumequick.app) `https://mcp.resumequick.app/mcp`
  [![ResumeQuick MCP connector](https://glama.ai/mcp/connectors/app.resumequick/resumequick/badges/score.svg)](https://glama.ai/mcp/connectors/app.resumequick/resumequick)
  🔐 - Job search in your AI client: resumes, tracked jobs with fit analysis, daily job matches, mock interviews and offers.
- [Routine Run](https://routinerun.com/assistants) `https://api.routinerun.com/mcp`
  [![Routine Run MCP connector](https://glama.ai/mcp/connectors/com.routinerun/routine-run/badges/score.svg)](https://glama.ai/mcp/connectors/com.routinerun/routine-run)
  🔐 - Start, plan and move step-by-step routines on your iPhone, review your week, and suggest changes you approve.
- [Ruzora](https://www.ruzora.com/developers/mcp) `https://mcp.ruzora.com/mcp`
  [![Ruzora MCP connector](https://glama.ai/mcp/connectors/com.ruzora/ruzora/badges/score.svg)](https://glama.ai/mcp/connectors/com.ruzora/ruzora)
  🔓 - Open LATAM engineering roles, job-post linting, interview kits, vetted-engineer search and shortlist requests.
- [SayBriefly](https://saybriefly.com/mcp) `https://mcp.saybriefly.com/mcp`
  [![SayBriefly MCP connector](https://glama.ai/mcp/connectors/com.saybriefly/saybriefly/badges/score.svg)](https://glama.ai/mcp/connectors/com.saybriefly/saybriefly)
  🔐 - Search your recorded meetings, transcripts, decisions and action items, and list your open to-dos.
- [SheetRender](https://sheetrender.com/docs/chatgpt-and-claude) `https://mcp.sheetrender.com/mcp`
  [![SheetRender MCP connector](https://glama.ai/mcp/connectors/io.github.sheetrender/sheetrender-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.sheetrender/sheetrender-mcp)
  🔓 - Fills built-in certificate, letter, receipt and offer-letter templates from rows, one PDF per row.
- [Taskaid](https://taskaid.ai) `https://taskaid.ai/mcp`
  [![Taskaid MCP connector](https://glama.ai/mcp/connectors/ai.taskaid/taskaid/badges/score.svg)](https://glama.ai/mcp/connectors/ai.taskaid/taskaid)
  🔐 - Task management between you and your agents: read and update tasks that every connected assistant shares.
- [Telegram Calendar](https://calendar-tg.app/mcp) `https://calendar-tg.app/mcp`
  [![Telegram Calendar MCP connector](https://glama.ai/mcp/connectors/app.calendar-tg/telegram-calendar-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/app.calendar-tg/telegram-calendar-mcp)
  🔐 - Search, create, update and manage events across Google, Apple, CalDAV and Telegram.
- [Telesherpa](https://www.telesherpa.com) `https://mcp.telesherpa.com/mcp`
  [![Telesherpa MCP connector](https://glama.ai/mcp/connectors/com.telesherpa/ontology-platform/badges/score.svg)](https://glama.ai/mcp/connectors/com.telesherpa/ontology-platform)
  🔐 - Ontology platform for facility management and field service; also a lightweight ERP/CRM.
- [Tempi](https://meettempi.com/ai) `https://meettempi.com/mcp`
  [![Tempi MCP connector](https://glama.ai/mcp/connectors/com.meettempi/tempi/badges/score.svg)](https://glama.ai/mcp/connectors/com.meettempi/tempi)
  🔓 - Find open times on anyone's Tempi booking link and book, reschedule or cancel meetings, no account needed.
- [Time of Meeting](https://timeofmeeting.com/mcp) `https://timeofmeeting.com/mcp`
  [![Time of Meeting MCP connector](https://glama.ai/mcp/connectors/com.timeofmeeting/time-of-meeting/badges/score.svg)](https://glama.ai/mcp/connectors/com.timeofmeeting/time-of-meeting)
  🔓 - Find fair meeting times across time zones: show the overlap, convert times and make calendar links.
- [Tokenrip](https://tokenrip.com) `https://api.tokenrip.com/mcp`
  [![Tokenrip MCP connector](https://glama.ai/mcp/connectors/io.github.silostack/tokenrip/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.silostack/tokenrip)
  🔐 - Shared workspace where Claude, ChatGPT, Codex and Grok share files, tasks, decisions and handoffs.
- [Verant](https://verant.ai) `https://verant.ai/mcp`
  [![Verant MCP connector](https://glama.ai/mcp/connectors/ai.verant/verant/badges/score.svg)](https://glama.ai/mcp/connectors/ai.verant/verant)
  🔐 - Proofread live web pages and whole sites for spelling, grammar, and placeholder text, with a fix for each.
- [VeritaHire Hiring Intelligence](https://veritahire.com/salary-benchmarking/) `https://veritahire.com/mcp/employers`
  [![VeritaHire Hiring Intelligence MCP connector](https://glama.ai/mcp/connectors/com.veritahire/hiring-intelligence/badges/score.svg)](https://glama.ai/mcp/connectors/com.veritahire/hiring-intelligence)
  🔓 - Posted pay, competing employers and time to close for a role in any US market, from employers' own career sites.
- [Walkie](https://trywalkie.com/mcp) `https://mcp.trywalkie.com/mcp`
  [![Walkie MCP connector](https://glama.ai/mcp/connectors/io.github.adamperlis/walkie-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.adamperlis/walkie-mcp)
  🔐 - Search and read your recorded meetings: notes, action items, participants and speaker-labeled transcripts.
- [wals.pro AI 4 weclapp](https://ai.wals.pro) `https://mcp.ai.wals.pro/v1/mcp`
  [![wals.pro AI 4 weclapp MCP connector](https://glama.ai/mcp/connectors/pro.wals.ai/weclapp/badges/score.svg)](https://glama.ai/mcp/connectors/pro.wals.ai/weclapp)
  🔐 - weclapp ERP: quotes, orders, invoices, stock and master data, with every write previewed and approved.
- [Watchtower](https://watchtower.lat/) `https://watchtower.lat/mcp`
  [![Watchtower MCP connector](https://glama.ai/mcp/connectors/lat.watchtower/watchtower/badges/score.svg)](https://glama.ai/mcp/connectors/lat.watchtower/watchtower)
  🔓 - Job alerts for agents: describe a role once and get only new postings from 1,500+ tech job boards, with webhooks.
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
- [Dollea Salon](https://www.dollea.de/agents/?language=en) `https://www.dollea.de/mcp/salon`
  [![Dollea Salon MCP connector](https://glama.ai/mcp/connectors/de.dollea/salon/badges/score.svg)](https://glama.ai/mcp/connectors/de.dollea/salon)
  🔓 - Public beauty service catalog and slots in Munich; OAuth for booking and private appointments.
- [FindingSteel Steel Sections](https://www.findingsteel.com/) `https://www.findingsteel.com/mcp/`
  [![FindingSteel Steel Sections MCP connector](https://glama.ai/mcp/connectors/io.github.cdaily1995-create/findingsteel-steel-sections/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.cdaily1995-create/findingsteel-steel-sections)
  🔓 - Query GB/T steel section properties and calculate theoretical steel weight for 143 Chinese profiles.
- [GEOMETRY](https://geometry.app) `https://mcp.geometry.app/mcp`
  [![GEOMETRY MCP connector](https://glama.ai/mcp/connectors/app.geometry.mcp/geometry/badges/score.svg)](https://glama.ai/mcp/connectors/app.geometry.mcp/geometry)
  🔓 - Deterministic date/calendar JSON for AI agents (Gregorian 1900-2100).

- [Helfer & Profi](https://helferundprofi.de/) `https://pcbyuhvyjgadanzlghmw.supabase.co/functions/v1/mcp`
  [![Helfer & Profi MCP connector](https://glama.ai/mcp/connectors/io.github.helferundprofi/helfer-und-profi/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.helferundprofi/helfer-und-profi)
  🔓 - Free German neighborhood marketplace: search help requests and providers by postal code, post requests and offers.

- [HelpySelf](https://helpyself.com) `https://helpyself.com/mcp`
  [![HelpySelf MCP connector](https://glama.ai/mcp/connectors/com.helpyself/tools/badges/score.svg)](https://glama.ai/mcp/connectors/com.helpyself/tools)
  🔓 - Convert, compress and split PDFs and images, redact personal data, and run text utilities.
- [Human Design](https://www.gethumandesign.com/mcp-docs/) `https://api.gethumandesign.com/mcp`
  [![Human Design MCP connector](https://glama.ai/mcp/connectors/com.gethumandesign.www/mcp/badges/score.svg)](https://glama.ai/mcp/connectors/com.gethumandesign.www/mcp)
  🔐 - Calculate Human Design bodygraphs from birth data, compare two people, and analyse group dynamics.
- [Japan External Execution](https://furoito.github.io/japan-physical-capability/) `https://bqgfqedetmxrfpvmdfmc.supabase.co/functions/v1/japan-physical-capability-mcp`
  [![Japan Physical Capability MCP connector](https://glama.ai/mcp/connectors/io.github.furoito/japan-physical-capability/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.furoito/japan-physical-capability)
  🔓 - Manual-review external execution in Japan for AI agents; physical verification is the first verified execution path.
- [Muslim Prayer Reminder MCP](https://tareq7.github.io/muslim-prayer-mcp/) `https://muslim-prayer-mcp.najetareqz.workers.dev/mcp`
  [![Muslim Prayer Reminder MCP connector](https://glama.ai/mcp/connectors/io.github.tareq7/muslim-prayer-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.tareq7/muslim-prayer-mcp)
  🔓 - Computes Muslim prayer times by location and regional method, with daily timetables and next-prayer countdowns.
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
- [RFQdecoder](https://rfqdecoder.com/api-mcp-ai-agents/) `https://rfqdecoder.com/api/mcp`
  [![RFQdecoder MCP connector](https://glama.ai/mcp/connectors/io.github.Mounirt879/rfqdecoder/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Mounirt879/rfqdecoder)
  🔓 - Should-cost of an industrial part from its PDF, DXF or STEP drawing, line by line, with assumptions and exclusions.
- [SerialHunt](https://bigballi.com/SerialHunt/connect) `https://bigballi.com/SerialHunt/mcp`
  [![SerialHunt MCP connector](https://glama.ai/mcp/connectors/com.bigballi/serialhunt/badges/score.svg)](https://glama.ai/mcp/connectors/com.bigballi/serialhunt)
  🔓 - US bill serial numbers: star note print runs from government figures and fancy serial patterns with exact odds.
- [SpinWheelNames](https://spinwheelnames.com) `https://spinwheelnames.com/mcp`
  [![SpinWheelNames MCP connector](https://glama.ai/mcp/connectors/io.github.heyiamluke/spinwheelnames/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.heyiamluke/spinwheelnames)
  🔓 - Spin random name picker wheels, pick random numbers, and search or open shared wheels.
- [Stellara](https://stellara.natlex.it/#api) `https://mcp.stellara.natlex.it/mcp`
  [![Stellara MCP connector](https://glama.ai/mcp/connectors/it.natlex/stellara-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/it.natlex/stellara-mcp)
  🔐 - Swiss Ephemeris astrology: natal charts, transits and synastry, with historical UTC offsets.
- [Toolalize](https://toolalize.com) `https://toolalize.com/mcp`
  [![Toolalize MCP connector](https://glama.ai/mcp/connectors/io.github.Vertisky/toolalize-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.Vertisky/toolalize-mcp)
  🔓 - Convert units (NIST SP 811 / SI factors) and currencies with live rates, and list every supported unit, in 13 languages.
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
- [ValorAI MCP](https://www.tryvalor.ai) `https://www.tryvalor.ai/mcp/public`
  [![ValorAI MCP connector](https://glama.ai/mcp/connectors/io.github.jchacker5/valor-mcp/badges/score.svg)](https://glama.ai/mcp/connectors/io.github.jchacker5/valor-mcp)
  🔓 - Free, read-only VA disability help: claims Q&A with VA.gov sources, BDD checklist, rating math.
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

