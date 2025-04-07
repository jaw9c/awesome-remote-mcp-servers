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
| Neon | Software Development | `https://mcp.neon.tech` | OAuth2.0 | [Neon](https://neon.tech) |
| OneContext | RAG-as-a-Service | `https://rag-mcp-2.whatsmcp.workers.dev/sse` | OAuth2.0 | [OneContext](https://onecontext.ai) |
| PayPal | Payments | `https://mcp.paypal.com/sse` | OAuth2.0 | [PayPal](https://paypal.com) |
| LLM Text | Data Analysis | `https://mcp.llmtxt.dev/sse` | Open | [LLM Text](https://llmtxt.dev) |
| Fetch | Language Models | `https://remote.mcpservers.org/fetch` | Open | [Chathub](https://chathub.gg) |
| Sequential Thinking | Language Models | `https://remote.mcpservers.org/sequentialthinking` | Open | [Chathub](https://chathub.gg) |
| YepCode | Software Development | `https://cloud.yepcode.io/mcp/{API_KEY}/sse` | API Key | [YepCode](https://yepcode.io) |
| GitMCP | Software Development | `https://gitmcp.io/docs` | Open | [GitMCP](https://gitmcp.com) |
| APIFY | Software Development | `https://actors-mcp-server.apify.actor/sse?token=<YOUR_API_TOKEN>&actors=<ACTOR_NAMES>` | API Key | [Apify](https://apify.com) |


## How to use remote MCP servers?

To use MCP, you'll need to use a client that supports the MCP spec. 
A list of MCP clients can be found [here](https://modelcontextprotocol.io/clients).


### Playground
The best place to start is with Cloudflare's MCP playground [here](https://playground.ai.cloudflare.com/).
Simply copy and paste the server URL into the playground, authenticate with the service if required, and you're away!

### Desktop Clients 

Note: As the MCP spec is still in development, not all clients may support all features. In particular client support of OAUTH is not yet widespread.

For desktop clients the configureation you need to add to your client's config file will be 

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