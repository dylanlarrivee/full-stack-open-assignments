# Part 0 

## Exercises 0.1.-0.6.

### 0.1: HTML
Html tutorial has been read.

## 0.2: CSS
CSS tutorial has been read.

## 0.3: HTML forms
Forms tutorial has been read.

## 0.4: new note
Diagram of a user creating a new note on the page: https://fullstack-exampleapp.herokuapp.com/notes 

The user enters a new note and clicks save on the web page in the browser.

browser --> server: HTTP POST https://fullstack-exampleapp.herokuapp.com/new_note ⋅⋅
server --> browser: HTTP response status code 302. URL redirect. Browser reloads the page⋅⋅
browser --> server: HTTP GET https://fullstack-exampleapp.herokuapp.com/notes⋅⋅
server --> browser: Sends HTML code⋅⋅
browser --> server: HTTP GET https://fullstack-exampleapp.herokuapp.com/main.css⋅⋅
server --> browser: main.css⋅⋅
browser --> server: HTTP GET https://fullstack-exampleapp.herokuapp.com/main.js⋅⋅
server --> browser: main.js⋅⋅

The browser starts to execute the js code that requests JSON data from the server.

browser --> server: HTTP GET https://fullstack-exampleapp.herokuapp.com/data.json
server --> browser: sends JSON data

The browser executes the event handler that renders notes (including new note created) on the page.

## 0.5: Single page app
Diagram of the situation where the user goes to the single page app version of the notes app.

browser --> server: HTTP GET https://fullstack-exampleapp.herokuapp.com/spa
server --> browser: Sends HTML code
browser --> server: HTTP GET https://fullstack-exampleapp.herokuapp.com/main.css
server --> browser: main.css
browser --> server: HTTP GET https://fullstack-exampleapp.herokuapp.com/spa.js
server --> browser: spa.js

The browser starts to execute the js code that requests JSON data from the server.

browser --> server: HTTP GET https://fullstack-exampleapp.herokuapp.com/data.json
server --> browser: sends JSON data

The browser executes the event handler that renders the notes on the page.

## 0.6: New note
Diagram of the situation where a user creates a new note using the single page version of the app.

User enters new note and clicks save on the page in the browser.

The browser executes the event handler code on the form submit event. The event handler creates a new note (note content and date json data), adds it to the notes list, renders the note list on the page and sends the new note to the server with the following action:

browser --> server: HTTP POST https://fullstack-exampleapp.herokuapp.com/new_note_spa