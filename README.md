# Awesome Remote MCP Servers

A curated, opinionated list of high-quality **remote** Model Context Protocol (MCP) servers. This repository focuses on listing official and well-maintained MCP servers that can be accessed over the internet, helping developers discover reliable and production-ready services for their AI applications.

## What is MCP?

[Model Context Protocol](https://modelcontextprotocol.io/) (MCP) is a protocol that enables AI models to interact with external tools and resources. Remote MCP servers allow clients to securely connect to these services over the internet. 

## Quality Criteria

This is not an exhaustive list of all remote MCP servers. We maintain high standards for inclusion:

- **Official Support**: Servers that are maintained by their underlying companies are preferred
- **Production Ready**: Must be stable and suitable for production use
- **Active Maintenance**: Regular updates and bug fixes
- **Security**: Proper authentication and security measures, with OAuth 2.0 support preferred
- **Reliability**: Proven track record of uptime and performance
- **Community**: Active user community and support channels

## Remote MCP Server List

| Name | Category | URL | Authentication | Maintainer |
|------|----------|-------------|----------------|------------|
| Atlasian | Software Development | `https://mcp.atlassian.com/v1/sse` | OAuth2.1 | [Atlassian](https://atlassian.com) |
| Asana | Project Management | `https://mcp.asana.com/sse` | OAuth2.1 | [Asana](https://asana.com) |
| Neon | Software Development | `https://mcp.neon.tech/see` | OAuth2.1 | [Neon](https://neon.tech) |
| PayPal | Payments | `https://mcp.paypal.com/sse` | OAuth2.1 | [PayPal](https://paypal.com) |
| Sentry | Software Development | `https://mcp.sentry.dev/sse` | OAuth2.1 | [Sentry](https://sentry.io) |
| Linear | Project Management | `https://mcp.linear.app/sse` | OAuth2.1 | [Linear](https://linear.app) |
| OneContext | RAG-as-a-Service | `https://rag-mcp-2.whatsmcp.workers.dev/sse` | OAuth2.1 | [OneContext](https://onecontext.ai) |
| Square | Payments | `https://mcp.squareup.com/sse` | OAuth2.1 | [Square](https://square.com) |
| Cloudflare Docs | Documentation | `https://mcp.cloudflare.com/sse` | Open | [Cloudflare](https://cloudflare.com) |
| Cloudflare Workers | Software Development | `https://bindings.mcp.cloudflare.com/sse` | OAuth2.1 | [Cloudflare](https://cloudflare.com) |
| Cloudflare Observability | Observability | `https://observability.mcp.cloudflare.com/sse` | OAuth2.1 | [Cloudflare](https://cloudflare.com) |
| Cloudflare Radar | Observability | `https://radar.mcp.cloudflare.com/sse` | OAuth2.1 | [Cloudflare](https://cloudflare.com) |
| LLM Text | Data Analysis | `https://mcp.llmtxt.dev/sse` | Open | [LLM Text](https://llmtxt.dev) |
| YepCode | Software Development | `https://cloud.yepcode.io/mcp/{API_KEY}/sse` | API Key | [YepCode](https://yepcode.io) |
| GitMCP | Software Development | `https://gitmcp.io/docs` | Open | [GitMCP](https://gitmcp.com) |
| Semgrep | Software Development | `https://mcp.semgrep.ai/sse` | Open | [Semgrep](https://semgrep.dev/) |
| APIFY | Software Development | `https://actors-mcp-server.apify.actor/sse?token=<YOUR_API_TOKEN>&actors=<ACTOR_NAMES>` | API Key | [Apify](https://apify.com) |

## How to use remote MCP servers?

To use MCP, you'll need to use a client that supports the MCP spec. 
A list of MCP clients can be found [here](https://modelcontextprotocol.io/clients).


### Playground
The best place to start is with Cloudflare's MCP playground [here](https://playground.ai.cloudflare.com/).
Simply copy and paste the server URL into the playground, authenticate with the service if required, and you're away!

### Desktop Clients 

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

- [Discord Server](https://discord.com/invite/TFE8FmjCdS)
- [Reddit Community](https://www.reddit.com/r/mcp/)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
