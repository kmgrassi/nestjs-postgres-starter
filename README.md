# Nestjs Postgres API starter repo

## Includes
1. [NestJS] (https://nestjs.com/)
2. TypeScript
3. [TypeORM] (https://typeorm.io/#/)
4. Postgres db config setup

## Setup
1. Clone repo `git clone https://github.com/kmgrassi/nestjs-postgres-starter.git`
2. Run command `npm install`
3. Setup postgres on your local machine ([tutorial])(https://www.postgresqltutorial.com/install-postgresql) and start server
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
See this [blog post]("https://medium.com/") for heroku deployment walk through 

Deploy to heroku
1. Set up [heroku CLI](https://devcenter.heroku.com/articles/heroku-cli) (if you don't have it installed)
2. Set up github [auto-deploy](https://devcenter.heroku.com/articles/github-integration)
3. Make sure the Procfile has the following command to run start: `web: node dist/api/main.js` (if you cloned this repo it's there)
4. Provision postgres addon in heroku: `heroku addons:create heroku-postgresql:hobby-dev` (in command line in root directory)
5. Find db credentials: heroku pg:credentials:url or click on the db instance in heroku → will open a db gui → settings → database credentials
6. Copy the credentials into the heroku config variables
7. Fix ssl error in the app.module file: 
`ssl: config.get("ENV") === "development" ? false : { rejectUnauthorized: false}`

