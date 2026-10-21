# Repolex Knowledge Graph of executablebooks/mdformat-deflist

RDF knowledge graph data for [executablebooks/mdformat-deflist](https://github.com/executablebooks/mdformat-deflist), parsed by [repolex](https://repolex.ai).

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
rlex download executablebooks/mdformat-deflist
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 83e4b1810cf17ccdaa238c3698628d7371e2fb48
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 83e4b1810cf17ccdaa238c3698628d7371e2fb48
│           └── chunk-001.nq.gz
├── blob
│   ├── 2450ea4e2ee5e9e63292e77e1b1109bcfb42de0b.nq.gz
│   ├── 2a08e1cec4aa469911e5692d0c23f0635b63ad41.nq.gz
│   ├── 2dbe033b6c9076223ceb94eb6cded6e79d655305.nq.gz
│   ├── 428a40d097e02ce2a1490f21caa959101a92bef5.nq.gz
│   ├── 436f013c1e5fe689578128213c743570f4555fba.nq.gz
│   ├── 594f21abce9035b5aca2c757edd606e50c83ec2a.nq.gz
│   ├── 60b71f35915c0a65aab70b3cb5db9e819f478e15.nq.gz
│   ├── 837d05b1efddd706c8c9ab9c3d1de493f80fec80.nq.gz
│   ├── 869da7c282d331aa928043715e17c226a703f292.nq.gz
│   ├── c204ed438877287f79216e240bafb9af5ae60546.nq.gz
│   ├── e06ffb1f404dd0b81395d397042a7d95f96c76dd.nq.gz
│   ├── eba8454097a2a46fe5a1f2d599a971d903ae270c.nq.gz
│   └── f2571d3c04568a5fa9fafa62c3afbd5bca5ec5d7.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 83e4b1810cf17ccdaa238c3698628d7371e2fb48.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 21 files
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

[executablebooks/mdformat-deflist](https://github.com/executablebooks/mdformat-deflist)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
