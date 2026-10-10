# Repolex Knowledge Graph of aio-libs/aiohttp-jinja2

RDF knowledge graph data for [aio-libs/aiohttp-jinja2](https://github.com/aio-libs/aiohttp-jinja2), parsed by [repolex](https://repolex.ai).

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
rlex download aio-libs/aiohttp-jinja2
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── e45cd674006cb621f0e6352ae8acfb7b184b5c59
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── e45cd674006cb621f0e6352ae8acfb7b184b5c59
│           └── chunk-001.nq.gz
├── blob
│   ├── 00dc91ebeb1d7f59712d2ecaa2c46ad0b2b3dc7f.nq.gz
│   ├── 065acdb8bdfb230e6f7f5686c2e5509fa6077cb8.nq.gz
│   ├── 09b93c8013b64806334fde8937953fda7f2b4067.nq.gz
│   ├── 0b43d6831d39531c9c1ad6d3ae65d2b521240d8e.nq.gz
│   ├── 0d2f8757175e1f0383d31a9555b3d093639d50f1.nq.gz
│   ├── 0de3fd10d2752b0d84d539b2b63d974b22f47fd7.nq.gz
│   ├── 11547df15a24841fe93e228ac85b3714c5605d93.nq.gz
│   ├── 15b83dfd752a8ed7683d03fc00b3e7a35c7f65c1.nq.gz
│   ├── 23fd4067e9f55d1db930557e56703dd2a28c5eb0.nq.gz
│   ├── 26d764b365064fe85510a71e7af07953c1b97e0a.nq.gz
│   ├── 2c59fd3726c3898d7c43987b84348e7e00e944c1.nq.gz
│   ├── 2d5ab3a110db685648ae8aedbc8e82eb1283aced.nq.gz
│   ├── 36979982708b367032730848375b2a457cf360b8.nq.gz
│   ├── 3cfee5c566c68af1f1cc7a83fde15a73bf2fc1c8.nq.gz
│   ├── 4be16f187440ffcd5ad2815c8ee0a3b2d24eb1f7.nq.gz
│   ├── 5234ff5b70b82dfbfeac55a3e80a76e8e6f9c88a.nq.gz
│   ├── 550f1861ee9446734401107ad43d9cd4a2c46c68.nq.gz
│   ├── 5f7f3c422a52947ccb5cd35c70c56f8b7d26c67a.nq.gz
│   ├── 67b4eb22b11329d2d8e06654a05fa0f8bfb3a33b.nq.gz
│   ├── 6f9b8ea343cbac872cad1d721c1d4a20ac4982e4.nq.gz
│   ├── 9570a7d257fc5c5de793ac8470bfc5dd84ab1551.nq.gz
│   ├── 99df37f64425e67de6ff3a5fc5090472838cffff.nq.gz
│   ├── 9b716d01182156c80c75b83294818ddb481b1dba.nq.gz
│   ├── 9efd3654373849c7ef1c1493a3cf0d88597dec96.nq.gz
│   ├── a55b24fac6fea3b1ce6631d8971bda791ed86439.nq.gz
│   ├── a88483fddf143d7675bfe60fad1b58dd80a24c66.nq.gz
│   ├── b1114c6e8364752ffa7724ec7cb1e7dddf527a3a.nq.gz
│   ├── b2437e540828b775a1334b98be385a74ce4fe05c.nq.gz
│   ├── b9fb8a6e0f4a5ce99899eb97d872c6b90f4bb678.nq.gz
│   ├── c69e451cecde08f43afd1f7ee9947832454146ff.nq.gz
│   ├── c8ba90d9f24667ca30d1cbde836cd9e79ac20512.nq.gz
│   ├── d5e05fdd585cf8bb2251215a96711191bc497e6a.nq.gz
│   ├── e5c94828c34f2622f11815e0eb4933a317ded249.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e6b82f3bf896e65b2c00fe60b10d4e603526ba23.nq.gz
│   ├── e87bef818e8b3af406145768ba6779181fc7b426.nq.gz
│   └── e9371928d2f131b14b76adfafaf8d8903b113202.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── e45cd674006cb621f0e6352ae8acfb7b184b5c59.nq.gz
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

[aio-libs/aiohttp-jinja2](https://github.com/aio-libs/aiohttp-jinja2)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
