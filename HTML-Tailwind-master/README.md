# Things you will need to have installed:

- VS code (or editor of your choice but it might be harder to follow without it)
  `https://code.visualstudio.com/Download`

- Latest version of Node JS.
  `https://nodejs.org/en/`
  (I'm currently using node version 19 )

useful extensions:

`https://marketplace.visualstudio.com/items?itemName=bradlc.vscode-tailwindcss`

`https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer`

## How I made this?

1. I created a package.json file by using the command `npm init` then fulling out the details in the prompts or just pressing enter until you go back to the normal window terminal.

   `(NB) you can always edit the file later`

2. next in your Terminal run: `npm install -D tailwindcss`.

   This will download the node_modules folder for you and give you the package-lock.json file.

3. next step run this command: `npx tailwindcss init`.

   Once you've run this command you need to specify the path to your html within your tailwind.config.js add this `"./src/**/*.{html,js}"` to the content section within the `[]`.

   Once you have done the above. Create a file named `dist` within the root of your application and create your `index.html` file

4. next step is to create a `src folder` then create a file in their called `input.css` then at the top of the file and add: `@tailwind base;`
   `@tailwind components;`
   `@tailwind utilities;`

   then run this in your terminal:
   `npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch`

5. once you have run this you'll notice a new CSS file in the `dist` folder called `output.css`

6. Once you have followed all of the above steps run: `npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch` in your Terminal and make your project live so that you can work with it in real time.

( NB: To make step 6 a lot easier, go into your package.json file and in your scripts section after test add `"dev": "tailwindcss -i ./src/input.css -o ./dist/output.css --watch"` and then before you make your project live run `npm run dev` in your command line)

## Housekeeping!

Within the dist folder I personally like to layout the structure of my application with an asset folder (to keep all assets live images ect) and create two more folders one for all of my JS files and one for my pages.
additionally I added a global CSS file that I usually like to have to add some custom CSS if I want to my Tailwind - You can fully customize your Tailwind within the config file if you want however I have a habit of doing things this way and old habits die hard.

## Pomadoro timer base project

start out by
