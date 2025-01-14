# Vanilla-js-OAuth

### Overview

This is a starter app that is to be used with the Getting Started with OAuth and JavaScript [YouTube tutorial](https://www.youtube.com/watch?v=E0GwNBFVGik). It implements a very basic version of a Plaid-powered application using HTML/VanillaJS on the front end, and NodeJS/Express on the backend.

### Running the app

If you want the most complete instructions for running the app, please follow along with the video tutorial linked above.

#### Clone the repo

Clone the tutorial resources repo to your machine and cd into the project's start directory:

```bash
git clone https://github.com/plaid/tutorial-resources && cd vanilla-js-oauth/start/
```

#### Equip the app with credentials

Copy the included **.env.example** to a file called **.env**.

```bash
cp .env.example .env
```

Fill out the contents of the **.env** file with the [client ID and Sandbox secret in your Plaid dashboard](https://dashboard.plaid.com/team/keys). Don't place quotes around the credentials. Use the "Sandbox" secret when setting the `PLAID_SECRET` variable.

#### Build and Start the server
The app is self-contained in a docker container. Start by building the image:

```bash
docker build --tag plaid-oauth .
```

Then start the app by running the following command:

```bash
docker run -it -p 8000:8000 --rm plaid-oauth
```

The server will start running on port 8000. To use the app, navigate to `localhost:8000` in your browser.

### Troubleshooting

#### MISSING_FIELDS error

If you encounter a **MISSING_FIELDS** error, it's possible you did not properly fill out the **.env** file. Be sure to add your client ID and Sandbox secret to the corresponding variables in the file.
