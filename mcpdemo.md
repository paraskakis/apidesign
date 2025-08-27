1. Ensure node.js is installed by opening a terminal window and typing `node`

- If not, watch the demo first and then come back and install it in one of two ways:

- Download & install from https://nodejs.org/

- Install nvm with the instructions at https://github.com/nvm-sh/nvm and then install the latest Node version: `nvm install latest`

2. Make sure you have Claude Desktop installed: https://claude.ai/download

3. Sign up for Gram at https://www.speakeasy.com/product/gram

4. Navigate to https://www.weather.gov/documentation/services-web-api and hit the `Specification` tab - inspect the documentation & download https://api.weather.gov/openapi.json to your Desktop

5. Go back to Gram and upload the OpenAPI file

6. Add/Remove Tools as needed

7. Make the MCP Server public

8. Copy the `mcpServers` file

9. Open Claude Desktop and hit `Settings|Developer|Edit Config`

11. Edit `claude_desktop_config.json` with your Editor and Save:
    - Rename the user agent

Your file should look like this:
```
{
  "mcpServers": {
    "GramWeatheropenapi": {
      "command": "npx",
      "args": [
          "mcp-remote",
          "https://app.getgram.ai/mcp/<Slug>",
          "--header",
          "MCP-WEATHER-OPENAPI-USER-AGENT:<User Agent>"
        ]
    }
  }
}
   
```
12. Restart Claude and ask "What Tools You Can Use"  - you should see "Weather & Alerts"

12. Now prompt Claude "Give me the active weather alerts for area CA"
You should see a confirmation dialog for tool use, accept it, and observe the response plus Claude's interpretation of it!

13. Go back to Gram and copy the MCP Server URL

14. Upload and set up the server to Registry such as https://mcp.so/submit

15. Alternatively, try https://zuplo.com/

16. Sign Up & Create a New Empty Project

17. Navigate to `Code` | `routes.oas.json` and Upload your OpenAPI

18. In the Route Designer, add an MCO Server

19. Edit the path and make it `/mcp`

20. Drop down `OpenAPI Files` and choose `./config/routes.oas.json`

21. Hit `Save` on the bottom left - this is important to deploy the gateway!

22. Navigate to `Project` and copy the URL

23. Sign Up on https://smithery.ai/ and `Deploy Server`

24. Publish Existing Server via URL

25. Paste in the URL from Ziplo and append `/mcp` - Smithery required this

26. You should get a playground where you can prompt and check out the tools you just published.

27. You can copy the Smithery URL from the `Overview` page and paste it into `claude_desktop_config.json` on your laptop to point Claude to Smithery

28. Restart CLaude and Smithery will prompt you to log in

29. Test Claude has access to the API tools

30. Your MCP server is now public to the world!
