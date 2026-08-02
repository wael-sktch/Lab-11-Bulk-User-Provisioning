# Lab 11 Report

## Executive Summary

Developed an automated onboarding solution for Active Directory using PowerShell.

## Build Phase

Created:

- Employees OU
- Department OUs
- Department Groups
- Provisioning Script

## Validation Phase

Validated:

- User creation
- Group assignment
- OU placement

## Break Phase

### Scenario 1

Missing Last Name

Test:

Salah,,HR

Result:

Provisioning failed.

### Scenario 2

Invalid Department

Test:

Ali,Saleh,Accounting

Result:

Invalid department detected.

### Scenario 3

Duplicate User

Test:

Ahmed,Ali,HR

Result:

Duplicate account error generated.

## Fix Phase

Implemented:

- Input validation
- Department validation
- Duplicate user detection
- Enhanced logging

## Security Considerations

- Least Privilege
- Department-based authorization
- Auditable provisioning process

## Lessons Learned

Identity provisioning requires input validation and error handling to be reliable.
