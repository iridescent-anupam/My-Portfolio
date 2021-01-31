# Profile Backend

Provide the PORT variable using echo PORT=8082 > .env. The server will pick up the port number from this file (.env), which is used for environment variables

## Testing

```bash
npm test
```

## Local Run

```bash
npm install && npm start
```

## Deployment

After signing up on Heroku, create a new app, and proceed to download Heroku CLI

```bash
heroku login -i
heroku builds:create -a <name_of_your_app>
```

You can now go to the URL shown in your output from your browser or call it with curl and it should display "Hello from the profile backend!"

## Changes upon deployment

If working in a new workspace, clone the repository first :

```bash
heroku git:clone -a <name_of_your_app>
cd <name_of_your_app>
```

Make some changes to the code you just cloned or if they're already there, deploy them to Heroku using Git.

```bash
git add .
git commit -am "changes message"
git push heroku master
```