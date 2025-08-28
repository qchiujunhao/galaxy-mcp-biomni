# Galaxy-Biomni Integration

This repository provides a quick setup to connect Biomni with an MCP-enabled Galaxy server.

---

## Quick Start

1. **Clone this repo**
   ```bash
   git clone <repo_url>
   cd galaxy-biomni
   ```

2. **Create and activate a virtual environment**
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Edit the `.env` file** with your Galaxy URL and API key.

5. **Run Biomni in shell or notebook (There’s an example notebook in this repo.)**
   ```python
   from biomni.agent import A1

   agent = A1()
   agent.add_mcp(config_path="./mcp_config.yaml")   
   agent.go("Use Galaxy MCP to create a new history named 'biomni-test'. Return the history_id.")
   and more queries.
   ```

---

## Folder Structure

```
galaxy-biomni/
├── .venv/               # Your virtual environment (not included in repo)
├── .env                 # Environment variables (edit with your own values)
├── mcp_config.yaml      # MCP configuration
├── requirements.txt     # Python dependencies
└── README.md
```

---

**That’s it — Biomni is now connected to MCP_Galaxy_Server!**
