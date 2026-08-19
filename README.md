# 🔗 URL Shortener

📌 Note: This is an older project I built while learning backend development. It was created as a hands-on project to understand Node.js, Express.js, MongoDB, Mongoose, routing, and server-side rendering. The backend functionality is complete, while the frontend is still incomplete.

A backend-focused URL Shortener built with **Node.js, Express.js, MongoDB, Mongoose, and EJS**. The application converts long URLs into short, unique links and redirects users to the original URL when the shortened link is accessed.

> 🚧 **Status:** Backend functionality is completed. Frontend/UI improvements are currently in progress.

## ✨ Features

* Generate unique short URLs
* Store URL mappings in MongoDB
* Redirect short URLs to their original destinations
* Dynamic routing using Express.js
* Server-side rendering with EJS
* MongoDB integration using Mongoose

## 🛠️ Tech Stack

* **Runtime:** Node.js
* **Backend:** Express.js
* **Database:** MongoDB Atlas
* **ODM:** Mongoose
* **Templating:** EJS

## 📂 Project Structure

```text
URL-Shortener/
│
├── Controllers/
│   └── url.js
│
├── Models/
│   └── Url.js
│
├── views/
│   └── index.ejs
│
├── .env
├── .gitignore
├── server.js
├── package.json
├── package-lock.json
└── README.md
```

## 🔄 Application Flow

```text
Long URL
   ↓
Express POST /short
   ↓
Generate Short Code
   ↓
Store URL Mapping in MongoDB
   ↓
Return Short URL
   ↓
User Opens Short URL
   ↓
Express GET /:shortCode
   ↓
Find URL in MongoDB
   ↓
Redirect to Original URL
```

## 📌 Routes

| Method | Endpoint      | Description                          |
| ------ | ------------- | ------------------------------------ |
| GET    | `/`           | Renders the URL shortening interface |
| POST   | `/short`      | Generates and stores a shortened URL |
| GET    | `/:shortCode` | Redirects to the original URL        |

## 🧪 Example

### Input

```text
https://www.example.com/very/long/url
```

### Generated URL

```text
http://localhost:1000/AbC123
```

When the shortened URL is opened, the application retrieves the corresponding URL from MongoDB and redirects the user to the original destination.

## 🗄️ Database Structure

The application uses MongoDB to store URL mappings.

```text
shortURLs
│
├── shortCode
└── longUrl
```

Example document:

```json
{
  "shortCode": "AbC123",
  "longUrl": "https://www.example.com"
}
```

## 🚧 Future Improvements

* [ ] Complete frontend UI
* [ ] Add URL validation
* [ ] Improve error handling
* [ ] Add click analytics
* [ ] Add URL expiration
* [ ] Add custom aliases
* [ ] Add user authentication
* [ ] Deploy the application
* [ ] Add automated API testing

## 📚 What I Learned

Through this project, I worked with:

* Express.js routing and middleware
* MVC-style backend structure
* MongoDB and Mongoose
* Dynamic route parameters
* HTTP redirects
* Server-side rendering with EJS
* Environment variable management
* Backend API development

---

## 📌 Project Status

The core backend functionality is complete and functional, including **URL shortening, MongoDB persistence, and redirection**. The frontend and additional features are currently under development.
