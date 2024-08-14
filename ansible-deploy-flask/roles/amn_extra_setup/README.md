## Note: for `simplegmail`

In requirements, use `simplegmail>=3.0`.

Account is `bot.association.annemarienihoul`. Go to <https://console.developers.google.com/apis/> and in "credentials", use "Create credential > OAuth Client ID". In that select "Web application" as "Application type", and in "Authorized redirect URIs", put "<http://localhost:8080/>" (with the trailing slash !!).

Save everything and download the json file as `client_secret.json`.

Then run

```bash
python -c 'from simplegmail import Gmail; Gmail()'
```

And complete the authentication process. The final URL should be something in <http://localhost:8080/> .. just use `curl` in another bash instance:

```bash
curl "http://localhost:8080/?code=*******&scope=****"
```

... Normally, you should end up with a `gmail_token.json` file.
