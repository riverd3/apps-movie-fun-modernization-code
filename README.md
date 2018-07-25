# Movie Fun!

## Tests

Smoke Tests require server running on port 8080 by default.

### Build JAR ignoring tests

```bash
$ ./gradlew clean build -xtest
```

### Run Smoke Tests against specific URL

```bash
$ MOVIE_FUN_URL=http://moviefun.example.com ./gradlew test
```

## Migrations

Create databases needed for local development with

```bash
mysql -uroot < databases/create_databases.sql
```

Run local migrations with

```bash
./gradlew flywayMigrate
```

Run migrations on the PCF environment which you're logged in to with

```bash
CF_MIGRATE=true ./gradlew cfMigrate
```

curl -k "https://p-identity.login.sys.evans.pal.pivotal.io/oauth/token" -i -u "0c51e3e8-69a8-4801-a803-06dc25577b9d:9e5675fb-f059-4b5c-a360-a22eba7e1da3" -X POST -H 'Accept: application/json' -H 'Content-Type: application/x-www-form-urlencoded' -d 'grant_type=client_credentials&response_type=token'

curl -k "https://p-identity.login.sys.evans.pal.pivotal.io/oauth/token" -i -u "0c51e3e8-69a8-4801-a803-06dc25577b9d:9e5675fb-f059-4b5c-a360-a22eba7e1da3" -X POST -H 'Accept: application/json' -H 'Content-Type: application/x-www-form-urlencoded' -d 'grant_type=client_credentials&response_type=token'

curl -k "https://p-identity.login.sys.evans.pal.pivotal.io/oauth/token" -i -u "user:password" -X POST -H 'Accept: application/json' -H 'Content-Type: application/x-www-form-urlencoded' -d 'grant_type=client_credentials&response_type=token'



   "client_id": "0c51e3e8-69a8-4801-a803-06dc25577b9d",
     "client_secret": "9e5675fb-f059-4b5c-a360-a22eba7e1da3"


https://movie-fun-app-allk.apps.evans.pal.pivotal.io/login


https://movie-fun-app-allk.apps.evans.pal.pivotal.io/login?code=rKohJhUPYt&state=3neBoc


curl -k https://p-identity.login.sys.evans.pal.pivotal.io/oauth/authorize?client_id=0c51e3e8-69a8-4801-a803-06dc25577b9d&redirect_uri=https://movie-fun-app-allk.apps.evans.pal.pivotal.io/login&response_type=code&state=1NDuML

https://movie-fun-app-allk.apps.evans.pal.pivotal.io/login?code=tO7EQbA6yv&state=lvPeV1

cd ~/workspace/assignment-submission
./gradlew modernizationSecurity -PmovieFunUrl=https://movie-fun-app-allk.apps.evans.pal.pivotal.io -PuaaUsername=user -PuaaPassword=password