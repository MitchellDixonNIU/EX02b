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
* PET_INFORMATION (**PetID**, PetName, PetType, PetBreed, PetDOB)

PetID | PetName | PetType | PetBreed | PetDOB
----- | ------- | ------- | -------- | ------
1 | King | Dog | Std. Poodle | 27-Feb-14
2 | Teddy | Cat | Cashmier | 1-Feb-13
3 | Fido | Dog | Std. Poodle | 17-Jul-15
4 | AJ | Dog | Collie Mix | 5-May-15
5 | Cedro | Cat | Unkown | 6-Jun-12
6 | Woolley | Cat | Unkown | Unknown
7 | Buster | Dog | Border Collie | 11-Dec-11
8 | Jiddah | Cat | Abyssinian | 1-Jul-08

1. Create a net table for OWNER_INFORMATION, making OwnerPhone the primary key and OwnerLastName, OwnerFirstName and OwnerEmail column heading
* OWNER_INFORMATION (**OwnerPhone**, OwnerLastName, OwnerFirstName)

OwnerPhone | OwnerLastName | OwnerFirstName | OwnerEmail
----- | ------- | ------- | --------
201-823-5467 | Downs | Marsha | Marsha.Downs@somewhere.com
201-735-9812 | James | Richard | Richard.James@somewhere.com
201-823-6578 | Frier | Liz | Liz.Frier@somewhere.com
201-634-7865 | Trent | Miles | Miles.Trent@somewhere.com
201-634-2345 | Evans | Hilary | Hailary.Evans@somewhere.com

1. Create a new table for SERVICE, making Service the primary key and Charge as the column heading.
* SERVICE (**Service**, Charge)

Service | Charge
----- | ------- 
Ear Infection | $65.00
Nail Clip | $27.50
One year shots | $42.50
Skin Infection | $35.00
Laceration Repair | $127.00
Booster Shots | $111.00

1. Establish referential integrity contraints for the foreign keys used.
* Since the three tables have multiple many-to-many relationships, junction tables would have to be created with foreign keys.  With the creation of junction tables, referential integrity would be inforced.
* If the junction table was created, we would use Service, PetID, and OwnerPhone as foreign keys with referential integrity.
