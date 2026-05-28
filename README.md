<div align="center">

<!-- ─────────────────────── HEADER ─────────────────────── -->

<h1>
  <img src="https://api.communalhq.com/assets/images/logo-light.png" alt="Communal" height="60" />
  <br />
  Communal Technologies
</h1>

<p>
  <strong>Modern banking infrastructure for savings &amp; credit cooperatives in Nigeria.</strong>
</p>

<p>
  <a href="https://communalhq.com"><img src="https://img.shields.io/badge/Website-communalhq.com-1B4FCA?style=flat-square&logo=googlechrome&logoColor=white" alt="Website" /></a>
  &nbsp;
  <a href="https://api.communalhq.com/api/docs"><img src="https://img.shields.io/badge/API%20Docs-Swagger-85EA2D?style=flat-square&logo=swagger&logoColor=black" alt="API Docs" /></a>
  &nbsp;
  <a href="mailto:hello@communalhq.com"><img src="https://img.shields.io/badge/Email-hello@communalhq.com-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
  &nbsp;
  <a href="https://twitter.com/communalhq"><img src="https://img.shields.io/badge/Twitter-@communalhq-1DA1F2?style=flat-square&logo=twitter&logoColor=white" alt="Twitter" /></a>
</p>

</div>

---

## About Us

**Communal Technologies Limited** builds the digital operating system for Nigerian savings and credit cooperatives. We replace paper ledgers, WhatsApp spreadsheets, and manual cash-handling with a fully integrated platform that covers everything from member onboarding and KYC compliance to loan disbursement, savings tracking, bill payments, and real-time bank transfers — all powered by regulated banking infrastructure.

Cooperatives of any size can launch on Communal in minutes, offer their members a seamless mobile banking experience, and let administrators run the full back-office from a single dashboard — with no prior technical knowledge required.

---

## What We Build

| Product | Description |
|---|---|
| **Communal Platform API** | Core Laravel monolith — auth, members, loans, obligations, transfers, KYC, bill payments, cooperative admin, super-admin, agent portal |
| **Member Mobile App** | Flutter app for cooperative members: deposits, loan applications, transfers, bill payments, KYC, biometric auth |
| **Cooperative Admin Dashboard** | Next.js web (and desktop) application for cooperative administrators: member management, loans, ledgers, financial reporting |
| **Marketing Website** | React + Vite landing site for communalhq.com |
| **KYC Microservice** | Go service that owns all KYC/KYB workflows and is the sole caller of the Anchor banking KYC API |
| **Notification Service** | Laravel microservice for email and SMS delivery with queue-backed delivery guarantees |
| **SMS Gateway App** | Flutter Android companion app that turns a device into an SMS relay, routing messages through local SIM infrastructure |

---

## Core Platform Features

<details>
<summary><strong>Member Financial Services</strong></summary>
<br />

- **Tiered KYC** — Two-tier identity verification (Tier 1: ₦30k daily / ₦300k wallet cap; Tier 2: ₦200k daily / ₦500k cap) with document encryption at rest
- **Savings & Contributions** — Configurable obligation types (mandatory / voluntary, interest-bearing, loan-eligible, withdrawable, share-based or fixed)
- **Loans** — Full lifecycle: application → guarantor approval → disbursement → amortization schedule → repayment tracking → late-fee fines
- **Bank Transfers** — Wallet-to-bank (NIP / NIPS interbank) and wallet-to-wallet internal transfers with biometric gate and daily limit enforcement
- **Bill Payments** — Airtime, mobile data, electricity (meter validation), and TV subscriptions via Anchor
- **Withdrawal Requests** — Member-initiated dividend and savings withdrawals routed through cooperative admin approval

</details>

<details>
<summary><strong>Cooperative Administration</strong></summary>
<br />

- **Multi-role Admin System** — Granular permission codes per cooperative; counter-signing workflows for high-value actions
- **Member Management** — Bulk CSV upload, individual onboarding, suspend / activate, freeze / unfreeze workflows
- **Loan Scheme Configuration** — Per-cooperative loan products with custom interest rates, tenure, eligibility rules, and guarantor ratios
- **Financial Obligations** — Fully configurable contribution categories with calculation methods, collateral factors, and interest accrual
- **Ledger & Reporting** — Transaction ledger, payment vouchers, statement exports, dividend tracking
- **KYB Verification** — Cooperative business identity verification via Anchor, with document upload and status tracking

</details>

<details>
<summary><strong>Security & Compliance</strong></summary>
<br />

- **Biometric Transaction Signing** — Challenge-response biometric verification for transfers and high-value actions (mobile)
- **2FA** — TOTP, SMS OTP, and email OTP second factors with backup codes
- **Transaction PIN** — Secondary PIN layer for payment operations
- **Session Management** — Per-device session listing and remote revocation
- **Account Freeze** — Admin and self-service freeze with unfreeze request workflow
- **Audit Logging** — Immutable activity log for all user and admin actions
- **Idempotency** — Idempotency-key middleware on all mutation endpoints to prevent double charges on network retries
- **Encrypted KYC Storage** — AES-encrypted sensitive columns for all identity data

</details>

<details>
<summary><strong>Platform & Infrastructure</strong></summary>
<br />

- **Agent Portal** — Field agent registration, cooperative referral tracking, and payout management
- **Subscription Tiers** — Cooperative plan management (member limits, SMS quotas, WhatsApp notifications, staff seats, customization levels)
- **Webhook Processing** — Anchor webhook ingestion with signature verification and idempotency deduplication
- **Event Bus** — RabbitMQ topic exchange for microservice event propagation (`kyc.member.status_update`, `kyc.cooperative.status_update`, notification events)
- **OpenTelemetry** — Distributed tracing across all services
- **JWKS Endpoint** — RS256 JWT verification for Go microservices to validate Passport-issued tokens without a round-trip to the monolith

</details>

---

## Technology Stack

<div align="center">

### Backend & Services
![PHP](https://img.shields.io/badge/PHP%208.2-777BB4?style=flat-square&logo=php&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel%2011-FF2D20?style=flat-square&logo=laravel&logoColor=white)
![Go](https://img.shields.io/badge/Go%201.22-00ADD8?style=flat-square&logo=go&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=flat-square&logo=rabbitmq&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)

### Frontend & Mobile
![Flutter](https://img.shields.io/badge/Flutter%203.x-02569B?style=flat-square&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=flat-square&logo=dart&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)

### Infrastructure & Observability
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-000000?style=flat-square&logo=opentelemetry&logoColor=white)
![OpenAPI](https://img.shields.io/badge/OpenAPI%203.0-6BA539?style=flat-square&logo=openapiinitiative&logoColor=white)

</div>

---

## Architecture Overview

```
┌─────────────────────────────────────────────────────────────────────┐
│                        Client Layer                                  │
│   Flutter Mobile App  ·  Next.js Dashboard  ·  React Website        │
└──────────────────────────────┬──────────────────────────────────────┘
                               │ HTTPS / REST (Passport RS256 JWT)
┌──────────────────────────────▼──────────────────────────────────────┐
│                    Platform API (Laravel 11)                         │
│  Auth · Members · Loans · Obligations · Transfers · Bill Payments   │
│  Cooperative Admin · Super Admin · Agent Portal · Webhooks          │
└────┬──────────────────┬────────────────┬───────────────┬────────────┘
     │ AMQP events      │ HTTP           │ HTTP          │ JWKS
┌────▼──────┐    ┌──────▼──────┐  ┌─────▼──────┐  ┌────▼────────┐
│  KYC svc  │    │Notification │  │   Anchor   │  │  Go / Other │
│  (Go)     │    │  svc (PHP)  │  │  Banking   │  │  Services   │
└───────────┘    └──────┬──────┘  └────────────┘  └─────────────┘
                        │ queues SMS
                 ┌──────▼──────┐
                 │ SMS Gateway │
                 │ (Flutter /  │
                 │  Android)   │
                 └─────────────┘
```

---

## Banking Infrastructure

Communal is powered by **[Anchor](https://getanchor.co)** — Nigeria's banking-as-a-service platform — for regulated financial operations:

| Capability | Provider |
|---|---|
| Member virtual accounts (deposit & electronic) | Anchor |
| KYC / KYB identity verification | Anchor |
| Interbank NIP transfers | Anchor (NIP/NIPS) |
| Airtime, data, electricity, TV bill payments | Anchor |
| Account number verification | Anchor |
| Balance queries | Anchor |

---

## API Documentation

The full REST API is documented with **OpenAPI 3.0** and served via Swagger UI:

- **Staging**: `https://api-staging.communalhq.com/api/docs`
- **Production**: `https://api.communalhq.com/api/docs`

The spec covers 250+ operations across 22 functional tag groups including Authentication, KYC, Transfers, Loans, Bill Payments, Cooperative Admin, Super Admin, Agent, and more.

---

## Repositories

| Repository | Stack | Description |
|---|---|---|
| `backend` | Laravel 11 · PHP 8.2 | Core platform API monolith |
| `dashboard` | Next.js · TypeScript | Cooperative admin web & desktop app |
| `mobile` | Flutter · Dart 3 | Member mobile application (iOS & Android) |
| `website` | React · Vite · TypeScript | Marketing website |
| `kycsvc` | Go 1.22 | KYC/KYB microservice |
| `notificationsvc` | Laravel · PHP | Email & SMS notification microservice |
| `sms_mobile_app` | Flutter · Android | Device-based SMS relay gateway |

---

## Contact & Support

<div align="center">

| | |
|---|---|
| **Product enquiries** | [hello@communalhq.com](mailto:hello@communalhq.com) |
| **Technical support** | [support@communalhq.com](mailto:support@communalhq.com) |
| **Website** | [communalhq.com](https://communalhq.com) |
| **Twitter / X** | [@communalhq](https://twitter.com/communalhq) |

</div>

---

<div align="center">
  <sub>Built with care for Nigerian cooperatives &mdash; &copy; Communal Technologies Limited</sub>
</div>
