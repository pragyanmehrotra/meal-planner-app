# 🍽️ ReciPal: AI-Powered Meal Planner & Recipe App

![ReciPal Logo](recipal/assets/icon.png)

## 🚀 Overview

**ReciPal** is a full-stack, AI-powered meal planner and recipe management app. It leverages modern web and mobile technologies, robust backend APIs, and seamless Stripe integration to deliver a premium user experience. Built for extensibility, security, and performance, ReciPal is the perfect showcase of advanced app development skills.

---

## ✨ Features & Highlights

- **AI Recipe Extraction**: Extract recipes from any URL using NVIDIA LLM (no external scrapers!)
- **Full-Stack Architecture**: Node.js/Express backend, React Native (Expo) frontend
- **Modern UI/UX**: Beautiful, responsive design with Tamagui and custom components
- **Meal Planning**: Drag-and-drop meal planner with custom sections and days
- **Grocery Lists**: Auto-generate and manage grocery lists from your meal plans
- **Favorites**: Save and manage your favorite recipes
- **Premium Subscriptions**: Stripe-powered $2.99/mo premium plan with webhook automation
- **User Auth**: Secure JWT authentication, email verification, password reset
- **Notifications**: (Pluggable) push notification support
- **Custom Recipes**: Add your own recipes if not found in the database
- **Offline Support**: Local storage for meal plans and recipes
- **Production-Ready**: Environment variable management, robust error handling, and more

---

## 🛠️ Technologies Used

- **Frontend**: React Native (Expo), Tamagui, React Navigation
- **Backend**: Node.js, Express, Drizzle ORM, PostgreSQL
- **Database**: Supabase/PostgreSQL
- **AI Integration**: NVIDIA LLM API
- **Payments**: Stripe API (Checkout, Webhooks)
- **Auth**: JWT, SecureStore, Email Verification
- **DevOps**: dotenv, ngrok, cli-progress, nodemailer

---

## 📸 Demo & Screenshots

> _Replace the image links below with your own screenshots!_

### 🏠 Home & Browse Recipes

![Home Screen](recipal/assets/images/home.png)

### 🍳 Recipe Details & Extraction

![Recipe Details](recipal/assets/images/recipe-details.png)

### 📅 Meal Planner

![Meal Planner](recipal/assets/images/meal-planner.png)

### 🛒 Grocery Lists

![Grocery List](recipal/assets/images/grocery-list.png)

### ❤️ Favorites

![Favorites](recipal/assets/images/favorites.png)

### 👤 Profile & Premium

![Profile](recipal/assets/images/profile.png)

### 💳 Stripe Checkout

![Stripe Checkout](recipal/assets/images/stripe-checkout.png)

---

## 🧑‍💻 Local Development & Usage

### 1. **Clone the Repo**

```bash
git clone https://github.com/yourusername/recipal.git
cd meal-planner-app
```

### 2. **Environment Variables**

Create a `.env` file in both `backend/` and `recipal/` directories. Example for backend:

```env
# backend/.env
DATABASE_URL=postgresql://postgres:postgres@localhost:54322/postgres
JWT_SECRET=your-super-secret-jwt-key
STRIPE_SECRET_KEY=sk_test_...
STRIPE_WEBHOOK_SECRET=whsec_...
NVIDIA_API_KEY=your-nvidia-api-key
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your-email@gmail.com
SMTP_PASS=your-app-password
SMTP_FROM=your-email@gmail.com
SMTP_SECURE=false
EXPO_PUBLIC_API_URL=http://localhost:4000
```

Example for frontend:

```env
# recipal/.env
EXPO_PUBLIC_API_URL=http://localhost:4000
```

### 3. **Database Setup**

- Install [Supabase CLI](https://supabase.com/docs/guides/cli)
- Start Supabase/Postgres locally:
  ```bash
  cd backend
  supabase start
  # or use Docker/Postgres as needed
  ```
- Run migrations:
  ```bash
  supabase db reset
  # or use drizzle-kit/db push if using Drizzle
  ```

### 4. **Install Dependencies**

```bash
cd backend && npm install
cd ../recipal && npm install
```

### 5. **Start the Backend**

```bash
cd backend
npm run dev
# or npm start
```

### 6. **Start the Frontend (Expo)**

```bash
cd recipal
npx expo start
```

### 7. **Stripe Webhook Setup**

- Expose your backend to Stripe using [ngrok](https://ngrok.com/):
  ```bash
  ngrok http 4000
  ```
- Add the webhook endpoint in Stripe Dashboard:
  ```
  https://<your-ngrok-url>/api/payments/webhook
  ```
- Listen for events: `checkout.session.completed`, `customer.subscription.deleted`, etc.

---

## 📝 Feature Walkthrough

### 🔍 AI Recipe Extraction

- Paste a recipe URL, and the app uses NVIDIA LLM to extract all details (no scraping!)
- [Screenshot Placeholder]

### 📅 Meal Planning

- Add, remove, and customize meal sections and days
- Drag and drop recipes into your plan
- [Screenshot Placeholder]

### 🛒 Grocery List Generation

- Auto-generate grocery lists from your meal plan
- Check off items as you shop
- [Screenshot Placeholder]

### ❤️ Favorites

- Save any recipe to your favorites for quick access
- [Screenshot Placeholder]

### 💳 Premium Subscription

- Subscribe for $2.99/mo to unlock premium features
- Stripe Checkout integration with webhook automation
- [Screenshot Placeholder]

### ➕ Custom Recipes

- Add your own recipes if not found in the database
- [Screenshot Placeholder]

### 👤 User Profile & Auth

- Secure JWT auth, email verification, password reset
- [Screenshot Placeholder]

---

## 🏆 Why This Project Stands Out

- **Production-Ready**: Real payment flows, robust error handling, and secure authentication
- **Modern Stack**: Uses the latest in React Native, Node.js, Drizzle ORM, and Stripe
- **AI Integration**: Real-world use of LLMs for data extraction
- **Extensible**: Easily add new features, endpoints, or UI components
- **Beautiful UI**: Custom theming, responsive layouts, and smooth UX
- **Full Documentation**: Every step, variable, and feature is documented for easy onboarding

---

## 🙌 Contributing & Feedback

Pull requests, issues, and feedback are welcome! If you use this project, please ⭐️ the repo and share your experience.

---

## 📧 Contact

For support, questions, or to show off your own meal plans:

- Email: recipal.meal.planner@gmail.com
- GitHub Issues: [Open an issue](https://github.com/yourusername/recipal/issues)

---

> _Built with ❤️ by [Your Name] — Happy Cooking!_
