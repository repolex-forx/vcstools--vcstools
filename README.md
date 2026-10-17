# Repolex Knowledge Graph of vcstools/vcstools

RDF knowledge graph data for [vcstools/vcstools](https://github.com/vcstools/vcstools), parsed by [repolex](https://repolex.ai).

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
rlex download vcstools/vcstools
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 5c9bbccbe68e331fe4e04a701830ef467bd6a763
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 5c9bbccbe68e331fe4e04a701830ef467bd6a763
│           └── chunk-001.nq.gz
├── blob
│   ├── 0ccc5d52262e1290a70226b759783878ebc949e9.nq.gz
│   ├── 0e07668abe2282aae1c69fd73fc11ed8496b65a1.nq.gz
│   ├── 107afcc354a8019f722612fb292660bd9f7d2afa.nq.gz
│   ├── 2273187b645483daf9e0230b56173c31c799e424.nq.gz
│   ├── 3e5391e7a6d94dd20bb9852c915d49365dcf269a.nq.gz
│   ├── 42faf0eb500d269e416bbdc95395004436d97418.nq.gz
│   ├── 43378289785dc91542ca26a55e4ddade86a39539.nq.gz
│   ├── 4fb7ec01215ecf2ab674a47b670d148c459f3d92.nq.gz
│   ├── 542c27d90ddf3cdac8acba24a3d5fd1543374812.nq.gz
│   ├── 5c3802469cbe1408c777fbbd3306aa33cf830023.nq.gz
│   ├── 5e6ff5469dd1e6af843fc572aa6de6c85183cda3.nq.gz
│   ├── 68cfd26c2ab015e5e33f5d274984494795267683.nq.gz
│   ├── 6c1fa7fee89a409d1f3d20d05f91d3ff3f375527.nq.gz
│   ├── 7812625d6f434c31cb793c755358a8af4794cd78.nq.gz
│   ├── 885b7c707ac43a703266171b9f9785c257505b7d.nq.gz
│   ├── 9090f0ef74bca8e6a7c5b96a3a2f818f5852eeae.nq.gz
│   ├── a38036e71480fd1c1c28abe04b13b69a76ecb783.nq.gz
│   ├── a3987da4e1d0892e56dbf9e0410c93e2aadc6a1e.nq.gz
│   ├── a8700d8068787705e9faf15f0c64f9f2c246135a.nq.gz
│   ├── a9da14cbf997001aa8929b3cabd0ecdd60106c8e.nq.gz
│   ├── abfe690870bc80c4806760f9620908bb862eacf3.nq.gz
│   ├── ac90b847bb9cc17da99aba98b860196fb1246eed.nq.gz
│   ├── afed6b8f9f44bdb285ddcb637f17193de50667bc.nq.gz
│   ├── b14910073ca8f499592efda78e9f0cfe1c865614.nq.gz
│   ├── b88ae4ae4f1f314cde6a65a8848bbf5bb241e8dc.nq.gz
│   ├── c34c4376ad3adff086e9cde8ca63c48c3b526858.nq.gz
│   ├── c350a9956835d172e97071e980674a051289716d.nq.gz
│   ├── c881a10994c73926f61bbf7cfa3a1383cd05ed76.nq.gz
│   ├── cb623fd1a4375b11dbf605f5c08240d128f5f059.nq.gz
│   ├── cc83a71edcd635217cd6fa864387dc7202c857da.nq.gz
│   ├── d21d73abcacb58b9b0ff7157d13335d1fc7a70bf.nq.gz
│   ├── d27df9e464346de3b390156d3e4ac774fe4a55fa.nq.gz
│   ├── dd003816487455a077fbc09073e11b384eaafbcc.nq.gz
│   ├── e330872de89671f7b49b69e9c229f115463dfea1.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e6f0fd551e969196854170c5f4081792481ff400.nq.gz
│   ├── e8bacd1b8a00972391acd2685069715092b8a943.nq.gz
│   ├── eacfe05d0ebdbd934f8b04a2456fb5469ceee8d4.nq.gz
│   ├── ee4f067715470b07c2258bee01df930420af4ee0.nq.gz
│   ├── efc57376a6e7a638325ba9e2da61bb46e26cbab3.nq.gz
│   ├── fa2f801c3ab1d2fc78859640678bd433d16d946b.nq.gz
│   ├── fb98c00df0a3297a440e7d96de1aaa6a988efa6e.nq.gz
│   └── fc301835d872925d677349e8488b85e664ce7a1a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 5c9bbccbe68e331fe4e04a701830ef467bd6a763.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 51 files
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

[vcstools/vcstools](https://github.com/vcstools/vcstools)

---
*Parsed on 2026-10-17 by [repolex](https://repolex.ai)*
