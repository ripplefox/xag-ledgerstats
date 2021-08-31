# XAG Ledger Stats

You can use this tool to fetch all the account balance information or a specific XAG ledger number.

The default server it will connect to is `g1.xrpgen.com`.

## Workflow

You'll need to have [node (nodejs)](https://nodejs.org/en/download/) installed on your computer.

After clone this repository, install dependencies:

`npm install`

## Syntax

### Fetch ledger account data into .json file

Run the code to fetch all account balances using:

```
npm run fetch
```

If you don't append any arguments, the latest (closed) ledger will be fetched from the public `g1.xrpgen.com` server.

If you want to fetch a specific ledger, append the ledger index:

```
npm run fetch 22508618
```

**The tool will save the balance information for the ledger in `./data/ledgerno.json`, eg. `./data/22508618.json`.

### Process ledger data from .json file (to stats)

Run:

```
npm run stats 22508618
```

... where `22508618` is the ledger index you want to process. You should -of course- have fetched this ledger first.

Sample:

```
 -- Ledger close time:   2021-Aug-31 05:51:02.000000000
Reading ledger stats: 22508618.json
 -- Accounts:              82600
 -- Ledger close time:     2021-Aug-31 05:54:42.000000000
 -- Ledger hash:           5396F8478976A4083A17BAA22F4141B284146ACB349626BE11252C8A337D27D0
 -- Ledger index:          22508618
 -- Total XAG existing:    99,999,998,065.321472
```