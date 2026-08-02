## Failure Scenario 1

### Issue

Missing Last Name

### Test Data

Salah,,HR

### Result

The provisioning script attempted to create the account and Active Directory generated an error.

### Root Cause

The script did not validate required fields before creating user objects.

### Fix

Added input validation to ensure FirstName and LastName are populated before provisioning.

### Business Impact

Reduced provisioning failures caused by incomplete HR data.
...

## Failure Scenario 2

### Issue

Invalid Department

### Test Data

Ali,Saleh,Accounting

### Result

The script attempted to process a department that did not exist within Active Directory.

### Root Cause

Department values were not validated before account creation.

### Fix

Added a list of approved departments and validation logic.

### Business Impact

Prevents accounts from being provisioned into unauthorized or non-existent organizational structures.
...

## Failure Scenario 3

### Issue:
Duplicate User

### Test:
Ahmed Ali submitted twice.

### Result:
Active Directory rejected account creation.

### Root Cause:
Script did not verify account existence.

### Fix:
Added duplicate user validation using Get-ADUser.

### Business Impact:
Prevented provisioning failures and reduced manual intervention.
...
