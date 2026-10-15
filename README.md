# Repolex Knowledge Graph of scikit-hep/hepunits

RDF knowledge graph data for [scikit-hep/hepunits](https://github.com/scikit-hep/hepunits), parsed by [repolex](https://repolex.ai).

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
rlex download scikit-hep/hepunits
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f78ca6d7518fee26a762841e792be1b0e9174a58
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── f78ca6d7518fee26a762841e792be1b0e9174a58
│           └── chunk-001.nq.gz
├── blob
│   ├── 0eb4cddce6772b5b2b0040634404f79048444e3e.nq.gz
│   ├── 15e21f495cae922407084bb63427cbe4d9cdca6e.nq.gz
│   ├── 16acf3bab70935789f137891d92f3ad36a713435.nq.gz
│   ├── 18606c83c9e1dfe5f4e4f7ccc4b777f7a9f66938.nq.gz
│   ├── 18e6b152c4f5b387082ef8fea47f30a6d9d0a4d2.nq.gz
│   ├── 1e7d83952e493ad1e5047f4b0c81768d1130091f.nq.gz
│   ├── 349777b412bf4d7d5992c94f343d4bd3cec430d9.nq.gz
│   ├── 3e5430ebb3a20e2fda044d2b5bacebb9abb00c58.nq.gz
│   ├── 5bb2b22f78faec68eeed9a623c15cad2747c9eba.nq.gz
│   ├── 7b26d1d8d6cb73a5ca1ea552ae5a6c157dbdc786.nq.gz
│   ├── 7d690d70715189af7061380c875d8b91f4ed2d52.nq.gz
│   ├── 7f56669e2a67ea8a899d151a7a39c1b9e1a4e0f7.nq.gz
│   ├── 7fb722cb85e6922750f0a8b73e53dab1f005dd97.nq.gz
│   ├── 8b13673c14657c63f5a23c7b514f9fca0725174f.nq.gz
│   ├── 8c79230d2be8bf1421c9e9614c108c87cae942a0.nq.gz
│   ├── 98756943aec17e67eb098452de2df5acf7ec0b44.nq.gz
│   ├── a062ed6c8adac60193986e22b994d23f8fd0448a.nq.gz
│   ├── a3417d4ffa67be1c561ec8270f617443687be75f.nq.gz
│   ├── a996da08aca1e2b5fc1462400e294c2f94239f21.nq.gz
│   ├── ae0914e0d655e4b0d573954d6f599a8b26c01578.nq.gz
│   ├── d652f1549db2566fdef0ef5aaf00640215a8151e.nq.gz
│   ├── da7908c0b8d3d8621e9810386d76db62ad7af97b.nq.gz
│   ├── e5cbcd5ce59bb5115edd7c1264c4cd647e759d4f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ea0fb8dd5a01f1ad09e3f194d4e94cd8b096eea6.nq.gz
│   └── fedd801d93d96f475ce541807ad278c96828a93c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── f78ca6d7518fee26a762841e792be1b0e9174a58.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 34 files
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

[scikit-hep/hepunits](https://github.com/scikit-hep/hepunits)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
