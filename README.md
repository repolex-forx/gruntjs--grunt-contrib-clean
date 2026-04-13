# Repolex Knowledge Graph of gruntjs/grunt-contrib-clean

RDF knowledge graph data for [gruntjs/grunt-contrib-clean](https://github.com/gruntjs/grunt-contrib-clean), parsed by [repolex](https://repolex.ai).

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
lexq download gruntjs/grunt-contrib-clean
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9bd20a6effd37c37d892d227812e16c83c679651
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 9bd20a6effd37c37d892d227812e16c83c679651.nq.gz
│   └── repolex
│       └── 9bd20a6effd37c37d892d227812e16c83c679651
│           └── chunk-001.nq.gz
├── blob
│   ├── 08c6efb29c734da9ef2bdddacef4e67d9c3dc576.nq.gz
│   ├── 105366b5888c4f34aa65d7687eda885c6d1113bc.nq.gz
│   ├── 1073d15045c5cc10546bb5c91cfdeb84cc460772.nq.gz
│   ├── 176a458f94e0ea5272ce67c36bf30b6be9caf623.nq.gz
│   ├── 393d814542b4d1801a2492dfa82bb0de424238dc.nq.gz
│   ├── 499a8e633a8187576557ac16b553e11c50520d2a.nq.gz
│   ├── 507f91281ddb349f4b46006c67c28165b7690cf6.nq.gz
│   ├── 54476e6a8245b70a2740c536ab506787d36d5ad8.nq.gz
│   ├── 5733e6f75901ba7e8cffd5b09717fe5321f4c624.nq.gz
│   ├── 5cb6bfd4d74d1d9cca0e57c40ce8855378b78d86.nq.gz
│   ├── 6ad8929516f42e5e0da0a655c2d48a4a172787c9.nq.gz
│   ├── 77751bff5f55ea6bf568a288d576689ebef10703.nq.gz
│   ├── 7afa398a1d67ec2c2618d0897c4b60ac4c64ba7a.nq.gz
│   ├── 83f9fcffd0078f983662cea622e98843de7f2b22.nq.gz
│   ├── 84a77e20b136184fab959fb3a9c0535afa25fba2.nq.gz
│   ├── c59478ad6875f70bb893ada23fea7d4cd5b1b36f.nq.gz
│   ├── d3567c075ee099fe993a3a9030547b9075b5bc9d.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e79c3cf760012e5dc6d03f117fdf9952bb35b7bc.nq.gz
│   └── ea099b5cfca0ee61249d365ac77c2432db6da49a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 9bd20a6effd37c37d892d227812e16c83c679651.nq.gz
├── filetree
│   └── 9bd20a6effd37c37d892d227812e16c83c679651.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 30 files
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

[gruntjs/grunt-contrib-clean](https://github.com/gruntjs/grunt-contrib-clean)

---
*Parsed on 2026-04-13 by [repolex](https://repolex.ai)*
