# オフィス予約アプリ
## Laravel-APIpj



## 環境構築

### クローンして環境構築する手順
1.リポジトリのクローンとサービス起動
```
git clone git@github.com:tutiyaren/laravel-apipj.git
```
必要であれば``mv``でディレクトリ名を変える
上記コマンド後、クローンしたディレクトリに移動する

dockerで必要なサービスを起動
```
make up
```

2.プロジェクトの設定
まずは下記コマンドで、Laravelのアプリケーションキーを生成する
```
make bash
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

- [pgAdmin](http://localhost:8080) にアクセスし、問題なく表示されれば OK です。
