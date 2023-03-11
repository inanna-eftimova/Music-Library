# Music Library

## Overview
**Music Library** is a front-end app (**SPA**) for **creating** and **managing** music albums. The **application** allows **visitors** to **browse** through the **albums catalog**. **Users** may **register** with an **email** and **password** which allows them to **create** their **own album card**. **Album authors** can also **edit** or **delete** their own **publications** at any time.

<kbd>![Music Library](https://user-images.githubusercontent.com/88777360/224483919-5325aa12-cf47-4609-87a1-a0bb55c3939b.png)</kbd>

## Music Library Web App

??Live demo in Replit: [Music Library](https://eventures-web-app.softuniorg.repl.co)

The **SPA** "**Music Library**" is an app for creating **catalog** of **albums**.
* Technologies: JavaScipt, HTML, CSS, Node.js, Express.js, Mocha, Chai
* The app supports the following operations:
 - Home page: `/home`
 - Login page: `/login`
 - Register page: `/register`
 - Dashboard page: `/dashboard`
 - Add Album (Singer/Band + Album + Image URL + Release date + Label + Sales): `/create`
 - Album Details: `/details/:id`
 - Edit Album: (Singer/Band + Album + Image URL + Release date + Label + Sales): `/edit/:id`
 - Delete Album: `/delete/:id`


## Music Library RESTful API

??Live demo in Replit: [Music Library Web API](https://eventures-web-api.softuniorg.repl.co)

The following endpoints are supported:
 - `GET /api` - list all API endpoints 
 - `GET /api/events` - list all events
 - `GET /api/events/count` - returns events count
 - `GET /api/events/:id` - returns an event by given `id` 
 - `POST /api/events/create` - create a new event (post a JSON object in the request body, e.g. `{ "name": "Open Fest", place": "Borisova Garden", start": "2022-08-14T10:00:00.000Z", "end": "2022-08-15T18:00:00.000Z", "totalTickets": 500, "pricePerTicket": 15 }`)
 - `PUT /api/events/:id` - edit event by `id` (send a JSON object in the request body, holding all fields, e.g. `{ "name": "Open Fest", place": "Borisova Garden", start": "2022-08-14T10:00:00.000Z", "end": "2022-08-15T18:00:00.000Z", "totalTickets": 500, "pricePerTicket": 15 }`)
 - `PATCH /api/events/:id` - partially edit event by `id` (send a JSON object in the request body, holding the fields to modify, e.g. `{ place": "South Park Sofia", "pricePerTicket": 12 }`)
 - `DELETE /api/events/:id` - delete event by `id`
 - `GET /api/users` - list all users
 - `POST /api/users/login` - logs in an existing user (send a JSON object in the request body, holding all fields, e.g. `{"username": "username", "password": "pass123"}`)
 - `POST /api/users/register` - registers a new user (send a JSON object in the request body, holding all fields, e.g. `{"username": "username", "email": "user@example.com", "password": "pass123", "confirmPassword": "pass123", "firstName": "Test", "lastName": "User"}`)


## Pages and permissions

### All users 🔓

📌 Home \
📌 Dashboard \
📌 Details \
📌 Login \
📌 Register 

### Authenticated users 🔐

📌 Dashboard\
📌 Create \
📌 Details \
📌 Edit (only if user is owner) \
📌 Delete (only if user is owner) 

## Technology stack

🛠 Angular 13 (version 13.2.5) \
🛠 Firebase \
🛠 HTML, CSS \
🛠 Toastr \
🛠 Bootstrap \
🛠 Angular Animations 

## Application starting

📌 First you must install all dependencies included in the package.json file by typing npm install in a terminal.
Then you must serve the angular application by typing ng serve in a terminal.
After that Books Place could be accessed on http://localhost:4200 url.

## Screenshots

Screenshots from the **Music Library SPA**.


### Music Library Web App

<kbd>![image](https://user-images.githubusercontent.com/88777360/224485979-4fa7fe7f-e940-4ed3-a078-aff2ad6b347d.png)</kbd>

<kbd>![image](https://user-images.githubusercontent.com/88777360/224486045-7efa21ab-7147-4e33-a54d-dad7a790857f.png)</kbd>

<kbd>![image](https://user-images.githubusercontent.com/88777360/224486061-53efa1ab-977c-45ac-81aa-d2abe76c90e7.png)</kbd>

<kbd>![image](https://user-images.githubusercontent.com/88777360/224486076-1b0c2c3d-f284-41cd-b43c-21e9af59f685.png)</kbd>

<kbd>![image](https://user-images.githubusercontent.com/88777360/224486087-524a47d9-fe46-4d90-8c59-c25eda7a52f2.png)</kbd>

<kbd>![image](https://user-images.githubusercontent.com/88777360/224486116-5827ddfa-77cf-44e4-b3c1-ec390d5eba4a.png)</kbd>

<kbd>![image](https://user-images.githubusercontent.com/88777360/224486143-fa7dec61-1786-4c73-900e-2bf6143e3b5c.png)</kbd>

<kbd>![image](https://user-images.githubusercontent.com/88777360/224485954-f29c6ba0-6ad1-4f94-bed3-5ad0c8f6cb1b.png)</kbd>

<kbd>![image](https://user-images.githubusercontent.com/88777360/224486174-39100fa4-6fb8-4406-884b-f58f18569135.png)</kbd>

<kbd>![image](https://user-images.githubusercontent.com/88777360/224486208-5296cf09-e097-4e8b-9681-48f59d6792f5.png)</kbd>

### Eventures RESTful API

<kbd>![image](https://user-images.githubusercontent.com/69080997/136526348-4a3c00d9-b4b0-40f8-81f9-9904785c0172.png)</kbd>
<kbd>![image](https://user-images.githubusercontent.com/69080997/136526560-721e6f6a-b3d4-4f1e-9646-2e2052c4912b.png)</kbd>
<kbd>![image](https://user-images.githubusercontent.com/69080997/136526724-01b3a68f-2909-4c4b-8799-97e6f19b6d87.png)</kbd>
