### Step 2: Transaction Analysis  
**For Each Disputed/Flagged Transaction:**  
```
Transaction Details:
- Transaction ID: [ID]
- Date/Time: [Exact timestamp]
- Amount: [£Amount]
- Type: [Transfer / Card / Check / Other]
- Merchant/Recipient: [Name, ID]
- Merchant Category: [Retail / Airline / Casino / Other]
- Device Used: [Online / Mobile App / ATM / Branch / Phone]
- IP Address (if digital): [IP]
- Geo-location: [City, Country]

Transaction Legitimacy Assessment:
- Is amount typical for customer? ☐ Yes ☐ No ☐ Unusual
- Is merchant typical for customer? ☐ Yes ☐ No ☐ Unusual
- Is timing consistent with known patterns? ☐ Yes ☐ No
- Is device new/unusual? ☐ Yes ☐ No
- Is geo-location different from normal? ☐ Yes ☐ No ☐ Impossible

Red Flags:
- ☐ Multiple transactions in short time (velocity)
- ☐ Transactions at 3 AM (unusual time)
- ☐ High-risk merchants (casinos, money transfer)
- ☐ Geo-impossibility (2 transactions on opposite sides of world within minutes)
- ☐ Change from habitual pattern (customer never transfers to this recipient)
```  
---