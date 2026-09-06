## 6. Organization Domain  
### Entity: Employee  
**Definition:** A person employed by FirstUK Bank.  
**Attributes:**
- `employee_id` — Unique identifier
- `first_name` — Given name
- `last_name` — Family name
- `department_id` — Department (see [[departments]])
- `job_title` — Job title (e.g., "Account Manager")
- `manager_id` — Direct manager (employee_id)
- `start_date` — Employment start date
- `status` — Active, On leave, Terminated
- `clearance_level` — Security clearance level  
**Relationships:**
- `works_in` → Department (1:1)
- `reports_to` → Employee (1:1, optional)
- `manages` → Employee (1:many)
- `performs_kyc_verification` → KYC_Verification (1:many)
- `reviews_sar` → SAR (1:many, optional)  
---