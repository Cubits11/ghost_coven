---
config:
  layout: fixed
---

flowchart TD
    A["ENTRY: Raw journal input"] --> B["ECHO CREATED: Encrypted object"]

    B --> C{"Whisper Consent?"}
    C -- Yes --> D["WHISPER GENERATED ✨"]
    C -- No --> E["Proceed Without Reflection"]

    D --> F["Seal Echo?"]
    E --> F

    F -- Yes --> G["SEALED STATE 🔒\nResurrectable only via tokens + breath"]
    F -- No --> H["SEASONAL DECAY 🌱 → ❄️"]

    G --> H

    H --> I{"Decay Threshold Passed?"}

    I -- No --> J["Resurrection Attempt?\nRitual Required ⚠️"]
    J -- Approved --> K["RESURRECTION RITUAL 🔥"]
    K --> L["RE-WHISPERED + LOGGED"]
    L --> H

    I -- Yes --> M["FINAL DECAY LOCK"]

    M --> N{"FUNERAL RITUAL ⚰️"}
    N -- Yes --> O["FORGOTTEN ☁️"]
    N -- No --> P["RESURRECTION RITUAL 🔥"]
    P --> Q["RE-WHISPERED + LOGGED"]
    Q --> O

    O --> R{"Legacy Echo Detected? 🌀"}
    R -- Yes --> A
    R -- No --> S["End of Echo"]

    %% Highlight ritual gates
    C:::ritual
    F:::ritual
    I:::ritual
    J:::ritual
    N:::ritual
    R:::ritual

    %% Ritual styling
    classDef ritual fill:#fdf3e7,stroke:#8c7853,stroke-width:2px,font-style:italic
