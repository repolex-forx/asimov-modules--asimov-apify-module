# Repolex Knowledge Graph of asimov-modules/asimov-apify-module

RDF knowledge graph data for [asimov-modules/asimov-apify-module](https://github.com/asimov-modules/asimov-apify-module), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-apify-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 819117270aa373a7fc99b955918a97e1565217f9
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 819117270aa373a7fc99b955918a97e1565217f9.nq.gz
│   └── repolex
│       └── 819117270aa373a7fc99b955918a97e1565217f9
│           └── chunk-001.nq.gz
├── blob
│   ├── 11c0954b766cadb7fa6bb38ade3b72269e0a6723.nq.gz
│   ├── 145f6632e0c8816a31091f510249d5181a0f97ea.nq.gz
│   ├── 1ceed1c0b12dabab6b269b6cd1f04053ef44e6fd.nq.gz
│   ├── 2081315a8334590e3044cafadc574aeca591ac2f.nq.gz
│   ├── 2391f73aa051d3804285ce744f2e9a1c7e08993d.nq.gz
│   ├── 403f733ba797942679b41cc2c39672651d4e67c3.nq.gz
│   ├── 48cc2b05a741a35865f145cbd14df9f1e658e3f9.nq.gz
│   ├── 516865cdd5e31e540221cf0bdff7d18e50e10c6c.nq.gz
│   ├── 59f6f4b0acfaaecf01ffbce347cea4e97d07265f.nq.gz
│   ├── 5d2aaf7f4ebf55ed082e076e777740f595a371aa.nq.gz
│   ├── 5f5cf896c81688e4360b37f1bcda92f7bc6f7423.nq.gz
│   ├── 6b23d61018f43b840f8d2ff3b45a1c02d76df38d.nq.gz
│   ├── 6efeac80ae1467b969bd715add88d4c158cd8247.nq.gz
│   ├── 7337759e7adaf5458132d571b9e92ae12be61b64.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 7796847f1ca9453a132d30c39874edfc7d180582.nq.gz
│   ├── 8068ba8945a77b35278d7af0bb639acfa531095a.nq.gz
│   ├── 8236d6c7238283a6dbcd483f68b4979b55b7867a.nq.gz
│   ├── 845639eef26c0e95586203ae78369f67552ccb17.nq.gz
│   ├── 9c558e357c41674e39880abb6c3209e539de42e2.nq.gz
│   ├── a36fedab8db68b26a76fbbf1de1f549e4a12261b.nq.gz
│   ├── abffb5bf752b1872b181c63ce8dcbdaa84e97f7b.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── b1d6b7287c46dc8b30174ae579741aed9a8d28b3.nq.gz
│   ├── c5799fec567ce4f90be77c334ed12c64bb85eec4.nq.gz
│   ├── c5caa726c5ba5241ec720c4a68fae31055c47bed.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── d91fff7f65d924b93a584de7393b12826e07e843.nq.gz
│   ├── e2cf9b5cdde50cc22c01c816303278560f8bb25c.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── e5a360a05c5ea4188b2a6caa12cd316bd7beb9e3.nq.gz
│   ├── ee7c8182cc50bc4b5127c6d5694f6299e6287cf6.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   ├── f2b7575e1e7593a8f933e240a8b6c09979b5844d.nq.gz
│   └── fc92e80bb63710e96b2864d2dd8c2eab851d0da0.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 819117270aa373a7fc99b955918a97e1565217f9.nq.gz
├── filetree
│   └── 819117270aa373a7fc99b955918a97e1565217f9.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 45 files
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

[asimov-modules/asimov-apify-module](https://github.com/asimov-modules/asimov-apify-module)

---
*Parsed on 2026-09-28 by [repolex](https://repolex.ai)*
