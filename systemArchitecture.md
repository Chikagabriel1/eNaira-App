System Overview:

eNaira Connect is a modular integration layer designed to extend existing banking applications. It allows banks to enable eNaira transactions within their mobile platforms while maintaining compliance with CBN infrastructure.


Architecture Layers:

Frontend (Mobile Banking App Extension)

Developed in React Native

Embeds eNaira dashboard and wallet switch interface

Handles user interactions, transactions, and balance display


Backend (Integration Layer)

Node.js + Express handles API orchestration

Authenticates users via existing bank KYC records

Facilitates conversion requests and transaction logging


Database Layer

MongoDB stores transaction metadata and user preferences

Sensitive financial data remains with the bank’s secure systems


External APIs
CBN eNaira API: For wallet creation, balance retrieval, transfers, and FX operations

NIBSS API: For settlement, interoperability, and payment processing


Security & Compliance

Implements token-based authentication (JWT)

End-to-end encryption for data in transit

Audit logs for traceability and CBN compliance


System Workflow

1. User Accesses Banking App → Logs in via existing credentials.

2. Switch to eNaira Mode → Accesses embedded eNaira wallet dashboard.

3. Backend Layer Authenticates User → Uses KYC data to validate identity.

4. CBN eNaira API Call → Fetches wallet balance and transaction options.

5. User Performs Transactions → Send, receive, or convert naira ↔ eNaira.

6. Confirmation & Sync → Updates both eNaira and bank balances in real time.


Technical Feasibility

1. Banks already integrate multiple payment rails (e.g., NIBSS, BVN, CBN APIs). Adding eNaira APIs is technically feasible.

2. Using the bank’s verified KYC reduces onboarding friction.

3. Modular microservice architecture ensures scalability across banks.
