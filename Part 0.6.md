sequenceDiagram
    participant User
    participant Browser
    participant Server

```Mermaid
    User->>Browser: Writes note and clicks Save
    Browser->>Browser: JavaScript prevents page reload
    Browser->>Server: POST /new_note_spa with JSON data {content: "New note", date: ...}
    Server-->>Browser: 201 Created (JSON response)
    Browser->>Browser: Updates note list dynamically (DOM update)```
