# 🔗 URL Shortener

A simple URL shortener built using **Node.js, Express, and MongoDB**. This project allows users to convert long URLs into short, shareable links and track visit history.

---

## 🚀 Features

* Generate short URLs
* Redirect to original URLs
* Store visit history
* REST API-based architecture
* MongoDB for persistence

---

## 🛠️ Tech Stack

* **Backend:** Node.js, Express
* **Database:** MongoDB (Mongoose)
* **ID Generator:** shortid
* **API Testing:** Postman 

---

## 📁 Project Structure

```
url-shortener/
│
├── models/
│   └── url.js
│
├── controllers/
│   └── url.js
│
├── routes/
│   └── url.js
│
├── connect.js
├── index.js
├── package.json
└── README.md
```

---

## ⚙️ Installation

### 1. Clone the repository

```
git clone https://github.com/Pravin-Rajpurohit/url-shortener.git
cd url-shortener
```

### 2. Install dependencies

```
npm install
```

### 3. Start MongoDB

Make sure MongoDB is running locally:

```
mongodb://localhost:27017/url-shortener
```

### 4. Run the server

```
node index.js
```

Server runs at:

```
http://localhost:8001
```

---

## 📡 API Endpoints

### 🔹 Create Short URL

**POST** `/url`

#### Request Body:

```json
{
  "url": "https://example.com"
}
```

#### Response:

```json
{
  "id": "shortId"
}
```

---

### 🔹 Redirect to Original URL (you should implement)

**GET** `/:shortId`

* Redirects user to original URL
* Tracks visit history

---

## 🧠 How It Works

1. User sends a long URL via POST request
2. Server generates a unique short ID
3. Stores mapping in MongoDB
4. Returns short ID
5. When accessed, server redirects to original URL

---

## 📈 Future Improvements

* Add UI
* Add analytics dashboard
* Track click count and timestamps
* Add rate limiting
* Deploy on cloud (AWS / Render / Railway)
* Add custom short URLs
* Implement authentication

---

## ❗ Common Issues

* `Cannot GET /url` → You are using GET instead of POST
* `req.body undefined` → Missing `express.json()` middleware
* MongoDB connection failed → Check if MongoDB is running

---

## 🧑‍💻 Author

**Pravin Rajpurohit**
