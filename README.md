# mysql-docker  

MySQLの環境をDockerでローカルに一瞬で作るためのリポジトリです。サンプルデータも自動で注入されます。　　

以下のコマンドを Mac のターミナルから実行してください。**3 ステップ**のみです。

1. リポジトリをクローンする

```
git clone git@github.com:tadatakuho/mysql-docker.git
```

2. クローンした`mysql-docker`に移動する

```
cd mysql-docker
```

3. 以下の Docker コマンドで MySQL を起動＆データ注入

```
docker-compose up -d
```


# 詳細

使い方詳細記事↓  
https://zenn.dev/takuho/articles/efc40344f3122e




# 加筆
4. 起動中のコンテナを確認
docker ps
```

5. このMySQLコンテナに入る（起動中と上記で確認する）
docker exec -it mysql_container bash
or
docker exec -it 123f15d25f5d bash
docker exec -it 123f15d25f5d /bin/bash
docker exec -it 123f15d25f5d sh
```

6. MySQLに接続
mysql -p
※[Docker+Windows]mysqlのdockerイメージがmy.cnfのマウントのエラーで起動しない時の対処法
mysql: [Warning] World-writable config file '/etc/mysql/conf.d/my.cnf' is ignored.
↓
my.cnfを右クリック→プロパティ→属性を読み取り専用


