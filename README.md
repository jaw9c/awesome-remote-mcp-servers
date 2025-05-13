# Awesome Remote MCP Servers

> 📧 **Subscribe to the Newsletter** Stay informed about new MCP servers and updates:
> [Subscribe](https://remotemcp.substack.com/subscribe)

A curated, opinionated list of high-quality **remote** Model Context Protocol (MCP) servers. This repository focuses on listing official and well-maintained MCP servers that can be accessed over the internet, helping developers discover reliable and production-ready services for their AI applications.

## What is MCP?

[Model Context Protocol](https://modelcontextprotocol.io/) (MCP) is a protocol that enables AI models to interact with external tools and resources. Remote MCP servers allow clients to securely connect to these services over the internet. 

## Quality Criteria

This is not an exhaustive list of all remote MCP servers. We maintain high standards for inclusion:

- **Official Support**: Servers that are maintained by their underlying companies are preferred
- **Production Ready**: Must be stable and suitable for production use
- **Active Maintenance**: Regular updates and bug fixes
- **Security**: Proper authentication and security measures, with OAuth 2.0 support required
- **Reliability**: Proven track record of uptime and performance
- **Community**: Active user community and support channels

## Remote MCP Server List

| Name | Category | URL | Authentication | Maintainer |
|------|----------|-------------|----------------|------------|
| Atlasian | Software Development | `https://mcp.atlassian.com/v1/sse` | OAuth2.1 | [Atlassian](https://atlassian.com) |
| Asana | Project Management | `https://mcp.asana.com/sse` | OAuth2.1 | [Asana](https://asana.com) |
| Intercom | Customer Support | `https://mcp.intercom.com/sse` | OAuth2.1 | [Intercom](https://intercom.com) |
| Neon | Software Development | `https://mcp.neon.tech/see` | OAuth2.1 | [Neon](https://neon.tech) |
| PayPal | Payments | `https://mcp.paypal.com/sse` | OAuth2.1 | [PayPal](https://paypal.com) |
| Plaid | Payments | `https://api.dashboard.plaid.com/mcp/sse` | OAuth2.1 | [Plaid](https://plaid.com) |
| Sentry | Software Development | `https://mcp.sentry.dev/sse` | OAuth2.1 | [Sentry](https://sentry.io) |
| Linear | Project Management | `https://mcp.linear.app/sse` | OAuth2.1 | [Linear](https://linear.app) |
| OneContext | RAG-as-a-Service | `https://rag-mcp-2.whatsmcp.workers.dev/sse` | OAuth2.1 | [OneContext](https://onecontext.ai) |
| Square | Payments | `https://mcp.squareup.com/sse` | OAuth2.1 | [Square](https://square.com) |
| Webflow | CMS | `https://mcp.webflow.com/sse` | OAuth2.1 | [Webflow](https://webflow.com) |
| Wix | CMS | `https://mcp.wix.com/sse` | OAuth2.1 | [Wix](https://wix.com) |
| Cloudflare Docs | Documentation | `https://mcp.cloudflare.com/sse` | Open | [Cloudflare](https://cloudflare.com) |
| Cloudflare Workers | Software Development | `https://bindings.mcp.cloudflare.com/sse` | OAuth2.1 | [Cloudflare](https://cloudflare.com) |
| Cloudflare Observability | Observability | `https://observability.mcp.cloudflare.com/sse` | OAuth2.1 | [Cloudflare](https://cloudflare.com) |
| Cloudflare Radar | Observability | `https://radar.mcp.cloudflare.com/sse` | OAuth2.1 | [Cloudflare](https://cloudflare.com) |
| Kollektiv | Documentation | `https://mcp.thekollektiv.ai/sse` | Oauth2.1 | [Kollektiv](https://github.com/alexander-zuev/kollektiv-mcp) |
| LLM Text | Data Analysis | `https://mcp.llmtxt.dev/sse` | Open | [LLM Text](https://llmtxt.dev) |
| GitMCP | Software Development | `https://gitmcp.io/docs` | Open | [GitMCP](https://gitmcp.com) |
| Globalping | Software Development | `https://mcp.globalping.dev/sse` | OAuth2.1 | [Globalping](https://globalping.io/) |
| Semgrep | Software Development | `https://mcp.semgrep.ai/sse` | Open | [Semgrep](https://semgrep.dev/) |
| Bitte | Blockchain Data Analysis | `https://mcp.bitte.ai/sse` | Open | [Bitte](https://bitte.ai) |
| McPoogle | MCP Server Search Engine | `https://mcp.mcpoogle.com/sse` | Open | [McPoogle](https://www.mcpoogle.com) |

## How to use remote MCP servers?

To use MCP, you'll need to use a client that supports the MCP spec. 
A list of MCP clients can be found [here](https://modelcontextprotocol.io/clients).


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
