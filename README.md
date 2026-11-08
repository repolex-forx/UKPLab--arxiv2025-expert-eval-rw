# Repolex Knowledge Graph of UKPLab/arxiv2025-expert-eval-rw

RDF knowledge graph data for [UKPLab/arxiv2025-expert-eval-rw](https://github.com/UKPLab/arxiv2025-expert-eval-rw), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download UKPLab/arxiv2025-expert-eval-rw
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c591ebafac030d04c55f221b1c4ef16002be9191
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── c591ebafac030d04c55f221b1c4ef16002be9191
│           └── chunk-001.nq.gz
├── blob
│   ├── 0d03bf268c448d14aeb9becbc045bcde4ae6c9b7.nq.gz
│   ├── 1324bdc18c25d48bfcf7dcc1a5f0af67ecbf3cf0.nq.gz
│   ├── 13efb805f8dee919a8b2c11c525d6872a2b972b3.nq.gz
│   ├── 229edba242bb190698662cdce6bdacde9f0769fe.nq.gz
│   ├── 4494992e95a890d760734ccf84e8f96ba53b132e.nq.gz
│   ├── 454317062a2122eb17b330d9739ae105fa08786a.nq.gz
│   ├── 484814b9d3100ee4eb0624a7eb3dde7abd21615f.nq.gz
│   ├── 503920022aba5addf4ed32e4157bf0b8c8bcdf2b.nq.gz
│   ├── 613306f60e56b5d41e6634f619710c92c9cf6e81.nq.gz
│   ├── 66129d6e3418670033496399be48ba18cb94bd75.nq.gz
│   ├── 8b137891791fe96927ad78e64b0aad7bded08bdc.nq.gz
│   ├── 9b3703a912d40f58fb0fb57d20742e53d9fe7671.nq.gz
│   ├── a16423a1da00fb40dcd97973f76ff35faa070acc.nq.gz
│   ├── a9c00eff9283b69b72d79c8f7cb8096c43c47936.nq.gz
│   ├── bb3acfbad78d35205a427d7c67e0a7209054bc16.nq.gz
│   ├── bf663a6a1302ecefdcfb649f86c6c9b8cb3f36a9.nq.gz
│   ├── c08a79032592be8f5e7318991b0242323389469d.nq.gz
│   ├── c1fdda3953c8991d795f9ba113bf585122c12505.nq.gz
│   ├── c2c1b8e9a8264df99ab982af6543d1adcac438e3.nq.gz
│   ├── c6718de5c5ae59d2c22141a147f5afba41af9cbb.nq.gz
│   ├── d62fc66df4b9acdd5381753fde4173a5775b1ddf.nq.gz
│   ├── daa4859c365585fd7ec65fa3c84abddf5829c32a.nq.gz
│   ├── e99df58b21a6f69062a97964f4c8577fd1174324.nq.gz
│   ├── ea6d05ea8f9d193059c6b06318dbcc5229e7b33a.nq.gz
│   ├── ed3a9d377ba3c30e6eb8b2a35e08e8dc814a0725.nq.gz
│   ├── edb8f160150b1405153e2a7058fa5f2cbbb11c79.nq.gz
│   └── fe5ce3d049c849867228a10f10991259a7b680a9.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── c591ebafac030d04c55f221b1c4ef16002be9191.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 34 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[UKPLab/arxiv2025-expert-eval-rw](https://github.com/UKPLab/arxiv2025-expert-eval-rw)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
