# Simple

## Prerequisites

- Make sure docker and docker-compose is available
- Make sure nothing is running on port 8080, 8090 and 3306
  - If necessary, adjust the exposed ports on docker-compose.yml file

## Make sure you have the latest images

```
docker-compose pull
```

## Run the stack

```
docker-compose up -d
```

> NOTE: Making requests or trying to authenticate at this point will raise errors, because the database is not installed.

## Install the database and user

Using a specific email and password

```
docker-compose run api install --email your@email.com --password somepass
```

Using a specific email and a random password

```
docker-compose run api install --email your@email.com
```

Using default email (admin@example.com) and a random password

```
docker-compose run api install --password somepass
```

## Accessing

- [api at http://localhost:8080/](http://localhost:8080/)
- [app at http://localhost:8090/](http://localhost:8090/)
