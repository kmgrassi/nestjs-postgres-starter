# Nestjs Postgres API starter repo

## Includes
1. [NestJS] (https://nestjs.com/)
2. TypeScript
3. [TypeORM] (https://typeorm.io/#/)
4. Postgres db config setup

## Setup
1. Clone repo `git clone https://github.com/kmgrassi/nestjs-postgres-starter.git`
2. Run command `npm install`
3. Setup postgres on your local machine ("https://www.postgresqltutorial.com/install-postgresql/") and start server
4. Rename `.env-example` in api to `.env` with the following postgres database properties that you will connect to for local development
    * DB_HOST="localhost"
    * DB_PORT=5432
    * DB_USER="*user_name*"
    * DB_PASSWORD=""
    * DB_DATABASE="*db_name*"
    * ENV="development"
5. Run command `npm run start:dev`
***

## Starting, Debugging, or Testing
1. Refer to `package.json` scripts
***

## Deployment
TODO

