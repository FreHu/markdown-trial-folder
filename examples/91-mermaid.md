# Mermaid

A ` ```mermaid ` block is drawn on GitHub, GitLab, Azure DevOps, Obsidian, Notion and most documentation sites. The first word says which diagram.

## Flowchart

```mermaid
flowchart LR
    A[Order placed] --> B{Paid?}
    B -- yes --> C[Pick]
    B -- no --> D[Remind customer]
    D --> B
    C --> E[(Warehouse DB)]
    C --> F([Ship])
```

## Sequence

```mermaid
sequenceDiagram
    actor Customer
    participant Shop
    participant Payments
    Customer->>Shop: Place order
    Shop->>Payments: Charge card
    Payments-->>Shop: Captured
    Shop-->>Customer: Confirmation email
    Note over Shop,Payments: Retries three times on a timeout
```

## Class

```mermaid
classDiagram
    class Order {
        +String number
        +Decimal total
        +ship()
    }
    class Line {
        +String sku
        +int quantity
    }
    Order "1" *-- "many" Line
```

## State

```mermaid
stateDiagram-v2
    [*] --> Pending
    Pending --> Paid
    Paid --> Shipped
    Shipped --> Delivered
    Pending --> Cancelled
    Delivered --> [*]
```

## Entity relationship

```mermaid
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE : contains
    PRODUCT ||--o{ LINE : "is in"
```

## Gantt

```mermaid
gantt
    title Stocktake
    dateFormat YYYY-MM-DD
    section Zone A
    Count      :a1, 2026-11-02, 2d
    Recount    :after a1, 1d
    section Zone C
    Count      :2026-11-05, 3d
```

## Pie

```mermaid
pie title Orders by channel
    "Web" : 612
    "Phone" : 140
    "Marketplace" : 248
```

## Git graph

```mermaid
gitGraph
    commit
    branch feature
    commit
    commit
    checkout main
    merge feature
    commit
```

## Mind map

```mermaid
mindmap
  root((Warehouse))
    Receiving
      Count
      Book in
    Storage
      Zones
    Shipping
```

## Timeline

```mermaid
timeline
    title Warehouse moves
    2024 : Lease signed
    2025 : Zone C added
    2026 : Scanners replaced
```

## Chart

```mermaid
xychart-beta
    title "Orders per month"
    x-axis [Jul, Aug, Sep, Oct, Nov]
    y-axis "Orders" 0 --> 1200
    bar [740, 810, 905, 1010, 980]
    line [740, 810, 905, 1010, 980]
```

## Quadrant

```mermaid
quadrantChart
    title Suppliers
    x-axis Slow --> Fast
    y-axis Expensive --> Cheap
    Northwind: [0.8, 0.3]
    Contoso: [0.4, 0.7]
    Fabrikam: [0.2, 0.2]
```

## User journey

```mermaid
journey
    title Returning a parcel
    section Online
      Find the returns page: 3: Customer
      Print the label: 2: Customer
    section At the post office
      Drop it off: 5: Customer
```
