#mysqlbackup-s3

A simple docker container to backup a mysql db to s3.  Easy to integrate with cron.


## Installation

```
docker build -t mysqlbackup-s3 git://github.com/firstandthird/mysqlbackup-s3.git
```

## Usage

```
docker run --rm --link mysql:mysql --env AWS_ACCESS_KEY_ID=123 --env AWS_SECRET_ACCESS_KEY=123 --env S3BUCKET=bucket --env DB=db --env PREFIX=backup mysqlbackup-s3
```
