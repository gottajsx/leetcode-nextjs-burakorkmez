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
