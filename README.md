# 🌸 Mezo Flower Products Saler

> **A Complete, Modern, Responsive, Full-Stack E-Commerce Website for Fresh Flowers in Pakistan**  
> **Brand & Profile Identity:** Muzammil Hussain

---

## 🌟 Overview & Key Highlights

**Mezo Flower Products Saler** is an elegant, full-stack e-commerce web platform engineered for selling fresh, high-grade flower bouquets and floral arrangements across Pakistan with native pricing in **Pakistani Rupees (PKR)**.

- **Branding:** Complete flower-themed visual identity featuring custom SVG logo with **"Mezo Flower Products Saler"** and **"Muzammil Hussain"** brand authorship.
- **Color Palette:** Soft Pink, White, Floral Green, Light Purple, Cream, and Soft Rose configured via CSS variables.
- **Full-Stack Architecture:**
  - **Frontend:** Responsive HTML5, Vanilla CSS3 (modular stylesheets), and modern ES6 JavaScript.
  - **Backend:** Node.js & Express.js.
  - **Database:** Relational SQLite engine utilizing Node.js built-in `node:sqlite` (SQLite 3.53.3) for persistent, transactional, and zero-configuration operation on Windows and all platforms.
  - **Authentication:** bcrypt password hashing, JWT sessions, 6-digit OTP email verification with countdown timer, and password reset.
  - **Security & CAPTCHA:** Server-validated cryptographic challenge puzzle (immune to frontend bypasses) plus optional Cloudflare Turnstile integration.
  - **Shopping Cart & Checkout:** Real-time PKR calculations, free shipping threshold (PKR 5,000), Pakistani city delivery coverage, and payment methods (Cash on Delivery, JazzCash, EasyPaisa, Direct Bank Transfer).
  - **User & Admin Dashboards:** Customer order tracking & history, plus role-protected Admin Dashboard for inventory management, image upload, and order status updates.

---

## 📁 Project Structure

```text
/mezo-flower-products-saler
│
├── frontend/
│   ├── index.html               # Main storefront homepage
│   ├── products.html            # Flower catalog with search & multi-filters
│   ├── product-details.html     # Product details with gallery & reviews
│   ├── cart.html                # Dedicated shopping cart page
│   ├── checkout.html            # Checkout & Pakistani delivery details
│   ├── login.html               # Login with server CAPTCHA
│   ├── signup.html              # Registration with server CAPTCHA
│   ├── verify-email.html        # 6-digit OTP verification & countdown
│   ├── forgot-password.html     # Password reset flow
│   ├── dashboard.html           # Customer dashboard & order history
│   ├── admin.html               # Admin dashboard & management
│   ├── about.html               # Brand story & Muzammil Hussain identity
│   ├── contact.html             # Customer support & inquiries
│   ├── css/
│   │   ├── style.css            # CSS variables, typography, reset, buttons, navbar, footer
│   │   ├── responsive.css       # 320px to 1440px+ breakpoints
│   │   ├── products.css         # 4-col responsive grid, card hover, details gallery
│   │   ├── auth.css             # Forms, OTP boxes, CAPTCHA widget
│   │   └── dashboard.css        # User & admin statistics, orders table, modals
│   ├── js/
│   │   ├── main.js              # Navbar, toast notifications, cart drawer
│   │   ├── auth.js              # Auth controller, CAPTCHA loader, OTP timer
│   │   ├── products.js          # Catalog fetch, search, filters, quick view
│   │   ├── product-details.js   # Image gallery, reviews submission
│   │   ├── cart.js              # Cart calculations in PKR
│   │   ├── checkout.js          # Order placement & confirmation modal
│   │   ├── dashboard.js         # User orders tracking & profile update
│   │   └── admin.js             # Admin statistics, product CRUD, status updater
│   └── assets/
│       └── images/
│           ├── logo.svg         # Floral brand vector logo
│           └── flowers/         # High-resolution flower photography
│
├── backend/
│   ├── server.js                # Express app entry & static file server
│   ├── config/
│   │   ├── db.js                # SQLite relational database & initial seeds
│   │   └── constants.js         # PKR currency settings & categories
│   ├── controllers/
│   │   ├── authController.js    # Register, login, OTP verify, password reset
│   │   ├── productController.js # Catalog, search, filters, admin CRUD
│   │   ├── orderController.js   # Order placement, user history, admin status
│   │   ├── reviewController.js  # Ratings & review moderation
│   │   └── captchaController.js # Challenge generator & validation
│   ├── middleware/
│   │   └── auth.js              # JWT authentication & requireAdmin guard
│   ├── services/
│   │   ├── emailService.js      # Nodemailer with HTML templates & dev preview
│   │   └── captchaService.js    # Cryptographic challenge generator & validator
│   └── routes/                  # Express REST routes
│
├── database/
│   └── mezo_flowers.db          # Persistent SQLite database file
├── .env                         # Server environment configuration
├── .env.example                 # Configuration template
├── package.json                 # Dependencies & startup scripts
└── README.md                    # Project documentation
```

---

## 🚀 Getting Started

### 1. Requirements
- Node.js version **v22.5.0** or higher (Node **v24.19.0** recommended, which is already present on this system).

### 2. Running the Application
From the workspace root:

```bash
npm start
```

Or for development:

```bash
npm run dev
```

Open your browser at:
**[http://localhost:3000](http://localhost:3000)**

---

## 🔑 Pre-Configured Demo Credentials

For quick evaluation and testing, the database is automatically seeded with:

### 1. Store Administrator Account
- **Email:** `admin@mezoflowers.com`
- **Password:** `Admin@12345`
- **Privileges:** Access to `/admin.html` with product CRUD, image upload, revenue statistics, and order status updates.

### 2. Customer Account
- **Email:** `customer@mezoflowers.com`
- **Password:** `Customer@12345`
- **Privileges:** Access to `/dashboard.html` with order history, profile updates, and order tracking.

---

## 🌸 Flower Catalog Categories & Sample PKR Prices

| Flower Category | Sample Bouquet Name | Quality Grade | Price in PKR |
|---|---|---|---|
| **Roses** | Rose Bouquet (12 Red Roses) | Fresh Cut Premium | PKR 2,500 |
| **Roses** | Premium Red Roses (24 Long Stem) | Luxury Export Grade | PKR 3,000 |
| **Tulips** | Tulip Bouquet | Imported Holland | PKR 3,500 |
| **Lilies** | Lily Bouquet (Casablanca) | Royal Oriental Grade | PKR 4,000 |
| **Orchids** | Premium Orchid Bouquet | Exotic Tropical Grade | PKR 6,500 |
| **Sunflowers** | Sunflower Bouquet | Golden Farm Harvest | PKR 2,800 |
| **Jasmine** | Jasmine Bouquet (Motia) | Handpicked Aromatic | PKR 2,200 |
| **Mixed Bouquets** | Mixed Premium Bouquet | Florist Masterpiece | PKR 5,500 |
| **Carnations** | Pastel Carnations Glow | Greenhouse Fresh | PKR 2,900 |
| **Daisies** | White Daisies Delight | Meadow Bloom | PKR 2,400 |
| **Wedding Flowers**| Royal Wedding Garland & Basket | Bridal Couture Quality | PKR 12,000 |
| **Birthday Flowers**| Vibrant Birthday Blossom Box | Festive Celebration | PKR 4,200 |
| **Gift Flowers** | Luxury Velvet Gift Hamper | Artisan Bespoke | PKR 7,800 |

---

## 🛡️ Security & Authentication

1. **Server-Side CAPTCHA:**
   - Visual SVG challenge with random color waves, letter distortion, and cryptographic HMAC signatures.
   - Verified strictly on the server backend — preventing bot automation and bypassing.
   - Also supports **Cloudflare Turnstile** by adding `TURNSTILE_SECRET_KEY` in `.env`.
2. **Email Verification:**
   - 6-digit random verification code valid for 10 minutes.
   - Real SMTP integration with Nodemailer (Gmail, SendGrid, Resend).
   - In local development mode, codes are automatically logged to the terminal console and previewed for instant testing.
3. **Password Security:**
   - 10-round bcrypt hashing — no plain-text passwords stored anywhere.
4. **Role-Based Authorization:**
   - Customer vs. Administrator route protection with HTTP-only cookies and Bearer tokens.

---

## 🇵🇰 Pakistani Payment Methods

The checkout system supports:
- **Cash on Delivery (COD)** across Pakistani cities.
- **JazzCash Mobile Wallet** integration point.
- **EasyPaisa Mobile Account / QR** integration point.
- **Direct Bank Transfer (IBFT)** (Meezan Bank, HBL, Allied Bank).

---

## 📜 Credits & Author
- **Platform:** Mezo Flower Products Saler
- **Brand Identity & Founder:** Muzammil Hussain
