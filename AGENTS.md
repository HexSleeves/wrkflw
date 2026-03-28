# Codebase Navigation — Use indxr MCP tools

An MCP server called `indxr` is available. Always use indxr tools before reading full files.

## Exploration workflow
1. `search_relevant` — find files/symbols by concept or partial name
2. `get_tree` — see directory/file layout
3. `get_file_summary` / `batch_file_summaries` — understand files without reading them
4. `explain_symbol` — get signature, docs, and relationships for a symbol
5. `get_public_api` — public API surface of a file or module
6. `get_callers` / `get_related_tests` — find references and tests
7. `get_token_estimate` — check cost before deciding to read a full file
8. `read_source` — read just one function/struct by name
9. Read (full file) — ONLY when editing or need exact formatting

## When to read full files instead
- You need to edit a file
- You need exact formatting/whitespace
- The file is not source code (e.g., config files, documentation)

## Do NOT
- Read full source files just to understand what's in them
- Dump all files into context
- Use `git diff` when `get_diff_summary` would suffice

## After making code changes
Run `regenerate_index` to keep the index current.
