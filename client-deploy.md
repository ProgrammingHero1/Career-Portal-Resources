# Deployment Steps on Firebase

### REASONS THAT FIREBASE MAY REMOVE YOUR APPLICATION

- If your Website and Content Doesn't match with your URL & TITLE
- If you console important credentials such as
  - user
  - passwords
  - API Keys / objects that contain important info's
- If Your API Does not Provide Valid name matched with your content

## DO Following Things First

- Give your Website a Title , Logo matches with your content
- Comment the your important credentials log
- Define Meta tags to keep it more understable to Web Engine
- See Below snippet

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link
      rel="shortcut icon"
      href="https://img.icons8.com/?size=160&id=2zhQitqbq98h&format=png"
      type="image/x-icon"
    />
    <meta
      name="description"
      content="Manage job postings effortlessly with JobPortal. Create, read, update, and delete job listings in a user-friendly, responsive web application."
    />
    <meta
      name="keywords"
      content="Job-Portal Career-Portal Jobs engineering-jobs react daisyui"
    />
    <meta name="author" content="Jhankar Mahabub" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>CAREER</title>
  </head>
  <body>
    <div id="root"></div>
    <script type="module" src="/src/main.jsx"></script>
  </body>
</html>
```

### Deployment Steps-1 : FIREBASE INIT

```bash
firebase init
```

this command will give you a CLI interface for create additional files that needed for deployment. Firebase will ask you some questions . such as

```bash
Are you ready to proceed? (Y/n) -> y



Which Firebase features do you want to set up for this directory? Press Space to select features, then Enter to
confirm your choices. (Press <space> to select, <a> to toggle all, <i> to invert selection, and <enter> to proceed)
 ( ) Data Connect: Set up a Firebase Data Connect service
 ( ) Firestore: Configure security rules and indexes files for Firestore
 ( ) Genkit: Setup a new Genkit project with Firebase
 ( ) Functions: Configure a Cloud Functions directory and its files
 ( ) App Hosting: Configure an apphosting.yaml file for App Hosting
 >(*) Hosting: Configure files for Firebase Hosting and (optionally) set up GitHub Action deploys
 ( ) Storage: Configure a security rules file for Cloud Storage



  ? What do you want to use as your public directory? dist

  ? Configure as a single-page app (rewrite all urls to /index.html)? y

  ? Set up automatic builds and deploys with GitHub? n

#   Additionaly This can appear if you have build it allready
  ? File dist/index.html already exists. Overwrite? n

```

### Deployment Steps-2 : Build Application

Remember , You are working on Dev mode . when you build your project, every js and css converted into a single js && css file on dist/assets folder. and every file you stored in public will copy to dist. and files/folder on assets also copied to dist.

- Do the command toi build your application For Production

```bash
npm run build
```

### Deployment Steps 3: Deploy your Application

```bash
firebase deploy
```

## YAHOO 😎 Deployment Done

## Redeploy System

- for any code changes .

```bash
npm run build
firebase deploy
```

# Deployment Steps on NETLIFY

### Deployment Steps-1 : Add Redirects

- Add Redirects to validate Routes

```bash
/*    /index.html   200
```

### Deployment Steps-2 : Build Application

```bash
npm run build
```

### Deployment Steps-3 : Drag and Deploy

Go to [https://app.netlify.com/drop](https://app.netlify.com/drop)

- Drop your Dist Folder
  <img src="https://i.ibb.co.com/qjbVKGQ/Screenshot-4.jpg" />

### Deployment Steps-4 : change Site-Name According to Your Website

<img src="https://i.ibb.co.com/k06s5hM/image.png">

### Deployment Steps-4 : Add Domain on Firebase for Auth Authorization

<img src="https://i.ibb.co.com/RbCYpL0/image.png">

## YAHOO 😎 Deployment Done

## Redeploy System

- for any code changes .

```bash
npm run build
```

Now Drop your Dist Folder to Netlify

# Deployment Steps on SURGE

### Deployment Steps-1 : Create CNAME on Public

Add Your Domain like this --> yourdomain.surge.sh

### Deployment Steps-2 : Build your Project

```bash
npm run build
```

### Deployment Steps-3 : Set up 200.html on Dist

- copy code from your [dist/index.html]("/dist/index.html")
- create new file 200.html on dist and paste code of index.html

run this command

```bash
surge dist
```

It will deploy automatically

### Deployment Steps-4 : Add Domain on Firebase for Auth Authorization

## YAHOO 😎 Deployment Done

## Redeploy System

Do Steps 2,3,4
