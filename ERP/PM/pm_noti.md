# Maintenance Notification (Noti) 
Maintenance Notification
: The Notification object represents a requirement for maintenance, as a description of defect or malfunction, and optionally related *Activities* or *Tasks*.  Typically it is related to a *Technical Object*, and is coded against Part, Damage, Cause codes for analysis purposes.

It can be used with an *Order*, or as a standalone object for simpler types of work.


## Maintenance Noti Concept 
<!--Simplified conceptual Model -->
```mermaid
%%{ init: { 'flowchart': { 'curve': 'linear' } } }%%
flowchart LR
    Noti -.-> FLoc/Equipment
    subgraph Notification
        Noti --> Items
        Noti --> Activities
        Noti --> Tasks
    end
    Noti -.-> Order
```
## Maintenance Noti Catalog
<!--Data Model -->
```mermaid
erDiagram
    Catalog ||--|{ Code_Group : contains
    Code_Group ||--|{ Code : "contains"

    Damage_Catalog||--|{ Sensor_Damage : contains
    Damage_Catalog||--|{ Compressor_Damage : contains
    Sensor_Damage ||--|{ Temperature : "contains"
    Sensor_Damage ||--|{ Humidity : "contains"
    Sensor_Damage ||--|{ Pressure : "contains"
```  
## Maintenance Noti
<!--Data Model -->
TODO
```mermaid
erDiagram
    Noti ||--|{ Item : contains
    Noti ||--|| Func_Location : "reference object"
    Noti ||--|| Work_Center : "belongs to"
    Noti ||--|{ Status : "has status"
    Noti ||--|{ Activities : has
    Noti ||--|{ Tasks : has 
    Item ||--|{ CodeA : has 
    Item ||--|{ CodeB : has 
    Noti {
        char12 Noti_Number
        char8 Noti_Type
        char Priority
    }
 
    Item {
        char12 Item_Number
    }
    
    Status {
        char5 Status
    }

```  
Also related to ..


