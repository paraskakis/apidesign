# API World 2025 - Build AI Ready APIs with MCP

## Demo

1. Navigate to https://www.weather.gov/documentation/services-web-api and hit the Specification tab - inspect the documentation & download https://api.weather.gov/openapi.json to your Desktop
2. Go to https://zuplo.com/ - Start Free
3. Sign Up & Create a New Empty Project
4. Navigate to Code | routes.oas.json and Upload your OpenAPI
5. In the Route Designer, add an MCP Server
6. Edit the path and make it `/mcp`
7. Drop down OpenAPI Files and choose ./config/routes.oas.json [1]
8. Hit Save on the bottom left - this is important to deploy the gateway!
9. Navigate to Project and copy the URL
10. Open Claude at https://claude.ai/new
11. Hit Search & Tools & Manage Connectors
12. Add Custom Connector
13. Name the MCP Server and enter the URL you copied (If you are using Zuplo: don't forget to append `/mcp`)
14. Trust & Add the connector
15. The MCP Server is now ready to use!
16. Make sure there are no errors and prompt Claude: "What Tools Can You Use?"
17. Note weather tools
18. Prompt: "Give me the weather alerts for California"
19. Hit Allow
20. Note weather alerts coming from the MCP Server
21. Sign Up on Smithery: https://smithery.ai/
22. Hit Deploy Server
23. Publish Existing Server via URL
24. Paste in the URL. (If you are using Zuplo: don't forget to append `/mcp`)
25. You should see a playground where you can prompt and check out the tools you just published.

[1] If this step doesn't work because the UI is different, try Speakeasy's Gram with the steps below and come back to step 10 above:

a. Sign up for Gram at https://app.getgram.ai/

b. Hit "Get Started"

c. Upload the OpenAPI file and hit "Continue"

d. Name the API, observe the tools generated and hit "Continue" again

e. Accept the default MPC Server Slug name and hit "Continue"

f. Make the MCP Server public by clicking on the "PRIVATE" button (scroll down), then toggling the Server Privacy switch

g. Navigate to the MCP option on the left, click on the three dots (⋮) then select "MCP Settings"

h. Copy the Hosted URL - and go back to step 10 above

(Note you don't need to append `/mcp` if using Gram)

## Tools
- Goose: https://block.github.io/goose/docs/quickstart/
- mcp-use: https://mcp-use.com/
- MJPJam: https://github.com/MCPJam/inspector
- FastMCP: https://gofastmcp.com/
- MCP Inspector: https://modelcontextprotocol.io/legacy/tools/inspector
- OpenAI Playground: https://platform.openai.com/chat/edit
- MCP Community Registry: https://blog.modelcontextprotocol.io/posts/2025-09-08-mcp-registry-preview/
- MCP in ChatGPT: https://platform.openai.com/docs/mcp

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
- Slides - https://docs.google.com/presentation/d/1iH1eEPzwMskgvTwN4IARiTi6yqgiJq8kmlK1yj12014/edit?usp=sharing
- Virtual Session: Coming on September 11, see https://sched.co/24dui (recording TBD)

