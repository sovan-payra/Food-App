
# 🍔 Food-App

A full-stack food discovery platform built with **React, Vite, Node.js, Express.js, MongoDB, Mongoose, JWT, and ImageKit**.

Food-App allows users to discover food through short vertical videos, like and save their favorite food, and explore food partner profiles. Food partners can register their businesses and upload food videos with descriptions. 🚀

🔗 **GitHub Repository:** https://github.com/sovan-payra/Food-App

---

## ✨ Features

### 👤 User Features

* 📝 User registration
* 🔑 User login
* 🚪 User logout
* 🔐 JWT-based authentication
* 🍪 Cookie-based authentication
* 🔒 Password hashing using bcrypt
* 🎥 Browse food videos in a reels-style feed
* ▶️ Automatic video playback
* ⏸️ Automatic video pause while scrolling
* ❤️ Like and unlike food videos
* 🔖 Save and unsave food videos
* 📚 View saved food videos
* 🏪 Visit food partner profiles

### 🏪 Food Partner Features

* 📝 Food partner registration
* 🔑 Food partner login
* 🚪 Food partner logout
* 🔐 JWT-based authentication
* 🎬 Upload food videos
* 👀 Preview videos before uploading
* 🖱️ Drag-and-drop video upload
* ✍️ Add food name
* 📄 Add food description
* ☁️ Upload videos to ImageKit
* 🏪 Food partner profile
* 🎥 Display uploaded food videos

### 🎨 UI Features

* 📱 Responsive design
* 🎥 Full-screen vertical reels
* 🧲 Scroll snapping
* 🧭 Bottom navigation
* ☀️ Light theme
* 🌙 Dark theme based on system preference
* ♿ Accessible navigation and form controls
* 📱 Mobile-friendly interface

---

## 🧰 Tech Stack

### 🎨 Frontend

* ⚛️ **React 19**
* ⚡ **Vite**
* 🧭 **React Router**
* 📡 **Axios**
* 🎨 **CSS**

### ⚙️ Backend

* 🟢 **Node.js**
* 🚂 **Express.js**
* 🍃 **MongoDB**
* 🧩 **Mongoose**
* 🔑 **JSON Web Token**
* 🔒 **bcryptjs**
* 🍪 **cookie-parser**
* 🌐 **CORS**
* 📤 **Multer**
* 🆔 **UUID**
* ☁️ **ImageKit**

---

## 📁 Project Structure

```text
Food-App/
│
├── 📁 frontend/
│   ├── 📁 src/
│   │   ├── 📁 components/
│   │   │   ├── BottomNav.jsx
│   │   │   └── ReelFeed.jsx
│   │   │
│   │   ├── 📁 pages/
│   │   │   ├── 📁 auth/
│   │   │   │   ├── ChooseRegister.jsx
│   │   │   │   ├── UserLogin.jsx
│   │   │   │   ├── UserRegister.jsx
│   │   │   │   ├── FoodPartnerLogin.jsx
│   │   │   │   └── FoodPartnerRegister.jsx
│   │   │   │
│   │   │   ├── 📁 general/
│   │   │   │   ├── Home.jsx
│   │   │   │   └── Saved.jsx
│   │   │   │
│   │   │   └── 📁 food-partner/
│   │   │       ├── CreateFood.jsx
│   │   │       └── Profile.jsx
│   │   │
│   │   ├── 📁 routes/
│   │   │   └── AppRoutes.jsx
│   │   │
│   │   ├── 📁 styles/
│   │   │   ├── auth-shared.css
│   │   │   ├── bottom-nav.css
│   │   │   ├── create-food.css
│   │   │   ├── profile.css
│   │   │   ├── reels.css
│   │   │   └── theme.css
│   │   │
│   │   ├── App.jsx
│   │   ├── App.css
│   │   └── main.jsx
│   │
│   └── package.json
│
├── 📁 backend/
│   ├── 📁 src/
│   │   ├── 📁 controllers/
│   │   │   ├── auth.controller.js
│   │   │   ├── food.controller.js
│   │   │   └── food-partner.controller.js
│   │   │
│   │   ├── 📁 db/
│   │   │   └── db.js
│   │   │
│   │   ├── 📁 middlewares/
│   │   │   └── auth.middleware.js
│   │   │
│   │   ├── 📁 models/
│   │   │   ├── user.model.js
│   │   │   ├── foodpartner.model.js
│   │   │   ├── food.model.js
│   │   │   ├── likes.model.js
│   │   │   └── save.model.js
│   │   │
│   │   ├── 📁 routes/
│   │   │   ├── auth.routes.js
│   │   │   ├── food.routes.js
│   │   │   └── food-partner.routes.js
│   │   │
│   │   ├── 📁 services/
│   │   │   └── storage.service.js
│   │   │
│   │   └── app.js
│   │
│   ├── server.js
│   └── package.json
│
├── .gitignore
└── README.md
```

---

## 📥 Installation

Clone the repository:

```bash
git clone https://github.com/sovan-payra/Food-App.git
```

Navigate into the project directory:

```bash
cd Food-App
```

---

## 🎨 Frontend Setup

Navigate to the frontend:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

The frontend will normally run at:

```text
http://localhost:5173
```

---

## ⚙️ Backend Setup

Open another terminal and navigate to the backend:

```bash
cd backend
```

Install dependencies:

```bash
npm install
```

Start the backend server:

```bash
node server.js
```

The backend will run at:

```text
http://localhost:3000
```

---

## 🔐 Environment Variables

Create a `.env` file inside the `backend` directory:

```env
MONGODB_URI=your_mongodb_connection_string

JWT_KEY=your_jwt_secret

IMAGEKIT_PUBLIC_KEY=your_imagekit_public_key
IMAGEKIT_PRIVATE_KEY=your_imagekit_private_key
IMAGEKIT_URL_ENDPOINT=your_imagekit_url_endpoint
```

### ⚠️ Important

Never commit your `.env` file to GitHub.

Make sure your `.gitignore` contains:

```text
node_modules/
.env
```

---

# 📚 API Documentation

## 🔑 Authentication APIs

### 👤 User Registration

```http
POST /api/auth/user/register
```

Request body:

```json
{
  "fullname": "John Doe",
  "email": "john@example.com",
  "password": "password123"
}
```

The password is hashed using `bcryptjs` before being stored in MongoDB. 🔒

After successful registration, a JWT is generated and stored in a cookie. 🍪

---

### 🔑 User Login

```http
POST /api/auth/user/login
```

Request body:

```json
{
  "email": "john@example.com",
  "password": "password123"
}
```

The server verifies the credentials and creates a JWT authentication cookie.

---

### 🚪 User Logout

```http
GET /api/auth/user/logout
```

The authentication cookie is cleared.

---

# 🏪 Food Partner Authentication

### 📝 Register Food Partner

```http
POST /api/auth/food-partner/register
```

Request body:

```json
{
  "name": "Tasty Bites",
  "contactName": "John Doe",
  "phone": "9876543210",
  "email": "business@example.com",
  "password": "password123",
  "address": "123 Market Street"
}
```

The food partner account is created and a JWT authentication cookie is generated.

---

### 🔑 Food Partner Login

```http
POST /api/auth/food-partner/login
```

Request body:

```json
{
  "email": "business@example.com",
  "password": "password123"
}
```

---

### 🚪 Food Partner Logout

```http
GET /api/auth/food-partner/logout
```

The authentication cookie is cleared.

---

# 🍔 Food APIs

## 🎬 Create Food

```http
POST /api/food
```

🔐 **Protected:** Food partner authentication required.

The request uses `multipart/form-data`.

Example fields:

```text
name
description
video
```

The uploaded video is processed through Multer and uploaded to ImageKit. ☁️

---

## 📋 Get Food Items

```http
GET /api/food
```

🔐 **Protected:** User authentication required.

Returns the available food items for the reels feed.

---

## ❤️ Like / Unlike Food

```http
POST /api/food/like
```

Request body:

```json
{
  "foodId": "FOOD_ID"
}
```

If the user has not liked the food:

```text
❤️ Create Like
     ↓
📈 Increase likeCount
```

If the user has already liked it:

```text
💔 Remove Like
     ↓
📉 Decrease likeCount
```

---

## 🔖 Save / Unsave Food

```http
POST /api/food/save
```

Request body:

```json
{
  "foodId": "FOOD_ID"
}
```

The API works as a toggle:

```text
🔖 Not Saved
     ↓
💾 Save Food
     ↓
📈 Increase savesCount
```

Or:

```text
🔖 Already Saved
     ↓
🗑️ Remove Save
     ↓
📉 Decrease savesCount
```

---

## 📚 Get Saved Food

```http
GET /api/food/save
```

🔐 **Protected:** User authentication required.

Returns the food items saved by the authenticated user.

---

# 🏪 Food Partner APIs

## 👀 Get Food Partner Profile

```http
GET /api/food-partner/:id
```

🔐 **Protected:** User authentication required.

The response contains:

* 🏪 Food partner information
* 📍 Address
* 📧 Email
* 📞 Phone
* 👤 Contact name
* 🎥 Food videos uploaded by the partner

Example:

```text
GET /api/food-partner/64abc123...
```

---

# 🎥 Reels Feed

The application provides a short-video experience using the reusable `ReelFeed` component.

The feed uses:

* 🎥 HTML5 Video
* 📜 Vertical scrolling
* 🧲 CSS scroll snapping
* 👀 IntersectionObserver
* ▶️ Automatic playback
* ⏸️ Automatic pause
* ❤️ Like action
* 🔖 Save action
* 💬 Comments UI placeholder
* 🏪 Visit store button

### ▶️ Video Autoplay

A video starts playing when at least approximately **60% of the video is visible**.

```text
          👀 User scrolls
                ↓
        IntersectionObserver
                ↓
       ┌─────────────────┐
       │  60%+ Visible   │
       └─────────────────┘
                ↓
             ▶️ Play
```

When the video is no longer sufficiently visible:

```text
👀 Video leaves viewport
          ↓
       ⏸️ Pause
```

---

# ☁️ Video Upload Flow

Food partners can upload food videos from the **Create Food** page.

```text
💻 React Frontend
        │
        │ FormData
        ▼
🚀 Express API
        │
        ▼
📤 Multer
        │
        ▼
💾 File Buffer
        │
        ▼
☁️ ImageKit
        │
        ▼
🔗 Video URL
        │
        ▼
🍃 MongoDB
```

The actual video file is hosted on ImageKit, while the video URL is stored in MongoDB.

---

# 🔐 Authentication System

The application uses **JWT authentication**.

### 🍪 Cookie Authentication

After registration or login, the backend creates a token:

```javascript
const token = jwt.sign(
  {
    id: user._id
  },
  process.env.JWT_KEY
);
```

The token is then stored in a cookie:

```javascript
res.cookie("token", token);
```

---

## 🛡️ Authentication Middleware

The backend contains separate authentication middleware for:

### 👤 User

```text
authUserMiddleware
```

### 🏪 Food Partner

```text
authFoodPartnerMiddleware
```

The middleware:

1. 🍪 Reads the JWT from the cookie
2. 🔍 Verifies the JWT
3. 🍃 Finds the account in MongoDB
4. 👤 Attaches the user/partner to the request
5. ➡️ Allows the request to continue

Invalid or missing tokens return:

```http
401 Unauthorized
```

---

# 🗄️ Database Models

## 👤 User Model

Stores:

* 👤 Full name
* 📧 Email
* 🔒 Hashed password
* 🕒 Created timestamp
* 🕒 Updated timestamp

```text
User
├── fullname
├── email
├── password
├── createdAt
└── updatedAt
```

---

## 🏪 Food Partner Model

Stores:

* 🏪 Business name
* 👤 Contact name
* 📞 Phone
* 📍 Address
* 📧 Email
* 🔒 Password
* 🕒 Created timestamp
* 🕒 Updated timestamp

```text
Food Partner
├── name
├── contactName
├── phone
├── address
├── email
├── password
├── createdAt
└── updatedAt
```

---

## 🍔 Food Model

Stores:

* 🍔 Food name
* 🎥 Video URL
* 📄 Description
* 🏪 Food partner reference
* ❤️ Like count
* 🔖 Save count

```text
Food
├── name
├── video
├── description
├── foodPartner
├── likeCount
└── savesCount
```

---

## ❤️ Like Model

Stores the relationship between a user and food item.

```text
Like
├── user
├── food
├── createdAt
└── updatedAt
```

---

## 🔖 Save Model

Stores the relationship between a user and saved food.

```text
Save
├── user
├── food
├── createdAt
└── updatedAt
```

---

# 🔄 Application Flow

## 👤 User Flow

```text
📝 Register / 🔑 Login
          ↓
        🏠 Home
          ↓
     🎥 Food Reels
          │
     ┌────┼────┐
     ↓    ↓    ↓
    ❤️   🔖   🏪
   Like  Save Store
               ↓
       🏪 Partner Profile
```

---

## 🏪 Food Partner Flow

```text
📝 Register / 🔑 Login
          ↓
     🎬 Create Food
          ↓
      📁 Select Video
          ↓
      👀 Video Preview
          ↓
   ✍️ Name + Description
          ↓
       ☁️ ImageKit
          ↓
       🍃 MongoDB
          ↓
      🎥 Food Available
```

---

# 🧭 Frontend Routes

## 🔐 Authentication

```text
/register
/user/register
/user/login
/food-partner/register
/food-partner/login
```

## 👤 User

```text
/
/saved
```

## 🏪 Food Partner

```text
/create-food
/food-partner/:id
```

---

# 🎨 Theme System

The frontend uses CSS variables to maintain a consistent design system.

### ☀️ Light Mode

```css
--color-bg: #f9fafb;
--color-surface: #ffffff;
--color-text: #0f172a;
--color-accent: #2563eb;
```

### 🌙 Dark Mode

Dark mode is automatically applied according to the system preference:

```css
@media (prefers-color-scheme: dark) {
  /* Dark theme variables */
}
```

---

---

# 🔒 Security

The application currently implements:

* 🔐 Password hashing using bcrypt
* 🔑 JWT authentication
* 🍪 Cookie-based authentication
* 🛡️ Protected routes
* 🌐 CORS configuration
* 🔑 Environment variables for sensitive credentials

### 🚧 Recommended Production Improvements

* 🔒 HTTP-only and Secure cookie configuration
* 🛡️ Request validation
* 🚦 Rate limiting
* 🌐 Production CORS configuration
* 🚨 Centralized error handling
* 📏 Server-side file size validation
* 🎥 Server-side video type validation
* 🔐 HTTPS in production

---

# 🚧 Future Improvements

* [ ] 💬 Complete comments system
* [ ] 👤 User profile
* [ ] 🏪 Food partner dashboard
* [ ] 🛒 Food ordering
* [ ] 📦 Order management
* [ ] 🔍 Food search
* [ ] 🏷️ Food categories
* [ ] ❤️ Follow food partners
* [ ] 🔔 Notifications
* [ ] ♾️ Infinite scrolling
* [ ] 📊 Food partner analytics
* [ ] 🧪 Automated testing
* [ ] ☁️ Production deployment
* [ ] 📱 React Native mobile application

---

# 🤝 Contributing

Contributions, suggestions, and improvements are welcome! ❤️

### 1️⃣ Fork the repository

### 2️⃣ Create a new branch

```bash
git checkout -b feature/your-feature
```

### 3️⃣ Make your changes

### 4️⃣ Commit your changes

```bash
git commit -m "Add your feature"
```

### 5️⃣ Push your branch

```bash
git push origin feature/your-feature
```

### 6️⃣ Create a Pull Request 🚀

---

# 👨‍💻 Author

## Sovan Payra

💻 Full-Stack Developer
🎓 Computer Science Graduate
🚀 Learning, building, and experimenting with modern web technologies

### 🔗 Connect With Me

🐙 **GitHub:** https://github.com/sovan-payra

💼 **LinkedIn** https://www.linkedin.com/in/sovan-payra-8a17b9321/

📸 **Instagram** https://www.instagram.com/x.sovannn/

🍔 **Food-App:** https://github.com/sovan-payra/Food-App


---

# ⭐ Support

If you like this project, consider giving it a ⭐ on GitHub!

**Thanks for checking out Food-App! 🍔❤️**
