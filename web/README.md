### HMLTファイルをコピー
`docker cp *.html web:/var/www/html/`

### 設定ファイルを修正したらリロード
`docker restart mimicry`




### コンテナで修正したとこ
vim /etc/nginx/conf.d/default.conf

```
location / {
    root  /usr/share/nginx/html/
    ↓ へ修正
    root  /var/www/html/
```