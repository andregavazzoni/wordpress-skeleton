# Install

`$ git clone REPO PATH`
`$ cd PATH`
`$ cp .env.example .env`

Edit `.env` DB_*

`$ vendor/bin/wp server`

Access localhost:8080 and complete install.

# Use Docker

Edit `.env`:

```
DB_NAME=docker
DB_USER=docker
DB_PASSWORD=docker
DB_HOST=docker-db
DB_CHARSET=
DB_COLLATE=
```
Run with docker-compose:

`$ docker-compose up`

Access http://localhost or http://127.0.0.1 or http://wordpress.pc