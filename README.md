# sqlite2postgresql-sample

## Procedure

```
$ docker compose up -d

$ curl -L -O https://www.sqlitetutorial.net/wp-content/uploads/2018/03/chinook.zip
$ unzip chinook.zip && rm chinook.zip
$ mv chinook.zip share

$ docker compose exec -it node-1 bash
$ cd /opt
$ apt update && apt-get install pgloader
$ pgloader --version

$ pgloader ./chinook.db postgresql://postgres:password@127.0.0.1:5432/chinook

$ psql -U postgres;
$ \c chinook;
$ \d;
$ SELECT * from artists;

# You can also migrate from mysql to postgresql.
$ pgloader mysql://user@192.168.1.2/chinook postgresql://postgres:password@127.0.0.1:5432/chinook
```
