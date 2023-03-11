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


### Pages and permissions

#### All users 🔓

📌 Home \
📌 Dashboard \
📌 Details \
📌 Login \
📌 Register 

#### Authenticated users 🔐

📌 Dashboard\
📌 Create \
📌 Details \
📌 Edit (only if user is owner) \
📌 Delete (only if user is owner) 


### How to start the application?

📌 First you must **install all dependencies** included in the **package.json** file by typing `npm install` in a **terminal**.
Then you must **serve** the app by typing `ng serve` in a **terminal**.
After that Music Library could be accessed on http://localhost:3000 URL.

<kbd>![image](https://user-images.githubusercontent.com/88777360/224491675-23012c21-eaf9-481a-ac48-66c5753a3a61.png)</kbd>

<kbd>![image](https://user-images.githubusercontent.com/88777360/224491696-ca268151-1076-45ea-a14f-926f1cffd4fd.png)</kbd>

### Executing the Tests

Before running the test suite, make sure a web server is operational, and the application can be found at the root of its network address. To start the included dev-server, open a terminal in the folder containing package.json and execute: `npm run start`

This is a one-time operation unless you terminate the server at any point. It can be restarted with the same command as above.
To execute the tests, open a new terminal (do not close the terminal, running the web server instance) in the folder containing package.json and execute:
`npm run test`

Test results will be displayed in the terminal, along with detailed information about encountered problems. You can perform this operation as many times as it is necessary by re-running the above command.

## Music Library RESTful API

??Live demo in Replit: [Music Library Web API](https://eventures-web-api.softuniorg.repl.co)

The following endpoints are supported:
 - `GET /data/albums?sortBy=_createdOn%20desc` - list all albums
 - `GET /data/albums/:id` - returns an album by given `id` 
 - `POST /data/albums` - create a new album (post a JSON object in the request body, e.g. `{ "singer": "Taylor Swift", album": "Midnights", imageUrl": "https://upload.wikimedia.org/wikipedia/en/9/9f/Midnights_-_Taylor_Swift.png", "release": "October 21, 2022", "label": "Republic", "sales": "1.58 million copies" }`)
 - `PUT /data/albums/:id` - edit album by `id` (send a JSON object in the request body, holding all fields, e.g. `{ "singer": "Taylor Swift", album": "Midnights", imageUrl": "https://upload.wikimedia.org/wikipedia/en/9/9f/Midnights_-_Taylor_Swift.png", "release": "October 21, 2022", "label": "Republic", "sales": "1.58 million copies" }`)
 - `DELETE /data/albums/:id` - delete album by `id`
 - `POST /users/login` - logs in an existing user (send a JSON object in the request body, holding all fields, e.g. `{"username": "username", "password": "pass123"}`)
 - `POST /users/register` - registers a new user (send a JSON object in the request body, holding all fields, e.g. `{"email": "user@example.com", "password": "pass123"}`)
 - `GET /users/logout` - logs out and existing user
 - `POST /data/likes` - add a like into album. The service expects a body with the following shape: `{albumId}`
 - `GET /data/likes?where=albumId%3D%22{**albumId**}%22&distinct=_ownerId&count` - get total likes count for an album
 - `GET :/data/likes?where=albumId%3D%22{**albumId**}%22%20and%20_ownerId%3D%22{**userId**}%22&count` - get the number of the likes for an album for specific user. {**albumId**} is the **id** of the desired album and {**userId**} is the **id** of the **currently logged-in user**.

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
