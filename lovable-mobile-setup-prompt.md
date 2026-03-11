Set up this Lovable React app to run as a native mobile app using Capacitor so it can be distributed on iOS and Android.

Follow these requirements carefully.

1. Install Capacitor

Add the following dependencies to the project:

@capacitor/core  
@capacitor/cli  
@capacitor/ios  
@capacitor/android

Update package.json accordingly.


2. Initialize Capacitor

Create a capacitor.config.ts file with this structure:

- appId: use a placeholder like "com.yourcompany.appname"
- appName: use the project name
- webDir: "dist"
- bundledWebRuntime: false

Do NOT hardcode a specific company or domain.


3. Development Hot Reload

Add an optional Capacitor server configuration that allows hot reload during development.

The URL should be a placeholder such as:

https://your-app-name.lovable.app

This should be clearly marked as a value the builder must update.


4. Mobile Build Scripts

Add scripts to package.json for mobile builds:

cap:sync  
cap:ios  
cap:android

Ensure these scripts run:

npx cap sync  
npx cap run ios  
npx cap run android


5. GitHub-Friendly Setup

Ensure the repository includes:

capacitor.config.ts  
package.json updates  
mobile build scripts

Do NOT generate ios/ or android/ folders yet because those are created locally with:

npx cap add ios  
npx cap add android


6. Optional Mobile UX Improvements

Add optional improvements that make the app feel more native:

- System-safe font stack
- Platform spacing conventions
- Touch-friendly layout
- Safe area handling for iOS

These should not break the web version.


7. Documentation

Create a README section titled:

"Running as a Mobile App"

Include instructions:

npm install  
npm run build  
npx cap add ios  
npx cap add android  
npx cap sync  
npx cap run ios  
npx cap run android


Important:
This setup should work for any Lovable React project without requiring custom infrastructure.
