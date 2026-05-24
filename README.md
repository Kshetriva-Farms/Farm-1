# 🌾 Kshetriva Farms | Fresh From Farm to Your Home

[![Bilingual: English & Telugu](https://img.shields.io/badge/Language-English%20%2F%20%E0%B0%A4%E0%B1%86%E0%B0%B2%E0%B1%81%E0%B0%97%E0%B1%81-green.svg)](#-bilingual-translation-system)
[![Tech Stack: HTML5 / CSS3 / Vanilla JS](https://img.shields.io/badge/Stack-HTML5%20%2F%20CSS3%20%2F%20JS-blue.svg)](#%EF%B8%8F-technology-stack)
[![Responsive: Mobile First](https://img.shields.io/badge/Responsive-Mobile%20%26%20Tablet%20Friendly-orange.svg)](#-responsive-layout)
[![Integration: WhatsApp Checkout](https://img.shields.io/badge/Integration-WhatsApp%20Checkout-25D366.svg)](#-whatsapp-checkout-integration)

Kshetriva Farms is a premium, modern single-page web application designed to connect hardworking local farmers from **Maryala, Telangana** directly with urban families. By eliminating middlemen, the platform ensures that families receive fresh, chemical-safe vegetables at fair prices, while local growers earn a sustainable, direct-to-consumer income.

This project is built using high-performance vanilla web technologies (HTML5, custom CSS3, and modern ES6+ Javascript) and features a state-of-the-art interactive shopping cart, native bilingual support, and direct-to-WhatsApp checkout.

---

## ✨ Features at a Glance

### 🟢 Direct-to-Consumer Model
- **No Middlemen:** Connects farmers directly to end-consumers.
- **Premium Local Support:** Dedicated space highlighting stories, cultivation methods, and locations of our farmers (**Ramesh Kumar**, **Sunita Devi**, and **Ashok Singh**).
- **Transparency:** Clear sourcing descriptions from the soil to the kitchen table.

### 🌐 Bilingual Translation System (English & Telugu)
- Powered by a native, fast JS-based translation engine.
- Translates everything including static section titles, nav bars, product cards, dynamic units (e.g., `kg`, `dozen`, `bunch`), customer reviews, interactive cart details, clear-all verification modals, and custom alerts.
- Features a **segmented language toggle switch** with custom CSS slide transitions.

### 🛒 Advanced Interactive Shopping Cart
- **Dynamic Catalog:** Renders products dynamically from local JSON structures with filters for *Leafy Greens*, *Root Vegetables*, *Seasonal*, *Organic*, and *Fruits*.
- **Quantity Selector:** Interactive increment/decrement triggers synced instantly with the DOM and cart state.
- **Visual Button Feedback:** Add-to-cart buttons change color dynamically and show localized confirmation states (e.g., `✓ Added!` in green, `✓ Reset!` in dark red).
- **Persistent State:** Saves the cart items and quantity to `localStorage` so a user’s shopping basket is retained across page reloads.
- **Right-Side Cart Drawer:** Interactive slide-out cart listing all selected items, prices, dynamic total amounts (in ₹), clear all action, and order checkout.
- **Custom Modals & Toasts:** Vanilla CSS/JS custom verification modal for clearing the cart and a custom animated toast notification for clipboard actions.

### 📱 Premium Responsive Design & Animations
- **Visual Vibrancy:** Custom CSS custom properties, Outfit & Inter google fonts, and an animated hover effect on the brand logo.
- **Self-Hosted Video Banner:** Beautiful autoplaying loop background video with a dark overlay to maintain readability.
- **Sticky Blur Navbar:** Uses `backdrop-filter: blur()` to stay floating transparently as users scroll.
- **Responsive Navigation:** Smooth scroll triggers, mobile menu slide-out drawer, and dual floating utility buttons (quick-access cart and instant WhatsApp chat).

### 💬 WhatsApp Checkout Integration
- Formulates a premium, formatted checkout invoice directly in English or Telugu based on user selection.
- Calculates sub-totals, items, and quantities, formats them cleanly into markdown, and launches an encoded direct link to the business WhatsApp channel.

---

## 🛠️ Technology Stack

- **Structure:** [HTML5](https://developer.mozilla.org/en-US/docs/Web/HTML) (Semantic and SEO-optimized markup)
- **Styling:** Custom CSS3 (Flexible custom properties, grid and flex layouts, custom keyframe animations, glassmorphism, responsive breakpoints)
- **Icons & Typography:**
  - [Font Awesome v6.4.0](https://fontawesome.com/) (Scalable vector icons)
  - [Google Fonts](https://fonts.google.com/) (Outfit for headers, Inter for copy text)
- **Logic:** Vanilla ES6+ [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript) (Event handling, custom modular translations, state synchronization, storage APIs)

---

## 📁 Directory Structure

```text
Kshetriva_farms/
│
├── index.html        # Main landing page with full semantic layout
├── styles.css        # Comprehensive styling, variables, animations & responsiveness
├── script.js        # Core application logic, mock data, translations & state management
│
├── images/           # Local visual assets (webp format optimized for quick loading)
│   ├── logo_nav.webp
│   ├── favicon.png
│   ├── spinach.webp
│   ├── carrots.webp
│   ├── ...           # Farmer profiles, gallery photos & product pictures
│
├── videos/           # Interactive background media
│   └── bg-video.mp4  # High-definition visual background video
│
└── README.md         # Current documentation file
```

---

## 🚀 Getting Started & Local Development

This is a pure frontend, zero-dependency static project. It requires no installation, compilers, or build systems to run.

### Method 1: Desktop Execution
1. Download or clone this repository.
2. Double-click the `index.html` file in your directory to open the website directly in any modern web browser.

### Method 2: Lightweight Local Server (Recommended)
To fully enjoy all custom features (like localized media files, video streaming, and robust storage access), run the project through a local development server:

*Using Python:*
```bash
# In the project directory, run:
python -m http.server 8000
```
Then open [http://localhost:8000](http://localhost:8000) in your web browser.

*Using Node.js (`live-server` or `vite` / `serve`):*
```bash
# Using live-server
npx live-server
```

---

## ⚙️ How the WhatsApp Ordering Works

When the user clicks the **Send Order on WhatsApp** button in the shopping drawer, `script.js` processes the cart object and translates the receipt. 

The invoice is dynamically constructed in JS:
```javascript
let message = `*New Order - Kshetriva Farms*\n`;
message += `===============================\n`;
// Loop through items in cart ...
message += `${index + 1}. *${product.name}* - ${qty} ${product.unit} (₹${itemTotal})\n`;
message += `===============================\n`;
message += `*Total Amount:* ₹${totalSum}\n\n`;
```

It is then fully encoded using `encodeURIComponent(message)` and bound to the URL:
`https://wa.me/918374276995?text={encoded_message}`

---

## 📐 Responsive Breakpoints

The custom stylesheet features premium responsiveness defined for standard viewports:
- **Desktops (`>= 1024px`):** Full grid layouts, multi-column about & farmer profiles, full desktop nav with sliding toggle switches.
- **Tablets & iPads (`768px - 1023px`):** Scaled typography, responsive grid columns (2-column layouts for farmer cards), accessible navigation.
- **Smartphones (`<= 767px`):** 1-column layouts, hamburger slide-out menu drawer, and visual floating buttons on screen corners for instant WhatsApp and basket access.

---

## 📧 Contact & Support

For queries, orders, or partner programs:
- **Phone:** +91 83742 76995 | +91 90148 33202
- **Email:** [farm@kshetrivafarms.com](mailto:farm@kshetrivafarms.com) (Click the envelope icon in the website footer to copy this address instantly!)
- **Address:** H no. 5-134, Maryala, Bommalaramaram, Telangana - 508116, India
- **Instagram:** [@kshetrivafarms](https://www.instagram.com/kshetrivafarms?igsh=dGV5d3I2d2Rhc2t2)
