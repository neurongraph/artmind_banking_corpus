### Risk Scoring  
**Impact Scale (1–5):**  
| Score | Impact | Loss Amount | Examples |
|-------|--------|-------------|----------|
| 1 | Minimal | <£10k | Minor delay, low customer impact |
| 2 | Low | £10k–£50k | Service disruption <1 hour, few customers |
| 3 | Medium | £50k–£250k | System outage 1–4 hours, many customers |
| 4 | High | £250k–£1M | Regulatory breach, significant loss, reputational |
| 5 | Critical | >£1M | Major breach, large loss, license risk |  
**Likelihood Scale (1–5):**  
| Score | Likelihood | Frequency | Examples |
|-------|------------|-----------|----------|
| 1 | Rare | <1 in 10 years | Asteroid impact (theoretically) |
| 2 | Unlikely | 1 in 3–10 years | Major system failure, unexpected event |
| 3 | Possible | 1 per year | Process error, occasional system glitch |
| 4 | Likely | Multiple per year | Fraud detection, customer complaint |
| 5 | Very Likely | Monthly+ | Daily transaction errors, system slowness |  
**Risk Rating Matrix:**  
```
Impact    1    2    3    4    5
Likelihood
5 (VH)    5    10   15   20   25 (Critical)
4 (H)     4    8    12   16   20
3 (M)     3    6    9    12   15 (High)
2 (L)     2    4    6    8    10
1 (R)     1    2    3    4    5
```  
**Risk Categories:**
- **Green (1–5):** Low risk, accept, standard controls
- **Yellow (6–10):** Medium risk, monitor, targeted controls
- **Orange (12–15):** High risk, mitigate, senior oversight
- **Red (16–25):** Critical, urgent action, immediate mitigation