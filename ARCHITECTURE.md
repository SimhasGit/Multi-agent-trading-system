# Architecture

## Flow
trading_floor.py (scheduler, runs every 60 mins)
        |
   4 Agents
   Warren (value) · Cathie (growth) · George (macro) · Ray (risk)
        |
   3 MCP Servers
   accounts_server.py · market_server.py · push_server.py
        |
   3 External APIs
   Groq LLaMA 3.3 · Polygon.io · Brave Search

## Key files
| File | Purpose |
|---|---|
| trading_floor.py | Main entry point, runs scheduler |
| traders.py | Agent definitions and model routing |
| mcp_params.py | MCP server configurations |
| market_server.py | Fetches live stock prices |
| accounts_server.py | Manages portfolio and trades |
| push_server.py | Executes buy/sell orders |
