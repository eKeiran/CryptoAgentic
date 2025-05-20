# Crypto Agentic Lab: AI Agent API Overview

This repository provides API definitions for configuring an AI Agent to interact with QuestDB, VSCode, and Grafana. These integrations enable database queries, dashboard management, and code editing.

## Structure
```
.
├── questdb/
│   ├── postgresql_wire_protocol.md
│   ├── rest_api.md
├── grafana/
│   ├── rest_api.md
├── vscode/
│   ├── vscode_api.md
└── README.md
```

## QuestDB
- **PostgreSQL Wire Protocol**: Enables SQL operations (`INSERT`, `UPDATE`, `SELECT`). [Details](./questdb/postgresql_wire_protocol.md)
- **REST API**: Supports SQL queries via HTTP. [Details](./questdb/rest_api.md)

## Grafana
- **REST API**: Manages dashboards, panels, users, and data sources. [Details](./grafana/rest_api.md)

## VSCode
- **API**: Automates tasks like editing, running, and debugging code. [Details](./vscode/vscode_api.md)

## Setup
1. **Clone the Repo**  
2. **Review APIs**: Check the respective folders for API details.  
3. **Configure Agent**: Use the provided definitions for setup.
