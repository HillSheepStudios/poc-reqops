# Target System Roadmap

## Overview

## Outcomes
### Manage Entry Outcome
```mermaid
graph TB
    s@{ shape: start, label: "start"}
    e@{ shape: stop, label: "end"}
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


### Maintain Card Outcome
```mermaid
graph TB
    s@{ shape: start, label: "start"}
    e@{ shape: stop, label: "end"}
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

## Constraints


## Diagnostic Increment History 
| Version | Date | Increment | Package |
|---------|------|-----------|---------|


