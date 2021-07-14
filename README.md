# TS-GraphQL-Heroku-PostgreSQL Boilerplate
This boilerplate was created using my setup from the Trading Dashboard API

## Local Installation

1. Clone project

```
git clone github_url
```

2. cd into folder

```
cd app_name
```

3. Download npm packages

```
yarn
```

4. Start PostgreSQL server

5. Create database called `database_name` (from outside psql command line utility)

```
createdb database_name
```

6. Add a user with the username `postgres` and password `admin`. You can choose your own username and password but be sure to specify them in the .env file.

7. Connect to the database with psql and add the uuid extension:

```
CREATE EXTENSION IF NOT EXISTS "uuid-ossp";
```

8. Install Redis

```
brew install redis
```

9. Start Redis

```
brew services start redis
```

10. Create a filed named `.env` that has the environment variables listed in .env.example. For example:

```
DATABASE_URL=postgresql://username:password@localhost:5432/database_name
REDIS_URL=127.0.0.1:6379
PORT=4000
SESSION_SECRET=my_secret
CORS_ORIGIN=http://localhost:3000
```