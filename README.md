# Repolex Knowledge Graph of modelcontextprotocol/experimental-ext-tool-annotations

RDF knowledge graph data for [modelcontextprotocol/experimental-ext-tool-annotations](https://github.com/modelcontextprotocol/experimental-ext-tool-annotations), parsed by [repolex](https://repolex.ai).

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
rlex download modelcontextprotocol/experimental-ext-tool-annotations
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── fecace78a9552f70ba735d750fc3c4b190e20429
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── fecace78a9552f70ba735d750fc3c4b190e20429
│           └── chunk-001.nq.gz
├── blob
│   ├── 26bd1ed51dbe1f25ce941e0323bef11bb283ecde.nq.gz
│   ├── 3258672ca40e0e9b127791df1d32ddc66eef7e82.nq.gz
│   ├── 4e1429807cdbf7a19f93557a6036e3e804921b88.nq.gz
│   ├── 6fe939e97385b115b31cd9938773d229c301aa4b.nq.gz
│   ├── 7a1fe832c173c3938eb93ad485ceae6b8ca46c04.nq.gz
│   ├── 858391f902b506abd3665962a4936f8daa0d3ed9.nq.gz
│   ├── 86898e76d608051c6142a4d6377141c27464a1bc.nq.gz
│   ├── 8d85156bc4d17e32060356f0db5f8981bd875eb5.nq.gz
│   ├── 962c715c9550f1093fd5529c16650be89df1b846.nq.gz
│   ├── a72eb4f22cfe215eee2d955a2d1fbbb11ba98493.nq.gz
│   ├── b024e547f73fbe857c8ad3801a7c36c0558cc489.nq.gz
│   ├── b59407c3777437bbda4d931d983ecef67edc5e0e.nq.gz
│   ├── dd27eeec5bb688dde0127c058b06c187295607cd.nq.gz
│   ├── e3cdd5a84221ec6e98e57cb53b3e213fc2b6fbe1.nq.gz
│   ├── f3e4946074ffab5e9fcf8822057d23c71c58974a.nq.gz
│   └── fb89154f79e2a3306da3833282bd0045bff39873.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── fecace78a9552f70ba735d750fc3c4b190e20429.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 24 files
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

[modelcontextprotocol/experimental-ext-tool-annotations](https://github.com/modelcontextprotocol/experimental-ext-tool-annotations)

---
*Parsed on 2026-10-09 by [repolex](https://repolex.ai)*
