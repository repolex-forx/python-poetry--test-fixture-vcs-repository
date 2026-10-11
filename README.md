# Repolex Knowledge Graph of python-poetry/test-fixture-vcs-repository

RDF knowledge graph data for [python-poetry/test-fixture-vcs-repository](https://github.com/python-poetry/test-fixture-vcs-repository), parsed by [repolex](https://repolex.ai).

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
rlex download python-poetry/test-fixture-vcs-repository
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0be1215c90fffe37c5629cf2764615e9d9530e67
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 0be1215c90fffe37c5629cf2764615e9d9530e67
│           └── chunk-001.nq.gz
├── blob
│   ├── 40cf6aabdb3cdebbb08e7e18c6a0c5e268f9b742.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f9b02507562a69fd78822b6331b00ab176431f1b.nq.gz
│   └── fd44b6679a9a197cf67ecb77080bacc7b59a848d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 0be1215c90fffe37c5629cf2764615e9d9530e67.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 11 files
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

[python-poetry/test-fixture-vcs-repository](https://github.com/python-poetry/test-fixture-vcs-repository)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
