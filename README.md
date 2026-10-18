# TheSushant Communication API
**A production-ready, multi-tenant email delivery infrastructure.**

[Link to Live Landing Page](https://communication.thesushant.in)
*Note: The core backend infrastructure is proprietary and closed-source. This repository serves as a technical case study and architectural overview.*

---

## 🚀 What is this?
A high-throughput email API designed for developers. Built to handle transactional and bulk email with enterprise-grade deliverability, sandboxing, and analytics. 

## ✨ Key Features
- **Test/Live Environment:** `sk_test_` keys return mock success responses and never touch SMTP. `sk_live_` keys deliver real mail.
- **DKIM/SPF/DMARC Automation:** Generates 2048-bit RSA keypairs per customer domain and verifies DNS propagation automatically.
- **VERP Bounce Tracking:** Unique envelope senders per email for 100% accurate bounce classification (hard/soft/complaint).
- **HMAC-Signed Webhooks:** Reliable event delivery with exponential backoff.
- **Priority Queues:** Tiered delivery (Urgent, Transactional, Normal, Bulk) backed by a custom cron worker.
- **SaaS Dashboard:** Built-in user auth (Turnstile protected), per-domain rate limits, and usage analytics.

## 🏗️ Architecture
- **Core:** PHP 8.4, MariaDB 11.4
- **Delivery:** PHPMailer with custom SMTP connection pooling
- **Auth:** Argon2id, Cloudflare Turnstile
- **Infrastructure:** cPanel / Cloudflare / IMAP Bounce Parsing

## 📸 Screenshots

*(I will add screenshots here)*
