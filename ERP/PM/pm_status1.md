# System and User Status
PM_Object can be any of Noti, Order, Operation, Floc, Equi, Maintenance Plan
System status represent the stage in the object life-cycle and determine the behaviour of the object.
User Status can be defined in configuraton, and can be multiple and a defined sequence(state machine).
```mermaid
erDiagram
    PM_Object ||--|{ System_Status : "has status"
    PM_Object ||--|{ User_Status : "has status"
    PM_Object ||--|| Status_Profile : "has status profile"
    System_Status ||--|{ Status_History : "has change documents"
    User_Status ||--|{ Status_History : "has change documents"
    

```
```mermaid
erDiagram
    OBJECT ||--|{ JEST : "has status"
    OBJECT ||--|{ JCDS : "has change documents"
    OBJECT ||--|| JSTO : "has status profile"
    
    OBJECT {
        char12 objnr PK
    }
    JEST ||--|| TJ02 : "has system status"
    JEST ||--|| TJ30 : "has user status"
    JEST {
        char12 aufnr
    }

    JCDS {
        char12 aufnr PK
        char5 stat  PK
        numc3 chgnr PK
    }

    JSTO {
        char12 aufnr FK
        char3 obtyp
        char8 stsma
    }

    TJ30 ||--|| TJ30T : "status text"  
    TJ30 {
        char12 aufnr FK
    }
    TJ30T {
        
    }

    TJ02 ||--|| TJ02T : "status text"
    TJ02 {
        char12 aufnr FK
    }

    TJ02T {
        
    }
```  

### JEST Individual Object Status
Contains list of System and User status records both active and inactive

### JCDS Change Documents for System/User Statuses (Table JEST)
Contains historic list of System and User status changes with user, date, time, TCode, etc.

### JSTO Status object information
Shows the Status Profile for the objnr 

OR000103670748	E0012		1	
OR000103670748	E0051	X	2	
OR000103670748	E0061		1	
OR000103670748	I0001	X	1	
OR000103670748	I0002		1	
OR000103670748	I0016		1	
OR000103670748	I0028		1	
OR000103670748	I0118	X	1	
OR000103670748	I0215		1	
OR000103670748	I0420	X	1	
OR000103670748	I0485		1	

