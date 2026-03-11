# Coding Principles

**Simple > Flexible > Performance**

## Core Rules

1. **grep first** — Search existing code before writing
2. **YAGNI** — No speculative code
3. **DRY** — Abstract after 3+ repetitions
4. **SRP** — One function, one responsibility
5. **Validate at boundaries** — Public API only

## Tooling for shell interactions 
Is it about finding FILES? use `fd` 
Is it about finding CODE STRUCTURE? use `ast-grep`
Is it about SELECTING from multiple results? pipe to `fzf` 
Is it about interacting with JSON? use `jq` 
Is it about interacting with YAML or XML? use `yq`
`ast-grep` is available; whenever a search requires syntax-aware or structural matching, default to `ast-grep --lang rust -p '<pattern>'` (or set `--lang` appropriately) and avoid falling back to text-only tools like `rg` unless I explicitly request a plain-text search.

## Pre-commit

- Simpler way exist?
- Any duplication?
- Any unused code?