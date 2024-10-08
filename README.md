## Project Creation

Create the project using `npx` command as following:
```bash
npx create-next-app@latest --ts
```

* *project named ?* xxx 
* *ESLint ?* Yes
* *src directory ?* Yes
* *experimental app directory ?* No
* *import alias ?* @/*


## Tailwind Installation

Install Tailwind module with
```bash
npm install -D tailwindcss postcss autoprefixer
```

Init Tailwind module with:
```bash
npx tailwindcss init -p
```

Then, as expected in [official documentation](https://tailwindcss.com/docs/guides/nextjs), configure the template path by modifying `tailwind.config.js`

Also modify the `globals.css` file with following:
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```
## Start Application

Start the application in development mode using:
```bash
npm run dev
```

## Firebase Setup

Go to [firebase console](https://console.firebase.google.com)

Create a project `leetcode-yt`

Add Firebase to the web app after project has been created.

Add Firebase to the project with:
```bash
npm install firebase
```

Create the `firebase.ts` configuration file that contains:
```javascript
import { initializeApp, getApp, getApps } from "firebase/app";
import { getAuth } from "firebase/auth";
import { getFirestore } from "firebase/firestore";

const firebaseConfig = {
	apiKey: process.env.NEXT_PUBLIC_FIREBASE_API_KEY,
	authDomain: process.env.NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN,
	projectId: process.env.NEXT_PUBLIC_FIREBASE_PROJECT_ID,
	storageBucket: process.env.NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET,
	messagingSenderId: process.env.NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID,
	appId: process.env.NEXT_PUBLIC_FIREBASE_APP_ID,
};

const app = !getApps.length ? initializeApp(firebaseConfig) : getApp();

const auth = getAuth(app);
const firestore = getFirestore(app);

export { auth, firestore, app };
```
Create the `.env.local` file that contains values for:
```
NEXT_PUBLIC_FIREBASE_API_KEY=
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=
NEXT_PUBLIC_FIREBASE_PROJECT_ID=
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=
NEXT_PUBLIC_FIREBASE_APP_ID
```
Inside firebase console, create a firestore database for the project. Database rules may be modified later

