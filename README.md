# EASY PAY 💳 — Payment Notify Bot

*Part of the EASY CODE collection — Apps Made Easy ✨*

**Live page:** https://mido9980.github.io/easy-pay/

A tiny Arabic page for the EASY CODE owner's clients: before transferring money, the client fills in name, phone, amount and purpose — and the owner instantly gets a WhatsApp notification with the details, so no payment ever goes unnoticed (and nothing gets delivered before the money actually lands).

## How it works
1. Client opens the page, enters name + phone + amount + purpose.
2. A record is created in the backend (Base44 entity `PaymentRequest`).
3. An entity-triggered workflow pings the owner's AI agent, which sends him a WhatsApp notification within seconds.
4. The page also shows the owner's wallet number with a copy button, so the client can transfer right away.

## Tech
- Single-file frontend (`index.html`), Arabic RTL.
- Backend function `payPublic` (Base44 Deno) — notify + config + client status check.
- Entities: `PaymentRequest`, `PayBotConfig`.
- Workflow: entity trigger on `PaymentRequest` create → superagent step → WhatsApp alert.

## Edit on your phone with SPCK
1. SPCK Editor → clone: `https://github.com/Mido9980/easy-pay.git`
2. Credentials: GitHub username + Personal Access Token as password.
3. Edit `index.html`, push from SPCK — GitHub Pages updates automatically.

---
© EASY CODE — Apps Made Easy
