# DBコンテナ

## ネットワークを作る（作ってなかったら）

`docker network create --driver bridge shared`

## .envファイルを準備
```
MYSQL_ROOT_PASSWORD=hoge
MYSQL_PORT=3333
POSTGRES_PASSWORD=hoge
POSTGRES_PORT=5555
MONGO_PORT=22222
MONGO_INITDB_ROOT_USERNAME=hoge
MONGO_INITDB_ROOT_PASSWORD=hoge

```

## バックグランドで起動

`docker-compose up -d`


# カスタムのcnfファイルを追加

```
ADD mysqld.cnf /etc/mysql/conf.d/
RUN	chmod 644 /etc/mysql/conf.d/mysqld.cnf
```
