<div align="center">
  <a href="https://cloudbitex.com">
    <img src="https://raw.githubusercontent.com/Cloudbit-Global/core/main/assets/cdbc-logo-256.png" alt="CloudbitDEX ($CDBC) Logo" width="135" height="135" />
  </a>
  <h1>CloudbitDEX (<code>cloudbitex.com</code>)</h1>
  <p><strong>Minimalist Multichain Decentralized Exchange, Liquidity Router &amp; Token Listing Hub for Cloudbit Classic ($CDBC)</strong></p>
  <p>
    <a href="https://cloudbitex.com">Launch CloudbitDEX</a> &bull;
    <a href="https://cdbc.io">cdbc.io</a> &bull;
    <a href="https://cdbc-api.vercel.app/api/cdbc/supply">Public API</a> &bull;
    <a href="https://cloudbit.to">cloudbit.to</a> &bull;
    <a href="https://t.me/cloudbit_ai_bot">@cloudbit_ai_bot</a> &bull;
    <a href="https://x.com/cloudbit_">X (@cloudbit_)</a>
  </p>
</div>

---

## Overview

**CloudbitDEX** ([`https://cloudbitex.com`](https://cloudbitex.com)) is the official Uniswap-style multichain decentralized exchange and liquidity interface for the **Cloudbit Classic ($CDBC)** ecosystem. Engineered with an obsidian dark-mode aesthetic and a lightweight PHP/JS backend optimized for high-availability IONOS hosting, CloudbitDEX connects EVM, Solana, Aptos, and Cosmos/Terra Classic liquidity under a single unified swap interface.

### Key Architecture Highlights
* **Multi-Ecosystem Wallet Engine:** Native support for EVM wallets (**Thirdweb / WalletConnect**, **Coinbase Smart Wallet**, MetaMask), Solana (**Phantom**, **Solflare**), Cosmos/Terra Classic (**Keplr**, **Leap**), plus an interactive **Demo Sandbox Mode** for risk-free testing.
* **Transparent Swap Routing & Fee Model:** Custom routing engine executing with a **0.25% CloudbitDEX Router Fee** (directed to the protocol treasury wallet) and a **0.25% Liquidity Provider (LP) Fee**, while the underlying `$CDBC` token maintains **0% Buy Tax and 0% Sell Tax**.
* **Live Market Rate Integration:** Server-side PHP proxy powered by the **CoinMarketCap (CMC) API** for real-time token pricing, slippage calculation, and fiat conversion without exposing API keys in client-side code.
* **Permissionless Token Import & Listing Portal:** Custom contract import module and automated token listing submission (`submit-listing.php`) with a standardized **0.5 BNB listing fee**.
* **Internationalization & Technical SEO:** Defaults to English (`en`) with an integrated multi-language flag switcher, structured JSON-LD schema, `sitemap.xml`, and `robots.txt` configuration.

---

## Protocol Fee & Tokenomics Specification

| Parameter | Value / Specification |
| :--- | :--- |
| **Native Ecosystem Token** | Cloudbit Classic (`$CDBC`) |
| **Fixed Maximum Supply** | `200,000,000 CDBC` |
| **Token Transfer Tax** | `0% Buy Tax / 0% Sell Tax` |
| **CloudbitDEX Router Fee** | `0.25%` (25 bps -> Protocol Treasury) |
| **Liquidity Provider Fee** | `0.25%` (25 bps -> Pool Liquidity Providers) |
| **Standard Token Listing Fee** | `0.5 BNB` (via `submit-listing.php`) |

---

## Verified Multichain Contract Registry on CloudbitDEX

### Primary Main Contract
* **BNB Smart Chain (BEP-20):** `0xaf8b1b1bb4a47f537932968C7DE6E251dd50C6a9` ([BscScan](https://bscscan.com/token/0xaf8b1b1bb4a47f537932968C7DE6E251dd50C6a9))

### Active Bridge & Cross-Chain Contracts
| Network | Standard | Verified Contract Address | Explorer |
| :--- | :--- | :--- | :--- |
| **Ethereum** | ERC-20 | `0xf2fef8fa2c52b927c0a589a1a645c77189f24541` | [Etherscan](https://etherscan.io/token/0xf2fef8fa2c52b927c0a589a1a645c77189f24541) |
| **Arbitrum One** | ERC-20 | `0xdc95becd16081bf00c3cabac5820a3e18b495cad` | [Arbiscan](https://arbiscan.io/token/0xdc95becd16081bf00c3cabac5820a3e18b495cad) |
| **Polygon (PoS)** | ERC-20 | `0x026a2ede22cc9525793120a3763d3a1c2c6840a8` | [Polygonscan](https://polygonscan.com/token/0x026a2ede22cc9525793120a3763d3a1c2c6840a8) |
| **Optimism** | ERC-20 | `0x92f1950d8c80a2d844b321e65e226a694801cc13` | [Optimistic Etherscan](https://optimistic.etherscan.io/token/0x92f1950d8c80a2d844b321e65e226a694801cc13) |
| **Avalanche C-Chain** | ARC-20 | `0x7462617313b26d7b72daed71a852e51588f7f1a7` | [Snowtrace](https://snowtrace.io/token/0x7462617313b26d7b72daed71a852e51588f7f1a7) |
| **Base** | ERC-20 | `0x35d545a52a8dd6abb588292ea6b7b9cb3898b53b` | [Basescan](https://basescan.org/token/0x35d545a52a8dd6abb588292ea6b7b9cb3898b53b) |
| **Solana** | SPL | `J74E2uSud3EH2aAUNLaxMRDyHde7oHDYopGLaim4DZta` | [Solscan](https://solscan.io/token/J74E2uSud3EH2aAUNLaxMRDyHde7oHDYopGLaim4DZta) |
| **Aptos** | Aptos Coin | `0x6917bec3bdfe7423619c1e128f8bebdc62405377aaf32365283e2ec5353fe1f7::coin::T` | [Aptos Explorer](https://explorer.aptoslabs.com/coin/0x6917bec3bdfe7423619c1e128f8bebdc62405377aaf32365283e2ec5353fe1f7::coin::T) |
| **Terra Classic** | CW-20 | `terra1q20zrqn278jm6e4a2z5ygky00h22l4js7wsge74xf4wwyald4r8qsyvyuj` | [Terra Finder](https://finder.terra.money/classic/address/terra1q20zrqn278jm6e4a2z5ygky00h22l4js7wsge74xf4wwyald4r8qsyvyuj) |

---

## Repository Structure & Configuration

* **`config/dex-config.json`** – Machine-readable CloudbitDEX configuration including fee parameters, supported wallet connectors, and verified multichain contract endpoints.
* **`.env.example`** – Environment template for configuring the IONOS PHP backend, CoinMarketCap API proxy, and treasury routing addresses.

---

## Official Cloudbit-Global Repositories
* **[`Cloudbit-Global/core`](https://github.com/Cloudbit-Global/core)** – Core architecture, multichain contract registry, verified ABIs, and brand assets.
* **[`Cloudbit-Global/cdbc-dex`](https://github.com/Cloudbit-Global/cdbc-dex)** – CloudbitDEX decentralized exchange interface and routing engine (`cloudbitex.com`).
* **[`Cloudbit-Global/cdbc-app`](https://github.com/Cloudbit-Global/cdbc-app)** – Official main project portal and ecosystem web builds (`cdbc.io`).
* **[`Cloudbit-Global/cdbc-api`](https://github.com/Cloudbit-Global/cdbc-api)** – Public supply endpoints and OpenAPI specifications (`cdbc-api.vercel.app`).
* **[`Cloudbit-Global/cdbc-bot`](https://github.com/Cloudbit-Global/cdbc-bot)** – Official Telegram GameFi & Tap2Earn Bot (`@cloudbit_ai_bot` / `cloudbit.to`).
---

## Official CloudbitDEX Android App (APK)

* **Download CloudbitDEX Android App (`v2.0.0`):** [CloudbitDEX-v3.0.0.apk](https://github.com/Cloudbit-Global/cdbc-dex/releases/download/v2.0.0/CloudbitDEX-v3.0.0.apk)
