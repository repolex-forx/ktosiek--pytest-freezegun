# Repolex Knowledge Graph of ktosiek/pytest-freezegun

RDF knowledge graph data for [ktosiek/pytest-freezegun](https://github.com/ktosiek/pytest-freezegun), parsed by [repolex](https://repolex.ai).

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
rlex download ktosiek/pytest-freezegun
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3202256486ea405904ded68b8bd61a409b856a75
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 3202256486ea405904ded68b8bd61a409b856a75
│           └── chunk-001.nq.gz
├── blob
│   ├── 069ddf71651adbeda3d3370e7b170529d3e5fab7.nq.gz
│   ├── 1ade348bb74d5b25edb2813cc00395dfc3e6c53f.nq.gz
│   ├── 3846fd95458babe609bce4fd7efe756328f56f29.nq.gz
│   ├── 57318620a2126685842ff42d8ab2b29716dbca2e.nq.gz
│   ├── a08133f5c3c2062e0866fb15b5ade7f0f04f1f59.nq.gz
│   ├── a6642a86b98d7a5d47794c6898e74969e9ef1499.nq.gz
│   ├── ad267de127ad8e5df555ab4f868d86f1e65d93a3.nq.gz
│   ├── bc711e55fefdd729816958fa0ce1563b55217c29.nq.gz
│   ├── c3bb05e8908036ef8446eff03f13be8a3c62ab9a.nq.gz
│   ├── c82334553632d12caf96bd3d3d332d9683d2635c.nq.gz
│   ├── cccceee725be83035c2e77830b6c7a2800312d76.nq.gz
│   ├── d3009b3055f3a938c82c9e01a257150d12a206a0.nq.gz
│   ├── db2479eb3248d9825db8ffbd57c99e5a6f0a7920.nq.gz
│   ├── e408160b3ceb3fd64459ba6e9d86a3321d46883d.nq.gz
│   └── e723cb06796121518d58dbca524d8f6650b9b953.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 3202256486ea405904ded68b8bd61a409b856a75.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 23 files
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

[ktosiek/pytest-freezegun](https://github.com/ktosiek/pytest-freezegun)

---
*Parsed on 2026-10-18 by [repolex](https://repolex.ai)*
