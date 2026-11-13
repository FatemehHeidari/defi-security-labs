# DeFi Security Labs

Five interactive simulators of how lending markets, AMMs, liquid staking and perpetual futures fail, and who ends up paying. Every lab traces each dollar between users, liquidators, lenders and insurance funds.

**Open the labs:** https://fatemehheidari.github.io/defi-security-labs/

## The labs

| Lab | What it shows |
|---|---|
| **DeFi Risk Lab** | Six protocol labs side by side: lending, AMMs with sandwich MEV, perpetuals, liquid staking, oracles and flash-loan manipulation, and ERC-4626 vaults. It also has a view that shows each user's ledger. |
| **Lending Crash Chain** | One lending market hit by a price crash, a lagging oracle, LPs leaving the DEX and a staking token losing its peg. What-if runs change one cause at a time, so you see which one created the bad debt. |
| **Panic Desk** | A real-time game. You get $10,000 and two hours of market, with headlines that may be false. There are ten scenarios, and the debrief attributes your result to each move you made. |
| **Perp Panic Desk** | The same game for a perpetual on a virtual AMM: funding, long and short squeezes, a slow oracle, a gap crash that empties the insurance fund, and a repeg. |
| **Perp Workbench** | Eleven guided lessons on a vAMM perpetual, from "who pays a winner" to a flash crash that drains the insurance fund. Every USDC movement is recorded in a ledger. |

## How it runs

- Plain HTML and JavaScript, with no backend, no build step and no libraries (only Google Fonts).
- Every number comes from deterministic simulations in the page, so the same inputs always give the same run.
- The tests check what must always be true: money is conserved, ledgers balance, and a replay matches the live run.

To run it locally, open `index.html` in a browser, or serve the folder:

```sh
python3 -m http.server 8000
# then open http://localhost:8000
```

## A note on the content

These are teaching models, with simplified rules and illustrative numbers. They are not production risk engines. The perpetual labs follow the public Perpetual Protocol v1 design, plus an automatic repeg rule. A few real, public incidents are mentioned for context, such as Mango Markets in 2022.

## About

I built these with Claude (Anthropic) as a coding agent, to understand DeFi risk the way I learn best: by running the mechanics myself. I decided what each lab had to show and reviewed the results. The agent wrote and tested the code. The index page explains how they were built and what my review caught.

## License

[MIT](LICENSE)
