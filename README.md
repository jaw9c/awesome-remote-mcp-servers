# Awesome Remote MCP Servers

> 📧 **Subscribe to the Newsletter** Stay informed about new MCP servers and updates:
> [Subscribe](https://remotemcp.substack.com/subscribe)

A curated, opinionated list of high-quality **remote** Model Context Protocol (MCP) servers. This repository focuses on listing official and well-maintained MCP servers that can be accessed over the internet, helping developers discover reliable and production-ready services for their AI applications.

## What is MCP?

[Model Context Protocol](https://modelcontextprotocol.io/) (MCP) is a protocol that enables AI models to interact with external tools and resources. Remote MCP servers allow clients to securely connect to these services over the internet. 

## Why Remote only?

Remote MCP servers are a more secure and easier way to use MCP. 
- Security wise, if you trust the provider's URL, and you are authenicated, then the secuity model is the same as using the Web.
- Ease of use wise, you can copy & paste the server URL and you're away. No installing NPM packages etc.

## How can I use an MCP server listed here?

There are two main ways to use remote MCP servers on this list. 

1. [Using a MCP ready client](#mcp-client) (Claude, Cursor, etc.)
2. [In an API request to an LLM provider](#api-request) (OpenAI, Anthropic, etc.)

## Authentication options

This list has a mix of authentication options, different methods are better suited to certain use cases:

- **OAuth 2.0**: This is an industry standard for authentication and is suppoerted by MCP Clients like Claude. Adoption amogst clients is growing, but not yet widespread.
 For this all you need to conenct is the server URL, and the client will guide you through the authentication flow.
- **API Key**: An alternative to OAuth 2.0, this required to have an API key for the server. This is useful when using an API request to an LLM provider, rather than an MCP client.
- **Open**: Easy to copy and paste and get started, but not as secure. This is the easiest way to get started, but not the most secure.


## Quality Criteria

This is not an exhaustive list of all remote MCP servers. We maintain high standards for inclusion:

- **Official Support**: Servers that are maintained by their underlying companies are preferred
- **Production Ready**: Must be stable and suitable for production use
- **Active Maintenance**: Regular updates and bug fixes
- **Security**: Proper authentication and security measures, with OAuth 2.0 or API Key support required
- **Reliability**: Proven track record of uptime and performance
- **Community**: Active user community and support channels

## Remote MCP Server List

| Name | Category | URL | Authentication | Maintainer |
|------|----------|-------------|----------------|------------|
| Atlasian | Software Development | `https://mcp.atlassian.com/v1/sse` | OAuth2.1 | [Atlassian](https://atlassian.com) |
| Asana | Project Management | `https://mcp.asana.com/sse` | OAuth2.1 | [Asana](https://asana.com) |
| Intercom | Customer Support | `https://mcp.intercom.com/sse` | OAuth2.1 | [Intercom](https://intercom.com) |
| Neon | Software Development | `https://mcp.neon.tech/sse` | OAuth2.1 | [Neon](https://neon.tech) |
| PayPal | Payments | `https://mcp.paypal.com/sse` | OAuth2.1 | [PayPal](https://paypal.com) |
| Plaid | Payments | `https://api.dashboard.plaid.com/mcp/sse` | OAuth2.1 | [Plaid](https://plaid.com) |
| Sentry | Software Development | `https://mcp.sentry.dev/sse` | OAuth2.1 | [Sentry](https://sentry.io) |
| Linear | Project Management | `https://mcp.linear.app/sse` | OAuth2.1 | [Linear](https://linear.app) |
| OneContext | RAG-as-a-Service | `https://rag-mcp-2.whatsmcp.workers.dev/sse` | OAuth2.1 | [OneContext](https://onecontext.ai) |
| Square | Payments | `https://mcp.squareup.com/sse` | OAuth2.1 | [Square](https://square.com) |
| Webflow | CMS | `https://mcp.webflow.com/sse` | OAuth2.1 | [Webflow](https://webflow.com) |
| Wix | CMS | `https://mcp.wix.com/sse` | OAuth2.1 | [Wix](https://wix.com) |
| Cloudflare Workers | Software Development | `https://bindings.mcp.cloudflare.com/sse` | OAuth2.1 | [Cloudflare](https://cloudflare.com) |
| Cloudflare Observability | Observability | `https://observability.mcp.cloudflare.com/sse` | OAuth2.1 | [Cloudflare](https://cloudflare.com) |
| Cloudflare Radar | Observability | `https://radar.mcp.cloudflare.com/sse` | OAuth2.1 | [Cloudflare](https://cloudflare.com) |
| Kollektiv | Documentation | `https://mcp.thekollektiv.ai/sse` | Oauth2.1 | [Kollektiv](https://github.com/alexander-zuev/kollektiv-mcp) |
| Globalping | Software Development | `https://mcp.globalping.dev/sse` | OAuth2.1 | [Globalping](https://globalping.io/) |
| Simplescraper | Web Scraping | `https://mcp.simplescraper.com/mcp` | OAuth2.1 | [Simplescraper](https://simplescraper.io) |
| Cloudflare Docs | Documentation | `https://mcp.cloudflare.com/sse` | Open | [Cloudflare](https://cloudflare.com) |
| DeepWiki | RAG-as-a-Service | `https://mcp.deepwiki.com/sse` | Open | [Devin](https://devin.ai/) |
| Semgrep | Software Development | `https://mcp.semgrep.ai/sse` | Open | [Semgrep](https://semgrep.dev/) |
| Bitte | Blockchain Data Analysis | `https://mcp.bitte.ai/sse` | Open | [Bitte](https://bitte.ai) |
| McPoogle | MCP Server Search Engine | `https://mcp.mcpoogle.com/sse` | Open | [McPoogle](https://www.mcpoogle.com) |
| LLM Text | Data Analysis | `https://mcp.llmtxt.dev/sse` | Open | [LLM Text](https://llmtxt.dev) |
| GitMCP | Software Development | `https://gitmcp.io/docs` | Open | [GitMCP](https://gitmcp.io) |
| HubSpot | CRM | `https://app.hubspot.com/mcp/v1/http` | API Key | [HubSpot](https://hubspot.com) |
| Stripe | Payments | `https://mcp.stripe.com/` | API Key | [Stripe](https://stripe.com) |
| Needle | RAG-as-a-service | `https://mcp.needle-ai.com/mcp` | API Key | [Needle](https://needle-ai.com) |
| WayStation | Productivity | `https://waystation.ai/mcp` | OAuth2.1 | [WayStation](https://waystation.ai) |
| Zapier | Automation | `https://mcp.zapier.com/api/mcp/mcp` | API Key | [Zapier](https://zapier.com) |
| Todoist | Tasks Management & Productivity | `https://todoistmcp.rosenpin.io` to create personal MCP URL | OAuth2.1 | [Todoist Unofficial Remote MCP](https://todoistmcp.rosenpin.io/) |

## How to use remote MCP servers?

There are two main ways to use remote MCP servers on this list. 

1. Using a MCP client (Claude, Cursor, etc.)
2. In an API request to an LLM provider (OpenAI, Anthropic, etc.)

### MCP Client

A list of MCP clients can be found [here](https://modelcontextprotocol.io/clients). Here are some examples of installation with Claude.

### Claude

Claude has two methods to add remote MCP servers:
- [*Custom Integrations*](#custom-integrations) for Max, Team, and Enterprise users on both [claude.ai](https://claude.ai) and the [desktop app](https://claude.ai/download)
- [*Manual configuration*](#manual-configuration) for all users on the [desktop app](https://claude.ai/download) only

#### Custom Integrations

Anthropic has added [native support for Remote MCP into Claude](https://www.anthropic.com/news/integrations). It's currently in beta on the Max, Team, and Enterprise plans, and will soon be available on Pro.

Add these servers as *Custom Integrations* in the integrations section of your Claude app settings.

##### Step-by-Step Instructions for Claude Max Users

1. Navigate to Settings > Profile
2. Locate the "Integrations" section
3. Click "Add more"
4. Add your integration's remote MCP server URL
5. Finish configuring your integration by clicking "Add"

Full instructions can be found [here](https://support.anthropic.com/en/articles/11175166-about-custom-integrations-using-remote-mcp).

#### Manual configuration

For all users, you can manually configure the remote MCP servers by adding the following to your Claude config file:

```json
{
  "mcpServers": {
    "<REMOTE_MCP_SERVER_NAME>": {
      "url": "<REMOTE_MCP_SERVER_URL>"
    }
  }
}
```

### Playground
The best place to start is with Cloudflare's MCP playground [here](https://playground.ai.cloudflare.com/).
Simply copy and paste the server URL into the playground, authenticate with the service if required, and you're away!

### Other MCP Clients 

Note: As the MCP spec is still in development, not all clients may support all features. In particular client support of OAUTH is not yet widespread.

For desktop clients the configuration you need to add to your client's config file will be 

```json
{
  "mcpServers": {
    "<REMOTE_MCP_SERVER_NAME>": {
      "command": "npx",
      "args": [
        "mcp-remote",
        "<REMOTE_MCP_SERVER_URL>"
      ]
    }
  }
}
```

### API Request

Offical support for MCP in API requests is suppored by the following LLM providers:

- [Anthropic](https://docs.anthropic.com/en/docs/agents-and-tools/mcp-connector)
- [OpenAI](https://platform.openai.com/docs/api-reference/mcp)
- [Gemini](https://ai.google.dev/gemini-api/docs/function-calling?example=meeting#model_context_protocol_mcp)

Note that its easier to get started with API Token, based authentication for these servers. See the [FAQs](#faqs) section for more details.


## FAQs

### Can I use an Oauth MCP server in an API request to an LLM provider?

Yes, but you will need to manage your own OAuth authentication flow, in order to obtain an access token.
A quick way to obtain an access token to test a server is follow the instructions in Anthropic's guide [Obtaining an access token for testing](https://docs.anthropic.com/en/docs/agents-and-tools/mcp-connector#obtaining-an-access-token-for-testing) section.
This is not generally recommended for production use, as it is not a secure way to authenticate users.

### Why do some servers have a `/sse` and others a `/mcp`?

The `/sse` endpoint is for the Server Sent Events (SSE) protocol. It is being slowly deprecated in favor of the `/mcp` endpoint.
The `/mcp` endpoint is for the Streamed HTTP protocol. 
In the future some clients may only support adding severs by the prefix preceeding the 'sse' or 'mcp' and self-discovering full URL.
We will update this list as we see this happening.

## Contributing

We welcome contributions! Please follow these guidelines:

1. Fork the repository
2. Add your remote MCP server to the appropriate category
3. Include the following information:
   - Server name
   - Category
   - URL
   - Authentication requirements (Only OAuth 2.0, following the MCP spec is supported)
   - Example usage
4. Submit a pull request

## Acknowledgments

- Inspired by the [Model Context Protocol](https://modelcontextprotocol.io/)

## Community

Join the MCP community to stay updated and connect with other developers:

- [WhatsApp Community ](https://chat.whatsapp.com/GJIf9Uee1kw9ee9myqJe0a)
- [Reddit Community](https://www.reddit.com/r/mcp/)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
