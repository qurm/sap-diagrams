## Work Center
```mermaid
erDiagram
    Work_Center ||--o{ Cost_Center : links 
    Work_Center ||--o{ Qualifications : links 
    Work_Center ||--o{ Positions : links 
    Work_Center ||--o{ People : links 

```
```mermaid
erDiagram
    Work_Center ||--o{ Basic_data : links 
    Work_Center ||--o{ Capacity : has 
    Work_Center ||--o{ Activity_Type : has 

    Work_Center {
        string description
        string category
        string usage
    }
```