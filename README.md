# KLUIMS - Modern Inventory Management System

**KLUIMS** (Koneru Lakshmaiah University Inventory Management System) is a responsive single-page web application designed for real-time warehouse logistics, stock tracking, and supplier coordination. 

This project was developed strictly using native browser technologies to satisfy the requirements of the **Front End Development Frameworks / SDC Project Review–1**.

## 🚀 Key Features

- **Admin Module Workspace**: Enables full inventory management including adding product rows, removing rows, tracking total items, and viewing low-stock visual notifications.
- **User Module Viewport**: Provides warehouse clerks a clean, read-only dashboard equipped with an instant search filter to scan stock catalogs dynamically.
- **Client-Side Auth & Persistence**: Implements secure user signup registration and role-based login authorization powered completely via the browser's `LocalStorage`.
- **Dynamic JS Navigation**: Handles conditional dashboard loading and route redirects using pure vanilla JavaScript logic.

## 🛠️ Built With

- **HTML5**: Semantic layout definitions.
- **CSS3 (Flexbox & CSS Grid)**: Visual design architecture. The authorization views leverage Flexbox alignments while the main workspace dashboards are driven by a dual-column CSS Grid responsive template.
- **Vanilla JavaScript**: Asynchronous state management, search filtering, and authentication mechanics.

## 📁 Repository Structure

- `index.html`: System gateway access portal containing Login and Signup modules.
- `admin.html`: High-privilege administrative operational command panel.
- `user.html`: Low-privilege clerk viewport template with active data searching.
- `style.css`: Unified stylesheet engine for grid alignments and low-stock warning indicators.
- `app.js`: Central core script data controller managing database simulation profiles.

## 🚀 How to Run Locally

1. Clone or download this repository.
2. Ensure all files are placed together in a single folder.
3. Open your browser (Google Chrome or Microsoft Edge) and drag `index.html` into the window or double-click to load instantly.
