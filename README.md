# 🤖 AI Agents Tutorials

A comprehensive collection of AI agent implementations showcasing various frameworks, models, and use cases. This repository contains practical examples of building intelligent agents using Phidata and MCP (Model Context Protocol).

## 📚 Table of Contents

- [Overview](#overview)
- [Projects](#projects)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Usage Examples](#usage-examples)
- [Technologies Used](#technologies-used)
- [Contributing](#contributing)

## 🎯 Overview

This repository serves as a learning resource for building AI agents with different capabilities:

- **Finance Agents**: Stock market analysis, company research, and financial data retrieval
- **Multi-Agent Teams**: Collaborative agents working together to solve complex tasks
- **MCP Servers**: Model Context Protocol servers for Claude Desktop integration

## 🚀 Projects

### 1. Phidata Finance Agent (`1_phidata_finance_agent/`)

A collection of finance-focused AI agents demonstrating various capabilities:

#### 📄 `1_simple_groq_agent.py`
A basic agent setup using Groq's Llama 3.3 70B model. Perfect starting point for understanding agent fundamentals.

**Features:**
- Simple agent initialization
- Groq model integration
- Basic conversation capabilities

#### 📄 `2_finance_agent_llama.py`
An advanced finance agent that can analyze stocks, compare companies, and retrieve financial data.

**Features:**
- Real-time stock price retrieval
- Analyst recommendations analysis
- Company fundamentals comparison
- Custom company symbol mapping
- Table-based data visualization

**Example Use Cases:**
- Compare analyst recommendations for multiple stocks
- Analyze company fundamentals
- Get real-time stock prices

#### 📄 `3_agent_teams_openai.py`
A multi-agent system where specialized agents collaborate to provide comprehensive answers.

**Features:**
- **Web Agent**: Searches the internet for latest news and information
- **Finance Agent**: Retrieves financial data and stock information
- **Team Coordinator**: Orchestrates both agents to provide complete answers
- OpenAI GPT-4o integration
- Source attribution

**Example Use Cases:**
- Get latest news + financial analysis for a stock
- Research companies with both web and financial data
- Comprehensive market analysis

### 2. MCP Leave Management (`2_mcp_leave_management/`)

A Model Context Protocol (MCP) server for employee leave management that integrates with Claude Desktop.

**Features:**
- Check leave balance
- Apply for leave with specific dates
- View leave history
- Personalized greetings
- In-memory database with mock employee data

**Perfect for:**
- Learning MCP server development
- Building HR management tools
- Claude Desktop integration examples

## ✨ Features

- 🔌 **Multiple Model Support**: Groq, OpenAI, and more
- 🛠️ **Rich Tool Integration**: YFinance, DuckDuckGo, custom tools
- 👥 **Multi-Agent Collaboration**: Teams of specialized agents
- 📊 **Data Visualization**: Table-based output for better readability
- 🔍 **Web Search Capabilities**: Real-time information retrieval
- 💼 **Finance Tools**: Stock prices, analyst recommendations, fundamentals
- 🖥️ **MCP Integration**: Claude Desktop server examples

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- Python 3.10 or higher
- pip or uv package manager
- API keys for:
  - Groq API (for Groq models)
  - OpenAI API (for GPT models)

## 🛠️ Getting Started

### 1. Clone the Repository

```bash
git clone <repository-url>
cd ai-agents
```

### 2. Install Dependencies

#### For Phidata Agents

```bash
# Install Phidata and dependencies
pip install phidata yfinance duckduckgo-search python-dotenv

# Or using uv
uv pip install phidata yfinance duckduckgo-search python-dotenv
```

#### For MCP Leave Management

```bash
cd 2_mcp_leave_management
uv add "mcp[cli]>=1.6.0"
```

### 3. Set Up Environment Variables

Create a `.env` file in the project root:

```env
GROQ_API_KEY=your_groq_api_key_here
OPENAI_API_KEY=your_openai_api_key_here
```

### 4. Run the Agents

#### Simple Groq Agent
```bash
python 1_phidata_finance_agent/1_simple_groq_agent.py
```

#### Finance Agent
```bash
python 1_phidata_finance_agent/2_finance_agent_llama.py
```

#### Agent Teams
```bash
python 1_phidata_finance_agent/3_agent_teams_openai.py
```

#### MCP Server
```bash
cd 2_mcp_leave_management
uv run mcp install main.py
# Restart Claude Desktop to see the tools
```

## 📁 Project Structure

```
ai-agents/
├── 1_phidata_finance_agent/
│   ├── 1_simple_groq_agent.py      # Basic agent example
│   ├── 2_finance_agent_llama.py    # Finance agent with tools
│   └── 3_agent_teams_openai.py     # Multi-agent team
├── 2_mcp_leave_management/
│   ├── main.py                     # MCP server implementation
│   ├── pyproject.toml              # Project dependencies
│   ├── uv.lock                     # Lock file
│   └── README.md                   # MCP-specific documentation
└── README.md                       # This file
```

## 💡 Usage Examples

### Finance Agent Example

```python
agent.print_response(
    "Summarize and compare analyst recommendations and fundamentals for TSLA and MSFT. Show in tables.",
    stream=True
)
```

### Multi-Agent Team Example

```python
agent_team.print_response(
    "Summarize analyst recommendations and share the latest news for NVDA",
    stream=True
)
```

### MCP Server Usage

Once installed in Claude Desktop, you can use commands like:
- "Check leave balance for employee E001"
- "Apply for leave on 2025-04-17 and 2025-05-01 for E001"
- "Show leave history for E002"

## 🛠️ Technologies Used

- **[Phidata](https://github.com/phidatahq/phidata)**: Framework for building AI agents
- **[Groq](https://groq.com/)**: Fast inference API for LLMs
- **[OpenAI](https://openai.com/)**: GPT-4o and other models
- **[YFinance](https://github.com/ranaroussi/yfinance)**: Financial data retrieval
- **[DuckDuckGo](https://duckduckgo.com/)**: Web search capabilities
- **[MCP](https://modelcontextprotocol.io/)**: Model Context Protocol for Claude Desktop
- **[FastMCP](https://github.com/jlowin/fastmcp)**: Fast MCP server framework

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📝 License

This project is for educational purposes. Please check individual project licenses.

## 🙏 Acknowledgments

- Phidata team for the excellent agent framework
- Codebasics Inc. / LearnerX Pvt Ltd for MCP examples

---

**Happy Building! 🚀**

For questions or issues, please open an issue on GitHub.
