# OYE4PF Social Hub - Complete Setup Guide

## What's New ✨

Your website now has **user authentication** with:
- ✅ Sign-up & Login modals
- ✅ Firebase authentication (no backend server needed)
- ✅ Protected features (users must login to access)
- ✅ User profile display
- ✅ Logout functionality

## Setup Instructions

### Step 1: Set Up Firebase Project

1. Go to https://firebase.google.com/
2. Click "Get Started" and create a new project
3. Name it "oye4pf-social-hub" (or your preferred name)
4. Enable Email/Password authentication:
   - Go to **Build > Authentication**
   - Click "Get Started"
   - Enable "Email/Password"

### Step 2: Get Firebase Configuration

1. In Firebase Console, go to **Project Settings** (gear icon)
2. Copy your Firebase config:
   ```
   apiKey
   authDomain
   projectId
   storageBucket
   messagingSenderId
   appId
   ```

### Step 3: Update app.js

Replace the placeholder values in `app.js` (lines 1-10) with your Firebase config:

```javascript
const firebaseConfig = {
    apiKey: "YOUR_API_KEY_HERE",
    authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
    projectId: "YOUR_PROJECT_ID",
    storageBucket: "YOUR_PROJECT_ID.appspot.com",
    messagingSenderId: "YOUR_SENDER_ID",
    appId: "YOUR_APP_ID"
};
```

### Step 4: Test the Features

1. Upload all files to your GitHub repository
2. Visit your website: https://oyedijimicheal3-design.github.io/oye4pf-social-hub/
3. Test:
   - Click "Sign Up" button
   - Create a new account
   - Click "Login" button
   - Login with your account
   - Try clicking "View Details" on services
   - Click "Logout"

## File Structure

- `index.html` - Updated with login/signup modals
- `style.css` - Updated with modal and authentication styles
- `app.js` - New file with Firebase authentication logic

## Features Explained

### 1. Sign Up
- Users enter: Name, Email, Password, Confirm Password
- Passwords validated (must be 6+ characters and match)
- Account created in Firebase

### 2. Login
- Users login with Email & Password
- After login, buttons change to show user email and logout option

### 3. Protected Features
- All "View Details" buttons require login
- Users get alert if not logged in
- Pricing plans also require login

### 4. Logout
- Users can logout anytime
- UI resets to show login/signup buttons

## Security Notes

- **Never commit your Firebase config with real keys** in production
- Firebase provides built-in security
- Passwords are hashed and encrypted
- Use Firebase Rules for database security (advanced)

## Next Steps (Advanced)

To add MORE functionality:

1. **Database Storage** - Save user data beyond Firebase
2. **Payment Integration** - Stripe or PayPal for pricing
3. **Email Verification** - Send confirmation emails
4. **Social Login** - Google, GitHub login
5. **Backend Server** - Node.js/Express (if you want more control)

## Support

For more info on Firebase Authentication:
https://firebase.google.com/docs/auth

For Node.js/Express backend setup (Option 2):
Check server.js documentation

For any issues, contact: support@oye4pf.com
