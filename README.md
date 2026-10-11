# Repolex Knowledge Graph of pytest-dev/pytest-env

RDF knowledge graph data for [pytest-dev/pytest-env](https://github.com/pytest-dev/pytest-env), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-env
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 484cdaed62d78a2a9515f6a0800fa8d927566e05
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 484cdaed62d78a2a9515f6a0800fa8d927566e05
│           └── chunk-001.nq.gz
├── blob
│   ├── 01805e669239cc023ab8c167e52d22e287c316a3.nq.gz
│   ├── 0a450a353bb97c631a7bf9ed6cb4f24abda31e13.nq.gz
│   ├── 0dbb8ae399c663c6af965f0b69249d39b95201fa.nq.gz
│   ├── 250e9a0837e41d65c294f217ff5d3d7007b61d5e.nq.gz
│   ├── 2a19e14d04dfad72f1d4a25f1620d8b1eb0135d8.nq.gz
│   ├── 2f688eb9a1d39b6bc75e9272858f5b0970420e83.nq.gz
│   ├── 54fa572b8f863c418372318734b338041c433110.nq.gz
│   ├── 5f89818f9e63c2f6829c7706c57f223cdb5bbd38.nq.gz
│   ├── 69d0cfd202c019ca1d5a92d59faf9a1380c61930.nq.gz
│   ├── 799f22ae0ad623375a65f7a7466379c44abff679.nq.gz
│   ├── 918061af64af8a6807560673a33407353d8fe798.nq.gz
│   ├── 9b32546ec8733f076298d92606d8676460fc0c2c.nq.gz
│   ├── beef6efa413b0e4cbec00dd27f98ce603df137de.nq.gz
│   ├── c8c51b2d6e885eeaaafe9d3fe97327bfdd3f5309.nq.gz
│   ├── d42451e35d36ff470a1abd6b59d94eadbedd7e56.nq.gz
│   ├── d42671c0d061a5b831ab428d6927e717264626b9.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f3e1a2966b81e3834a0ad29ab04aa87074873871.nq.gz
│   ├── f7b9fb6ad4f0a2892d6b5905db07656dddb10264.nq.gz
│   ├── fd9d35f2e7d68aa969246eac2c1a809f9e9a95ef.nq.gz
│   └── ff7a622dc80267282c099fe233cb089fe60fdc97.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 484cdaed62d78a2a9515f6a0800fa8d927566e05.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 29 files
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

[pytest-dev/pytest-env](https://github.com/pytest-dev/pytest-env)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
