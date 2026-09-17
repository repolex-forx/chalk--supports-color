# Repolex Knowledge Graph of chalk/supports-color

RDF knowledge graph data for [chalk/supports-color](https://github.com/chalk/supports-color), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download chalk/supports-color
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d4068e70f02d9bf3813fc877bdad7360d8e51d71
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── d4068e70f02d9bf3813fc877bdad7360d8e51d71.nq.gz
│   └── repolex
│       └── d4068e70f02d9bf3813fc877bdad7360d8e51d71
│           └── chunk-001.nq.gz
├── blob
│   ├── 0e8a9ccb8665265a0b38d98f5f08c60c3d347c24.nq.gz
│   ├── 1c6314a31833395fd5ff016a6506bdd51860657c.nq.gz
│   ├── 239ecff1372358a22aa99dcbb375fdad7abba817.nq.gz
│   ├── 346585cf904a9126a589404f48706564d3791659.nq.gz
│   ├── 43c97e719a5a824700932f72e6e7e6748ce45d01.nq.gz
│   ├── 5358dc50b2883157fca0fa4a12d2bb18acb093ee.nq.gz
│   ├── 5c192719b39f7b5eb3e80aa99b938533ee966ab6.nq.gz
│   ├── 609d0e6da714adb432d5f5a5b337f268071f22e7.nq.gz
│   ├── 6313b56c57848efce05faa7aa7e901ccfc2886ea.nq.gz
│   ├── 6aec1485aa58a3643ff76077c67d327ce13abaf5.nq.gz
│   ├── 6ce6fbe871e87763aea4da04051d4c78085abaa3.nq.gz
│   ├── 8915597ab45a0b35dc50bc2d08b64ea9382c9546.nq.gz
│   ├── 906a6f9b83224e75daf5d5d6a8cda554a6b1e996.nq.gz
│   ├── db44a785196f345cf7e41265aa3d388e9905d5fd.nq.gz
│   ├── f9008d8e713572cdf836f8ad4d54f2afe66b96c8.nq.gz
│   └── fa7ceba3eb4a9657a9db7f3ffca4e4e97a9019de.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── d4068e70f02d9bf3813fc877bdad7360d8e51d71.nq.gz
├── filetree
│   └── d4068e70f02d9bf3813fc877bdad7360d8e51d71.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 26 files
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

## Source repository

[chalk/supports-color](https://github.com/chalk/supports-color)

---
*Parsed on 2026-09-17 by [repolex](https://repolex.ai)*
