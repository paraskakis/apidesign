1. Ensure node.js is installed by opening a terminal window and typing `node`
If not, watch the demo first and then come back and install it in one of two ways:
a. Download & install from https://nodejs.org/
b. Install nvm with the instructions at https://github.com/nvm-sh/nvm and then install the latest Node version: `nvm install latest`

2. Make sure you have Claude Desktop installed: https://claude.ai/download

3. Go to https://www.buildwithlayer.com/ and hit `Build a Demo MCP Server` (you can also sign up if you'd like)

4. Navigate to https://www.weather.gov/documentation/services-web-api and hoit the `Specification` tab - inspect the documentation & download https://api.weather.gov/openapi.json to your Desktop

5. Go back to https://dashboard.buildwithlayer.com/demo upload the OpenAPI file & hit `Generate Tools`

6. Pick the `alerts_active_area` endpoint and `Add 1 endpoint`

7. Check the box again on the next screen, and hit `Demo MCP Server`

8. Navigate tot he `Claude` tab and copy the text using the Copy button

9. Open Claude Desktop and hit `Settings|Developer|Edit Config`

10. Edit `claude_desktop_config.json` with your Editor and Save:
    - Rename the user agent
    - You can remove the area parameter
Your file should look like this:
```
{
  "mcpServers": {
    "layerdemo": {
      "command": "npx",
      "args": [
        "@buildwithlayer/generator",
        "demo",
        "mcp",
        "<your-layer-key>",
        "--userAgent=<some name>"
      ]
    }
  }
}   
```
11. Restart Claude and ask "What Tools You Can Use"  - yiou should see "Weayher & Alerts"

12. Now prompt Claude "Give me the active weather alerts for area CA"
You should see a confirmation dialog for tool use, accept it and obseve the response plus Claude's interpretation of it!

Feel free to try any other API using the same steps above.

The recording will be available at https://maven.com/p/ec0698/build-ai-ready-ap-is-with-mcp
