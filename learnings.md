# What I learned building this

## What was hard
- MCP server paths are relative — must match where you run the script from
- All API clients initialize on startup even if unused — need dummy keys for unused ones
- OpenAI Agents SDK is tightly coupled — swapping to Groq required changing base_url and model routing logic

## What I changed from the original
- Swapped OpenAI for Groq (free) by changing GROK_BASE_URL to Groq's endpoint
- Added llama routing in traders.py alongside grok routing
- Fixed MCP server paths in mcp_params.py to use 6_mcp/ prefix
- Disabled OpenAI tracing (not needed without OpenAI key)

## What I'd do differently
- Use environment variables for all paths instead of hardcoding
- Add error handling per agent so one failure doesn't stop all 4
- Add a simple dashboard to see agent decisions in real time

## Tech I now understand
- MCP (Model Context Protocol) — standard way for agents to call tools
- OpenAI Agents SDK — orchestrates agents, handles tool calls and loops
- AsyncOpenAI — async client that lets 4 agents run in parallel
- Polygon.io — REST API for live and historical stock data
