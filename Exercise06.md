sequenceDiagram
participant User
participant Browser
participant Server

User->>Browser: Write a note and click "Save"
Browser->>Server: POST /new_note_spa (JSON)
Server-->>Browser: HTTP 201 Created
Note right of Browser: JS updates the notes list instantly, no page reload
