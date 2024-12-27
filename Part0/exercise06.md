```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa Body: {content: "string", date:"time"}
    Note right of browser: Update DOM to add new note
    activate server
    server->>server: Save note
    server-->>browser: HTTP 201 Created
    deactivate server
    
```