# Firebase Setup for Personal Blog

This document outlines the steps to set up Firebase for the `personal-blog` project.

## Firebase Console Setup

1. **Go to Firebase Console**: [Firebase Console](https://console.firebase.google.com/).
2. **Create a Project**:
   - Project Name: `personal-blog`
   - Project ID: `personal-66d1f` (default)
3. **Add a Web App**:
   - App Name: `personal-blog`
   - Deploy: Yes
   - URL Name: `sonali-blog.web.app`

## Add Firebase SDK

1. Use the `<script>` tag to include Firebase SDK:
   ```html
   <script type="module">
     import { initializeApp } from "https://www.gstatic.com/firebasejs/11.1.0/firebase-app.js";
     import { getAnalytics } from "https://www.gstatic.com/firebasejs/11.1.0/firebase-analytics.js";

     const firebaseConfig = {
       apiKey: "AIzaSyBKFrJtGjx7a94jzQj6Nm3gmMSXNxhxBHU",
       authDomain: "personal-66d1f.firebaseapp.com",
       projectId: "personal-66d1f",
       storageBucket: "personal-66d1f.firebasestorage.app",
       messagingSenderId: "967583217488",
       appId: "1:967583217488:web:d966ba8da112d7dbba5e55",
       measurementId: "G-S89N3SWHRJ"
     };

     const app = initializeApp(firebaseConfig);
     const analytics = getAnalytics(app);
   </script>
   ```

## Install Firebase CLI

1. Install the CLI:
   ```bash
   npm install -g firebase-tools
   ```
2. Verify Installation:
   ```bash
   firebase --version
   node -v
   npm -v
   ```
3. Login:
   ```bash
   firebase login
   ```

## Initialize Firebase in the Project

1. Run the initialization command:
   ```bash
   firebase init
   ```
2. Select the Firebase features:
   - Firestore: Configure security rules and indexes.
   - Hosting: Configure files for Firebase Hosting.
3. Associate the project directory with Firebase:
   - Select the project: `personal-66d1f (personal-blog)`.

## Firestore Setup

1. Go to Firestore setup: [Firestore Console](https://console.firebase.google.com/project/personal-66d1f/firestore).
2. Create Database:
   - Location: `asia-south1 (Mumbai)`
   - Secure Rules: Start in production mode.

## Authentication Setup

1. Go to Authentication under Build in Firebase Console.
2. Get Started with Authentication.
3. Enable Email/Password and Email Link (passwordless sign-in).
4. Add Users:
   - Provide email and password for new users.

## Hosting/Deploying

1. Install Firebase CLI:
   ```bash
   npm install -g firebase-tools
   ```
2. Configure Hosting in `firebase.json`:
   ```json
   {
     "hosting": {
       "site": "sonali-blog",
       "public": "public"
     }
   }
   ```

## Directory Structure

After initialization, the directory contains:
```plaintext
.firebaserc
.gitignore
firebase.json
firestore.indexes.json
firestore.rules
public/
index.html
```

## Deployment

1. Deploy the project:
   ```bash
   firebase deploy
   ```

## Additional Resources

- [Firebase Documentation](https://firebase.google.com/docs/)
- [Firestore Rules Guide](https://firebase.google.com/docs/firestore/security/get-started)
