# Functional Location
Use case
Organise by Technology,Spatial etc
<!--Simplified conceptual Model -->
<!--Key objects and relationships to other key objects.  Try to show the ocntext of how this object is used. -->
## Functional Location Concept
```mermaid
%%{ init: { 'flowchart': { 'curve': 'linear' } } }%%
flowchart LR
    Func_Location --> Address
    Func_Location <--> Task_list
    Func_Location --> Object_list
    Func_Location --> Class_&_Characteristics
    
    Parent_Location --hierarchy--> Location --hierarchy--> Child_Location
    Location --> Equipment --hierarchy--> Child_Equipment
    
```

## Functional Location
<!--Data Model -->
<!--Main objects only, only show any important fields -->
```mermaid
erDiagram
    Func_Location ||--|{ Address : "located at"
    Func_Location ||--|| Parent_Child : ""
    Func_Location ||--|{ Status : "has status"
    Func_Location ||--|| Object_List : "has"
    Func_Location ||--|| Task_List : "has"
    Func_Location ||--|| Partners : has 
    
    Func_Location {
        char12 Location_Number
        char8 Location_Type
        char Category
        
    }
    
    Status {
        char5 Status
    }

```  
Also related to Equipment, Order, Noti, Maintenance item, 

## Functional Location - Data model
<!--Technical Data Model -->
<!--Any useful, show fields that are PK, FK, or any others.  May need multiple diagrams for detail-->
```mermaid
erDiagram
    ILOA ||--|| IFLOT : relates
    ILOA ||--|| ADRC : "located at"
    ILOA ||--|{ IHPA : "has partners"
    ILOA ||--|{ JEST : "has status"
    ILOA ||--|| ILOAN : "relates to"
    ILOA ||--|{ AUSP : "has characteristic"
    IFLOT ||--|| TAPL : "has task list"
    IFLOT ||--|| TAPL : "has task list"
    IFLOT ||--|| TPST : "has BoM"
    
    ILOA {
        char12 iloan PK
        char8 categ
        numc2 typ
        char22 objnr FK
    }
     
    JEST {
        char12 objnr PK
        char5 stat PK
    }

```  
Note link to AUSP can be direct or via INOB when "Multiple Objects Allowed"

<!--Describe key tables or special relationships -->
### ILOA Func_Location master data
iloan   103670748
objnr   OR000103670748

### ADRC  Address
