```mermaid
sequenceDiagram
participant User
participant Browser
participant Server

User->>Browser: Write a note and click on "Save" button.
Browser->>Server: Post /new_note with note information.
Server->>Browser: HTTP 302 Redirect to /notes
Browser->>Server: Get /notes
Server->>Browser: HTML notes page
Browser->>Server: GET /main.css
Server-->>Browser: CSS file
Browser->>Server: GET /main.js
Server-->>Browser: JavaScript file
Browser->>Server: GET /data.json
Server-->>Browser: list notes (JSON)
Note right of Browser: Browser update the list and show all notes.
