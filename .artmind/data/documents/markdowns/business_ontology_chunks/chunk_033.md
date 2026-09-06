## Example: Complete Entity Instance  
**Customer:** John Smith
**Opening New Account:** SmartSaver with Joint Holder  
```
PARTY:
party_id: PARTY-00100
party_type: Natural Person

CUSTOMER:
customer_id: CUST-00050
first_name: John
last_name: Smith
date_of_birth: 1980-05-20
nationality: UK
email: john.smith@email.com
customer_status: Active

ADDRESS:
address_id: ADDR-00150
street: 42 Acacia Avenue
city: Manchester
postcode: M1 1AA
address_type: Registered

IDENTIFICATION_DOCUMENT:
doc_id: ID-00200
doc_type: UK Driving License
doc_number: SMITH802056M99AB
expiry_date: 2032-05-20
verification_status: Verified

KYC_VERIFICATION:
kyc_id: KYC-00250
customer_id: CUST-00050
identity_verified: TRUE
address_verified: TRUE
pep_screened: TRUE
verification_status: Verified

AML_SCREENING:
screening_id: AML-00300
customer_id: CUST-00050
matches_found: 0
risk_level: Low
screening_status: Passed

ACCOUNT:
account_id: ACC-00500
product_id: SAV-001 (SmartSaver Account)
opening_date: 2026-01-15
account_status: Active
account_balance: 0 (new account)

ACCOUNT_HOLDER (Primary):
holder_id: AHLD-00600
account_id: ACC-00500
customer_id: CUST-00050
holder_type: Primary

ACCOUNT_HOLDER (Joint):
holder_id: AHLD-00601
account_id: ACC-00500
customer_id: CUST-00051 (Jane Smith)
holder_type: Joint

TRANSACTION (First transaction: opening deposit):
transaction_id: TXN-00700
account_id: ACC-00500
transaction_type: Deposit
amount: 500000 (£5,000.00)
transaction_date: 2026-01-15
status: Completed
description: Opening deposit

CARD:
card_id: CARD-00800
account_id: ACC-00500
customer_id: CUST-00050
card_type: Debit
card_status: Active
daily_limit: 500000 (£5,000)
```  
---