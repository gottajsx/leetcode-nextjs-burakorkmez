## Project creation

```bash
npx create-next-app@latest --typescript
```
* *project named ?* xxx 
* *ESLint ?* Yes
* *src directory ?* Yes
* *experimental app directory ?* No
* *import alias ?* @/*

## Tailwind CSS

Install Tailwind:
```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```
Then, as expected in [official documentation](https://tailwindcss.com/docs/guides/nextjs), modify `tailwind.config.js`:
```javascript
module.exports = {
  content: [
    "./app/**/*.{js,ts,jsx,tsx,mdx}",
    "./pages/**/*.{js,ts,jsx,tsx,mdx}",
    "./components/**/*.{js,ts,jsx,tsx,mdx}",
 
    // Or if using `src` directory:
    "./src/**/*.{js,ts,jsx,tsx,mdx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

Also modify `globals.css`:
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

## Firebase Setup

Go to [firebase console](https://console.firebase.google.com) to create related project

Add Firebase to the Nextjs project with:
```bash
npm install firebase
```

Create the `.env.local` file that contains values for:
```javascript
NEXT_PUBLIC_FIREBASE_API_KEY=
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=
NEXT_PUBLIC_FIREBASE_PROJECT_ID=
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=
NEXT_PUBLIC_FIREBASE_APP_ID
```

## Start Application

Start the application in development mode using:
```bash
npm run dev
```