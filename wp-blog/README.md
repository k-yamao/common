# common

## ファイルのコピー

* 移行元コンテナからファイルをコピー
`docker cp wp-blog:/var/www/html/wp-content ./wp-content`

* 移行先コンテナへファイルをアップロード

`docker cp ./wp-content/uploads wp-blog:/var/www/html/wp-content`
`docker cp ./wp-content/plugins wp-blog:/var/www/html/wp-content`
`docker cp ./wp-content/themes wp-blog:/var/www/html/wp-content`


