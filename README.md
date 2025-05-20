# Crypto Agentic Lab

Crypto Agentic Lab is a compact toolkit for experimenting with GPT-3.5 models in crypto analysis. It features a pre-configured Docker stack with QuestDB, Grafana, Code-Server, Nginx, and an AI Agent for streamlined data management, visualization, and coding. Real-time data streaming from Binance and Coinbase is supported for financial insights.

## Features

- **QuestDB**: Time-series database for real-time crypto data.
- **Grafana**: Dashboards for cryptocurrency visualization.
- **Code-Server**: Web-based coding IDE.
- **Nginx**: Web server and reverse proxy.
- **AI Agent**: Backend for AI processing.
- **AI Agent UI**: Web interface for AI interaction.

## Quick Start

1. Install [Docker](https://docs.docker.com/get-docker/).
2. Clone the repository:
    ```bash
    git clone https://github.com/quantiota/AI-Agent-Lab.git
    cd AI-Agent-Lab/docker
    ```
3. Follow the [Docker setup guide](https://github.com/quantiota/AI-Agent-Lab/tree/main/docker).
4. Launch the stack:
    ```bash
    docker compose up --build -d
    ```
5. Access services:
    - QuestDB: `https://questdb.domain.tld`
    - Grafana: `https://grafana.domain.tld`
    - Code-Server: `https://vscode.domain.tld`
    - AI Agent UI: `https://aigentui.domain.tld`

## Real-Time Data

Stream real-time Binance and Coinbase data into QuestDB for querying and visualization in Grafana.

## JupyterHub Integration

1. Set up JupyterHub with GPT-3.5 dependencies.
2. Connect from Code-Server in the lab.

## Diagram

![Architecture Diagram](./ai-agent-lab-diagram.png)  
[View High-Resolution](https://raw.githubusercontent.com/quantiota/AI-Agent-Lab/master/ai-agent-lab-diagram.png)

## References

- [JupyterHub Guide](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_connect-to-a-remote-jupyter-server)
- [QuestDB](https://questdb.io/)
- [Grafana](https://grafana.com/)
- [LangChain](https://python.langchain.com)
- [Binance API](https://binance-docs.github.io/apidocs/)
- [Coinbase API](https://developers.coinbase.com/)
