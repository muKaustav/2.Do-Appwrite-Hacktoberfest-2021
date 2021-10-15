<h1 align="center">Taskwrite: Appwrite - React Demo 💻</h1>
<p align = center>
    <img alt="Project Logo" src="https://raw.githubusercontent.com/muKaustav/Taskwrite-Appwrite-Hacktoberfest-2021/main/assets/thumbnail_taskwritepsd.jpg" target="_blank" />
</p>
<h2 align='center'>A demo web app built with React JS and Appwrite backend.</h2><br/>

## 📚 | Introduction

- This web app implements a **To-Do** list and allows users to **add, edit & delete** tasks.
- This app demonstrates <i>Authentication and Database Management</i> via <b>Google OAuth using an Appwrite backend and Appwrite Database respectively</b>.
- **Taskwrite** is built with <b>React JS and Appwrite Web</b>.<br>

<br/>

## 🚀 | Usage

- Appwrite Web: <a target='_blank' href='https://appwrite.io/'>Installation</a>, <a target='_blank' href='https://appwrite.io/docs'>Documentation</a> and <a target='_blank' href='https://30days.appwrite.io/'>Resources</a>.
- Clone this repository:<br>

```sh
git clone https://github.com/muKaustav/Taskwrite-Appwrite-Hacktoberfest-2021.git
```

- Install necessary libraries:<br>

```sh
npm install
```

- Enjoy the project! 😉

<br/>

## 📁 | Folder Structure

- Replace the <b>Endpoint and Project ID</b> in <i>src/Appwrite.js</i>.

```js
const sdk = new Appwrite();
sdk
	.setEndpoint("ENDPOINT_URL") // set your own endpoint
	.setProject("PROJECT_ID"); // set your own project id
```

- Replace the redirect and failure routes for Google OAuth in <i>src/Appwrite.js</i>. <i>(<a target='_blank' href='https://dev.to/appwrite/30daysofappwrite-oauth-providers-3jf6'>Article for reference</a>)</i>

```js
sdk.account.createOAuth2Session(
	"google",
	"http://localhost:3000/",
	"http://localhost:3000/login",
	["profile"]
);
```

- Replace the CollectionID in <i>src/Appwrite.js</i>. <i>(<a target='_blank' href='https://dev.to/appwrite/30daysofappwrite-oauth-providers-3jf6'>Article for reference</a>)</i>

```js
sdk.database.createDocument(
	"COLLECTION_ID", // set your own Collection ID after creating it from the Appwrite console
	obj,
	[`user:${user["$id"]}`],
	[`user:${user["$id"]}`]
);
```

<br>

```sh
public
├───index.html
src
├───components
│   ├───Footer
│   │   ├───Footer.jsx
│   │   └───Footer.scss
│   ├───Tasks
│   │   ├───Task.jsx
│   │   └───Task.scss
│   └───Navbar
│       ├───Navbar.jsx
│       └───Navbar.scss
└───Routes
    ├───Application
    │    ├───App.jsx
    │    └───Application.scss
    ├───Login
    │   ├───Login.jsx
    │   └───Login.scss
    └───ProtectedRoute.jsx
```

<br/>

## 📷 | Screenshots

<p align = center>
    <img alt="Project Logo" src="https://raw.githubusercontent.com/muKaustav/Taskwrite-Appwrite-Hacktoberfest-2021/main/assets/googlelogin.png" target="_blank" />
    <img alt="Project Logo" src="https://raw.githubusercontent.com/muKaustav/Taskwrite-Appwrite-Hacktoberfest-2021/main/assets/home.png" target="_blank" />
    <img alt="Project Logo" src="https://raw.githubusercontent.com/muKaustav/Taskwrite-Appwrite-Hacktoberfest-2021/main/assets/editDeleteTask.png" target="_blank" />
</p>

<br/>

## 🍻 | Contributing

Contributions, issues and feature requests are welcome.<br>
Feel free to check [issues page](https://github.com/muKaustav/Taskwrite-Appwrite-Hacktoberfest-2021/issues) if you want to contribute.

<br/>

## 🧑🏽 | Author

**Kaustav Mukhopadhyay**

- Linkedin: [@kaustavmukhopadhyay](https://www.linkedin.com/in/kaustavmukhopadhyay/)
- Github: [@muKaustav](https://github.com/muKaustav)

<br/>

## 🙌 | Show your support

Drop a ⭐️ if this project helped you!

<br/>

## 📝 | License

Copyright © 2021 [Kaustav Mukhopadhyay](https://github.com/muKaustav).<br />
This project is [MIT](./LICENSE) licensed.

---
