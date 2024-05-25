<!-- Create a diagram depicting the situation where the user creates a new note using the single-page version of the app. -->

```mermaid

sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
        Note left of server: fetches the form element from the page, prevents default handling of form's sumbit and sends note to the server.
    server-->>browser: The server responds with status code 201 created
    deactivate server
