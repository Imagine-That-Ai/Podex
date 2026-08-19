# Podex

GitHub slug: [`Podex`](https://github.com/Imagine-That-Ai/Podex). The product name is simply Podex; the repository uses the same spelling.

Podex is Imagine That's companion layer for **Codex CLIProxy** already on a Mac. This public repository is the shareable design and runtime home. It does not include the official app, patched application bundles, credentials, seat databases, or private machine state, and work in this tree does not patch `/Applications/ChatGPT.app` or `/Applications/Codex CLIProxy.app`.

## Repository split

- **Public:** [`Imagine-That-Ai/Podex`](https://github.com/Imagine-That-Ai/Podex) contains the shareable landing surface, design language, and runtime contract.
- **Private:** `Imagine-That-Ai/Podex-private` is the operator-only repository for private build notes, artifact fingerprints, and protected app work. Keep it private.

Podex is the canonical product and repository spelling.

## Intent

A named home for the companion: white light by day, carbon-black night, warm copper ember, no blue chrome. Sibling in spirit to grok"D" — we overlay what you already have. We do not redistribute the official runtime.

## Local development

The current entry point is the landing page at the repository root. Read [`DESIGN.md`](DESIGN.md) before changing the visual language, and [`RUNTIME.md`](RUNTIME.md) for the private seat/Remote Control boundary.

```bash
python3 -m http.server 4173
```

Then open [http://127.0.0.1:4173](http://127.0.0.1:4173). Light / Night in the header is the first surface.

## Status

Shareable landing surface and design source of truth. The private repository owns protected operator artifacts; this public repository stays safe to link and share.

## License

MIT for this overlay repository. Official Codex CLIProxy remains its owner's.
