# オフィス予約アプリ
## Laravel-APIpj



## 環境構築

### クローンして環境構築する手順
1.リポジトリのクローンとサービス起動
```
git clone git@github.com:tutiyaren/apipj-laravel.git
```
必要であれば``mv``でディレクトリ名を変える
上記コマンド後、クローンしたディレクトリに移動する

docker composeを使って必要なサービスを起動
```
docker compose up -d --build

```

2.プロジェクトの設定
まずは下記コマンドで、Laravelのアプリケーションキーを生成する
```
docker compose exec php bash
cd api
php artisan key:generate
exit
```

次に、.envファイルを編集して必要な設定をするために、.env.exampleをコピーして.envファイルを作成と編集する
```
cd src/api
cp .env.example .env
```


### 結果.ブラウザで確認

- [Laravelウェルカムページ](http://localhost:8081) にアクセスし、問題なく表示されれば OK です。  
パーミッションエラー発生した場合、``sudo chmod -R 777 src/api/*``を実行

- [pgAdmin](http://localhost:8080) にアクセスし、問題なく表示されれば OK です。
