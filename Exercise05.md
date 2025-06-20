sequenceDiagram
participant User
participant Browser
participant Server

User->>Browser: Accesses /spa
Browser->>Server: GET /spa
Server-->>Browser: SPA HTML
Browser->>Server: GET /main.css
Server-->>Browser: CSS file
Browser->>Server: GET /spa.js
Server-->>Browser: JavaScript SPA
Browser->>Server: GET /data.json
Server-->>Browser: List of notes (JSON)
Note right of Browser: JavaScript renders notes, no page reload
