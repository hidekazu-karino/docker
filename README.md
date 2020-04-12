Docker の勉強メモ

# docker-compose-HelloWorld

docker-compose を使って PostgreSQL を動かすコンテナと CentOS のサーバを同じネットワークに所属させて，CentOS サーバからデータベースコンテナに接続できるようにする．
# mount
docker run時にバインドマウントすることでホストでのコード変更をコンテナに反映させる．

fishシェルにおいてmountにて`docker run -d -p 5000:5000 --name server_sample -v "$PWD/app":/app mount_sample`を実行するとコンテナの/appディレクトリがホストにバインドマウントされる．この状態でserver.pyを書き換えるとその内容がそのままコンテナに反映される．

```
$ curl localhost:5000
# server.pyのdef hello_world()のreturn文を書き換える
$ curl localhost:5000
```
