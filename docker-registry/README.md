# DBコンテナ

## ネットワークを作る（作ってなかったら）

`docker network create --driver bridge shared`

## .envファイルを準備

```
VIRTUAL_HOST=registry.hoge.com
LETSENCRYPT_HOST=registry.hoge.com
LETSENCRYPT_EMAIL=hoge@hoge.com
REGISTRY_STORAGE=s3
REGISTRY_STORAGE_S3_ACCESSKEY=XXXXXXXXXXXXXXXXX
REGISTRY_STORAGE_S3_SECRETKEY=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
REGISTRY_STORAGE_S3_BUCKET=<<バケット名>>
REGISTRY_STORAGE_S3_REGION=ap-northeast-1
REGISTRY_STORAGE_S3_ROOTDIRECTORY=/
```

## バックグランドで起動

`docker-compose up -d`


