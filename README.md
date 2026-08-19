# Po"Codex

GitHub slug: [`PoCodex`](https://github.com/Imagine-That-Ai/PoCodex). The stylized product name keeps the quote; repository slugs cannot.

Po"Codex is Imagine That's overlay for **Codex CLIProxy** already on a Mac. This repository does not include the official app, and work in this tree does not patch `/Applications/ChatGPT.app` or `/Applications/Codex CLIProxy.app`.

## Intent

A named home for the overlay: white light by day, carbon-black night, warm copper ember, no blue chrome. Sibling in spirit to grok"D" — we overlay what you already have. We do not redistribute it.

## Local development

The current entry point is the landing page at the repository root. Read [`DESIGN.md`](DESIGN.md) before changing the visual language, and [`RUNTIME.md`](RUNTIME.md) for the private seat/Remote Control boundary.

```bash
python3 -m http.server 4173
```

Then open [http://127.0.0.1:4173](http://127.0.0.1:4173). Light / Night in the header is the first surface.

## Status

Initial landing surface and design source of truth. No installer and no application architecture yet.

## License

MIT for this overlay repository. Official Codex CLIProxy remains its owner's.
