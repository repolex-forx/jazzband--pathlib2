# Repolex Knowledge Graph of jazzband/pathlib2

RDF knowledge graph data for [jazzband/pathlib2](https://github.com/jazzband/pathlib2), parsed by [repolex](https://repolex.ai).

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
rlex download jazzband/pathlib2
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0ac11b8d697069abea58a8188061f1a1870977af
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 0ac11b8d697069abea58a8188061f1a1870977af
│           └── chunk-001.nq.gz
├── blob
│   ├── 08f4f701d335be10abb54437dfb34fdcf4b1da33.nq.gz
│   ├── 145343636175c68998ad0fcdfdf31f9b22387028.nq.gz
│   ├── 1715d3d7a2cd2aa937af86adaf52e290f071371d.nq.gz
│   ├── 269795badaf134979c296829a435e41e5d0d75a4.nq.gz
│   ├── 40d2450319b23a0763a82da51816bca985a930d5.nq.gz
│   ├── 44b55ce062f0dd4c3450143f7180bd3fa40ea746.nq.gz
│   ├── 4bf4074c75ba30db5904040736a496d6912fce46.nq.gz
│   ├── 4e6a92c443efecb47ac790fb7170e4a27d8069fd.nq.gz
│   ├── 50a693014c55c288f1b3196a96e5706cf4221557.nq.gz
│   ├── 59ab15d43f1960cf3d74a829c2ceb08f15f74e42.nq.gz
│   ├── 6426d547b8dd438b1c15ab671ff3d05d9523c634.nq.gz
│   ├── 68534a5865dbb9e3883aaa676f35a524dc5c6bc4.nq.gz
│   ├── 6e29bb75bb49e50b9532d4647592bd69f72af802.nq.gz
│   ├── 743f681394e20729c6e7a88d7ee08c529e923394.nq.gz
│   ├── 75d12c7f9bf37079a33aa8619b810563bc19ab13.nq.gz
│   ├── 7625894c8c78d414c3529f3ffa38656a4d2742dc.nq.gz
│   ├── 7aed1e8d297b6e686d93094ec89da69c198fcd00.nq.gz
│   ├── 7d00a97f1ac6348d2e5304e2d855d0f88e2463ad.nq.gz
│   ├── 8084272b4b7828a0748ae9209f92611e196801de.nq.gz
│   ├── 88515d77dcf246fb21c7e2636bad02c39e98c223.nq.gz
│   ├── a0df9e8a5ea6b2f21069602c16168983390e78f8.nq.gz
│   ├── ad3a7db4b56b3a3c2315d159b98891f5805008f2.nq.gz
│   ├── c33c42f9125187845e2a848d2121c46dd1aab450.nq.gz
│   ├── cc85cef0c5529fa606a2ea107b04e884776c1bfd.nq.gz
│   ├── d4bb2cbb9eddb1bb1b4f366623044af8e4830919.nq.gz
│   ├── e079f8a6038dd2dc8512967540f96ee0de172067.nq.gz
│   ├── e0d5efab56fb94577e7804603eb6f21f36977cb2.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── fc3af324a4ec2b5fc548aa6d22de7eb54bfda44a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 0ac11b8d697069abea58a8188061f1a1870977af.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 37 files
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

[jazzband/pathlib2](https://github.com/jazzband/pathlib2)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
