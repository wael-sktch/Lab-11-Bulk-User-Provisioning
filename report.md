# Lab 11 Technical Report

## Executive Summary

This project implemented an automated identity provisioning solution for Active Directory using PowerShell.

The solution imports employee data from a CSV file and automatically creates user accounts, assigns users to departmental groups, and records provisioning actions.

---

## Business Problem

Manual user creation is time-consuming, error-prone, and difficult to audit.

A repeatable provisioning process was required to support scalable user onboarding.

---

## Environment

- Windows Server 2022
- Active Directory Domain Services
- PowerShell 5.1
- Atlas.local

---

## Build Phase

Created:

- Employees OU
- HR OU
- Finance OU
- IT OU
- Marketing OU
- Sales OU

Created Security Groups:

- GG_HR
- GG_FINANCE
- GG_IT
- GG_MARKETING
- GG_SALES

Created:

- employees.csv
- New-WGEUsers.ps1

---

## Validation Phase

Validated:

- User account creation
- Correct OU placement
- Correct security group assignment
- Provisioning log generation

---

## Break Phase

### Scenario 1 - Missing Last Name

Test:

```csv
Salah,,HR
```

Result:

User creation failed.

Issue:

No input validation existed.

---

### Scenario 2 - Invalid Department

Test:

```csv
Ali,Saleh,Accounting
```

Result:

Invalid organizational placement attempt.

Issue:

Department validation was missing.

---

### Scenario 3 - Duplicate User

Test:

```csv
Ahmed,Ali,HR
```

Result:

Active Directory rejected duplicate account creation.

Issue:

Duplicate user detection was not implemented.

---

## Fix Phase

Implemented:

- Required field validation
- Department validation
- Duplicate user detection
- Enhanced logging
- Error handling

---

## Security Considerations

- Least Privilege
- Department-Based Access Control
- Auditable Provisioning
- Standardized Account Creation

---

## Lessons Learned

Identity provisioning must include validation and error handling to ensure reliable onboarding workflows.

---

## Future Improvements

- Password generation
- Home folder creation
- Email notifications
- Approval workflows
