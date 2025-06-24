# Project Task Manager 🚀

A web-based application for tracking tasks, deadlines, and company details, built with Firebase and Tailwind CSS. Designed for internal company use, with real-time updates and secure authentication.

---

## 📚 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Project Structure](#project-structure)
- [Firebase Setup](#firebase-setup)
- [Authentication](#authentication)
- [Data Structure](#data-structure)
- [Usage Instructions](#usage-instructions)
- [Customization](#customization)
- [Troubleshooting](#troubleshooting)
- [FAQ](#faq)
- [Support & Contact 💬](#support--contact-)
- [Version & Maintenance 🏷️](#version--maintenance)

---

## 📝 Overview

**Project Task Manager** is a company-internal tool for managing project tasks and company information. It supports multiple users, secure authentication, and real-time data updates using Firebase Firestore. The UI is built with Tailwind CSS for a modern, responsive experience.

There are two versions included:
- **Production Version:** `index.html` (root) — full authentication, public company details, for real deployment.
- **Demo Version:** `Project Task Manager/index.html` — anonymous auth, user-private data, for testing or embedded use.

---

## 💡 Features
- 🔒 User authentication (email/password, anonymous)
- 📝 Add, edit, delete, and filter tasks
- 🏢 Track company details
- ⚡ Real-time updates with Firestore
- 📱 Responsive, modern UI
- 🔗 Public and private data separation

---

## 🗂️ Project Structure

```
project-task-manager docs/
│
├── index.html                  # Main production app
└── Project Task Manager/
    └── index.html              # Demo/embedded version
```

---

## 🔥 Firebase Setup

1. **Create a Firebase Project** at [Firebase Console](https://console.firebase.google.com/).
2. **Register a Web App** and copy your config.
3. **Enable Authentication** (Email/Password, Anonymous as needed).
4. **Enable Firestore Database**.

**Config Example:**
```js
const firebaseConfig = {
  apiKey: "...",
  authDomain: "...",
  projectId: "...",
  storageBucket: "...",
  messagingSenderId: "...",
  appId: "..."
};
```
Paste this into the `firebaseConfig` in your `index.html`.

---

## 👤 Authentication

- **Production version** (`index.html`):  
  - Supports email/password sign up and login.
  - Users can log out.
  - User's email is displayed in the UI.
- **Demo version** (`Project Task Manager/index.html`):  
  - Uses anonymous or custom token authentication.
  - No login/logout UI.

---

## 🗄️ Data Structure

- **Tasks:**  
  Stored per user at `artifacts/{appId}/users/{userId}/tasks`
- **Company Details:**  
  - Production: Public at `artifacts/{appId}/public/data/companyDetails`
  - Demo: Private per user at `artifacts/{appId}/users/{userId}/companyDetails`

---

## 🛠️ Usage Instructions

1. **Open the app in your browser.**
2. **Sign up or log in** (production version).
3. **Add tasks** using the form.
4. **Edit or delete tasks** using the action buttons.
5. **Filter tasks** by status.
6. **Add or edit company details** using the company form.
7. **Log out** when finished (production version).

---

## 🎨 Customization

- **Add more companies:** Edit the `<select>` options in the HTML.
- **Change styles:** Modify Tailwind classes or add custom CSS.
- **Change authentication:** Adjust Firebase Auth providers as needed.

---

## 🛡️ Troubleshooting

- **Firebase errors:**  
  - Check your Firebase config.
  - Ensure Firestore and Auth are enabled.
  - Check browser console for error messages.
- **Permission denied:**  
  - Update Firestore security rules to allow appropriate access.

---

## ❓ FAQ

**Q: Can I use Google login?**  
A: Yes, enable it in Firebase Auth and update the code.

**Q: Can I deploy this publicly?**  
A: Yes, but secure your Firebase rules and never expose sensitive keys.

**Q: How do I reset my password?**  
A: Use Firebase Auth's password reset features.

---

## Support & Contact 💬

For technical support or questions about this Project Task Manager system, please contact your system administrator or the development team.

**Version**: 1.0  
**Last Updated**: January 2024  
**Maintained By**: RBX Development Team 