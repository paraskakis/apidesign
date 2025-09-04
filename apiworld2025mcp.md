# API World 2025 - Build AI Ready APIs with MCP

## Demo

1. Navigate to https://www.weather.gov/documentation/services-web-api and hit the Specification tab - inspect the documentation & download https://api.weather.gov/openapi.json to your Desktop
2. Go to https://zuplo.com/ - Start Free
3. Sign Up & Create a New Empty Project
4. Navigate to Code | routes.oas.json and Upload your OpenAPI
5. In the Route Designer, add an MCO Server
6. Edit the path and make it /mcp
7. Drop down OpenAPI Files and choose ./config/routes.oas.json
8. Hit Save on the bottom left - this is important to deploy the gateway!
9. Navigate to Project and copy the URL
10. Open Claude at https://claude.ai/new
11. Hit Search & Tools & Manage Connectors
12. Add Custom Connector
13. Name the MCP Server and enter the URL you copied (don't forget to append `/mcp`)
14. Trust & Add the connector
15. The MCP Server is now ready to use!
16. Make sure there are no errors and prompt Claude: "What Tools Can You Use?"
17. Note weather tools
18. Prompt: "Give me the weather alerts for California"
19. Hit Allow
20. Note weather alerts coming from MCP Server
21. Sign Up on Smithery: https://smithery.ai/
22. Hit Deploy Server
23. Publish Existing Server via URL
24. Paste in the URL from Zuplo and append `/mcp` - Smithery requires this
25. You should see a playground where you can prompt and check out the tools you just published.

## Tools
- Goose: https://block.github.io/goose/docs/quickstart/
- mcp-use: https://mcp-use.com/
- MJPJam: https://github.com/MCPJam/inspector
- FastMCP: https://gofastmcp.com/
- MCP Inspector: https://modelcontextprotocol.io/legacy/tools/inspector
- OpenAI Playground: https://platform.openai.com/chat/edit

## Links
- Design APIs for AI: https://maven.com/p/d4116d/ai-agents-are-coming-for-your-api-are-you-ready
- OpenAPI: https://training.linuxfoundation.org/express-learning/openapi-fundamentals-lfel1011
- Official MCP Docs: https://modelcontextprotocol.io/docs/getting-started/intro
- Follow Kevin Swiber: https://www.linkedin.com/in/kevinswiber/
- What is MCP? Speakeasy: https://www.speakeasy.com/mcp/getting-started/what-is-mcp
- MCP Server Security Masterclass, Adrian Machado: https://fathom.video/share/GRg-1xRTqkBL568-akJK5sP49nQNkYcc
- MCP Server Scaling Masterclass, Adrian Machado: https://fathom.video/share/vF1KQgmQfBgPLLf2AaCs7nxjEwAdCBGG
- Learn with Emmanuel Paraskakis with a Course on Maven: https://maven.com/emmanuel
- Build AI-Ready APIs Course - $100 off: https://maven.com/emmanuel/build-ai-ready-apis?promoCode=MCP
- Next Topic Poll: https://www.linkedin.com/posts/emmanuelparaskakis_last-week-i-taught-a-well-attended-lightning-activity-7369051586116972546-dTVR
- Emmanuel Paraskakis on LinkedIn: https://www.linkedin.com/in/emmanuelparaskakis/
- Slides - https://docs.google.com/presentation/d/1RoS48ypl1T0fAokyBV_J__ygA7XWRmYJcQzI3ayGwVA/edit?usp=sharing
- Recorded Session: Coming on September 11, see https://sched.co/24dui

