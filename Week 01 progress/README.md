# Week 01 Progress Report: Frontend Experience & Portal Preview

**Project:** iSmart Investment Platform  
**Sprint / Milestone:** Week 01 – Frontend Foundation, Landing Page & Investor Portal UI  
**Current Release Year:** 2026  
**Status:** Completed & Delivered for Client Review  
**Engineering:** Frontend Development Team  

---

## 1. Executive Summary

During **Week 01**, we completed the frontend foundation for the **iSmart Investment** platform. The scope of this milestone covers the public marketing front, the brand identity, and the three primary authenticated investor interfaces:

1. **Public Landing Page & Showcase** (Hero, value propositions, packages overview, and social proof)
2. **Investor Dashboard** (`login/dashboard/`)
3. **User Profile Interface** (`login/profile/`)
4. **Investment Packages Interface** (`login/packages/`)

All UI elements, responsive breakpoints, stylesheets, and vendor libraries are bundled into this self-contained **`Week 01 progress`** package.

---

## 2. Deliverables & Features Covered

### A. Public Landing Page Experience
- **Hero & Value Proposition:** Modern typography, dynamic CTAs (*Login* and *Register*), and high-resolution 3D financial illustrations.
- **Service Highlights:** Interactive cards detailing weekly yields (+35%), investment security, and fast capital turnaround.
- **Testimonial Slider:** Automated testimonials powered by `Owl Carousel 2` and scroll-triggered animations via `AOS`.
- **Branding & Footer:** Unified 2026 copyright and contact routing.

### B. Investor Dashboard (`login/dashboard/`)
- Real-time balance and earnings cards: **Account Balance**, **Active Investments**, **Total Profit**, and **Referral Bonus**.
- Quick action navigation tabs for rapid switching between **Packages**, **Profile**, **Transactions**, and **Withdrawals**.
- Responsive side navigation bar and top profile status dropdown.

### C. Investor Profile Management (`login/profile/`)
- User credential and account summary view (Username, Email, Phone, Account UID, and Joined Date).
- Profile details card formatted for identity verification and account updates.

### D. Investment Packages Portal (`login/packages/`)
- Tiered investment card grid with deposit thresholds, percentage return rates, maturity duration, and active plan indicators.
- One-click package selection modals ready for funding and confirmation triggers.

---

## 3. Directory Layout (Week 01 Deliverable)

```text
Week 01 progress/
├── index.html                  # Public marketing & landing page (2026 edition)
├── README.md                   # This report & handover guide
├── css/                        # Core styling & custom responsive overrides
├── js/                         # Landing page script logic & animations
├── img/                        # 3D assets, icons, backgrounds & avatars
├── vendor/                     # Bootstrap, jQuery, OwlCarousel libraries
└── login/
    ├── index.html              # Member login interface
    ├── login.css & js          # Authentication UI styles & handlers
    ├── dashboard/              # Investor Dashboard view & controller
    ├── profile/                # Profile management view & controller
    ├── packages/               # Investment tiers & package selection view
    ├── transactions/           # Transaction history UI preview
    └── withdraw/               # Withdrawal request UI preview
```

---

## 4. Firebase Configuration & Client Handover Instructions

The application uses **Firebase Authentication** for user accounts and **Firebase Realtime Database (RTDB)** for user balances, packages, and transaction logs.

### Where Firebase Config is Located in the Code
The configuration object (`firebaseConfig`) is currently set across these scripts:
- `login/firebase-login.js` (Lines 16–24)
- `login/dashboard/refresh.js` (Lines 16–24)
- `login/profile/refresh.js` (Lines 13–21)
- `login/packages/refresh.js` (Lines 12–20)
- `login/transactions/refresh.js` (Lines 14–22)
- `login/withdraw/refresh.js` (Lines 15–23)
- `register/firebase-register.js` (Lines 151–159)

### Information the Client Needs to Provide
To connect their own independent Firebase project, ask the client for:

```javascript
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
  databaseURL: "https://YOUR_PROJECT_ID-default-rtdb.firebaseio.com",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_PROJECT_ID.appspot.com",
  messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
  appId: "YOUR_APP_ID"
};
```

---

## 5. Next Steps for Week 02

- [ ] Plug in the client's production Firebase credentials and test live user registration.
- [ ] Connect Realtime Database balance updates directly to the Dashboard and Package activation buttons.
- [ ] Implement live withdrawal request status tracking and admin approval workflows.
