# react-avancado-landing-api

Strapi API created for Advanced React landing page

## Useful postgres cmds on docker

Backup specific database:

```bash
docker exec -i database pg_dump --u postgres DATABASE_NAME_HERE > DUMP_`date +%d-%m-%Y"_"%H_%M_%S`.sql
```

Backup all databases:

```bash
docker exec -t -u postgres CONTAINER_NAME_HERE pg_dumpall -c > DUMP_`date +%d-%m-%Y"_"%H_%M_%S`.sql
```

Restore file:

```bash
cat YOUR_FILE.sql | docker exec -i CONTAINER_NAME_HERE psql -U USER_NAME_HERE -d DATABASE_NAME_HERE
```

Example:

```bash
cat strapi.sql | docker exec -i postgres_container psql -U strapi -d strapi
```
