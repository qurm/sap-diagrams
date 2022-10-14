# Maintenance Process - Standard 
Standard Process
: Uses Notis linked to Maintenance Orders and can be used for many purposes, including reactive/breakdowns, or proactive/planned work.


## Process Flow 
<!--Simplified process flow -->
```mermaid
%%{ init: { 'flowchart': { 'curve': 'linear' } } }%%
flowchart LR
    Noti --> Order --> Schedule --> R[Check & Release] -->E[Execute] -->Confirm-->Complete
```

## User Journey
<!--Simplified process flow -->
```mermaid
journey
    title Standard Noti-Order 
    section Maintenance Requirement 
      Create Noti: 5: User, Planner
    section Plan Order
      Identify Work: 3: Planner
      Resources: 3: Planner
      Materials: 3: Planner
    section Check Release Order
        Check Material: 1: Planner
        Schedule resources: 1 Planner
    section Execute
      Execute Order: 5: Technician
      Confirm Order: 5: Technician, Planner
    section Complete
      Technical Completion: 5: Planner
      Business Completion: 5: Supervisor, Controller
```

