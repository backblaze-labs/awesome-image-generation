# CLAUDE.md — awesome-image-generation

## What this list is

A curated directory of AI image-generation tools that developers can integrate today: text-to-image APIs, open-weight models, frameworks, editing/enhancement, and the surrounding infrastructure.

## Scope

**Include**
- Commercial text-to-image APIs with developer access.
- Open-weight models with a hosted endpoint, `diffusers` support, or a runnable reference implementation.
- Frameworks and UIs for running diffusion pipelines (ComfyUI, A1111, InvokeAI, etc.).
- Editing/enhancement tooling: ControlNet, adapters, upscalers, restorers.
- SDKs and client libraries for integrating image generation into apps.
- GPU platforms commonly used to serve image models.
- Storage and CDN services suited to generated-image workloads.
- Evaluation metrics, benchmarks, and leaderboards.
- Template/demo projects and reference implementations.

**Exclude**
- Research papers without runnable code or an API.
- Paywalled tools that gate developer access.
- Duplicate entries — cross-listing into our other awesome-* lists is fine, duplicates within this list are not.
- Self-promotional content with no developer value.

**Inclusion requirements (every entry)**
- Public product or docs page; URL resolves.
- Activity signal within the last 12 months (commit, release, docs update).
- Either a public API or an open-source install path.

## Files in this repo

- `entries.yaml` — source of truth. Only hand-edit this file.
- `categories.yaml` — the section taxonomy. Authoritative for what slugs are valid.
- `header.md`, `footer.md` — hand-written prose bracketing the generated list.
- `README.md`, `llms.txt` — **generated**. Do not edit.
- `CONTRIBUTING.md` — instructions for human PR authors.
- `.enrichment-cache.json` — local star-count cache; gitignored.

## Schema

Full schema at `~/awesome-lists/_shared/schema.json`. Required: `name`, `url`, `description`, `category`, `last_verified`. Optional: `docs_url`, `github`, `sdks`, `license`, `tags`, `b2_integration`.

`b2_integration` is a URL pointing to docs for the tool's B2 integration. Leave as the empty string `""` when none exists yet. When a new integration ships, set this field and drop the tool from `~/awesome-lists/_internal/priorities.yaml`.

`category` must be a slug defined in `categories.yaml` — validate.py will reject anything else.

## Workflow

Adding or updating an entry:

1. Edit `entries.yaml` only.
2. `python ~/awesome-lists/scripts/validate.py --repo .`
3. (Optional) `python ~/awesome-lists/scripts/enrich.py --repo .`
4. `python ~/awesome-lists/scripts/generate.py --repo .`
5. Commit `entries.yaml`, `README.md`, `llms.txt` together. One entry per PR.

## Hard rules

- Never edit `README.md` or `llms.txt` by hand — any manual edit is overwritten on the next `generate.py` run.
- Never commit `.enrichment-cache.json`.
- Never delete an entry outright. If a tool is dead or discontinued, tag it `tags: [needs-review]` and file a note in `~/awesome-lists/_tasks/`.

## Good vs. rejected entries

**Good**
```yaml
- name: ComfyUI
  url: https://github.com/Comfy-Org/ComfyUI
  docs_url: https://docs.comfy.org/
  description: Node-based graph UI and backend for diffusion models. Highly customizable, API-accessible.
  category: frameworks-and-uis
  github: Comfy-Org/ComfyUI
  license: GPL-3.0
  b2_integration: ""
  last_verified: 2026-03-01
```

**Rejected**
- Out of scope: an LLM-only tool with no image capability.
- Vaporware: a landing page with a waitlist, no docs, no repo.
- Dead link: homepage 404s or repo archived >12 months ago with no successor.
