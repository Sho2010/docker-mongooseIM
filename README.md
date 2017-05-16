# 起動

~~~shell
$ docker-compose up -d db
# ...DB起動を待って
$ docker-compose up

~~~

# 設定

`./config/mongoose01/ejabberd.cfg` が読み込まれるようになってます

`vm.args.org`, `app.config.org` のファイルも上書き可能(必要であれば.orgを削除してください) ですが
通常は上書きする必要はありません。


### 元々の設定が見たい場合

~~~
# containerが立ち上がった状態で
$ docker-compose exec mongoose cat /usr/lib/mongooseim/etc/ejabberd.cfg > ejabberd_default.cfg
~~~
