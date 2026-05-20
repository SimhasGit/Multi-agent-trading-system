# Multi-Agent Trading System

An autonomous trading system where 4 AI agents collaborate 
to make real-time equity trading decisions independently.

## What I built

4 specialized agents working together in a pipeline:
- **Data Agent** — fetches live market data via APIs
- **Sentiment Agent** — analyzes financial news and trends  
- **Decision Agent** — determines buy/sell based on analysis
- **Risk Agent** — validates every decision before execution

Powered by 6 MCP servers giving agents access to 44 tools.

## Tech Stack
Python · LangGraph · OpenAI Agents SDK · MCP · REST APIs

## How to run
git clone https://github.com/SimhasGit/multi-agent-trading-system.git
cd multi-agent-trading-system
pip install -r requirements.txt
cp .env.example .env
python main.py

## Status
Currently building — project files will be added as I complete 
each agent module.
