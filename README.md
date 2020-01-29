# EX02b
## Normalizing the vet table (Adam Rivas and Mitchell Dixon)

### Step 1: Identify candidate keys
1. OwnerPhone
1. OwnerEmail
1. Service
### Step 2: identify functional dependencies
1. OwnerPhone -> (OwnerLastName, OwnerFirstName, OwnerEmail)
1. OwnerEmail -> (OwnerLastName, OwnerFirstName, OwnerPhone)
1. Service -> (Charge)
