# System Vision

## Purpose:


## Manage Entry Outcome
```mermaid
graph TB
    s@{ shape: start, label: "start"}
    e@{ shape: stop, label: "stop"}
    subgraph Verify Card
        f1a1@{ shape: rounded, label: "Input card"}
        f1a2@{ shape: rounded, label: "Validate card"}
        f1a1-->f1a2
    end
    subgraph Allow Entry
        f2a1@{ shape: rounded, label: "Log allowed entry"}
        f2a2@{ shape: rounded, label: "Notify entry allowed"}
        f2a1-->f2a2
    end
    subgraph Deny Entry
        f3a1@{ shape: rounded, label: "Log rejected entry"}
        f3a2@{ shape: rounded, label: "Notify entry denied"}
        f3a1-->f3a2
    end
    
    s-->f1a1
    f1a2-->|accepted|f2a1
    f1a2-->|rejected|f3a1
    f2a2 & f3a2-->e
```
```mermaid
graph TB
    s@{ shape: start, label: "start"}
    e@{ shape: stop, label: "stop"}
    subgraph Verify Card
        f1a1@{ shape: rounded, label: "Input card"}
        f1a2@{ shape: rounded, label: "Validate card"}
        f1a1-->f1a2
    end
    subgraph Allow Entry
        f2a1@{ shape: rounded, label: "Log allowed entry"}
        f2a2@{ shape: rounded, label: "Notify entry allowed"}
        f2a1-->f2a2
    end
    subgraph Deny Entry
        f3a1@{ shape: rounded, label: "Log rejected entry"}
        f3a2@{ shape: rounded, label: "Notify entry denied"}
        f3a1-->f3a2
    end
    
    s-->f1a1
    f1a2-->|accepted|f2a1
    f1a2-->|rejected|f3a1
    f2a2 & f3a2-->e
```

### Level 1 Diagnostic 
```mermaid
graph TB
    s@{ shape: start, label: "start"}
    e@{ shape: stop, label: "stop"}
    f1@{ shape: rect, label: "Verify Card"}
    f2@{ shape: rect, label: "Allow Entry"}
    f3@{ shape: rect, label: "Deny Entry"}

    s-->f1
    f1-->|accepted|f2-->e
    f1-->|rejected|f3-->e
```
### Level 2 Diagnostics—Verify Card
```mermaid
graph TB
    s@{ shape: start, label: "start"}
    f2@{ shape: stop, label: "Allow Entry"}
    f3@{ shape: stop, label: "Deny Entry"}
    f1a1@{ shape: rounded, label: "Input card"}
    f1a2@{ shape: rounded, label: "Validate card"}
    
    s-->f1a1-->f1a2
    f1a2-->|accepted|f2
    f1a2-->|rejected|f3
```
### Level 2 Diagnostics—Allow Entry
```mermaid
graph TB
    f1@{ shape: start, label: "Verify Card"}
    e@{ shape: stop, label: "stop"}
    f2a1@{ shape: rounded, label: "Log allowed entry"}
    f2a2@{ shape: rounded, label: "Notify entry allowed"}
    
    s-->f2a1-->f2a2-->e
```
### Level 2 Diagnostics—Deny Entry
```mermaid
graph TB
    s@{ shape: start, label: "Verify Card"}
    e@{ shape: stop, label: "stop"}
    f3a1@{ shape: rounded, label: "Log rejected entry"}
    f3a2@{ shape: rounded, label: "Notify entry denied"}
    
    s-->f3a1-->f3a2-->e
```

## Maintain Card Outcome
```mermaid
graph TB
    s@{ shape: start, label: "start"}
    e@{ shape: stop, label: "stop"}
    subgraph Add Card
        f4a1@{ shape: rounded, label: "Generate card"}
        f4a2@{ shape: rounded, label: "Input card details"}
        f4a3@{ shape: rounded, label: "Save new card"}
        f4a1-->f4a2-->f4a3
    end
    subgraph Update Card
        f5a1@{ shape: rounded, label: "Select card to update"}
        f5a2@{ shape: rounded, label: "Update card details"}
        f5a3@{ shape: rounded, label: "Save updated card"}
        f5a1-->f5a2-->f5a3
    end
    subgraph Delete Card
        f6a1@{ shape: rounded, label: "Select card to delete"}
        f6a2@{ shape: rounded, label: "Delete card"}
        f6a1-->f6a2
    end
    
    s-->f4a1 & f5a1 & f6a1
    f4a3 & f5a3 & f6a2-->e
```
### Level 1 Diagnostic
```mermaid
graph TB
    s@{ shape: start, label: "start"}
    e@{ shape: stop, label: "stop"}
    f4@{ shape: rect, label: "Add Card"}
    f5@{ shape: rect, label: "Update Card"}
    f6@{ shape: rect, label: "Delete Card"}

    s-->f4 & f5 & f6-->e
```
### Level 2 Diagnostics-Add Card
```mermaid
graph TB
    s@{ shape: start, label: "start"}
    e@{ shape: stop, label: "stop"}
    f4a1@{ shape: rounded, label: "Generate card"}
    f4a2@{ shape: rounded, label: "Input card details"}
    f4a3@{ shape: rounded, label: "Save new card"}
    
    s-->f4a1-->f4a2-->f4a3-->e
```
### Level 2 Diagnostics-Update Card
```mermaid
graph TB
    s@{ shape: start, label: "start"}
    e@{ shape: stop, label: "stop"}
    f5a1@{ shape: rounded, label: "Select card to update"}
    f5a2@{ shape: rounded, label: "Update card details"}
    f5a3@{ shape: rounded, label: "Save updated card"}
    
    s-->f5a1 --> f5a2 --> f5a3-->e
```
### Level 2 Diagnostics-Delete Card
```mermaid
graph TB
    s@{ shape: start, label: "start"}
    e@{ shape: stop, label: "stop"}
    f6a1@{ shape: rounded, label: "Select card to delete"}
    f6a2@{ shape: rounded, label: "Delete card"}
    
    s-->f6a1-->f6a2-->e
```