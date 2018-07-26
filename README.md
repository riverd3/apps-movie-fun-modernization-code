# Movie Fun!

## Build

### Build JAR

```bash
$ ./gradlew clean assemble
```

### Run Smoke Tests

```bash
./gradlew test
```

Smoke Tests require server running on port 8080 by default. To run against a custom URL run
```bash
$ MOVIE_FUN_URL=http://moviefun.example.com ./gradlew test
```

## Deploying to PCF

After running the build, deploy the application with
```bash
./gradlew deploy
```

Reset the entire PCF environment with
```bash
./gradlew resetPcfEnv
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


https://movie-fun-app-allk.apps.evans.pal.pivotal.io/login?code=lg1TdoZwnk&state=UC4I23

curl -Xpost https://movie-fun-app-allk.apps.evans.pal.pivotal.io/refresh --header "XSRF-TOKEN=3229ccec-42f9-490c-8c95-70e97a9dfa87" --header "JSESSIONID=EA7AB22198BAF69B79D35D44CCDC62E9"

'{\"code\": \"lg1TdoZwnk&state=UC4I23\"}'

--cookie "JSESSIONID=EA7AB22198BAF69B79D35D44CCDC62E9; __VCAP_ID__=67c45f8c-9487-40d5-6342-18c5; XSRF-TOKEN=3229ccec-42f9-490c-8c95-70e97a9dfa87"

GET /moviefun HTTP/1.1
Host: movie-fun-app-allk.apps.evans.pal.pivotal.io
User-Agent: Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:61.0) Gecko/20100101 Firefox/61.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: en-GB,en;q=0.5
Accept-Encoding: gzip, deflate, br
Referer: https://movie-fun-app-allk.apps.evans.pal.pivotal.io/
Cookie: JSESSIONID=EA7AB22198BAF69B79D35D44CCDC62E9; __VCAP_ID__=67c45f8c-9487-40d5-6342-18c5; XSRF-TOKEN=3229ccec-42f9-490c-8c95-70e97a9dfa87
Connection: keep-alive
Upgrade-Insecure-Requests: 1