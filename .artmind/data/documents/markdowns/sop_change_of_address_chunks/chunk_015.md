### Validation Checks  
**UK Address Validation:**
- [ ] Postcode format correct (AA9A 9AA)
- [ ] Postcode matches city/town (use Royal Mail lookup)
- [ ] Address not on blacklist (fraudulent addresses)
- [ ] Property number/name is valid  
**International Address Validation:**
- [ ] Country is real and recognized
- [ ] Postal code format correct for country
- [ ] Address not in sanctions country (see Step 5: AML)
- [ ] Address format matches country requirements  
**Escalation If Validation Fails:**
- Don't accept invalid address
- Ask customer to re-confirm
- Provide postal code lookup tool
- Escalate if customer insists on non-standard address