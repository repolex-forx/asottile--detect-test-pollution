# Repolex Knowledge Graph of asottile/detect-test-pollution

RDF knowledge graph data for [asottile/detect-test-pollution](https://github.com/asottile/detect-test-pollution), parsed by [repolex](https://repolex.ai).

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
rlex download asottile/detect-test-pollution
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 64b684098f1df26b150570fe8498cb42918a67aa
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 64b684098f1df26b150570fe8498cb42918a67aa
│           └── chunk-001.nq.gz
├── blob
│   ├── 0833183b4b36f1da722cb77cf1fca83b5cd4dcd5.nq.gz
│   ├── 18483232503156c190648b7285a49d8e699ad87a.nq.gz
│   ├── 22da610e781c811776d2f9bec559b75dc2572654.nq.gz
│   ├── 246663a38635cb729538904ac13a7d53e92cbb06.nq.gz
│   ├── 3d93aefb2da505dba9c0114404cfaaeee5ad0d3f.nq.gz
│   ├── 5370c9485451439199ab7ab9ba30c95d9a046275.nq.gz
│   ├── 799aeaaaf8d72c5f74ca1fb6fddccbc99c58f874.nq.gz
│   ├── 8c38c3fa07daab3596dae959bfec1e3571868cb0.nq.gz
│   ├── 9157d3dff945ba0feac3e6aae924b0b182ad874a.nq.gz
│   ├── b1447c3015af9511f2dee402ca4b5ad62adf5dce.nq.gz
│   ├── ca1d90ea180858ae143c0e62d920e350d3acc62d.nq.gz
│   ├── e0e580db34d5b169bd97455f1c9020d88f81ae3e.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 64b684098f1df26b150570fe8498cb42918a67aa.nq.gz
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

[asottile/detect-test-pollution](https://github.com/asottile/detect-test-pollution)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
