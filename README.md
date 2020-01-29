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
### Step 3: Make all determinants into candidate keys
1. Create a new table for PET_INFORMATION, creating PetID as the primary key and PetName, PetType, PetBreed, and PetDOB column headings.
* PET_INFORMATION (PetID, PetName, PetType, PetBreed, PetDOB)

PetID | PetName | PetType | PetBreed | PetDOB
----- | ------- | ------- | -------- | ------
1 | King | Dog | Std. Poodle | 27-Feb-14
2 | Teddy | Cat | Cashmier | 1-Feb-13
3 | Fido | Dog | Std. Poodle | 17-Jul-15
4 | AJ | Dog | Collie Mix | 5-May-15
5 | Cedro | Cat | Unkown | 6-Jun-12
6 | Woolley | Cat | Unkown | Unknown
7 | Buster | Dog | Border Collie | 11-Dec-11
8 | Jiddah | Car | Abyssinian | 1-Jul-08
