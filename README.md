# Parcel bundling

## How to run

- `npm install`
- `npm start`

Now parcel will start a local development server (usually on http://localhost:1234)

## Project structure

In the src folder you put your HTML files and your SASS files.

Parcel detects SASS files imported in your HTML files and translates them to CSS files automagically!

Herefore you can directly import the SCSS files in your HTML like so:

```
  <link rel="stylesheet" href="./styles/home.scss">
```

Make sure to always use RELATIVE paths in the stylesheet links (so paths starting with ./ or ../ like above)

Once you run "npm start" this command will run `npx parcel src/index.html`.

Parcel now scans the index.html files for SCSS or JavaScript files, translates them and stores all generates files in folder with the name `dist`.

## Deployment to Github Pages

If you want to use this project as a template: 
Simply grab the repo content as ZIP folder, unpack it to a folder on your local machine and upload this folder to your own GitHub repository.

The generated "dist" folder will be the folder that we need to deploy to GitHub (or any other provider).

Ideally you test to run this server LOCALLY on your machine first, so detect any deployment issues early.

Therefore simply open the "dist" folder using e.g. Live-Server in VsCode (but do not run live-server in the main folder, this will not work! Make sure you run it in the dist folder!)

If this is working and you see, your SASS styles are applied, we can perform the deployment to GitHub pages.

Simply perform:
`npm run deploy`

This will use the gh-pages package deploy the generated dist folder to the gh-pages branch of your repository.
GitHub will automatically pickup that branch and will deploy it.

You can check the deployment in your GitHub Repo > Settings > Section "Pages" on the left.

If the deploy URL is not visible yet at the top, GitHub is still deploying your project. 

Simply wait 1-5 minutes and reload, then usually the deployment is finished and the URL will appear.

Enjoyyyy deploying like there is no mornin! Yay!

