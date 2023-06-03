# StockMarket - Users module

An API for stock market to manage users and authenticate

## Installation

```bash
   $ npm install
```

## Set Enviroment for secret key JWT and other configurations

```bash
   $ cp .env.example .env
```

## Config settings .env for send notification when a user registers, forgot password or change password
You can use https://mailtrap.io - platform for email testing
```
   EMAIL_HOST=smtp.mailtrap.io
   EMAIL_PORT=2525
   EMAIL_AUTH_USER=[:user]
   EMAIL_AUTH_PASSWORD=[:password]
   EMAIL_DEBUG=true
   EMAIL_LOGGER=true
   EMAIL_LAYOUT_DIR='templates/emails/'
   EMAIL_PARTIAL_DIR='templates/emails/'
   EMAIL_VIEW_PATH='/templates/emails/'
   EMAIL_DEFAULT_LAYOUT='index'
```

## Config settings .env for connect MySQL

Once the database has been configured, start the Nest App via `npm run start:dev` it automatically synchronizes the entities so ready to use. :heart_eyes_cat:

```
   TYPEORM_CONNECTION = "mysql"
   TYPEORM_HOST = "localhost"
   TYPEORM_PORT = 3306
   TYPEORM_USERNAME = [:user]
   TYPEORM_PASSWORD = [:password]
   TYPEORM_DATABASE = [:database]
   TYPEORM_AUTO_SCHEMA_SYNC = true
   TYPEORM_ENTITIES = "dist/**/*.entity.js"
   TYPEORM_SUBSCRIBERS = "dist/subscriber/**/*.js"
   TYPEORM_MIGRATIONS = "dist/migrations/**/*.js"
   TYPEORM_ENTITIES_DIR = "src/entity"
   TYPEORM_MIGRATIONS_DIR = "src/migration"
   TYPEORM_SUBSCRIBERS_DIR = "src/subscriber"
```

## Running the app

```bash
    # development
    $ npm run start

    # watch mode
    $ npm run start:dev

    # production mode
    $ npm run start:prod
```