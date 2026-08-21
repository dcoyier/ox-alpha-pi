# ox-alpha-pi

Complete [OpenCode](https://opencode.ai) **v1.18.20** in this repo, with **Ox Alpha** as the default model and thinking level **`max`**.

- `opencode/` — full OpenCode source (snapshot of [anomalyco/opencode](https://github.com/anomalyco/opencode) `v1.18.20`)
- `opencode.json` — this workspace’s default model and thinking level

Default model ID: `opencode/x-preview-f-free` (Ox Alpha Free on [OpenCode Zen](https://opencode.ai/docs/zen)).

Ox Alpha thinking levels:

| Level | What it does |
| --- | --- |
| `low` | Light reasoning, faster replies |
| `high` | Stronger reasoning |
| `max` | Highest reasoning budget (project default) |

Build and plan agents default to `max`. Cycle levels in the TUI, or set `"variant": "low"` / `"high"` on an agent in `opencode.json`. Root `model` does not keep a variant; agent `variant` does.

## Run OpenCode

From this repo (uses the pinned CLI):

```bash
npm install
npx opencode
```

Or install globally:

```bash
curl -fsSL https://opencode.ai/install | bash
```

Other options: `npm i -g opencode-ai@latest`, or `brew install anomalyco/tap/opencode`.

To work from the vendored source (needs [Bun](https://bun.sh)):

```bash
cd opencode
bun install
bun run dev
```

## Connect

In the TUI:

1. Run `/connect` and select **OpenCode Zen**.
2. Sign in at [opencode.ai/auth](https://opencode.ai/auth), then paste your API key.
3. New sessions use Ox Alpha at thinking level `max`. Switch models anytime with `/models`.

Ox Alpha is also available on OpenRouter as `openrouter/stealth/ox-alpha` if you `/connect` OpenRouter instead.

## Project config

[`opencode.json`](./opencode.json) pins the default model for this repo.
