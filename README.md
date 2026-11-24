# Thrillex
Competitive entry for make.fun token-radar-01: comps-based pre-token protocol valuation radar with farm plans

## Run locally

Requires Node.js 22.18 or later. Run the radar from the repository root:

```sh
node main.ts --input input/snapshot.json --output out
```

Serve the generated files with `npx --yes serve out -p 3000`, then open
`http://localhost:3000/dashboard/`.

The static dashboard reads the sealed snapshot only; it makes no network requests.
`out/board.json` contains the ranked estimates and farm steps. The model uses TVL,
seven-day TVL change, and DefiLlama listing age. Listing age is only a proxy, and
missing token metadata means “not recorded,” not proof that no token exists.
