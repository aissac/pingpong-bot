# TOOLS.md - Local Notes

Skills define _how_ tools work. This file is for _your_ specifics — the stuff that's unique to your setup.

## 🏓 Token Efficiency Stack (April 9, 2026)

**Priority order when answering code questions:**
1. **Graphify** → run `mcporter call graphify query_graph ...` for architecture/codebase questions (vs reading raw files)
2. **jcodemunch** → `mcporter call jcodemunch <tool>` for refactoring, smell detection, dead code, dependency analysis, docs generation
3. **RTK** → manually prepend `rtk` to expensive shell commands: `rtk git status`, `rtk cargo build`, `rtk ls`, `rtk grep`
4. **grep/rg** → last resort for file contents, not architecture navigation

**RTK usage:**
```bash
rtk git status     # ~200 tokens vs ~2000 raw
rtk git diff      # condensed vs noisy
rtk git log -n 10 # one-liner commits
rtk cargo build   # filtered output
rtk cargo test    # failures only
rtk ls            # compact tree
rtk rtk gain      # show savings so far
```

**jcodemunch tools (50 available):** refactor_ask, find_dead_code, analyze_complexity, suggest_tests, explain_code, generate_tests, code_suggestions, dependency_relationship, analyze_file_health, generate_docs, etc.

**RTK hook installed but not wired to OpenClaw exec.** Bash hook works for Claude Code only. RTK v0.35.0 at `~/.local/bin/rtk`.

---

## NotebookLM Integration

**Tool:** `notebooklm-py` (Python library + CLI)
**Purpose:** Research automation, ask questions about sources, generate content

**Setup:**
```bash
pip install notebooklm-py
export PATH="$HOME/.local/bin:$PATH"  # for CLI
```

**Usage:**
```bash
notebooklm login                    # Authenticate first (opens browser)
notebooklm list                     # List notebooks
notebooklm use <notebook_id>        # Set active notebook
notebooklm ask "question"           # Ask about notebook sources
notebooklm source list              # List sources in notebook
notebooklm artifact list            # List generated artifacts
```

**Notebooks:**
- Strategic Foundations for Polymarket and Algorithmic Trading: `857bce48-57e6-4ee7-a621-6fe8a588a239`

**Key pattern from NotebookLM research:**
- Track YES and NO prices SEPARATELY with `Option<f64>`
- Only compute combined cost when BOTH exist
- Reset to None on reconnect to avoid stale prices

---

## 🏓 Wiki Usage Commitment (April 6, 2026)

**Rule:** Before answering questions about bot behavior, strategies, performance, or infrastructure:

1. **Query the wiki first** — `/home/aissac/.openclaw/workspace/wiki/`
2. **Then supplement with memory** — Only if wiki doesn't have it
3. **Write new knowledge to wiki** — Not just memory files

**Why:** The wiki is the curated, compounding knowledge base. Memory files are raw logs.

**Trigger phrases that should hit the wiki:**
- "What's our current latency?"
- "How does [strategy] work?"
- "Show me bug fixes"
- "What's the AWS status?"
- "Ghost simulation results?"

**Habit reinforcement:** This note persists across sessions. Read it, follow it.

## 🏛️ MemPalace Integration (April 9, 2026)

**MCP Server:** `mempalace` (wired via mcporter, stdio transport)
**Command:** `python3 -m mempalace.mcp_server`
**Tools:** 19 (search, status, KG query/add/invalidate, diary write/read, taxonomy, tunnels, etc.)

### Wake-up Protocol
On every session start, call `mcporter call mempalace.mempalace_status` to load palace overview + AAAK spec.

### Recall Priority
1. **Wiki** — for bot/infrastructure questions
2. **MemPalace** — for people, projects, decisions, past events (semantic search via ChromaDB)
3. **memory_search** — fallback (currently broken due to Ollama `/api/embeddings` vs `/api/embed` mismatch)
4. **Daily memory files** — raw logs

### Key Commands
- `mcporter call mempalace.mempalace_search query="auth decisions"`
- `mcporter call mempalace.mempalace_kg_query entity="Alice"`
- `mcporter call mempalace.mempalace_diary_write agent_name="Pingpong" entry="SESSION:..."`
- `mcporter call mempalace.mempalace_diary_read agent_name="Pingpong"`

### AAAK Dialect
MemPalace uses AAAK for compressed diary entries. Entity codes (3-letter uppercase), emotion markers (*warm*, *fierce*), pipe-separated fields. Get full spec via `mcporter call mempalace.mempalace_get_aaak_spec`.
