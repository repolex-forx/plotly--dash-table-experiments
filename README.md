# Repolex Knowledge Graph of plotly/dash-table-experiments

RDF knowledge graph data for [plotly/dash-table-experiments](https://github.com/plotly/dash-table-experiments), parsed by [repolex](https://repolex.ai).

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
rlex download plotly/dash-table-experiments
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c3ecb3b1a708d8c07d0486a07cae400022b6a9a1
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── c3ecb3b1a708d8c07d0486a07cae400022b6a9a1
│           └── chunk-001.nq.gz
├── blob
│   ├── 0c305818b3fd759af2366cd2046309f5911494fc.nq.gz
│   ├── 0dd7d69d15e6690b23b3ce9c06a4764e03710bde.nq.gz
│   ├── 1946da8f08745afe02e1ea8c7212910e76fb55ae.nq.gz
│   ├── 1aa51bbd3d5e439ac47e95a4191b548738e74ea3.nq.gz
│   ├── 256021120a20a12673d1594f401579623c3e1770.nq.gz
│   ├── 262204d8fc45d6e9692d2a046e5df5840e37363b.nq.gz
│   ├── 29e35e67413068c512037c9de6b9e9cc1d71a528.nq.gz
│   ├── 29ed1e615255bc3ef2b83f0fe31a9a37e5b27f90.nq.gz
│   ├── 2b1c0f244f534500ca8ed4c4b52900c73b92d23a.nq.gz
│   ├── 2c7d38d6774f954489f8616ad7e07fd9acfdebf8.nq.gz
│   ├── 30451a6363a463603e882e1c24ae810ac20867b9.nq.gz
│   ├── 349264fd26a2e1b2b2368f13c83fd24f710665d9.nq.gz
│   ├── 3d42b04db711d06d3ab013fe888948536b58aecb.nq.gz
│   ├── 5714e06781976fcc45a44428010df4fd0f706da5.nq.gz
│   ├── 57f4f8db2c5fd8df73a7bef76978a25be9f1761f.nq.gz
│   ├── 59592a45eb1883af5b712749bbba49b7d356057e.nq.gz
│   ├── 634a2e2252d40fd424d77c2e15558ffc3195a363.nq.gz
│   ├── 634fcff051856c2fc48e3eaf5731e1d54939fa82.nq.gz
│   ├── 6e5a5323fce38a29805a993d06d8ce585bebb14b.nq.gz
│   ├── 8296462109b6fece56a01d69b2220c4a4f30121b.nq.gz
│   ├── 88fdb2ee6a42402ca0ecbe2a87040233ba329433.nq.gz
│   ├── 8c45e8e76f02a0f0c914182cf110db25c119270f.nq.gz
│   ├── 8cf7af30d0a91e6de7916174ff91ac8d28d5f2a5.nq.gz
│   ├── 8dd9c091ef189f284067cf94ba15cd70f6945ab9.nq.gz
│   ├── 9529b1e0aae05a6928b2b0c8e03b92c0f84bfb9f.nq.gz
│   ├── 953af33c647da369e1a051fe5072994fea2ca2ca.nq.gz
│   ├── 9826b544f26f376d1845b689a569dfc9ee1a1084.nq.gz
│   ├── a10f351e1dee5dffa9fd4fc21e358ad9c4dca66d.nq.gz
│   ├── cf2e014bc2d6740bc1afbc758f5e877f43e82204.nq.gz
│   ├── e052eb6625f39a01e8896f4760cadbff07f382cc.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e79d91a9e6db0b9376b7e1751474cf8fd5249640.nq.gz
│   ├── eea850f759a02f5cc40452e268c76e40dcdf6662.nq.gz
│   ├── ef7eb44d9ac437a9b7fff8294e69b5dfe9c65d2f.nq.gz
│   ├── ef8270cd516561d0744f8c4d0c913c3376b799e5.nq.gz
│   ├── f399dd7fcf9fbff093e5056c70c0eeb145167853.nq.gz
│   └── f41bcd85a2138175c576b603b8cf58133659c85b.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── c3ecb3b1a708d8c07d0486a07cae400022b6a9a1.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 45 files
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

[plotly/dash-table-experiments](https://github.com/plotly/dash-table-experiments)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
