# Profile FE

## Testing

```bash
npm test
```

## Local Run

Set up your development environment

```bash
npm install
cp .env.template .env.development
```

Provide correct values in `.env.development` : `http://workspace_ip:8082/entries`. Note that you need to replace the `workspace_ip` in the string with the actual public IP of your workspace. This is the Backend API endpoint to which the Frontend should make a POST request, with the contact form entry data that’ll get stored in the Backend. Proceed with local run:

```bash
npm start
```

## Deployment

Similar to `.env.development`, create a `.env.production` file with necessary variables. Just like we provided the BACKEND_URL environment variable in the `.env.development`, set the value in `.env.production` as `https://<backend_host_on_heroku>/entries`, where the `backend_host_on_heroku` is your backend website deployed on Heroku.

Sign up for Netlify and install Netlify CLI

```bash
netlify login
```

Proceed with deployment:
```bash
npm run-script build
netlify deploy --dir=public --prod
```

The Projects section code is executed every time the webpage is loaded. The code structure resembles the following:
    Make REST API call to Github using the GITHUB_TOKEN environment variable.
    If the API call succeeds and data has been fetched, display the Projects section, otherwise hide it.

We can check that the entries made on the FrontEnd are being stored in the Backend by using `curl https://<backend_host_on_heroku>/entries` which will return the list of all contact details submitted.