# Maintenance Order (Work Order) 
Maintenance Order
: The Maintenance Order object represents the planning an execution of work including the breakdown into steps, allocation to Work Centres, scheduling and materials, tools and other resources.


## Maintenance Order Concept 
<!--Simplified conceptual Model -->
```mermaid
%%{ init: { 'flowchart': { 'curve': 'linear' } } }%%
flowchart LR
    Noti <--> Order
    Order --> Operations
    Order <--> Location
    Order <--> Work_Center
```

## Maintenance Order (Work Order) 
<!--Data Model -->
```mermaid
erDiagram
    Order ||--|{ Operation : contains
    Operation ||--|{ Materials : requires
    Operation ||--|{ PRTs : requires
    Order ||--|| Work_Center : "belongs to"
    Order ||--|{ Status : "has status"
    Order ||--|| Func_Location : "has location"
    Order ||--|| Settlement_Rule : has
    Order ||--|| Costs : has
    
    Order {
        char12 Order_Number
        char8 Order_Type
        char Material_Activity_Type
        char Priority
        date start-finish
    }
 
    Operation {
        char12 Operation_Number
    }
    
    Status {
        char5 Status
    }
```  
Also related to Materials Reservations, Goods movements (AUFM), Noti, Revision

## Maintenance Order - Data model
<!--Technical Data Model -->
```mermaid
erDiagram
    AUFK ||--|| AFIH : relates
    AUFK ||--|{ AFVC : contains
    AUFK ||--|| AFKO : relates
    AUFK ||--|| AFPO : relates
    AUFK ||--|{ JEST : "has status"
    AUFK ||--|| ILOAN : "has location"
    
    AUFK {
        char12 aufnr PK
        char8 aufart
        numc2 auftyp
        char22 objnr FK
    }
 
    AFIH {
        char12 aufnr
        
    }
    AFVC {
        char12 aufnr
    }
    
    JEST {
        char12 objnr PK
        char5 stat PK
    }
```  

