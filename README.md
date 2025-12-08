# Dockerized Next.js Dashboard Tutorial

Since the original tutorial does not provide instruction for local development, here is the project for Docker and Postgres 18.

## Instructions

Create an .env.local file:

```
POSTGRES_URL="postgres://<your postgres username>:<your DB password>@next_db:5432/next_db"
POSTGRES_USER="<your postgres username>"
POSTGRES_HOST="next_db"
POSTGRES_DATABASE="next_db"
... (other credentials) 
``` 

Build with:
```
docker compose build --no-cache
```

Start with:
```
docker compose up
```

## Troubleshooting 
- docker compose up throw message: mkdir: cannot create directory ‘/var/lib/postgresql/18’: Permission denied

<b>  Solution: </b> Add permissions to /data

- http://localhost:3000/seed throw PostgresError: "Key (extname)=(uuid-ossp) already exists."

<b>  Solution: </b> Refresh (F5) page.

## About the tutorial

For more information, see the [course curriculum](https://nextjs.org/learn) on the Next.js Website.
