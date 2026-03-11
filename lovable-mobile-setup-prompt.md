Set up this Lovable React app so it can run as an installable iOS and Android mobile app using Capacitor.

Follow these requirements carefully.

1. Install Capacitor

Install the required dependencies:

npm install @capacitor/core @capacitor/cli @capacitor/ios @capacitor/android

Update package.json accordingly.


2. Initialize Capacitor

Create a capacitor.config.ts file with this configuration structure:

appId: use a placeholder like "com.yourcompany.appname"
appName: use the project name
webDir: "dist"
bundledWebRuntime: false

Do NOT hardcode a real company or domain.


3. Development Hot Reload

Add an optional Capacitor server configuration to allow hot reload during development.

Use a placeholder URL such as:

https://your-app-name.lovable.app

Clearly mark this as something the builder must update.


4. Mobile Build Scripts

Add the following scripts to package.json:

cap:sync
cap:ios
cap:android

Ensure they run:

npx cap sync
npx cap run ios
npx cap run android


5. GitHub-Friendly Setup

Ensure the repository contains:

capacitor.config.ts
package.json updates
mobile build scripts

Do NOT generate ios/ or android/ folders yet.

These should be created locally with:

npx cap add ios
npx cap add android


6. Optional Mobile UX Improvements

Add optional improvements that make the UI feel mobile-friendly:

- system-safe font stack
- touch-friendly spacing
- safe area handling for iOS

These improvements must not break the web version.


7. Documentation

Create a README section titled:

Running as a Mobile App

Include these instructions:

npm install
npm run build
npx cap add ios
npx cap add android
npx cap sync
npx cap run ios
npx cap run android


Important:
This configuration should work for any Lovable React project without requiring custom infrastructure.
