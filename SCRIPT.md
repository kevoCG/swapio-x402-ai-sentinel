# Video Pitch Script: AI Agent Liquidity Rebalancer on Solana via Swap.io x402
**Target Duration:** 85 seconds (Within 60–120s limit)  
**Track:** Superteam Earn — Pitch an x402 Use Case with Swap.io ($500 USDC)  
**Presenter / Brand:** Kevin Cabrera (`@0xQueryLab` / `@kevoCG`)  
**Sponsor:** `@swapdotio` / `@Superteam`  

---

### [00:00 - 00:15] Hook: The Autonomous Agent Billing Dilemma
* **Visual:** Slide 1 / Animation — AI Agent running on an edge server encountering an API key wall / monthly SaaS invoice ($500/mo) vs. empty idle time.
* **Voiceover:**
  > *"Autonomous AI agents don't have credit cards, and they shouldn't pay $500 monthly SaaS subscriptions for API keys they only use during high-volatility spikes. Meet the AI Liquidity Sentinel: an autonomous agent that monitors on-chain orderbook skew on Solana, and pays per single quote strictly when rebalancing is required using Swap.io's x402 protocol."*

---

### [00:15 - 00:35] Concrete Use Case: The AI Liquidity Sentinel
* **Visual:** Slide 2 / Architecture Diagram — Sentinel monitoring CLMM inventory skew (e.g. Orca SOL/USDC 85% skew). Trigger condition: slippage risk threshold reached -> Trigger Swap.io Agent API.
* **Voiceover:**
  > *"Instead of polling an expensive centralized API thousands of times a day on a fixed plan, our Sentinel monitors on-chain events for free. When an inventory imbalance or liquidation cascade threatens pool health, it prepares an instant rebalancing swap. But how does it buy the quote with zero human intervention?"*

---

### [00:35 - 00:55] How x402 Works in Action (HTTP 402 Protocol Flow)
* **Visual:** Slide 3 / Live Protocol Inspection — Terminal showing actual raw `POST https://hermes.swap.io/v1/swap/quote` returning HTTP 402 with `x402Version: 1`, `network: solana`, `payTo: BPz2u6eoWL...`, and `maxAmountRequired: 4405` (0.0044 USDC).
* **Voiceover:**
  > *"This is where x402 changes the game. The agent hits Swap.io's Hermes endpoint. The server responds with standard HTTP 402 Payment Required, requesting exactly 4,405 micro-USDC to address `BPz2u...`. The agent signs a sub-cent micropayment directly on Solana, replays the request with the payment header, and instantly receives the optimal multi-DEX route."*

---

### [00:55 - 01:15] Why x402 Beats Traditional Web2 APIs for AI Agents
* **Visual:** Slide 4 / Comparison Matrix:
  - Web2 APIs: Credit cards, KYC, API key leakage risks, expensive fixed monthly tiers.
  - Swap.io x402: Native programmatic settlement, micro-metered pay-per-call (0.0044 USDC), zero subscription waste, multi-chain (Solana & Base).
* **Voiceover:**
  > *"Why does x402 beat traditional alternatives? 
  > First: Zero human credentialing. Agents self-fund from their own on-chain treasury.
  > Second: True pay-per-execution economics. If volatility is quiet for a week, cost is exactly zero dollars.
  > And third: Uncensorable, trustless settlement settled in milliseconds on Solana."*

---

### [01:15 - 01:25] Call to Action & Conclusion
* **Visual:** Slide 5 / Outro — Swap.io logo, documentation link (`docs.swap.io`), `@0xQueryLab`, `@swapdotio`, `@Superteam`.
* **Voiceover:**
  > *"Autonomous trading agents don't need subscriptions. They need frictionless, machine-to-machine financial primitives. Build the autonomous on-chain future with Swap.io x402. Visit swap.io today."*
