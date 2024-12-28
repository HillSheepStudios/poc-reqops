# Ideas page - To Be Delete

## Manage Entry Outcome
### Level 1 Diagnostic
```mermaid
graph TB
    s@{ shape: start, label: "start"}
    e@{ shape: stop, label: "end"}
    f1@{ shape: rect, label: "Verify Card"}
    f2@{ shape: rect, label: "Allow Entry"}
    f3@{ shape: rect, label: "Deny Entry"}

    s-->f1
    f1-->|accepted|f2-->e
    f1-->|rejected|f3-->e
```
### Level 2 Diagnostics — Verify Card
```mermaid
graph TB
    s@{ shape: start, label: "start"}
    e1@{ shape: stop, label: "accepted"}
    e2@{ shape: stop, label: "rejected"}
    f1a1@{ shape: rounded, label: "Input card"}
    f1a2@{ shape: rounded, label: "Validate card"}
    
    s-->f1a1-->f1a2
    f1a2-->|accepted|e1
    f1a2-->|rejected|e2
```
### Level 2 Diagnostics — Allow Entry
```mermaid
graph TB
    s@{ shape: start, label: "start"}
    e@{ shape: stop, label: "end"}
    f2a1@{ shape: rounded, label: "Log allowed entry"}
    f2a2@{ shape: rounded, label: "Notify entry allowed"}
    
    s-->f2a1-->f2a2-->e
```
### Level 2 Diagnostics — Deny Entry
```mermaid
graph TB
    s@{ shape: start, label: "Verify Card"}
    e@{ shape: stop, label: "end"}
    f3a1@{ shape: rounded, label: "Log rejected entry"}
    f3a2@{ shape: rounded, label: "Notify entry denied"}
    
    s-->f3a1-->f3a2-->e
```

## Maintain Card Outcome
### Level 1 Diagnostic
```mermaid
graph TB
    s@{ shape: start, label: "start"}
    e@{ shape: stop, label: "end"}
    f4@{ shape: rect, label: "Add Card"}
    f5@{ shape: rect, label: "Update Card"}
    f6@{ shape: rect, label: "Delete Card"}

    s-->f4 & f5 & f6-->e
```
### Level 2 Diagnostics - Add Card
```mermaid
graph TB
    s@{ shape: start, label: "start"}
    e@{ shape: stop, label: "end"}
    f4a1@{ shape: rounded, label: "Generate card"}
    f4a2@{ shape: rounded, label: "Input card details"}
    f4a3@{ shape: rounded, label: "Save new card"}
    
    s-->f4a1-->f4a2-->f4a3-->e
```
### Level 2 Diagnostics - Update Card
```mermaid
graph TB
    s@{ shape: start, label: "start"}
    e@{ shape: stop, label: "end"}
    f5a1@{ shape: rounded, label: "Select card to update"}
    f5a2@{ shape: rounded, label: "Update card details"}
    f5a3@{ shape: rounded, label: "Save updated card"}
    
    s-->f5a1 --> f5a2 --> f5a3-->e
```
### Level 2 Diagnostics - Delete Card
```mermaid
graph TB
    s@{ shape: start, label: "start"}
    e@{ shape: stop, label: "end"}
    f6a1@{ shape: rounded, label: "Select card to delete"}
    f6a2@{ shape: rounded, label: "Delete card"}

    s-->f6a1-->f6a2-->e
```