# Lab 11 - Bulk User Provisioning

## Overview

This project demonstrates automated Active Directory user provisioning using PowerShell and CSV-based employee data.

The solution automates user creation, department assignment, group membership assignment, and provisioning logging while implementing validation and error handling.

---

## Objectives

- Automate Active Directory user creation
- Standardize account provisioning
- Reduce manual administrative effort
- Improve consistency and auditability

---

## Technologies Used

- Windows Server 2022
- Active Directory Domain Services (AD DS)
- PowerShell
- CSV Data Sources

---

## Architecture

```text
employees.csv
        ↓
PowerShell Script
        ↓
Active Directory
        ↓
Department Groups
        ↓
Provisioning Logs
```

---

## Features

### Version 1

- CSV-based user creation
- Department assignment
- Security group assignment

### Version 2

- Input validation
- Duplicate account detection
- Department validation
- Enhanced logging
- Error handling

---

## Skills Demonstrated

- Identity Provisioning
- Active Directory Administration
- PowerShell Automation
- Troubleshooting
- IAM Fundamentals

---

## Project Files

| File | Purpose |
|--------|---------|
| employees.csv | Employee data source |
| New-WGEUsers.ps1 | Initial provisioning script |
| New-WGEUsers-v2.ps1 | Improved provisioning script |
| report.md | Technical report |
