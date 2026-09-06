### Entity: Suspicious Activity Report (SAR)  
**Definition:** A report filed with National Crime Agency (NCA) for suspected financial crime.  
**Attributes:**
- `sar_id` — Unique identifier
- `customer_id` — Customer involved
- `filing_date` — Date filed with NCA
- `nca_reference` — NCA assigned reference number
- `activity_type` — Money laundering, Fraud, Sanctions, Other
- `activity_description` — Detailed description of suspicious activity
- `amount_involved` — Money involved (if applicable)
- `evidence` — Supporting evidence summary
- `status` — Filed, Acknowledged, Investigated, Closed
- `internal_reviewer` — Staff member who filed SAR  
**Example Activity Types:**
- Large cash deposit followed by immediate transfer out
- Multiple accounts opened with similar identity
- Transactions with sanctioned country
- Round-tripping (money in and out same day)  
**Key Business Rules:**
- SAR must be filed within 30 days of suspicion
- Customer not informed (reporting confidential)
- Account may be frozen pending investigation
- Failure to file SAR = regulatory breach  
**Relationships:**
- `for_customer` → Customer (1:many)
- `triggered_by_transactions` → Transaction (1:many)
- `based_on_aml_screening` → AML_Screening (0:1)  
---