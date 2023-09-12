# Nest Full Starter

Nest.js + PostgreSQL API with TypeORM.

This project was bootstrapped with [Nest.js](https://nestjs.com/).

## Features

- PostgreSQL database management with TypeORM
- Users management with roles and statuses
- Auth with Passport (JWT strategy & refresh strategy)
- Auth sign in and sign up with email and social (Google, Facebook, Apple and Twitter)
- Database management, migrations and seeds
- Multi languages with I18N
- Infinity pagination
- Send mails with node-mailer
- Mail templates
- File upload (Local and Amazon S3)
- Units and E2E Testing with Jest + Supertest
- Docker
- CI Github
- Swagger documentation

## Installation

This is a [Node.js](https://nodejs.org/en/) module available through the [npm registry](https://www.npmjs.com/).\
Before installing, [download and install Node.js](https://nodejs.org/en/download/).\
Node.js 0.10 or higher is required.

### Cloning the repository

```console
git clone https://github.com/nrocchi/nest-full-starter.git
```

### Run Docker container

```console
docker compose up -d postgres adminer maildev
```

### Install packages

Installation is done using the [`npm install` command](https://docs.npmjs.com/getting-started/installing-npm-packages-locally):

```console
npm install
```

### Run the migrations

```console
npm run migration:run
```

### Run the seeds

```console
npm run seed:run
```

### Start the application

Starting the app is done using the `npm run start` command:

```console
npm run start
```

## Available Scripts

Run the app in the watch mode.

```console
npm run start:dev
```

Run the app in the production mode.

```console
npm run start:prod
```

Generate migration.

```console
npm run migration:generate -- src/database/migrations/CreateNameTable
```

Run migration.

```console
npm run migration:run
```

Revert migration.

```console
npm run migration:revert
```

Drop all tables in database.

```console
npm run schema:drop
```

Run seed.

```console
npm run seed:run
```

Run the unit tests.

```console
npm run test
```

Run the e2e tests.

```console
npm run test:e2e
```

Run the test coverage.

```console
npm run test:cov
```

Run the tests in Docker.

```console
docker compose -f docker-compose.ci.yaml --env-file env-example -p ci up --build --exit-code-from api && docker compose -p ci rm -svf
```

Run the test benchmarking.

```console
docker run --rm jordi/ab -n 100 -c 100 -T application/json -H "Authorization: Bearer USER_TOKEN" -v 2 http://<server_ip>:3000/api/v1/users
```

Check the Docker logs.

```console
docker compose logs
```

## Links

- Swagger: <http://localhost:4000/docs>
- Adminer: <http://localhost:8080>
- Maildev: <http://localhost:1080>

## Nest.js Documentation

[https://docs.nestjs.com/](https://docs.nestjs.com/)

## Contributors

The original author is [Nicolas Rocchi](https://github.com/nrocchi).
