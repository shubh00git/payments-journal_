# MNC Payments Domain Journal

A dedicated tracking log for core concepts, system architectures, and daily milestones in the payment domain.

---

## 📌 Domain Overview

- **Focus Rails:** Card Processing (Visa/Mastercard), Real-Time Payments (UPI, FedNow/SEPA)
- **Tech Stack & Resilience:** Idempotent APIs, Webhooks, Reconciliation, PCI-DSS

---

## 📅 Daily Milestones & Log

### Day 1: The Core Card Transaction Lifecycle
- **Authorization:** Merchant validates if the cardholder has sufficient funds and captures a temporary hold.
- **Capture:** Merchant confirms the sale after fulfillment to convert the hold into an actual charge.
- **Clearing:** Batched exchange of transaction data via card networks at the end of the business day.
- **Settlement:** The actual movement of money from Issuer Bank $\rightarrow$ Acquirer Bank $\rightarrow$ Merchant.

### Day 2: Ecosystem Participants
- **Customer / Cardholder:** The party initiating the transaction.
- **Merchant:** The business receiving the payment.
- **Payment Gateway:** Captures and encrypts payment credentials on the checkout page.
- **Acquirer / Acquiring Bank:** Merchant's bank processing the authorization request.
- **Payment Scheme / Network:** Visa, Mastercard, RuPay, Amex routing network.
- **Issuer / Issuing Bank:** Cardholder's bank holding account funds and authorizing/declining.

---

## 🔒 Next Topics on the Roadmap
- [ ] ISO 8583 and ISO 20022 message standards
- [ ] Chargeback and refund flows
- [ ] Idempotency keys in payment gateway APIs
- [ ] Tokenization and PCI-DSS compliance scope
