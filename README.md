# Universal Links Setup for Cognito App

This repository hosts the Universal Links configuration for the Cognito iOS app.

## Setup Instructions

1. **Create a new GitHub repository** (e.g., `cognito-universal-links`)
2. **Upload these files** to the repository:
   - `index.html`
   - `.well-known/apple-app-site-association`
3. **Enable GitHub Pages**:
   - Go to Settings → Pages
   - Source: Deploy from a branch
   - Branch: main/master
4. **Note your GitHub Pages URL** (e.g., `https://username.github.io/cognito-universal-links`)

## Universal Links Testing

Once deployed, your Universal Links will be:

- **OAuth Callback**: `https://yourusername.github.io/cognito-universal-links/callback?code=123&state=xyz`
- **Auth Login**: `https://yourusername.github.io/cognito-universal-links/auth/login`

## App Configuration

The iOS app is configured to handle these domains:
- **Team ID**: `8D26Y9S2HV`
- **Bundle ID**: `im.pencil.cognito`
- **Supported paths**: `/callback*`, `/auth/*`, `/oauth/*`

## How it Works

1. User taps Universal Link (e.g., from WhatsApp, Safari, etc.)
2. iOS checks the `.well-known/apple-app-site-association` file
3. If the app is installed, it opens the app
4. If not installed, it opens the website

## Testing

1. Install the Cognito app on your device
2. Open Safari and visit: `https://yourusername.github.io/cognito-universal-links/callback?code=test123`
3. The app should open instead of staying in Safari