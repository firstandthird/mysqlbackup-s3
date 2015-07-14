#mysqlbackup-s3

A simple docker container to backup a mysql db to s3.  Easy to integrate with cron.

## Usage

### Backup

```
docker run --rm --link mysql:mysql --env AWS_ACCESS_KEY_ID=123 --env AWS_SECRET_ACCESS_KEY=123 --env S3BUCKET=bucket --env DB=db --env PREFIX=backup firstandthird/mysqlbackup-s3 "backup"
```

### Restore
```
docker run --rm --link mysql:mysql --env AWS_ACCESS_KEY_ID=123 --env AWS_SECRET_ACCESS_KEY=123 --env S3BUCKET=bucket --env DB=db firstandthird/mysqlbackup-s3 "db-file.sql.gz"
```
