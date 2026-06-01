# agent-resources

Active workspace resources for AI agent tooling at [BabaDeluxe](https://babadeluxe.com).

## Structure

| File / Dir | Purpose |
|---|---|
| `perplexity-prompts/` | Git submodule — canonical source for `AGENTS.md`, all modules, and personas |
| `AGENT_PROMPT.agent.md` | System prompt loaded by `aider` and other coding agents |
| `AGENT_COMMIT.agent.md` | Commit message convention enforced by the agent |
| `.aider.conf.yml` | `aider` configuration (model, flags, conventions) |
| `.env.example` | Required environment variable reference (never commit `.env`) |

## Getting Started

```bash
git clone https://github.com/simwai/agent-resources.git
cd agent-resources
git submodule update --init --recursive
```

After init, `perplexity-prompts/AGENTS.md` is the active agent contract.
All modules live under `perplexity-prompts/modules/` and personas under `perplexity-prompts/personas/`.

## Keeping the Submodule in Sync

```bash
git submodule update --remote --merge
```

Run this to pull the latest from `perplexity-prompts` when it changes upstream.
