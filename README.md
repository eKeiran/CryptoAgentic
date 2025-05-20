# Crypto Agentic Lab

![image](https://github.com/user-attachments/assets/82d248f2-b35d-488c-a49a-9314f3116d59)


Crypto Agentic Lab is a compact toolkit for experimenting with GPT-3.5 models in crypto analysis. It features a pre-configured Docker stack with QuestDB, Grafana, Code-Server, Nginx, and an AI Agent for streamlined data management, visualization, and coding. Real-time data streaming from Binance and Coinbase is supported for financial insights.

## Features

- **QuestDB**: Time-series database for real-time crypto data.
- **Grafana**: Dashboards for cryptocurrency visualization.
- **Code-Server**: Web-based coding IDE.
- **Nginx**: Web server and reverse proxy.
- **Crypto Agentic AI Lab**: Backend for AI processing.
- **Crypto Agentic AI UI**: Web interface for AI interaction.

## Quick Start

1. Install [Docker](https://docs.docker.com/get-docker/).
2. Clone the repository:
    ```bash
    git clone https://github.com/eKeiran/CryptoAgentic
    cd CryptoAgentic/docker
    ```
3. Follow the [Docker setup guide](https://github.com/eKeiran/CryptoAgentic/tree/main/docker).

   ![image](https://github.com/user-attachments/assets/4f2c431e-e001-4313-875b-c72772dbc5c5)

5. Launch the stack:
    ```bash
    docker compose up --build -d
    ```
6. Access services:
    - QuestDB: `https://questdb.domain.tld`
    - Grafana: `https://grafana.domain.tld`
    - Code-Server: `https://vscode.domain.tld`
    - Crypto AI Agent UI: `https://aigentui.domain.tld`
      
![image](https://github.com/user-attachments/assets/38f5ad5d-dca7-4bf8-865f-cd67543f3a32)

## Real-Time Data

Stream real-time Binance and Coinbase data into QuestDB for querying and visualization in Grafana.

## JupyterHub Integration

1. Set up JupyterHub with GPT-3.5 dependencies.
2. Connect from Code-Server in the lab.

## References

- [JupyterHub Guide](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_connect-to-a-remote-jupyter-server)
- [QuestDB](https://questdb.io/)
- [Grafana](https://grafana.com/)
- [LangChain](https://python.langchain.com)
- [Binance API](https://binance-docs.github.io/apidocs/)
- [Coinbase API](https://developers.coinbase.com/)
