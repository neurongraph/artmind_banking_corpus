### Entity: Address  
**Definition:** Physical location associated with a customer, account, or branch.  
**Attributes:**
- `address_id` — Unique identifier
- `address_line1` — Street address (primary)
- `address_line2` — Street address (secondary, optional)
- `city` — City/town name
- `postcode` — UK postcode (format: A(1,2)9(1,2)A 9A(2))
- `country` — Country code (ISO 3166-1 alpha-2)
- `address_type` — Registered, Correspondence, Branch
- `effective_date` — When address became active  
**Key Business Rules:**
- UK customers must have a UK address
- Address must be verified (utility bill, council tax, etc.)
- Addresses use UK postcode format  
---