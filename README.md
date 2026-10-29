# Awesome-Payment-Gateway

# Top Payment Gateway Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Payment Orchestration, Self-Hosted Gateways & Multi-Processor Routing*  
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Payment Gateways**. These tools enable businesses to accept payments online and in-person, route transactions across processors, manage subscriptions, and handle settlements—turning payment complexity into a controlled, observable revenue channel.

**Examples** include Shopify Payments, Stripe, Adyen, Authorize.Net, PayPal Braintree, Square, Checkout.com, Worldpay, Chase Payment Solutions, and Fiserv (the category leaders).

**Open-source emphasis**: Payment Gateways are a domain where open-source tooling is **maturing rapidly at the orchestration layer**. The strongest active project is **Hyperswitch** (Juspay), a Rust-based, PCI-compliant payment switch that routes transactions across 120+ processors (Stripe, Adyen, Braintree, Worldpay, Checkout.com) with intelligent routing, revenue recovery, vaulting, and reconciliation—positioned as "Linux for Payments" . For crypto-native payments, **BTCPay Server** provides a fully self-hosted, non-custodial Bitcoin gateway with no processing fees , and **Bitcart** extends this to BTC, LTC, BCH, XMR, ETH, and USDT . **TPT Pay** offers an MIT-licensed, self-hostable Stripe-compatible API with a double-entry ledger, though it remains early-stage . No open-source project matches the full acquiring, settlement, and compliance infrastructure of Stripe or Adyen out of the box—Hyperswitch is the closest orchestration layer, but actual acquiring and fund settlement remain with licensed processors.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Shopify Payments](https://www.shopify.com/payments)**  
  Native payment processing for Shopify merchants; integrates directly with checkout, supports major card networks and local payment methods, and handles fraud prevention and chargebacks.

- **[Stripe](https://stripe.com/)**  
  Developer-first payment infrastructure with comprehensive APIs for payments, subscriptions, invoicing, and payouts; supports 135+ currencies and extensive payment method coverage.

- **[Adyen](https://www.adyen.com/)**  
  Enterprise payment platform with a single API for online, in-person, and mobile payments across 100+ countries; includes risk management and revenue optimization tools.

- **[Authorize.Net](https://www.authorize.net/)**  
  Long-established payment gateway (now part of Visa) for card-present and card-not-present transactions; widely integrated with ecommerce platforms and shopping carts.

- **[PayPal Braintree](https://www.braintreepayments.com/)**  
  Full-stack payment platform supporting cards, PayPal, Venmo, and local payment methods; includes a merchant account, gateway, and recurring billing.

- **[Square](https://squareup.com/)**  
  Integrated payment processing and POS ecosystem with transparent pricing; strong for in-person and omnichannel retail.

- **[Checkout.com](https://www.checkout.com/)**  
  Enterprise payment platform with direct acquiring connections and a focus on high-growth merchants; supports 150+ currencies and local acquiring.

- **[Worldpay](https://www.worldpay.com/)**  
  Global payment processing and acquiring platform (now part of FIS); supports omnichannel payments and extensive local payment method coverage.

- **[Chase Payment Solutions](https://www.chase.com/business/payments)**  
  Payment processing and merchant services from JPMorgan Chase; integrates with Chase banking and offers POS and ecommerce solutions.

- **[Fiserv](https://www.fiserv.com/)**  
  Financial services and payment technology provider with merchant acquiring, POS, and ecommerce payment solutions.

## Open-Source GitHub Projects

### Payment Orchestration & Routing

- **[Hyperswitch (Juspay)](https://github.com/juspay/hyperswitch)**  
  The most comprehensive open-source **payment switch** available (Rust, PCI-compliant); routes transactions across **Stripe, Adyen, Braintree, Worldpay, Checkout.com, CyberSource, and 120+ other processors** with intelligent routing to maximize authorization rates . Modules include **Cost Observability** (audit and optimize payment costs), **Revenue Recovery** (intelligent retry strategies), **Vault** (PCI-compliant card storage with bring-your-own-vault support for VGS/TokenEx), **Reconciliation** (2-way and 3-way automated), and **Alternate Payment Methods** (PayPal, Apple Pay, Google Pay, Klarna) . Docker deployable with a hosted sandbox for exploration. **Positioned as "Linux for Payments"** —the strongest open-source foundation for businesses wanting to own their payment stack without building processor integrations from scratch .

### Self-Hosted Payment APIs (Stripe Alternatives)

- **[TPT Pay](https://github.com/tpt-solutions/tpt-payments)**  
  MIT-licensed, self-hostable **Stripe-compatible payment API** built in Go; features a PostgreSQL **append-only double-entry ledger**, webhook engine with NATS JetStream, card tokenization via HashiCorp Vault, and REST API compatibility with Stripe API v2024-06-20 . The `CardNetworkAdapter` interface abstracts card network access (sandbox adapter for testing; production requires a bank sponsor or direct acquiring adapter) . **Early-stage but architecturally serious**—provides a sovereign alternative to Stripe's API surface, though actual card acquiring and settlement require banking partnerships .

### Crypto-Native Payment Gateways

- **[BTCPay Server](https://github.com/btcpayserver/btcpayserver)**  
  Free, open-source, **self-hosted Bitcoin payment gateway** (non-custodial); accepts Bitcoin on-chain and via Lightning Network with **no processing fees** and no middleman . Features point-of-sale app, crowdfunding app, payment buttons, refunds, and full node wallet integration. Docker deployment recommended. **The standard for self-sovereign Bitcoin payments**—requires a synced Bitcoin node and technical setup .

- **[Bitcart](https://github.com/bitcart/bitcart)**  
  Free, open-source, self-hosted payment processor supporting **BTC, LTC, BCH, XMR, ETH, TRX, USDT, and more**; includes admin panel, ready store, Docker packaging, Python SDK, and BitCCL scripting for checkout flow automation . ~958 GitHub stars with active releases (v0.10.3.0 in March 2026) . **Broader multi-coin support than BTCPay** but similar self-hosted, non-custodial model .

- **[OphirPay](https://github.com/OphirPay/OphirPay)**  
  Open-source payment platform for the **Stellar blockchain**; features batch payments (multi-recipient in one transaction), recurring schedules, payment requests with QR codes, multi-wallet support (Freighter, xBull, Rabet, Albedo, Lobstr, Ledger), multi-asset support (USDC, custom tokens), path payments with slippage protection, multisig approvals, RBAC, on-chain audit log, and DAO governance . **Blockchain-specific**—useful for Stellar ecosystem businesses, not a general payment gateway .

### Additional Strong Open-Source Options

- **Medusa Payment Plugins** — Medusa (headless commerce) has a growing ecosystem of community payment integrations including Adyen, PayU, CyberSource, Paystack, Tpay, and others via npm packages . **Ecommerce-specific**—useful for Medusa-based storefronts needing regional payment methods .
- **Apache Fineract / Mifos X** — Open-source core banking platform with payment processing capabilities, used by 400+ financial institutions serving 20M+ customers . **Core banking engine**—not a payment gateway per se, but provides the account-keeping and ledger infrastructure for financial services .
- **SHKeeper** — Self-hosted cryptocurrency payment processor with CMS integrations; 211 GitHub stars . **Crypto-only**, narrower scope than BTCPay or Bitcart .

**Frameworks for building custom systems**: **Hyperswitch** provides the strongest open-source foundation for multi-processor payment orchestration, routing, and vaulting—the layer most businesses need before acquiring . For **crypto payments**, BTCPay Server or Bitcart provide mature self-hosted gateways . For a **Stripe-compatible self-hosted API**, TPT Pay offers an early-stage but architecturally complete alternative . No open-source project handles actual fund acquiring and settlement—those require licensed banking relationships.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Payment gateways handling card data must comply with **PCI DSS** requirements; self-hosted solutions require careful security hardening, network segmentation, and compliance validation before processing live card payments.
- **Open-source payment gateways are strongest at orchestration, not acquiring**—Hyperswitch provides multi-processor routing and vaulting but requires existing processor accounts . BTCPay and Bitcart handle crypto natively . TPT Pay provides a Stripe-compatible API but requires banking partnerships for card acquiring . No open-source project replaces the licensed acquiring, settlement, and compliance infrastructure of Stripe or Adyen.
- Verify license terms for commercial use; Hyperswitch is open-source (Rust) , TPT Pay uses MIT , BTCPay Server is open-source , and Bitcart is open-source .

---

**Made for payment engineers, fintech architects, ecommerce operators, and finance systems teams.**  
Let's make payment gateways more open, but with clear eyes about the licensed acquiring layer that open-source cannot replace.
