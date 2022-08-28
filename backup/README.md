## Docker-compose.yml
```
version: '3.1'
services:
  db:
    image: postgres
    restart: always
    environment:
      POSTGRES_USER: airflow
      POSTGRES_PASSWORD: airflow
      POSTGRES_DB: airflow_db
    volumes:
      - pg_data_volume:/var/lib/postgresql/data
volumes:
  pg_data_volume:
```

## Backup Command
```
~/dev/postgres ❯ docker run --rm --volumes-from postgres_db_1 -v $(pwd):/backup ubuntu tar cvf /backup/backup.tar /var/lib/postgresql/data
```

## Restore Command
```
~/dev/postgres ❯ docker run --rm --volumes-from postgres_db_1 -v $(pwd):/backup ubuntu bash -c "cd /var/lib/postgresql/data && rm -rf * && tar xvf /backup/backup.tar --strip 4"
```
