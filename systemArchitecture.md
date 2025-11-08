**SYSTEM OVERVIEW:**

eNaira Connect is a modular integration layer designed to extend existing banking applications. It allows banks to enable eNaira transactions within their mobile platforms while maintaining compliance with CBN infrastructure.


**ARCHITECTURE LAYERS:**

Frontend (Mobile Banking App Extension)

Developed in React Native

Embeds eNaira dashboard and wallet switch interface

Handles user interactions, transactions, and balance display


**BACKEND (INTEGRATION LAYER):**

Node.js + Express handles API orchestration

Authenticates users via existing bank KYC records

Facilitates conversion requests and transaction logging


**DATABASE LAYER:**

MongoDB stores transaction metadata and user preferences

Sensitive financial data remains with the bank’s secure systems


**EXTERNAL APIs:**
CBN eNaira API: For wallet creation, balance retrieval, transfers, and FX operations

NIBSS API: For settlement, interoperability, and payment processing


**SECURITY & COMPLIANCE**

Implements token-based authentication (JWT)

End-to-end encryption for data in transit

Audit logs for traceability and CBN compliance


**SYSTEM WORKFLOW:**

1. User Accesses Banking App → Logs in via existing credentials.

2. Switch to eNaira Mode → Accesses embedded eNaira wallet dashboard.

3. Backend Layer Authenticates User → Uses KYC data to validate identity.

4. CBN eNaira API Call → Fetches wallet balance and transaction options.

5. User Performs Transactions → Send, receive, or convert naira ↔ eNaira.

6. Confirmation & Sync → Updates both eNaira and bank balances in real time.
   
LINK TO MY EXTENSIVE FLOW CHART: https://docs.google.com/document/d/1l7H8evj54zjY3Ldug8TNFSvjZQDSMyvJvAQc5_vOHtY/edit?usp=sharing


**TECHNICAL FEASIBILITY**

1. Banks already integrate multiple payment rails (e.g., NIBSS, BVN, CBN APIs). Adding eNaira APIs is technically feasible.

2. Using the bank’s verified KYC reduces onboarding friction.

3. Modular microservice architecture ensures scalability across banks.
