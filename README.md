# hermitcrab-kernel

A naked LLM that builds its own shell from pscale blocks.

## What this is

The kernel loads JSON blocks, constructs a system prompt, calls an LLM, and renders whatever the LLM produces. The kernel has no identity. The blocks are the shell. Any LLM can animate any shell.

## Generations

- **G0** — the generative act. Blocks + LLM API = kernel generation. The aspiration.
- **G1** — browser-based kernel. Loads blocks, builds system prompt, calls Claude API, renders React. What exists now.
- **G-1** — Python sovereign variant. Same blocks, different runtime. Not yet built.

## G1 Quick start

1. Clone this repo
2. Open `g1/index.html` in a browser
3. Enter a Claude API key when prompted
4. The hermitcrab boots, reads its blocks, and builds its own interface

## Architecture

- `g1/kernel.js` — the G1 kernel (~950 lines). Pure JavaScript, no build step.
- `g1/shell.json` — seed blocks (touchstone, constitution, capabilities + 4 growth blocks)
- `g1/index.html` — minimal HTML host

The kernel uses **bsp** (Block · Spindle · Point) for all pscale navigation — one function, three modes. See [pscale-touchstone](https://github.com/beach-commons/pscale) for the format and bsp spec.

## Dependencies

- A Claude API key (Opus for boot, Haiku for compression)
- React + ReactDOM (loaded from CDN)
- Babel standalone (for JSX compilation)
- Nothing else

## Related

- [pscale](https://github.com/beach-commons/pscale) — the format. Semantic numbers as addresses for meaning.
- [sand](https://github.com/beach-commons/sand) — the protocol. How entities coordinate.
- [pscale-commons](https://github.com/beach-commons/pscale-commons) — the shared coordination surface.
- [beach](https://github.com/beach-commons/beach) — discovery. Who's here.
