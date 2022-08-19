## 概要

事前にdockerエンジンをインストールしておく。
https://docs.docker.com/engine/install/

|  ミドルウェア  |  バージョン  |
| ---- | ---- |
|  Djnago  |   4.1   |
|  Python  |   3.10.6   |
|  uWSGI  |   2.0.20   |
|  Nginx  |   1.23.1   |
|  MariaDB | 10.8.3   |

他のライブラリなどは、コード参照

マウントは、docker-compose.ymlを見て確認。

<br>

## 構築手順

cloneする
```
git clone git@github.com:Shota0616/pathy_docker.git
```

docker イメージ、コンテナ作成。及び起動
```
#docker-compose.ymlがあるディレクトリで実行する。
cd pathy_docker
docker-compose up -d
```

疎通確認

http://localhost:8000/admin/

<br>

## 操作

コンテナID確認
```
docker ps -a
```

コンテナ起動(docker-composeの場合)
```
docker-compose up -d
```

コンテナ停止（docker-composeの場合）
```
docker-compose stop
```

コンテナ削除（docker-composeの場合）
```
docker-compose down
```

コンテナに入る
```
docker exec -it [コンテナID] bash
```
