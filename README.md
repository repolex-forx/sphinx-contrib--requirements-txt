# Repolex Knowledge Graph of sphinx-contrib/requirements-txt

RDF knowledge graph data for [sphinx-contrib/requirements-txt](https://github.com/sphinx-contrib/requirements-txt), parsed by [repolex](https://repolex.ai).

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
rlex download sphinx-contrib/requirements-txt
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c72576cd0d3af103f9d921132a219de223e83cad
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── c72576cd0d3af103f9d921132a219de223e83cad
│           └── chunk-001.nq.gz
├── blob
│   ├── 03969d46c77d7a97615f3504dd366ac292fb9ac2.nq.gz
│   ├── 1a5d436a26705eb778cb99b1e78237056391b8af.nq.gz
│   ├── 1da65476d7a0b956d8267c046b636fc9a45d1416.nq.gz
│   ├── 209d62fd65c87c0afd187808464af4a346d40d2c.nq.gz
│   ├── 46097108c4e8feebe61e9569e3fd88d2887e8c9e.nq.gz
│   ├── 4dcda19c20aa286b65b28b4998f63f7dc8bfc36b.nq.gz
│   ├── 50a88aa8f4c12bd3b6f9016f0fd43680b9e13973.nq.gz
│   ├── 54082ccd5dea414080bd6c6fc5378d8600a9a216.nq.gz
│   ├── 6c837615295dd7dfb19724c0c46859eec4888a46.nq.gz
│   ├── 7658cd60562871ffeb629e72b9a3f3a412ce70b1.nq.gz
│   ├── 7927438aec60b30e66ddcce5edf81aa2d26aa9a7.nq.gz
│   ├── 798253cb9e04f0e42eb7aae8ceb5dac0f93603d4.nq.gz
│   ├── 7dd10c9ffb2894d7873e06630fa2cf7c4a8d9e58.nq.gz
│   ├── 83d20578280f9c98a0001074e0ef076be8b921e9.nq.gz
│   ├── 89a3f3213ac6c9438d70dec80ec4627ee5dbd078.nq.gz
│   ├── 90889edbb932eec3ecdb080cecb993b2cdb0dc58.nq.gz
│   ├── 9b4b11c874606f397aa5e18ac132c5d8cf270ef9.nq.gz
│   ├── a462dc4f041f7240a696cd7c8af6ba2878e5990c.nq.gz
│   ├── ac7fdc0b39f56a34f68e3ece03d177243c9bef18.nq.gz
│   ├── ae4800099b7b0582bf30ff9a4f5efc90e1c9dab5.nq.gz
│   ├── c42eb772f510b4ee8bd3df978017478afa75daad.nq.gz
│   ├── c5e7ddbb51a58432dad491182f0bcce4e07ed839.nq.gz
│   ├── d280a7d6d269a87c975d0351e52bfed0270b18f2.nq.gz
│   ├── e3a21f400791009ab45ef6b1ddbaa9e474c0684e.nq.gz
│   ├── e525ed9a265af771c02411a7451623f872749003.nq.gz
│   ├── f288702d2fa16d3cdf0035b15a9fcbc552cd88e7.nq.gz
│   └── f93aaed978ea8e9801f0e2067770c07595df91ee.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── c72576cd0d3af103f9d921132a219de223e83cad.nq.gz
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

[sphinx-contrib/requirements-txt](https://github.com/sphinx-contrib/requirements-txt)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
