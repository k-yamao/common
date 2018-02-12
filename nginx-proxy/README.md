# nginx-proxy

## ネットワークを作る

`docker network create --driver bridge shared`

## バックグランドで起動

`docker-compose up -d`

## Let’s Encryptで証明書が取得できてるか確認する

* nginx-proxyのコンテナに入る

  `docker exec -it nginx-proxy /bin/bash`

* 証明書を取得して設置されている場所を確認

  `ls -la /etc/nginx/certs`

## nginx.confファイルの修正

* nginx.confをコンテナからコピーする

`docker cp nginx-proxy:/etc/nginx/nginx.conf nginx.conf`

## 「client_max_body_size」のアップロード上限を変更

* httpのところに追加

```
client_max_body_size 1G;
```

## コンテナに「nginx.conf」をコピー
`docker cp nginx.conf nginx-proxy:/etc/nginx/nginx.conf`


## コンテナをリロード

`docker exec nginx-proxy nginx -s reload`

* nginxプロセスを操作するには「-s 操作内容」


## default.confファイルの修正

* default.confをコンテナからコピーする
`docker cp nginx-proxy:/etc/nginx/conf.d/default.conf default.conf`

## URLを書き換える



## github

* nginx-proxy

  https://github.com/jwilder/nginx-proxy

* letsencrypt-nginx-proxy-companion

  https://github.com/JrCs/docker-letsencrypt-nginx-proxy-companion