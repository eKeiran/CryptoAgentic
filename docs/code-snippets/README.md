
Crypto Agentic Lab
------------------

Quick validation snippets for ensuring connectivity and functionality in the Crypto Agentic Lab setup.

### Code-Server Validation

**Goal:** Verify secure connection and authentication with code-server over HTTPS.

_Snippet:_ Script to authenticate via API or simulate login over HTTPS. Check for success response.

### QuestDB Validation

**Goal:** Test connectivity to QuestDB via PostgreSQL or REST API.

_PostgreSQL:_ Connect using a client library, run `SELECT version();`, and verify the result.

_REST API:_ Send an HTTP GET to `/exec` with a query and validate the JSON response.

### Grafana Validation

**Goal:** Confirm API connectivity for dashboard management.

_Snippet:_ Fetch or create a dashboard using Grafana's API. Verify success response.

### OpenAI API Validation

**Goal:** Test AI Agent's ability to interact with OpenAI API.

_Snippet:_ Send a test prompt and check for a valid response with generated text.

Ensure error handling and secure practices for all snippets.
