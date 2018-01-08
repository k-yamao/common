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


## github

* nginx-proxy

  https://github.com/jwilder/nginx-proxy

* letsencrypt-nginx-proxy-companion

  https://github.com/JrCs/docker-letsencrypt-nginx-proxy-companion